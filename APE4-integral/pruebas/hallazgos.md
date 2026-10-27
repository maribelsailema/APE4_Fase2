# Hallazgos de Usabilidad — CaféU (APE 4 Integral)

## 1. Resumen de resultados

| Indicador | Resultado |
| :--- | :--- |
| Participantes externos al equipo | **2** (Bryan Ortiz, Mateo Morales) |
| Tareas por participante | **3** |
| Registros totales | **6** (2 × 3) |
| Tareas completadas | **6 / 6 (100 %)** |
| Errores que impidieron completar la tarea | **0** |
| Dudas registradas | **2** (ambas del Usuario 2) |
| Tiempo promedio de tarea | **8,0 segundos** (rango: 5–19 s) |
| Dificultad reportada | Baja (Usuario 1) / Media (Usuario 2) |

**Fuente:** [`resultados.csv`](resultados.csv) · **Evidencia narrativa:** [`../evidencias/pruebas/registro_pruebas.md`](../evidencias/pruebas/registro_pruebas.md)

---

## 2. Hallazgos identificados y priorizados

| ID | Hallazgo | Severidad | Participante (Tarea) | Impacto | Prioridad |
| :---: | :--- | :---: | :--- | :--- | :---: |
| **HI-01** | Ambigüedad en el selector de cantidad: con 1 unidad el `[-]` no deja claro si borrará el ítem | **Alta** | Mateo Morales (T2) | Temor a perder productos y desconfianza en el carrito; la duda detuvo la acción | **1** |
| **HI-02** | El acceso al carrito sólo se percibe en la barra flotante inferior; el usuario busca el icono en el encabezado | **Media** | Mateo Morales (T1) | Retraso en llegar al carrito; fricción en el paso crítico del pedido | **2** |
| **HI-03** | Contraste insuficiente del enlace **"+ Seguir comprando"** en la revisión del pedido | **Media** | Bryan Ortiz (T2) | Dificultad leve de lectura; posible pase WCAG AA dudoso | **3** |
| **HI-04** | Ausencia de pago digital por QR (sugerencia de evolución) | **Baja** | Bryan Ortiz (T1) | Fuera del alcance actual; backlog de producto | **4** |

**Criterio de priorización:** severidad del daño potencial (pérdida de datos > fricción > estética), frecuencia de aparición en las sesiones y correspondencia con heurísticas de Nielsen.

> **Trazabilidad con la Fase 2:** HI-01 ≡ H-02, HI-02 ≡ H-01, HI-03 ≡ S-02, HI-04 ≡ S-01 de [`../../docs/matriz_mejoras.md`](../../docs/matriz_mejoras.md). Los identificadores `HI-` corresponden a la numeracisón integral.

---

## 3. Detalle de cada hallazgo

### HI-01 · Ambigüedad del stepper `[-]` con 1 unidad — Severidad: Alta

