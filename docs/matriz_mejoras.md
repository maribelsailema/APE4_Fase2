# Matriz de Hallazgos y Mejoras — CaféU

> Este documento recoge la **Actividad 5: Corrección y Conclusiones** de la Fase 2.
> Identifica y prioriza los hallazgos observados en la prueba cognitiva, propone una mejora para cada dificultad relevante, registra la coordinación con **Viviana Sarco**, **Sebastián Santana** y **Wilson Pillapa** y verifica las correcciones aplicadas al prototipo.

---

## 1. Identificación y priorización de hallazgos

| ID | Hallazgo | Severidad | Participante que lo evidenció | Impacto | Prioridad |
| :---: | :--- | :---: | :--- | :--- | :---: |
| **H-02** | Ambigüedad en el selector de cantidad: `[-]` atenuado en 1 unidad sin indicar si borra el ítem | **Alta** | Mateo Morales (Tarea 2) | Riesgo de pérdida de productos y pérdida de confianza en el carrito | **1** |
| **H-01** | Acceso al carrito sólo mediante barra flotante inferior; el usuario busca el icono en el header | **Media** | Mateo Morales (Tarea 1) | Retraso en llegar al carrito; fricción en el paso crítico del pedido | **2** |
| **H-03** | Instrucción genérica de retiro: "Paga y retira en caja rápida" sin ubicación precisa | **Media** | Observación transversal de la sesión | Incertidumbre sobre dónde retirar; ansiedad al confirmar | **3** |
| **S-01** | Ausencia de pago digital QR (sugerencia de evolución) | Baja | Bryan Ortiz (Tarea 1) | Fuera del alcance actual; backlog de producto | **4** |
| **S-02** | Contraste insuficiente del enlace **"+ Seguir comprando"** | Baja | Bryan Ortiz (Tarea 2) | Dificultad leve de lectura en la revisión del pedido | **5** |

**Criterio de priorización:** severidad del daño potencial (pérdida de datos > fricción > estética), frecuencia de aparición en las sesiones y correspondencia con heurísticas de Nielsen.

> Los tres hallazgos de prioridad alta y media (H-01, H-02, H-03) fueron corregidos y verificados. S-01 y S-02 quedan registrados como mejoras de backlog (S-02 se atiende de forma colateral con la corrección de H-01 al reforzar la navegación de revisión).

---

## 2. Propuesta de mejora por dificultad relevante

### H-02 · Ambigüedad del stepper (Severidad: Alta)
* **Dificultad detectada:** al llegar a 1 unidad, el botón `[-]` quedaba atenuado sin explicación; el usuario temió que la pulsación borrara el ítem completo.
* **Mejora propuesta:** transformar `[-]` en un **icono de basurero** cuando la cantidad es 1, acompañado de **diálogo de confirmación** ("¿Deseas eliminar?").
* **Justificación:** Heurísticas **#5 (Prevención de errores)** y **#6 (Reconocimiento en vez de recuerdo)**; *signifier* claro de acción destructiva según Don Norman.
* **Responsable de la corrección:** **Wilson Pillapa** (estados, feedback y microinteracciones — el stepper es Microinteracción 1).

### H-01 · Acceso al carrito (Severidad: Media)
* **Dificultad detectada:** el participante buscó el carrito en la esquina superior derecha antes de notar la barra flotante inferior.
* **Mejora propuesta:** **acceso dual sincronizado**: barra flotante inferior + **icono con badge de contador** en el header superior.
* **Justificación:** Heurística **#7 (Flexibilidad y eficiencia de uso)**: satisface tanto el modelo web clásico como el uso móvil con una sola mano.
* **Responsable de la corrección:** **Sebastián Santana** (prototipado navegable y arquitectura de navegación).

### H-03 · Incertidumbre de retiro (Severidad: Media)
* **Dificultad detectada:** la instrucción "Paga y retira en caja rápida" no indicaba el punto físico exacto de retiro.
* **Mejora propuesta:** **insignia destacada** en la confirmación: *"VENTANILLA EXCLUSIVA #2: Pasa directo sin fila, muestra #CU-104"*.
* **Justificación:** reducción de **carga cognitiva** y cierre de la acción; modela el entorno físico real y evita ansiedad en el estudiante (consistencia entre interfaz y servicio).
* **Responsable de la corrección:** **Viviana Sarco** (refinamiento de wireframes, jerarquía visual y contenido de la pantalla de confirmación).

### S-01 · Pago digital QR (Baja — backlog)
* **Propuesta:** habilitar pago digital por QR en futuras versiones; fuera del alcance de la Fase 2.

### S-02 · Contraste del enlace "+ Seguir comprando" (Baja)
* **Propuesta:** elevar el peso y el contraste del enlace para superar WCAG 2.1 AA; se refuerza de forma colateral al retocar la navegación de revisión (H-01).

---

## 3. Coordinación de correcciones con el equipo

| Reunión de coordinación | Participantes | Acuerdos |
| :--- | :--- | :--- |
| Priorización de hallazgos | Alex Guachi (coordina), Viviana Sarco, Sebastián Santana, Wilson Pillapa | Se acuerda corregir H-02 (alta), H-01 y H-03 (medias) antes de cerrar la Fase 2; S-01 y S-02 quedan en backlog |
| Reparto de responsabilidades | Alex → equipo | H-02 → Wilson; H-01 → Sebastián; H-03 → Viviana |
| Verificación de correcciones | Alex Guachi | Revisión de cada cambio en el prototipo corregido y registro antes/después |

**Seguimiento:**

