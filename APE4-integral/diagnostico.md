# Diagnóstico de usabilidad — CaféU

## 1. Introducción

CaféU es una propuesta de aplicación orientada a facilitar la realización de pedidos de productos de cafetería. Su propósito es permitir que los estudiantes consulten el menú, seleccionen productos, revisen su pedido y reciban una confirmación mediante una interfaz sencilla y organizada.

Durante la Fase 1 se desarrollaron los requisitos del usuario, la estructura de navegación, los recorridos principales y cinco wireframes que representan el proceso de compra. Posteriormente, en la Fase 2 se trabajó en el refinamiento de las pantallas, las decisiones de diseño y la elaboración de un prototipo en Figma.

La APE 4 Integral retoma estos avances para revisar la experiencia de uso, identificar posibles dificultades y comprobar que el prototipo permita completar las tareas principales. De esta manera, se aprovecha el trabajo anterior y se establecen los aspectos que deben verificarse antes de las pruebas con usuarios.

## 2. Objetivo del diagnóstico

Analizar los diseños y recorridos desarrollados en las Fases 1 y 2 de CaféU para identificar posibles problemas de usabilidad, establecer prioridades de revisión y definir las tareas que serán evaluadas en el prototipo integral.

## 3. Usuario objetivo

La aplicación está dirigida principalmente a estudiantes universitarios que desean consultar y solicitar productos de cafetería mediante una interfaz digital.

El usuario necesita encontrar productos de manera rápida, conocer sus precios, seleccionar cantidades, modificar su pedido cuando sea necesario y confirmar que la solicitud se haya realizado correctamente.

Para responder a estas necesidades, la aplicación debe presentar información clara, controles fáciles de identificar y mensajes que permitan conocer el resultado de cada acción.

## 4. Material revisado

El diagnóstico parte de los entregables desarrollados en las fases anteriores:

**Fase 1**

- Requisito y descripción del usuario.
- Sitemap de la aplicación.
- User flows del proceso de pedido.
- Wireframe de Inicio.
- Wireframe de Menú.
- Wireframe de Detalle de producto.
- Wireframe de Revisar pedido.
- Wireframe de Confirmación.

**Fase 2**

- Refinamiento de los wireframes.
- Decisiones de diseño basadas en principios de interacción humano-computador.
- Prototipo rediseñado en Figma.
- Propuestas de estados, retroalimentación y microinteracciones.

Estos elementos sirven como punto de partida para la evaluación integral. Las funciones implementadas en Figma deberán comprobarse durante la revisión del prototipo.

## 5. Tareas representativas

Se establecieron tres tareas que representan las acciones principales que debe poder realizar un usuario de CaféU.

### Tarea 1. Buscar y seleccionar un producto

**Objetivo:** localizar un producto del menú y agregarlo al pedido.

**Situación:** el estudiante ingresa a CaféU porque desea comprar una bebida.

**Pasos esperados:**

1. Acceder a la pantalla de Inicio.
2. Ingresar al Menú.
3. Buscar o localizar la bebida.
4. Abrir el detalle del producto.
5. Seleccionar la cantidad deseada.
6. Agregar el producto al pedido.

**Resultado esperado:** el producto seleccionado aparece en el resumen del pedido con su cantidad y precio correspondiente.

### Tarea 2. Modificar un pedido

**Objetivo:** corregir un producto o cantidad antes de confirmar la compra.

**Situación:** el estudiante revisa su pedido y se da cuenta de que necesita modificar la cantidad de uno de los productos.

**Pasos esperados:**

1. Acceder a Revisar pedido.
2. Identificar el producto que necesita modificar.
3. Seleccionar la opción de edición.
4. Cambiar la cantidad.
5. Guardar o aplicar la modificación.
6. Verificar que el resumen y el total se actualicen.

**Resultado esperado:** el pedido muestra los cambios realizados y el usuario puede continuar con la compra.

### Tarea 3. Confirmar el pedido

**Objetivo:** completar la compra y comprobar que el pedido fue registrado.

**Situación:** el estudiante ha seleccionado los productos deseados y quiere finalizar su pedido.

**Pasos esperados:**

1. Acceder al resumen del pedido.
2. Revisar los productos y cantidades.
3. Comprobar el total.
4. Seleccionar Confirmar pedido.
5. Esperar la respuesta de la aplicación.
6. Visualizar el mensaje de confirmación.

**Resultado esperado:** se presenta una pantalla de éxito con un mensaje claro y un código de identificación del pedido.

## 6. Revisión de posibles problemas de usabilidad

