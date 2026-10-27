# Conclusiones — CaféU · APE 4 Integral

> Tres conclusiones sobre **usabilidad y aprendizaje** derivadas de la evaluación integral con usuarios externos ([`pruebas/resultados.csv`](pruebas/resultados.csv)), la comparación entre versión inicial y corregida ([`iteracion/antes-despues.md`](iteracion/antes-despues.md)) y la aplicación de principios de Interacción Humano-Computador.

---

## Conclusión 1 — El rediseño integral validó el flujo completo de compra

La evaluación con dos usuarios externos arrojó **6 de 6 tareas completadas (100 %)** con **0 errores bloqueantes** y un **tiempo promedio de 8 segundos por tarea** (rango 5–19 s), incluyendo las tres etapas críticas: buscar/seleccionar productos, modificar cantidades y confirmar con verificación del ticket **#CU-104**. Esto demuestra que la navegación de tres recorridos y las seis pantallas funcionales del prototipo integral permiten completar el ciclo de pedido sin instrucciones del moderador, confirmando la hipótesis del diagnóstico de que el usuario necesita encontrar productos rápido, corregir errores y recibir confirmación clara.

> *Evidencia:* [`pruebas/resultados.csv`](pruebas/resultados.csv) — 6 registros con tiempos, cumplimiento y comentarios reales.

---

## Conclusión 2 — Pocos usuarios bastaron para revelar los fallos críticos de modelo mental

El *Cognitive Walkthrough* sin indicación de clics permitió detectar con **sólo dos participantes** los dos problemas que el equipo no había previsto al construir el prototipo: la **expectativa del carrito en el encabezado** (HI-02) y el **temor a borrar un ítem con `[-]`** (HI-01), ambos concentrados en el Usuario 2 mientras el Usuario 1 completó sus tres tareas sin dudas. Esto ratifica el principio de Jakob Nielsen: evaluar con pocos usuarios de forma temprana revela la gran mayoría de los problemas de usabilidad cualitativa. Además, el cruce con el diagnóstico mostró que **cuatro de los cinco riesgos previstos no se presentaron**, lo que ahorra esfuerzo de corrección y confirma la calidad del refinamiento de la Fase 2.

> *Evidencia:* [`pruebas/hallazgos.md`](pruebas/hallazgos.md) — 4 hallazgos priorizados y cruce con los 5 riesgos del diagnóstico; 2 dudas observadas en 6 tareas.

---

## Conclusión 3 — Cada hallazgo se corrigió con un principio HCI explícito y verificable

Las **tres correcciones aplicadas** (acceso dual al carrito → C-01, basurero con confirmación → C-02, insignia de ventanilla exclusiva → C-03) no responden a preferencias estéticas sino a principios verificables: heurísticas **#5, #6 y #7 de Nielsen**, reducción de carga cognitiva y acoplamiento digital–físico de Don Norman. Cada modificación fue **coordinada con el responsable correspondiente** (Sebastián, Wilson y Viviana), **implementada** en el prototipo integral y **verificada** con evidencia visual antes/después, cumpliendo el ciclo completo: hallazgo → justificación → corrección → verificación.

> *Evidencia:* [`iteracion/cambios.md`](iteracion/cambios.md) y [`iteracion/antes-despues.md`](iteracion/antes-despues.md) — correcciones justificadas, verificadas y comparadas.

---

## Síntesis del aprendizaje del equipo

| Aprendizaje | Aplicación en la fase integral |
| :--- | :--- |
| El usuario no asume la ubicación de los controles | Acceso dual al carrito (C-01, HI-02) |
| Toda acción destructiva debe reconocerse y confirmarse | Basurero + diálogo de eliminación (C-02, HI-01) |
| La interfaz debe cerrar el ciclo con el mundo físico | Insignia de ventanilla exclusiva #2 (C-03) |
| Pocas sesiones bien instrumentadas revelan los problemas relevantes | 2 participantes × 3 tareas, sin indicación de clics |

---

## Demostración preparada para la defensa

La demostración de la defensa incluye **un recorrido completo** y **un caso de error**, con sus evidencias:

### 1. Recorrido completo (happy path)

**Inicio → Menú → Detalle del producto → Mi Pedido → Confirmación (#CU-104)**

1. El usuario inicia en **Inicio** y presiona "Ver menú".
2. En **Menú** localiza y selecciona el *Café americano*.
3. En **Detalle** ajusta la cantidad y pulsa "Añadir al pedido".
4. En **Mi Pedido** verifica el resumen ($4,25) y pulsa "Confirmar pedido".
5. El sistema muestra **procesamiento** ("Preparando tu pedido...") y finaliza en **Confirmación** con el ticket **#CU-104** y la insignia de ventanilla exclusiva #2.

**Evidencias:** [`evidencias/flujo/recorrido1.gif`](evidencias/flujo/recorrido1.gif), [`evidencias/flujo/recorrido2.png`](evidencias/flujo/recorrido2.png), [`evidencias/flujo/recorrido3.png`](evidencias/flujo/recorrido3.png)

### 2. Caso de error (prevención y recuperación)

**Acción destructiva accidental → Modal de alerta → Recuperación sin pérdida de datos**

1. En la pantalla de estado, el usuario pulsa accidentalmente **"Cancelar pedido"**.
2. El sistema **no cancela de inmediato**: despliega el **modal "¿Deseas cancelar tu pedido?"** con fondo oscurecido y explicación de consecuencias (se perderá la orden #CU-104).
3. El usuario elige **"Volver al pedido"** (salida de emergencia) y retoma el seguimiento sin alterar su estado; o bien confirma "Sí, cancelar" de forma deliberada.

Este caso corresponde al estado **Error / Prevención** (Heurística #5) y evidencia la protección ante acciones destructivas. Se relaciona además con el hallazgo **HI-01** (ambigüedad del `[-]`), corregido con la solución **C-02** (basurero + confirmación).

**Evidencias:** [`evidencias/pantallas/06_modal.png`](evidencias/pantallas/06_modal.png), [`evidencias/microinteracciones/micro_modal_cancelacion.png`](evidencias/microinteracciones/micro_modal_cancelacion.png), [`evidencias/estados/03_estado_error_recuperacion.png`](evidencias/estados/03_estado_error_recuperacion.png)

### 3. Problema y corrección para mostrar

* **Problema:** HI-01 (Alta) — ambigüedad del `[-]` con 1 unidad, evidenciado por Mateo Morales.
* **Corrección:** C-02 — basurero + diálogo "¿Deseas eliminar?" (Wilson Pillapa), verificada en [`iteracion/cambios.md`](iteracion/cambios.md).

---

## Documentos relacionados

* [`pruebas/protocolo.md`](pruebas/protocolo.md) — protocolo, tareas y guion de sesión.
* [`pruebas/resultados.csv`](pruebas/resultados.csv) — los seis registros de la evaluación.
* [`pruebas/hallazgos.md`](pruebas/hallazgos.md) — hallazgos priorizados y cruce con el diagnóstico.
* [`iteracion/cambios.md`](iteracion/cambios.md) — correcciones coordinadas y verificadas.
* [`iteracion/antes-despues.md`](iteracion/antes-despues.md) — comparación antes/después.
* [`informe_final.pdf`](informe_final.pdf) — informe consolidado con las evidencias de los cuatro integrantes.

---

**☕ CaféU — Conclusiones · APE 4 Integral**