* **Tarea:** T2 (modificar el pedido o corregir una cantidad).
* **Observación:** al llegar a 1 unidad, Mateo dudó si presionar `[-]` **borraría el ítem de golpe**. La duda detuvo su acción hasta que comprendió el control por sí mismo.
* **Modelo mental esperado:** todo control que aparenta una acción destructiva debe reconocerse como tal y confirmarse (Heurísticas **#5 Prevención de errores** y **#6 Reconocimiento en vez de recuerdo**; *signifier* claro según Don Norman).
* **Riesgo:** pérdida accidental de productos y desconfianza en el carrito.
* **Estado:** corregido y verificado → [`../iteracion/cambios.md`](../iteracion/cambios.md) (C-02).

### HI-02 · Ubicación del acceso al carrito — Severidad: Media

* **Tarea:** T1 (buscar y seleccionar un producto).
* **Observación:** Mateo **buscó el carrito en la esquina superior derecha** antes de notar la barra flotante inferior; se recuperó de forma autónoma, pero el tiempo de localización aumentó.
* **Modelo mental esperado:** convención aprendida en otras aplicaciones: icono de carrito con contador en el encabezado (Heurística **#7 Flexibilidad y eficiencia de uso**).
* **Riesgo:** retraso y fricción en el paso crítico del pedido.
* **Estado:** corregido y verificado → [`../iteracion/cambios.md`](../iteracion/cambios.md) (C-01).

### HI-03 · Contraste del enlace "+ Seguir comprando" — Severidad: Media

* **Tarea:** T2 (modificar el pedido).
* **Observación:** Bryan sugirió **incrementar el contraste** del enlace de continuidad en la pantalla de revisar pedido.
* **Criterio afectado:** contraste WCAG 2.1 AA (4,5:1 para texto regular).
* **Estado:** registrado como backlog de accesibilidad (S-02 en Fase 2); su tratamiento colateral se describe en [`../iteracion/cambios.md`](../iteracion/cambios.md).

### HI-04 · Pago digital por QR — Severidad: Baja

* **Tarea:** sugerencia transversal.
* **Observación:** Bryan propuso añadir **pago digital directo por QR** en futuras versiones.
* **Estado:** backlog de producto, fuera del alcance de la fase integral (S-01 en Fase 2).

---

## 4. Cruce con los riesgos preliminares del diagnóstico

El [`../diagnostico.md`](../diagnostico.md) (sección 6) estableció cinco aspectos prioritarios a comprobar. El cruce con los resultados reales determina cuáles se confirmaron:

| N.º | Riesgo preliminar del diagnóstico | Prioridad prevista | Resultado en la prueba | Evidencia |
| :---: | :--- | :--- | :--- | :--- |
| 1 | Localización de productos en el Menú | Alta | **No se presentó**: ambos participantes localizaron y agregaron productos (T1 completada en 6 s por ambos) | `resultados.csv`, T1 |
| 2 | Identificación de la acción "Agregar" | Media | **No se presentó**: 0 dudas y 0 errores en T1/T2 para ambos participantes | `resultados.csv` |
| 3 | Modificación de cantidades | Alta | **Sí se presentó (HI-01)**: ambigüedad del `[-]` con 1 unidad | `resultados.csv`, Mateo T2 |
| 4 | Mensajes de procesamiento y error | Alta | **No se presentó**: la confirmación se verificó sin bloqueos (T3 en 5 s por ambos) | `resultados.csv`, T3 |
| 5 | Confirmación final del pedido | Alta | **No se presentó**: ambos verificaron el ticket #CU-104 | `resultados.csv`, T3 |

**Conclusión del cruce:** de los cinco riesgos previstos, **uno se confirmó con evidencia empírica** (HI-01) y dos riesgos no previstos en el diagnóstico aparecieron como observación directa del participante (HI-02, HI-03). El riesgo 1 (localización) resultó innecesario: el prototipo de Fase 2 ya lo había resuelto.

---

## 5. Relación hallazgo → corrección

| Hallazgo | Corrección | Responsable | Verificación |
| :---: | :--- | :--- | :--- |
| **HI-01** | C-02 · Icono de basurero + diálogo de confirmación en 1 unidad | Wilson Pillapa | [`../iteracion/cambios.md`](../iteracion/cambios.md) |
| **HI-02** | C-01 · Acceso dual al carrito (header con badge + barra flotante) | Sebastián Santana | [`../iteracion/cambios.md`](../iteracion/cambios.md) |
| **HI-03** | S-02 · Backlog de contraste (refuerzo colateral con C-01) | Wilson Pillapa | [`../iteracion/cambios.md`](../iteracion/cambios.md) |
| **HI-04** | S-01 · Backlog de producto (pago QR) | — | Fuera de alcance |

---

## 6. Evidencias asociadas

* [`resultados.csv`](resultados.csv) — los seis registros con tiempos, cumplimiento, dudas, errores y comentarios.
* [`../evidencias/pruebas/matriz_registro_pruebas.png`](../evidencias/pruebas/matriz_registro_pruebas.png) — matriz de registro oficial renderizada.
* [`../evidencias/pruebas/registro_pruebas.md`](../evidencias/pruebas/registro_pruebas.md) — registro narrativo de las sesiones.
* Pantallas evaluadas: [`01_Inicio.png`](../evidencias/pruebas/01_Inicio.png), [`02_Menu.png`](../evidencias/pruebas/02_Menu.png), [`03_Detalle_Producto.png`](../evidencias/pruebas/03_Detalle_Producto.png), [`04_Revisar_Pedido.png`](../evidencias/pruebas/04_Revisar_Pedido.png), [`05_Confirmacion.png`](../evidencias/pruebas/05_Confirmacion.png).

---

**☕ CaféU — Hallazgos de usabilidad · APE 4 Integral**