A partir de los recorridos definidos, se establecieron cinco aspectos prioritarios para revisar en el prototipo integral.

Los siguientes puntos son **riesgos de usabilidad por comprobar**, no errores observados en participantes. Su finalidad es orientar la revisión del prototipo y las pruebas posteriores.

| N.º | Aspecto que se debe comprobar | Posible dificultad | Impacto estimado | Prioridad de revisión |
|---|---|---|---|---|
| 1 | Localización de productos en el Menú | El usuario podría tardar en encontrar el producto deseado si las categorías o la búsqueda no son claras. | Alto | Alta |
| 2 | Identificación de la acción Agregar | El usuario podría tener dudas sobre si el producto fue incorporado al pedido. | Medio | Media |
| 3 | Modificación de cantidades | El usuario podría no identificar cómo corregir un pedido o comprobar el nuevo total. | Alto | Alta |
| 4 | Mensajes de procesamiento y error | El usuario podría desconocer si una acción está en curso o cómo continuar después de un error. | Alto | Alta |
| 5 | Confirmación final del pedido | El usuario podría no distinguir claramente si la compra se completó correctamente. | Alto | Alta |

La prioridad se ha establecido de manera preliminar considerando cuánto podría afectar cada situación al cumplimiento de las tareas. Estos valores deberán revisarse con los resultados de las pruebas.

## 7. Criterios utilizados para priorizar

Para organizar los aspectos de revisión se utilizaron tres niveles:

**Prioridad alta:** situaciones que podrían impedir completar una tarea, generar errores en el pedido o provocar incertidumbre sobre su confirmación.

**Prioridad media:** situaciones que podrían causar dudas, demoras o acciones innecesarias, pero que no necesariamente impedirían finalizar el proceso.

**Prioridad baja:** detalles que podrían afectar la comodidad o presentación de la interfaz sin comprometer directamente el cumplimiento de la tarea.

Esta clasificación inicial permite concentrar la revisión en las funciones más importantes del proceso de compra.

## 8. Relación con las Fases 1 y 2

La Fase 1 permitió establecer qué necesita el usuario y cómo debería organizarse el proceso de pedido. Los cinco wireframes originales representan las pantallas principales y sirven como referencia para identificar los pasos de cada tarea.

La Fase 2 permitió plantear mejoras en la presentación de la información, la organización de controles, la consistencia visual y la retroalimentación de las acciones. El prototipo en Figma constituye la base para comprobar cómo se comportan estos elementos durante la navegación.

En la fase integral no se propone reconstruir estos entregables. Se busca reutilizarlos, verificar su funcionamiento y realizar únicamente los ajustes necesarios.

## 9. Aspectos que deben comprobarse en el prototipo

Antes de realizar las pruebas con usuarios, el equipo deberá verificar que:

1. Existan al menos seis pantallas funcionales.
2. Se puedan completar tres recorridos navegables.
3. Estén representados los estados normal, procesamiento, error y éxito.
4. Exista al menos una microinteracción funcional.
5. Los controles permitan regresar, modificar y confirmar acciones.
6. Los mensajes informen al usuario sobre el resultado de las operaciones.

La comprobación de pantallas y recorridos corresponde al responsable del prototipo. La revisión de estados, heurísticas y accesibilidad corresponde al responsable de evaluación de interfaz.

## 10. Relación con las pruebas de usabilidad

Los aspectos identificados en este diagnóstico servirán como referencia para elaborar el protocolo de evaluación.

Las tres tareas serán realizadas por dos participantes externos al equipo. Durante las pruebas se registrarán los tiempos, el cumplimiento de las tareas, los errores y los comentarios de cada participante.

Con los resultados obtenidos será posible determinar cuáles de los riesgos previstos se presentaron realmente y si existen otros problemas que no se habían considerado.

Las correcciones de la fase integral deberán justificarse mediante estos hallazgos y acompañarse de evidencias antes y después de los cambios.

## 11. Conclusión del diagnóstico

El trabajo desarrollado en las Fases 1 y 2 proporciona una base para continuar con la evaluación integral de CaféU, ya que se dispone de una estructura inicial de navegación, cinco wireframes y una propuesta de rediseño en Figma.

El diagnóstico permitió organizar tres tareas representativas y establecer cinco aspectos prioritarios de revisión relacionados con la búsqueda de productos, la selección, la modificación y la confirmación del pedido.

El siguiente paso consiste en comprobar el funcionamiento del prototipo y realizar pruebas con usuarios para determinar qué dificultades se presentan realmente. A partir de esa información se podrán justificar las mejoras necesarias sin repetir el trabajo desarrollado en las fases anteriores.