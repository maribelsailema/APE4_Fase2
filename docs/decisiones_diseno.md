# Justificación de Decisiones de Diseño — CaféU

## 1. Introducción

El refinamiento de los wireframes de CaféU requiere tomar decisiones de diseño que contribuyan a mejorar la experiencia del estudiante durante el proceso de compra.

Estas decisiones deben fundamentarse en principios de Interacción Humano-Computador, considerando la forma en que los usuarios perciben la información, reconocen los controles y comprenden las acciones disponibles.

Para este proyecto se establecen tres decisiones de diseño relacionadas con la organización visual, la consistencia de los componentes y la claridad de la información.

## 2. Objetivo

Justificar tres decisiones de diseño aplicables al refinamiento de los wireframes de CaféU mediante principios de Gestalt, consistencia, accesibilidad y carga cognitiva, con el propósito de mejorar la comprensión de la interfaz y facilitar la realización de pedidos.

---

## 3. Decisión de diseño 1: Agrupación visual de productos e información

### Principio aplicado

**Leyes de Proximidad y Región Común de Gestalt.**

### Situación identificada

En la pantalla de menú de CaféU se presentan varios productos organizados en tarjetas que contienen imagen, nombre, precio y botón para añadir.

En la pantalla de revisión del pedido también se muestran diferentes elementos relacionados con los productos seleccionados.

Para facilitar la comprensión de estas pantallas, es importante que los elementos pertenecientes a un mismo producto permanezcan agrupados visualmente.

### Decisión de diseño

Mantener una organización mediante tarjetas y agrupaciones visuales que permitan identificar claramente qué información corresponde a cada producto.

Se considera:

- Agrupar imagen, nombre, precio y botón de selección.
- Mantener una separación uniforme entre tarjetas.
- Diferenciar el listado de productos del resumen del pedido.
- Conservar una alineación consistente.
- Evitar que elementos de diferentes productos se perciban como relacionados.

### Justificación

La Ley de Proximidad establece que los elementos cercanos tienden a percibirse como parte de un mismo grupo.

Por su parte, la Ley de Región Común señala que los elementos ubicados dentro de un mismo espacio delimitado se interpretan como relacionados.

La aplicación de estos principios facilita el reconocimiento de los productos y reduce el esfuerzo necesario para relacionar cada nombre con su precio y acción correspondiente.

### Resultado esperado

Que el estudiante identifique rápidamente cada producto y comprenda su información sin confundirla con la de otros elementos.

**Pantallas relacionadas:** Menú, detalle de producto y revisión del pedido.

---

## 4. Decisión de diseño 2: Consistencia de botones y controles

### Principios aplicados

**Consistencia visual y reducción de carga cognitiva.**

### Situación identificada

CaféU incluye diferentes acciones durante el proceso de compra, como acceder al menú, añadir productos, modificar cantidades, revisar el pedido y confirmar la compra.

Estas acciones deben mantener un comportamiento y una representación visual coherentes para que el estudiante pueda reconocerlas durante la navegación.

### Decisión de diseño

Establecer un estilo consistente para los componentes que cumplen funciones similares.

Se considera:

- Mantener el mismo estilo en los botones principales.
- Diferenciar visualmente las acciones principales y secundarias.
- Utilizar controles uniformes para aumentar y disminuir cantidades.
- Mantener una ubicación predecible de las acciones de continuación.
- Utilizar etiquetas claras que indiquen la función de cada botón.

### Justificación

La consistencia permite que el usuario aproveche lo aprendido en una pantalla al interactuar con las siguientes.

Cuando los controles conservan una apariencia y ubicación coherentes, disminuye la necesidad de interpretar nuevamente cómo funcionan.

Esto contribuye a reducir la carga cognitiva, especialmente en un contexto como el de una cafetería universitaria, donde el estudiante necesita completar su pedido en poco tiempo.

### Resultado esperado

Que el estudiante reconozca fácilmente los botones y controles, identifique las acciones disponibles y avance por el proceso de compra sin confusiones innecesarias.

