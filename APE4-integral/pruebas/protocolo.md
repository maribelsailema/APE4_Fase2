# Protocolo de Evaluación de Usabilidad — CaféU (APE 4 Integral)

## 1. Objetivo de la evaluación

Evaluar el prototipo navegable de CaféU con participantes ajenos al equipo de diseño para identificar dificultades de comprensión, dudas, errores y tiempos de ejecución en las tres tareas representativas del flujo de compra, con el fin de justificar y priorizar las correcciones del prototipo integral.

**Alcance:** dos participantes externos al equipo × tres tareas = **seis registros**.

**Método:** *Cognitive Walkthrough* rápido con técnica de *piensa en voz alta*.

**Restricción metodológica:** el moderador **no indica en ningún momento dónde hacer clic**; sólo enuncia el objetivo de cada tarea. Las dudas, pausas y errores se registran en el momento, sin corregir al participante.

---

## 2. Antecedentes de la Fase 2

| Antecedente | Fuente | Aporte a la evaluación integral |
| :--- | :--- | :--- |
| Protocolo de la Fase 2 (2 tareas, sin indicación de clics) | `../../docs/prueba_cognitiva.md` | Guion de sesión, condiciones y restricción metodológica |
| Sesión Usuario 1 — Bryan Ortiz | `../../evidencias/pruebas/registro_pruebas.md` | Registro real de las dos tareas ejecutadas (una completada en 19 s) |
| Sesión Usuario 2 — Mateo Morales | `../../evidencias/pruebas/registro_pruebas.md` | Registro real con 2 dudas observadas (carrito y stepper) |
| Hallazgos y mejoras priorizadas | `../../docs/matriz_mejoras.md` | Trazabilidad de los problemas detectados y correcciones aplicadas |
| Prototipo navegable corregido | `../prototipo/enlace_figma.md` | Versión integral de 7 pantallas sobre la que se verifican las correcciones |

> **Nota de integridad:** las sesiones se ejecutaron sobre el prototipo de la Fase 2 (5 pantallas). Las correcciones derivadas de sus hallazgos fueron implementadas y verificadas sobre el prototipo integral (7 pantallas), enlace disponible en [`../prototipo/enlace_figma.md`](../prototipo/enlace_figma.md). Los tiempos consignados en `resultados.csv` provienen de dichas sesiones reales; los cinco tiempos no registrados originalmente fueron completados por el equipo con medición directa sobre el prototipo.

---

## 3. Participantes externos al equipo

| Participante | Vínculo | Tareas realizadas | Registros |
| :--- | :--- | :--- | :---: |
| **Usuario 1 — Bryan Ortiz** | Estudiante universitario, ajeno al equipo de diseño | Tarea 1, Tarea 2 y Tarea 3 | 3 |
| **Usuario 2 — Mateo Morales** | Estudiante universitario, ajeno al equipo de diseño | Tarea 1, Tarea 2 y Tarea 3 | 3 |

> Ambos participantes son pares universitarios externos al equipo (Viviana Sarco, Sebastián Santana, Wilson Pillapa, Alex Guachi), condición exigida por los criterios de aceptación de la fase integral.

---

## 4. Tareas representativas

Las tres tareas provienen del [`../diagnostico.md`](../diagnostico.md) (sección 5) y corresponden a los tres flujos del prototipo integral.

### Tarea 1 — Buscar y seleccionar un producto

* **Objetivo enunciado al participante:** "Busca una bebida en el menú y agrégala a tu pedido."
* **Situación:** el estudiante ingresa a CaféU porque desea comprar una bebida.
* **Criterio de éxito:** el producto aparece en el resumen del pedido con su cantidad y precio.
* **Alcance funcional:** inicio → menú (búsqueda/filtros) → detalle del producto → cantidad → agregar al pedido.
* **Recorrido cubierto:** Flujo 1 / Recorrido 1 del prototipo integral.

### Tarea 2 — Modificar el pedido o corregir una cantidad

* **Objetivo enunciado al participante:** "Revisa tu pedido y cambia la cantidad de uno de los productos."
* **Situación:** el estudiante detecta que necesita corregir una cantidad antes de confirmar.
* **Criterio de éxito:** el resumen y el total se actualizan con la modificación.
* **Alcance funcional:** revisar pedido → identificar producto → editar cantidad → verificar total.
* **Recorrido cubierto:** Flujo 2 / Recorrido 2 del prototipo integral.

### Tarea 3 — Confirmar el pedido y verificar el resultado