* **Wilson Pillapa** implementa el cambio de estado del stepper y el diálogo de confirmación, coherente con los estados y microinteracciones ya documentados en [`estados_microinteracciones.md`](estados_microinteracciones.md).
* **Sebastián Santana** añade el acceso dual al carrito manteniendo la sincronización con la barra flotante, sobre los recorridos documentados en [`recorridos_prototipo.md`](recorridos_prototipo.md).
* **Viviana Sarco** ajusta la jerarquía y el contenido de la pantalla de confirmación con la insignia de ventanilla, en línea con [`decisiones_diseno.md`](decisiones_diseno.md).
* **Alex Guachi** verifica las tres correcciones, documenta la comparación y consolida las evidencias.

---

## 4. Verificación de las correcciones aplicadas

| Corrección | Hallazgo | Verificación realizada | Resultado | Evidencia |
| :--- | :---: | :--- | :--- | :--- |
| **1. Acceso dual al carrito** (header con badge + barra flotante) | H-01 | Se comprobó que ambas rutas llevan a `04_Revisar_Pedido` y que el contador se mantiene sincronizado | **Verificada** | [`antes_despues/correcciones_h01_h02_h03.png`](../evidencias/antes_despues/correcciones_h01_h02_h03.png) |
| **2. Icono de basurero + confirmación en 1 unidad** | H-02 | Se comprobó que al llegar a 1 u el `[-]` muta a basurero y que el diálogo "¿Deseas eliminar?" protege la acción destructiva | **Verificada** | [`antes_despues/correcciones_h01_h02_h03.png`](../evidencias/antes_despues/correcciones_h01_h02_h03.png) |
| **3. Insignia "Ventanilla Exclusiva #2"** | H-03 | Se comprobó que la confirmación muestra la ubicación exacta de retiro junto al ticket #CU-104 | **Verificada** | [`antes_despues/05_Confirmacion.png`](../evidencias/antes_despues/05_Confirmacion.png) |

> Las tres correcciones previstas por los criterios de aceptación fueron **aplicadas y verificadas** sobre el prototipo corregido.

---

## 5. Comparación: versión inicial vs versión corregida

| Hallazgo / Severidad | Versión inicial | Versión corregida | Justificación técnica (HCI) |
| :--- | :--- | :--- | :--- |
| **H-01: Acceso al carrito** (Media) | Solo accesible mediante barra flotante inferior en Menú. | Acceso dual sincronizado: barra flotante inferior + icono con badge en header superior. | Heurística #7 (Flexibilidad y eficiencia): satisface tanto el modelo web clásico como el móvil con una sola mano. |
| **H-02: Ambigüedad en Stepper** (Alta) | Botón `[-]` quedaba atenuado sin explicación en 1 unidad. | Al llegar a 1 u, muta a icono de basurero con diálogo de confirmación: "¿Deseas eliminar?". | Heurísticas #5 y #6 (Prevención de errores y Reconocimiento): signifier claro de acción destructiva según Don Norman. |
| **H-03: Incertidumbre de retiro** (Media) | Instrucción genérica: "Paga y retira en caja rápida". | Insignia destacada: "VENTANILLA EXCLUSIVA #2: Pasa directo sin fila, muestra #CU-104". | Reducción de carga cognitiva y cierre de acción: modela el entorno físico real evitando ansiedad en el estudiante. |

![Correcciones aplicadas — antes/después](../evidencias/antes_despues/correcciones_h01_h02_h03.png)

### Comparativa general de evolución UX (Fase 1 → Fase 2)

![Comparativa antes/después](../evidencias/antes_despues/comparativa_antes_despues.png)

| Dimensión | Antes (wireframe / prototipo inicial) | Después (prototipo corregido) |
| :--- | :--- | :--- |
| Jerarquía tipográfica | Textos planos y pesos idénticos | Escala tipográfica H1/Sub y precios en negrita |
| Controles e interacción | Botón "Ver detalle" redundante | Tarjeta interactiva + botón directo "Añadir" |
| Accesibilidad | Contraste gris muy claro (< 2.8:1) | Contraste > 14:1 y áreas táctiles ≥ 44×44 px |
| Gestión de errores y feedback | Diseño estático, sin retroalimentación | Estados visibles, ticket #CU-104 y tiempo estimado |
| Carga cognitiva y layout | Márgenes caóticos e íconos genéricos | Espaciado 8pt con Auto Layout y flujo de 5 pasos |
| Acceso al carrito (H-01) | Sólo barra flotante inferior | Acceso dual sincronizado |
| Eliminación de ítems (H-02) | `[-]` atenuado y ambiguo | Basurero + confirmación explícita |
| Retiro del pedido (H-03) | Instrucción genérica | Insignia de ventanilla exclusiva #2 |

**Capturas de la versión corregida:**

* [`antes_despues/04_Revisar_Pedido.png`](../evidencias/antes_despues/04_Revisar_Pedido.png) — revisión y edición del pedido con controles explícitos.
* [`antes_despues/05_Confirmacion.png`](../evidencias/antes_despues/05_Confirmacion.png) — confirmación con ticket #CU-104 e indicación de retiro.

---

## 6. Resultado de la priorización

| Prioridad | Acción | Estado |
| :---: | :--- | :--- |
| 1 | Corregir H-02 (stepper) | Aplicada y verificada |
| 2 | Corregir H-01 (acceso dual al carrito) | Aplicada y verificada |
| 3 | Corregir H-03 (insignia de retiro) | Aplicada y verificada |
| 4 | S-01 pago QR | Backlog de producto (fuera de alcance) |
| 5 | S-02 contraste de "+ Seguir comprando" | Backlog de accesibilidad, refuerzo colateral con H-01 |

---

