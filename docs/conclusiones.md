# Conclusiones — CaféU · Fase 2

> Tres conclusiones sobre **usabilidad y aprendizaje** derivadas de la evaluación del prototipo interactivo de CaféU con participantes externos al equipo, de la comparación entre versión inicial y corregida y de la aplicación de principios de Interacción Humano-Computador.

---

## Conclusión 1 — De diseños estáticos a experiencias verificables

La evolución de wireframes estáticos a un prototipo navegable con microinteracciones y estados explícitos **no es un mero refinamiento cosmético, sino una validación empírica del modelo mental del usuario**. Incorporar retroalimentación reactiva (botón "Enviando orden…", banner de error con "Reintentar envío", checkmark animado de éxito) y visibilidad del estado reduce sustancialmente el abismo de ejecución y evaluación teorizado por Donald Norman, aportando certidumbre en transacciones monetarias y de tiempo crítico como es el pedido de café durante un receso.

> *Evidencia:* las cuatro tareas ejecutadas por los participantes terminaron en confirmación (#CU-104) sin errores bloqueantes, pese a tratarse de un flujo con pago y tiempo de espera.

---

## Conclusión 2 — Eficiencia metodológica de las pruebas con pares

El *Cognitive Walkthrough* rápido demostró ser un instrumento de diagnóstico sumamente eficiente: **dos sesiones con pares ajenos al diseño permitieron identificar fallos sutiles pero críticos** —como la expectativa de encontrar el carrito en la parte superior o el temor a borrar un ítem con `[-]`— que el equipo no había detectado al construir el prototipo. Esto ratifica el principio de Jakob Nielsen: evaluar con pocos usuarios de forma temprana revela la gran mayoría de los problemas de usabilidad cualitativa, siempre que se respete la condición de no indicar dónde hacer clic.

> *Evidencia:* 4/4 tareas completadas, 2 dudas registradas y 3 hallazgos priorizables derivados de sólo 30 minutos de prueba.

---

## Conclusión 3 — Convergencia entre principios HCI y accesibilidad

La aplicación sistemática de las directrices **WCAG 2.1** (contraste superior a 14:1 y áreas táctiles de 44×44 px), combinada con las **leyes de la Gestalt** (región común y proximidad) y las **heurísticas de Nielsen** (#1, #5, #6 y #7), demostró que la usabilidad universal beneficia a todos los usuarios: cada hallazgo observado se corrigió apelando a un principio explícito y verificable, no a preferencias estéticas. Un diseño legible y libre de fricción motora permite a los estudiantes ordenar con rapidez bajo la presión del receso universitario.

> *Evidencia:* H-01, H-02 y H-03 corregidos y verificados con justificación HCI documentada en [`matriz_mejoras.md`](matriz_mejoras.md).

---

## Síntesis del aprendizaje del equipo

| Aprendizaje | Aplicación en la Fase 2 |
| :--- | :--- |
| El usuario no asume implícitamente la ubicación de los controles | Acceso dual al carrito (H-01) |
| Toda acción destructiva debe reconocerse y confirmarse | Basurero + diálogo de eliminación (H-02) |
| La interfaz debe cerrar el ciclo con el mundo físico | Insignia de ventanilla exclusiva #2 (H-03) |
| Pocas sesiones bien instrumentadas revelan los problemas relevantes | 2 participantes × 2 tareas, sin indicación de clics |

---

## Documentos relacionados

* [`prueba_cognitiva.md`](prueba_cognitiva.md) — tareas, participantes, registro y matriz de pruebas.
* [`matriz_mejoras.md`](matriz_mejoras.md) — priorización, correcciones y comparación antes/después.
* [`../resultados/informe_final.pdf`](../resultados/informe_final.pdf) — informe consolidado de la Fase 2.

---

