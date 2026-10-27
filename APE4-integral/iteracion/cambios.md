# Registro de Cambios — CaféU (APE 4 Integral)

> Correcciones justificadas por los hallazgos de la evaluación, coordinadas con **Viviana Sarco**, **Sebastián Santana** y **Wilson Pillapa**, implementadas en el prototipo y verificadas con evidencia.

---

## 1. Coordinación de las correcciones con el equipo

| Reunión de coordinación | Participantes | Acuerdos |
| :--- | :--- | :--- |
| Priorización de hallazgos | Alex Guachi (coordina), Viviana Sarco, Sebastián Santana, Wilson Pillapa | Se acuerda corregir HI-01 (alta), HI-02 y HI-03 (medias) antes de cerrar la fase; HI-04 queda en backlog |
| Reparto de responsabilidades | Alex → equipo | HI-01 → Wilson; HI-02 → Sebastián; HI-03 → Wilson (colateral con HI-02) |
| Verificación de correcciones | Alex Guachi | Revisión de cada cambio en el prototipo integral y registro antes/después |

---

## 2. Correcciones implementadas y verificadas

### C-01 · Acceso dual al carrito (header con badge + barra flotante)

| Campo | Detalle |
| :--- | :--- |
| **Hallazgo justificante** | **HI-02 (Media)** — Mateo Morales buscó el carrito en la esquina superior derecha antes de notar la barra flotante inferior (Tarea 1) |
| **Problema resuelto** | El usuario no encontraba el acceso al pedido; retraso y fricción en el paso crítico del flujo |
| **Solución aplicada** | Icono de carrito con **badge de contador** en el header superior, sincronizado con la barra flotante inferior (acceso dual) |
| **Justificación HCI** | Heurística **#7 de Nielsen (Flexibilidad y eficiencia de uso)**: satisface el modelo mental web (icono en encabezado) y el uso móvil con una sola mano (barra inferior) |
| **Responsable** | **Sebastián Santana** (prototipado navegable y arquitectura de navegación) |
| **Verificación** | Se comprobó que ambas rutas llevan a `04_Revisar_Pedido` y que el contador se mantiene sincronizado |
| **Estado** | **Verificada** |
| **Evidencia** | [`../evidencias/correcciones/correcciones_h01_h02_h03.png`](../evidencias/correcciones/correcciones_h01_h02_h03.png) |

### C-02 · Icono de basurero y confirmación de eliminación en 1 unidad

| Campo | Detalle |
| :--- | :--- |
| **Hallazgo justificante** | **HI-01 (Alta)** — Mateo Morales dudó si presionar `[-]` con 1 unidad borraría el ítem de golpe (Tarea 2) |
| **Problema resuelto** | Ambigüedad de acción destructiva; temor a perder productos y desconfianza en el carrito |
| **Solución aplicada** | Al llegar a 1 unidad, el `[-]` **muta a icono de basurero** y se abre un **diálogo de confirmación** ("¿Deseas eliminar?"), con botón seguro de retorno |
| **Justificación HCI** | Heurísticas **#5 (Prevención de errores)** y **#6 (Reconocimiento en vez de recuerdo)**; *signifier* claro de acción destructiva según Don Norman |
| **Responsable** | **Wilson Pillapa** (estados, retroalimentación y microinteracciones) |
| **Verificación** | Se comprobó que al llegar a 1 u el `[-]` muta a basurero y que el diálogo protege la acción destructiva |
| **Estado** | **Verificada** |
| **Evidencia** | [`../evidencias/correcciones/correcciones_h01_h02_h03.png`](../evidencias/correcciones/correcciones_h01_h02_h03.png), [`../evidencias/microinteracciones/micro_modal_cancelacion.png`](../evidencias/microinteracciones/micro_modal_cancelacion.png) |

### C-03 · Insignia de retiro "Ventanilla Exclusiva #2" en la confirmación

| Campo | Detalle |
| :--- | :--- |
| **Hallazgo justificante** | Incertidumbre sobre dónde retirar y pagar el pedido (observación transversal de la sesión, trazada como H-03 en la Fase 2 y coherente con el riesgo 5 del diagnóstico) |
| **Problema resuelto** | Instrucción genérica "Paga y retira en caja rápida" sin ubicación precisa; ansiedad al confirmar |
| **Solución aplicada** | Insignia destacada en la confirmación: **"VENTANILLA EXCLUSIVA #2: Pasa directo sin fila, muestra #CU-104"** |
| **Justificación HCI** | Reducción de **carga cognitiva** y cierre de la acción; acoplamiento entre el mundo digital y físico (Don Norman): la interfaz modela el entorno real de la cafetería |
| **Responsable** | **Viviana Sarco** (refinamiento de wireframes, jerarquía visual y contenido de la pantalla de confirmación) |
| **Verificación** | Se comprobó que la confirmación muestra la ubicación exacta de retiro junto al ticket #CU-104 |
| **Estado** | **Verificada** |
| **Evidencia** | [`../evidencias/correcciones/05_Confirmacion.png`](../evidencias/correcciones/05_Confirmacion.png) |

---

## 3. Backlog registrado (fuera del alcance de la corrección inmediata)

| ID | Mejora | Responsable futuro | Estado |
| :---: | :--- | :--- | :--- |
| HI-03 / S-02 | Elevar el contraste del enlace **"+ Seguir comprando"** para superar WCAG 2.1 AA (4,5:1) | Wilson Pillapa | Backlog de accesibilidad; refuerzo colateral con C-01 al retocar la navegación de revisión |
| HI-04 / S-01 | Pago digital directo por QR | Equipo de producto | Backlog de producto, fuera de alcance |

---

## 4. Matriz de verificación de las correcciones

| N.º | Corrección | Hallazgo | Responsable | Verificación realizada | Resultado | Evidencia |
| :---: | :--- | :---: | :--- | :--- | :---: | :--- |
| 1 | Acceso dual al carrito | HI-02 | Sebastián Santana | Ambas rutas llevan a revisar pedido; contador sincronizado | **Verificada** | [`correcciones_h01_h02_h03.png`](../evidencias/correcciones/correcciones_h01_h02_h03.png) |
| 2 | Basurero + confirmación en 1 unidad | HI-01 | Wilson Pillapa | `[-]` muta a basurero; diálogo "¿Deseas eliminar?" protege la acción | **Verificada** | [`correcciones_h01_h02_h03.png`](../evidencias/correcciones/correcciones_h01_h02_h03.png) |
| 3 | Insignia "Ventanilla Exclusiva #2" | H-03 | Viviana Sarco | Confirmación muestra ubicación exacta junto a #CU-104 | **Verificada** | [`05_Confirmacion.png`](../evidencias/correcciones/05_Confirmacion.png) |

> Las tres correcciones exigidas por los criterios de aceptación fueron **aplicadas y verificadas** sobre el prototipo integral.

---

## 5. Relación con los entregables

* Hallazgos que justifican los cambios: [`../pruebas/hallazgos.md`](../pruebas/hallazgos.md)
* Comparación visual antes/después: [`antes-despues.md`](antes-despues.md)
* Resultados de la evaluación: [`../pruebas/resultados.csv`](../pruebas/resultados.csv)
* Conclusiones derivadas: [`../conclusiones.md`](../conclusiones.md)

---

**☕ CaféU — Registro de cambios · APE 4 Integral**