**Pantallas relacionadas:** Inicio, menú, detalle de producto y revisión del pedido.

---

## 5. Decisión de diseño 3: Claridad de la información y retroalimentación

### Principios aplicados

**Accesibilidad, jerarquía visual y visibilidad del estado del sistema.**

### Situación identificada

Durante la revisión del pedido, el estudiante necesita comprobar los productos seleccionados, sus cantidades y el total antes de confirmar.

Posteriormente, debe comprender si el sistema recibió correctamente la solicitud.

En los wireframes iniciales se observa un resumen con el total de **$4,25** y una pantalla final con el mensaje **"¡Pedido recibido!"** y el código **#CU-104**.

Estos elementos son importantes porque permiten verificar la compra y reconocer el resultado de la acción.

### Decisión de diseño

Priorizar visualmente la información necesaria para tomar decisiones y comprender el estado del pedido.

Se considera:

- Destacar el valor total en la pantalla de revisión.
- Mantener textos legibles y con contraste adecuado.
- Diferenciar el botón de confirmación de las acciones secundarias.
- Presentar un mensaje de éxito comprensible.
- Mantener visible el código de referencia del pedido.
- Mostrar claramente las indicaciones posteriores a la confirmación.

### Justificación

La accesibilidad visual permite que los textos y controles sean reconocibles y comprensibles para diferentes usuarios.

La jerarquía visual ayuda a dirigir la atención hacia los elementos más importantes de cada pantalla.

Además, el principio de visibilidad del estado del sistema establece que la interfaz debe informar al usuario sobre lo que está ocurriendo.

Por ello, la presentación del total y del mensaje de confirmación contribuye a que el estudiante comprenda el resultado de su interacción.

### Resultado esperado

Que el estudiante pueda revisar correctamente su pedido y reconocer cuándo ha sido recibido, disminuyendo la incertidumbre durante la compra.

**Pantallas relacionadas:** Revisión del pedido y confirmación.

---

## 6. Resumen de decisiones de diseño

| N.º | Decisión | Principios aplicados | Pantallas | Mejora esperada |
|:---:|---|---|---|---|
| 1 | Agrupación visual de productos | Gestalt: proximidad y región común | Menú, detalle y revisión | Facilitar la identificación de información relacionada. |
| 2 | Consistencia de botones y controles | Consistencia y carga cognitiva | Inicio, menú, detalle y revisión | Facilitar el reconocimiento de las acciones. |
| 3 | Claridad de información y retroalimentación | Accesibilidad, jerarquía visual y visibilidad del estado | Revisión y confirmación | Mejorar la comprensión del total y del resultado del pedido. |

## 7. Relación con el refinamiento de wireframes

Las decisiones descritas constituyen criterios para revisar y mejorar las pantallas de CaféU.

Su aplicación debe reflejarse en los diseños refinados y en la comparación visual entre las versiones originales y rediseñadas.

La documentación del refinamiento se encuentra en:

`APE4_Fase2/docs/refinamiento_wireframes.md`

El prototipo correspondiente se encuentra disponible en:

[Prototipo CaféU — Figma](https://www.figma.com/proto/wl3jFYJqHiM852P94kUzlz/cafeU_redise%C3%B1o?node-id=2-636&p=f&t=skNAcfcT0YcAa70l-1&scaling=min-zoom&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=2%3A636)

## 8. Conclusión

Las tres decisiones de diseño propuestas para CaféU se fundamentan en principios de Interacción Humano-Computador que buscan mejorar la organización de la información, la consistencia de los componentes y la claridad de la interacción.

La aplicación de Gestalt permite agrupar los elementos relacionados, mientras que la consistencia contribuye a reducir el esfuerzo necesario para reconocer los controles.

Por otra parte, la accesibilidad y la visibilidad del estado del sistema favorecen la comprensión del pedido y su confirmación.

Estas decisiones servirán como referencia para el refinamiento visual de las pantallas y deberán contrastarse con los cambios efectivamente implementados en Figma y los resultados de las pruebas de usuario.