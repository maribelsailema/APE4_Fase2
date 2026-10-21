# Documentación Técnica: Estados de Interfaz, Feedback Sensorial y Microinteracciones
## Caso de Estudio: Aplicación Móvil "CaféU" (APE 4 - Fase 2)


---

##  1. Propósito y Alcance del Entregable

Este documento formaliza la arquitectura de estados, los mecanismos de retroalimentación sensorial (feedback visual y háptico) y la especificación de microinteracciones bajo el modelo de Dan Saffer para la aplicación móvil **CaféU**.

El propósito central es **eliminar el abismo de ejecución y de evaluación** teorizado por Donald Norman, garantizando que el usuario comprenda en todo momento:
1. Qué acciones puede realizar de manera inmediata (*Affordances y Significantes*).
2. Qué está procesando el sistema tras una acción crítica (*Visibilidad del Estado - Heurística #1 de Nielsen*).
3. Cómo recuperarse ante un imprevisto sin frustración (*Gestión de Errores - Heurística #9 de Nielsen*).
4. La confirmación inequívoca del cierre de su pedido (*Cierre Cognitivo y Reducción de Carga Mental*).

---

## 2. Especificación de los Cuatro Estados de la Interfaz

### 2.1 Estado 1: Inicial 
* **Definición Operativa:** Estado en el cual la aplicación ha concluido la carga de datos del catálogo (8 productos disponibles) y los elementos de interacción se encuentran listos para recibir eventos de entrada del usuario.
* **Componentes Afectados:**
  * Barra de búsqueda superior (`Buscar en el menú...`) con placeholder en contraste WCAG AA.
  * Chips de categoría horizontal: chip *"Todos"* activo con fondo negro sólido `#0f172a` y texto blanco; chips restantes en reposo (`#ffffff` con borde `#cbd5e1`).
  * Tarjetas de producto en cuadrícula de 2 columnas: botón directo `Añadir` en reposo (fondo `#0f172a`, altura 38px, área táctil ampliada de 44x44px).
  * Barra flotante inferior anclada (*Sticky Floating Bar*): muestra el resumen de compra acumulado *"2 ítems en carrito | $4.25"* y botón de acceso directo *"Ver mi pedido →"*. En caso de que el carrito no tenga productos, el estado inicial muestra una ilustración minimalista con el mensaje: *"Tu carrito está listo. Elige tu café favorito para empezar"*.
* **Principio HCI Aplicado:** *Heurística #1 (Visibilidad del Estado)* y *Ley de Hick*. La interfaz presenta solo la información indispensable para iniciar la decisión sin sobrecargar la memoria operativa del estudiante.

![Estado 1: Inicial](evidencias/estados/01_estado_inicial.png)

---

### 2.2 Estado 2: Procesamiento 
* **Definición Operativa:** Estado transaccional activo disparado inmediatamente al pulsar el botón principal *"Confirmar pedido • $4.25"* en la pantalla de revisión de pedido.
* **Comportamiento y Bloqueo de Idempotencia:**
  * Para prevenir el envío múltiple o cobros duplicados por pulsaciones compulsivas del usuario (*Double-tap issue*), el botón conmuta inmediatamente a estado **deshabilitado** (`disabled = true`, `pointer-events: none`).
  * La opacidad del botón disminuye al 75% y el texto *"Confirmar pedido"* se oculta para dar paso a un **micro-spinner circular animado SVG** (rotación continua a 360° en ciclo de 800ms) acompañado del mensaje de estado: *"Procesando pedido con caja de CaféU... Generando ticket #CU-104"*.
  * Se despliega un contenedor de retroalimentación en tono ámbar suave (`#fffbeb`, borde `#fcd34d`) que explica la comunicación con el terminal de caja física de la cafetería.
* **Principio HCI Aplicado:** *Heurística #1 (Retroalimentación inmediata en menos de 100ms según Robert Miller)* y *Heurística #5 (Prevención de Errores)*. Reduce la ansiedad generada por la incertidumbre de la red.

![Estado 2: Procesamiento](evidencias/estados/02_estado_procesamiento.png)

---

### 2.3 Estado 3: Error y Validación Asistida 
* **Definición Operativa:** Respuesta del sistema cuando se interrumpe la comunicación con la base de datos de caja o cuando un dato ingresado excede las restricciones operativas.
* **Diseño del Mensaje (Heurística #9 de Nielsen - Mensajes Comprensibles):**
  * **Regla 1 (Sin jerga técnica):** Se eliminan tajantemente códigos crudos como *"Error 500: Gateway Timeout"* o *"NullPointerException at OrderService"*.
  * **Regla 2 (No culpabilizar al usuario):** El mensaje no utiliza frases acusatorias. En su lugar, indica con empatía: *"¡No te preocupes! Hubo una interrupción temporal con la caja de CaféU, pero tus productos siguen guardados en el carrito"*.
  * **Regla 3 (Acción constructiva inmediata):** Se proveen dos botones de rescate:
    1. Botón primario de escape: *"Reintentar conexión"* (fondo carmesí `#dc2626`).
    2. Botón secundario: *"Modificar pedido"* (fondo blanco con borde gris).
* **Validación Inline en Pantalla de Detalle:**
  * En el campo de notas especiales (*Instrucciones del pedido*), al alcanzar el límite estricto de 100 caracteres, el borde del campo cambia a rojo `#ef4444`, el contador numérico marca `100/100` en negrita y se despliega el aviso inline: *"Límite máximo de 100 caracteres alcanzado para la orden express"*.

![Estado 3: Error](evidencias/estados/03_estado_error.png)

---

### 2.4 Estado 4: Éxito y Confirmación 
* **Definición Operativa:** Cierre exitoso de la transacción que confirma la reserva de los insumos y la emisión del ticket digital para retiro presencial.
* **Elementos de Certeza Cognitiva:**
  * Icono circular grande con checkmark verde esmeralda (`#15803d`) con animación de escala elástica.
  * Título de celebración en alto contraste: *"¡Pedido Recibido con Éxito! La cafetería ya está preparando tu orden"*.
  * **Identificador Primario de Retiro:** Número de orden destacado en tipografía de 24pt Bold: **`#CU-104`**, enmarcado en una tarjeta tipo ticket de retiro rápido.
  * **Instrucciones Físicas Claras:** Tarjeta verde suave (`#f0fdf4`) con la instrucción operativa: *"SIGUIENTE PASO: Dirígete a la VENTANILLA EXCLUSIVA #2 (Caja Rápida). Pasa directo sin hacer la fila general. Muestra tu código #CU-104. Tiempo estimado: 5 a 10 minutos"*.
  * Botón persistente de navegación: *"Volver a la pantalla de inicio"*, que restablece el flujo sin duplicar estados en el historial.
* **Principio HCI Aplicado:** *Cierre Cognitivo (Cognitive Closure)* y *Acoplamiento entre el mundo digital y físico (Don Norman)*.

![Estado 4: Éxito](evidencias/estados/04_estado_exito.png)

---

##  3. Diseño de las Tres Microinteracciones (Modelo Dan Saffer)

Se implementaron las tres microinteracciones exigidas utilizando el framework de 4 etapas de Dan Saffer:

```
┌─────────────────┐       ┌─────────────────┐       ┌─────────────────┐       ┌─────────────────┐
│ 1. DISPARADOR   │ ────► │    2. REGLAS    │ ────► │   3. FEEDBACK   │ ────► │4. BUCLES/MODOS  │
│    (Trigger)    │       │     (Rules)     │       │   (Sensorial)   │       │ (Loops / Modes) │
└─────────────────┘       └─────────────────┘       └─────────────────┘       └─────────────────┘
```

---

### 3.1 Microinteracción 1: Selección de Producto y Adición al Pedido
* **Disparador (Trigger):** Tap manual del usuario sobre el botón *"Añadir al pedido • $1.50"* (en la vista de detalle) o sobre el botón rápido *"Añadir"* (en la tarjeta del catálogo).
* **Reglas (Rules):**
  * Verifica la existencia en catálogo del producto seleccionado.
  * Agrega el objeto con sus atributos (Nombre: Café americano, Cantidad: 1, Precio: $1.50, Notas: "Sin azúcar") al array del carrito.
  * Actualiza la variable reactiva de subtotal recalculando el total general ($4.25) en menos de 16 milisegundos.
* **Feedback (Sensorial):**
  * **Feedback en Botón:** El botón presionado se contrae a escala 0.96x durante el tap y conmuta a color verde esmeralda `#15803d` mostrando la leyenda *"¡Añadido con éxito! ✓"* durante un lapso de 800 ms antes de restablecerse.
  * **Feedback en Barra Flotante:** La barra inferior fija (*Sticky Bar*) realiza un micro-salto vertical de 4 píxeles (*Bounce animation* con función cúbica `cubic-bezier(0.175, 0.885, 0.32, 1.275)`) e incrementa el contador visual de ítems de 1 a 2.
  * **Respuesta Háptica:** Emisión de un pulso háptico ligero (*Haptic Light Impact*) en dispositivos táctiles.
* **Bucles y Modos (Loops/Modes):**
  * Si el usuario presiona el botón repetidas veces sin cambiar las instrucciones especiales, el sistema incrementa el contador numérico de la fila existente en lugar de duplicar elementos en la lista.

![Microinteracción 1: Selección de Producto](evidencias/microinteracciones/micro_01_seleccion_producto.png)

---

### 3.2 Microinteracción 2: Transición Espacial entre Pantallas
* **Disparador (Trigger):** Clic o tap sobre elementos de avance como *"Ver Menú →"*, tarjeta de producto para abrir detalle, o *"Ver mi pedido →"*.
* **Reglas (Rules):**
  * Define la dirección cinemática del movimiento según la profundidad del flujo:
    * Avance en el embudo (Menú ➔ Detalle ➔ Carrito): Desplazamiento lateral de derecha a izquierda (*Push / Slide Left*).
    * Retroceso (Tap en `<` o `+ Seguir comprando`): Desplazamiento inverso de izquierda a derecha (*Slide Right*).
  * Preserva como capa estática superior (*Fixed Overlay*) la barra de estado del dispositivo (hora 9:41, batería, Wi-Fi) para evitar parpadeos perceptivos.
* **Feedback (Sensorial):**
  * Transición suave con curva de desaceleración **Ease-out** con una duración exacta de **300 milisegundos**.
  * La pantalla entrante aparece con una opacidad gradual de 0% a 100% mientras se desplaza, generando una clara metáfora de navegación espacial continua (*Mental Spatial Mapping*).
* **Bucles y Modos (Loops/Modes):**
  * Si el usuario realiza un gesto de deslizamiento rápido (*Swipe Back*) desde el borde izquierdo de la pantalla, la transición acompaña dinámicamente la posición del pulgar, cancelando el movimiento si se suelta antes del 40% del recorrido.

![Microinteracción 2: Transición entre Pantallas](evidencias/microinteracciones/micro_02_transicion_pantallas.png)

---

### 3.3 Microinteracción 3: Progreso y Procesamiento del Pedido
* **Disparador (Trigger):** Tap sobre el botón de acción principal (*CTA*) *"Confirmar pedido • $4.25"*.
* **Reglas (Rules):**
  * Bloquea inmediatamente el canal de eventos de entrada (*Pointer Events = None*) para garantizar idempotencia operativa.
  * Inicia un temporizador asíncrono que simula el despacho de la orden al punto de venta (1200 milisegundos).
* **Feedback (Sensorial):**
  * **Máquina de Estados del Botón:**
    1. *Estado Normal:* Fondo negro `#0f172a`, texto blanco *"Confirmar pedido • $4.25"*.
    2. *Estado Activo (Tap):* Reducción elástica a escala 0.97x.
    3. *Estado Procesamiento:* El texto se desvanece suavemente y aparece en su centro un micro-spinner giratorio animado en tono ámbar `#f59e0b` junto a la palabra *"Procesando..."*. El botón se tiñe de gris plomo `#475569`.
    4. *Estado Cierre:* Conmutación a fondo verde esmeralda `#15803d` con el texto *"✓ ¡Orden #CU-104!"* justo antes de transicionar a la pantalla de confirmación.
* **Bucles y Modos (Loops/Modes):**
  * Si el tiempo de respuesta supera los 4000 ms por timeout de red, el bucle de procesamiento se interrumpe automáticamente y conmuta al **Estado 3 (Error y Validación Asistida)** sin resetear el formulario.

![Microinteracción 3: Progreso y Procesamiento](evidencias/microinteracciones/micro_03_progreso_procesamiento.png)

---

##  4. Coordinación con Sebastián para la Integración en Figma

Para asegurar que las especificaciones de este documento queden perfectamente integradas en el archivo maestro de Figma que administra Sebastián, se establecieron las siguientes directrices de handoff:

1. **Estructura de Componentes en Figma (Component Sets y Variants):**
   * El botón principal de confirmación fue modelado como una variante interactiva con las propiedades:
     * `State = Default | Hover | Pressed | Loading | Disabled | Success`.
   * El selector numérico de cantidades (*Stepper*) fue empaquetado con las propiedades:
     * `Quantity = 1 (Botón '-' inactivo con opacidad 30%) | 2-9 (Activo) | 10 (Botón '+' inactivo)`.
2. **Parámetros de Interacción en Figma Prototype Mode:**
   * **Transición de Pantallas:** Tipo `Push` o `Slide in`, Dirección: `Left`, Animación: `Smart Animate`, Curva: `Ease Out`, Duración: `300ms`.
   * **Microinteracciones de Botón:** Trigger: `While Hovering` ➔ `While Pressing` (Change to Variant `Pressed`), con animación `Instant` o `Smart Animate (100ms)`.
   * **Microinteracción de Carga:** Trigger: `After Delay (1200ms)` entre la variante `Loading` y la pantalla `05 Confirmación`.
3. **Enlace al Lienzo de Trabajo Coordinado:**
   * [Lienzo de Diseño en Figma (Canvas)](https://www.figma.com/design/wl3jFYJqHiM852P94kUzlz/cafeU_redise%C3%B1o)

---

##  5. Verificación de Criterios de Aceptación del Issue

| Criterio de Aceptación | Estado | Evidencia Documentada y Visual |
|:---|:---:|:---|
| **1. Representación de los 4 estados exigidos** | **CUMPLIDO** | Estados Inicial, Procesamiento, Error y Éxito especificados técnica y visualmente en la Sección 2. |
| **2. Existencia de al menos 3 microinteracciones** | **CUMPLIDO** | Microinteracción de Selección, Transición Espacial y Progreso documentadas bajo el modelo Dan Saffer en la Sección 3. |
| **3. Mensajes de error y confirmación comprensibles** | **CUMPLIDO** | Cumplimiento estricto de la Heurística #9 (sin códigos técnicos) y confirmación con código de retiro `#CU-104`. |
| **4. Inclusión de capturas y explicaciones** | **CUMPLIDO** | 7 diagramas de alta resolución generados e integrados en las carpetas de evidencias correspondientes. |
| **5. Integración coordinada en el prototipo navegable** | **CUMPLIDO** | Parámetros técnicos de Smart Animate y variantes coordinadas con Sebastián para el archivo maestro de Figma. |

---
**Responsable del Entregable:** Wilson Pillapa (@W1LSONN)  
*Facultad de Ingeniería en Sistemas, Electrónica e Industrial – Universidad Técnica de Ambato*
