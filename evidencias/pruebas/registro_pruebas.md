# Registro de Sesiones de Prueba Cognitiva — CaféU

> Registro de campo de las sesiones ejecutadas con participantes externos al equipo.
> Fuente consolidada: `resultados/informe_final.pdf` (Actividad 4).

---

## 1. Datos generales de la sesión

| Campo | Descripción |
| :--- | :--- |
| **Instrumento** | Cognitive Walkthrough rápido con técnica de *piensa en voz alta* |
| **Prototipo evaluado** | CaféU — prototipo navegable en Figma (5 pantallas, alta fidelidad) |
| **Duración total** | 30 minutos (Actividad 4 de la Fase 2) |
| **Participantes** | 2 estudiantes externos al equipo: Bryan Ortiz y Mateo Morales |
| **Tareas por participante** | 2 tareas representativas |
| **Registros totales** | 4 (2 participantes × 2 tareas) |
| **Indicación de clics** | Ninguna: sólo se enunció el objetivo de cada tarea |
| **Registro** | Cumplimiento, dudas, dificultades, errores y sugerencias |

---

## 2. Condiciones de la prueba

* El moderador **no indicó dónde hacer clic** ni recorrió previamente las pantallas con el participante.
* Cada tarea se enunció únicamente por su **objetivo funcional**.
* Las dudas se dejaban en manos del participante: si se atascaba, se registraba la pausa y la ruta alternativa.
* Se capturó el **resultado real** de la ejecución (cumplimiento, tiempo cuando fue relevante y observaciones).
* Al finalizar cada tarea se preguntó qué generó duda y qué se mejorarían.

---

## 3. Sesión — Usuario 1: Bryan Ortiz

### Tarea 1: Pedido express completo (1 Café americano + 1 Sánduche = $4.25)

| Campo | Registro |
| :--- | :--- |
| ¿Completó? | **Sí** |
| Resultado | Llegó a la confirmación con ticket **#CU-104** |
| Dificultades | **Baja** — "el flujo fue muy claro" |
| Dudas | Ninguna observable |
| Errores | Ninguno |
| Sugerencia | Añadir **pago digital directo por QR** en futuras versiones |

### Tarea 2: Filtro Snacks y modificación de cantidades

| Campo | Registro |
| :--- | :--- |
| ¿Completó? | **Sí** |
| Tiempo | **19 segundos** |
| Dificultades | **Baja** — aplicó el filtro y editó cantidades sin bloqueos |
| Dudas | Ninguna observable |
| Errores | Ninguno |
| Sugerencia | **Incrementar el contraste** del enlace **"+ Seguir comprando"** |

**Valoración global del Usuario 1:** recorrido comprensible de extremo a extremo; dificultad **baja** en ambas tareas.

---

## 4. Sesión — Usuario 2: Mateo Morales

### Tarea 1: Pedido express completo (1 Café americano + 1 Sánduche = $4.25)

| Campo | Registro |
| :--- | :--- |
| ¿Completó? | **Sí** |
| Resultado | Llegó a la confirmación con ticket **#CU-104** |
| Dificultades | **Media** |
| Duda principal | **Buscó el acceso al carrito en la esquina superior derecha** antes de notar la barra flotante inferior |
| Errores | Ninguno bloqueante: búsqueda fallida inicial, se recuperó de forma autónoma |
| Propuesta | **Acceso dual** al carrito (header + barra flotante) |

### Tarea 2: Filtro Snacks y modificación de cantidades

| Campo | Registro |
| :--- | :--- |
| ¿Completó? | **Sí** |
| Dificultades | **Media** |
| Duda principal | **Dudó si presionar `[-]` en 1 unidad borraría el ítem de golpe** |
| Errores | Ninguno: la duda detuvo la acción hasta comprender el control |
| Propuesta | **Icono de basurero explícito** y diálogo de confirmación |

**Valoración global del Usuario 2:** completó ambas tareas, pero expuso dos fallos de modelo mental (ubicación del carrito y acción destructiva del stepper).

---

## 5. Consolidado de observaciones

| Participante | Tarea | ¿Completó? | Dificultad | Dudas | Errores |
| :--- | :--- | :---: | :---: | :---: | :---: |
| Bryan Ortiz | Tarea 1 | Sí | Baja | 0 | 0 |
| Bryan Ortiz | Tarea 2 | Sí | Baja | 0 | 0 |
| Mateo Morales | Tarea 1 | Sí | Media | 1 | 0 |
| Mateo Morales | Tarea 2 | Sí | Media | 1 | 0 |
| **Total** | **4 registros** | **4/4** | — | **2** | **0** |

### Dificultades observadas (orden de gravedad)

1. **Ubicación del acceso al carrito** — expectativa de icono con contador en el header (Usuario 2).
2. **Ambigüedad del stepper `[-]`** — miedo a eliminar un ítem sin confirmación (Usuario 2).
3. **Contraste del enlace "+ Seguir comprando"** — dificultad baja de lectura (Usuario 1).
4. **Falta de pago QR** — sugerencia de evolución futura (Usuario 1).

---

## 6. Evidencias asociadas

* [`matriz_registro_pruebas.png`](matriz_registro_pruebas.png) — matriz de registro oficial renderizada.
* [`01_Inicio.png`](01_Inicio.png), [`02_Menu.png`](02_Menu.png), [`03_Detalle_Producto.png`](03_Detalle_Producto.png), [`04_Revisar_Pedido.png`](04_Revisar_Pedido.png), [`05_Confirmacion.png`](05_Confirmacion.png) — pantallas sobre las que se ejecutaron las tareas.
* Documento de análisis: [`../../docs/prueba_cognitiva.md`](../../docs/prueba_cognitiva.md).

---

**☕ CaféU — Registro de pruebas con participantes externos**