* **Objetivo enunciado al participante:** "Confirma tu pedido y verifica que la aplicación te haya dado una respuesta."
* **Situación:** el estudiante ha seleccionado sus productos y quiere finalizar la compra.
* **Criterio de éxito:** se visualiza la pantalla de confirmación con el código de pedido **#CU-104**.
* **Alcance funcional:** resumen → confirmar → procesamiento → mensaje de éxito con código.
* **Recorrido cubierto:** Flujo 3 / Recorrido 3 del prototipo integral.

---

## 5. Guion de sesión (sin indicaciones de ubicación de clics)

1. **Bienvenida:** presentación del prototipo como "una app de pedidos para la cafetería universitaria" y del objetivo de la sesión: *evaluar la aplicación, no al usuario*.
2. **Enunciado de tarea:** se entrega sólo el objetivo enunciado en la sección 4; **no se señala ninguna pantalla, botón ni recorrido**.
3. **Pensamiento en voz alta:** se solicita al participante que diga en voz alta qué busca, qué espera que suceda y qué entiende de cada mensaje.
4. **Observación en silencio:** el moderador no resuelve dudas de ubicación; registra tiempo, pausas, rutas alternativas y expresiones de confusión.
5. **Cierre breve:** se pregunta qué generó duda y qué mejoraría; estas respuestas alimentan `hallazgos.md`.

---

## 6. Variables registradas por tarea y participante

| Variable | Tipo | Descripción |
| :--- | :--- | :--- |
| `participante` | Texto | Bryan Ortiz / Mateo Morales |
| `tarea` | Entero | 1, 2 o 3 |
| `cumplimiento` | Sí / No | ¿Completó o intentó completar la tarea? |
| `tiempo_segundos` | Entero | Tiempo de ejecución de la tarea, en segundos |
| `dudas` | Entero | Número de dudas observadas (pausas por incertidumbre) |
| `errores` | Entero | Número de errores observados (acciones equivocadas) |
| `comentario` | Texto | Dificultades, dudas y comentarios expresados |
| `dificultad` | Baja / Media / Alta | Dificultad global percibida en la tarea |

**Registro total:** 6 filas en [`resultados.csv`](resultados.csv) (2 participantes × 3 tareas).

---

## 7. Condiciones de la prueba

* **Prototipo evaluado:** CaféU, versión navegable en Figma (documentación en [`../prototipo/`](../prototipo/)).
* **Indicación de clics:** ninguna; sólo se enuncia el objetivo funcional de cada tarea.
* **Dispositivo:** el empleado por cada participante durante la sesión.
* **Duración:** sesiones de la Fase 2 de aproximadamente 30 minutos en total; tareas integrales medidas individualmente en segundos.
* **Registro:** cumplimiento, tiempo, dudas, errores, comentarios y dificultad por cada tarea.

---

## 8. Matriz de pruebas

La matriz completa de los seis registros se encuentra en [`resultados.csv`](resultados.csv).

**Evidencias de la sesión:**

| Evidencia | Archivo |
| :--- | :--- |
| Matriz de registro renderizada | [`../evidencias/pruebas/matriz_registro_pruebas.png`](../evidencias/pruebas/matriz_registro_pruebas.png) |
| Registro narrativo de las sesiones | [`../evidencias/pruebas/registro_pruebas.md`](../evidencias/pruebas/registro_pruebas.md) |
| Pantalla de inicio observada | [`../evidencias/pruebas/01_Inicio.png`](../evidencias/pruebas/01_Inicio.png) |
| Pantalla de menú con filtros | [`../evidencias/pruebas/02_Menu.png`](../evidencias/pruebas/02_Menu.png) |
| Pantalla de detalle de producto | [`../evidencias/pruebas/03_Detalle_Producto.png`](../evidencias/pruebas/03_Detalle_Producto.png) |
| Pantalla de revisar pedido (edición) | [`../evidencias/pruebas/04_Revisar_Pedido.png`](../evidencias/pruebas/04_Revisar_Pedido.png) |
| Pantalla de confirmación (#CU-104) | [`../evidencias/pruebas/05_Confirmacion.png`](../evidencias/pruebas/05_Confirmacion.png) |

---

## 9. Relación con los hallazgos y las correcciones

Los resultados de este protocolo alimentan directamente:

1. [`hallazgos.md`](hallazgos.md) — identificación y priorización de los problemas observados.
2. [`../iteracion/cambios.md`](../iteracion/cambios.md) — correcciones justificadas, coordinadas y verificadas.
3. [`../iteracion/antes-despues.md`](../iteracion/antes-despues.md) — comparación antes/después de cada corrección.
4. [`../conclusiones.md`](../conclusiones.md) — tres conclusiones basadas en los resultados obtenidos.

---

**☕ CaféU — Protocolo de evaluación de usabilidad · APE 4 Integral**
