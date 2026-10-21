# ☕ CaféU — Prototipado Interactivo y Mejora UX

> **APE 4 — Fase 2: Prototipado interactivo, evaluación y mejora UX**  
> **Universidad Técnica de Ambato — FISEI**  
> **Carrera:** Software  
> **Asignatura:** Interacción Humano-Computador (IHC)  
> **Semestre:** Quinto semestre — Paralelo "A"  
> **Grupo:** 1  
> **Año:** 2026

---

## 📌 1. Descripción del proyecto

**CaféU** es un proyecto académico que propone el diseño de una interfaz digital para facilitar la realización de pedidos en una cafetería universitaria.

El sistema está orientado a estudiantes que disponen de poco tiempo durante sus descansos y necesitan consultar el menú, seleccionar productos, revisar su pedido y recibir una confirmación sin depender de la comunicación verbal en una fila concurrida.

En la **Fase 1** se establecieron los requisitos del usuario, la estructura de navegación, los flujos de interacción, los componentes y los wireframes iniciales.

La **Fase 2** se enfoca en transformar estos diseños estáticos en un prototipo interactivo, incorporando estados de interfaz, retroalimentación y microinteracciones. Posteriormente, el prototipo será evaluado con usuarios para identificar dificultades y aplicar mejoras.

---

## 🎯 2. Objetivos

### Objetivo general

Desarrollar y evaluar un prototipo interactivo de CaféU a partir de los wireframes elaborados en la Fase 1, aplicando principios de Interacción Humano-Computador para mejorar la navegación, la comprensión de las acciones y la retroalimentación del sistema.

### Objetivos específicos

1. **Refinar cuatro wireframes** mediante mejoras de jerarquía visual, distribución, tipografía, color y componentes, justificando al menos tres decisiones de diseño con principios de IHC.

2. **Construir un prototipo navegable** en Figma que conecte al menos cuatro pantallas, incluya dos recorridos completos y represente cuatro estados de interfaz y tres microinteracciones.

3. **Evaluar y mejorar el prototipo** mediante dos tareas realizadas por al menos dos usuarios externos al equipo, documentando los hallazgos, las correcciones y tres conclusiones sobre usabilidad.

---

## 🔎 3. Problema de diseño

En una cafetería universitaria, los estudiantes suelen contar con un tiempo limitado para adquirir alimentos y bebidas durante sus descansos.

El proceso tradicional requiere esperar en una fila, comunicar verbalmente el pedido y verificar que los productos solicitados sean correctos.

Esta situación puede ocasionar dificultades como:

- Tiempo limitado para realizar el pedido.
- Confusión al seleccionar productos.
- Errores en cantidades o precios.
- Dificultad para modificar una selección.
- Incertidumbre sobre la recepción del pedido.

### 💡 Solución propuesta

Diseñar una interfaz digital que permita al estudiante realizar su pedido mediante un recorrido claro y comprensible, con controles reconocibles y mensajes que informen el resultado de cada acción.

---

## 👤 4. Usuario objetivo

| Característica | Descripción |
|---|---|
| **Usuario principal** | Estudiante universitario |
| **Edad referencial** | 18 a 25 años |
| **Contexto** | Cafetería universitaria durante los descansos |
| **Dispositivo** | Teléfono móvil |
| **Necesidad** | Realizar pedidos de forma rápida y sencilla |
| **Objetivo** | Seleccionar, revisar y confirmar un pedido |
| **Dificultad principal** | Poco tiempo disponible y necesidad de evitar errores |

### Escenario de uso

Un estudiante desea adquirir un café americano y un sanduche durante su descanso.

| Producto | Cantidad | Precio |
|---|:---:|---:|
| Café americano | 1 | $1,50 |
| Sanduche | 1 | $2,75 |
| **Total** | | **$4,25** |

El estudiante debe poder revisar los productos, editar el pedido si es necesario y confirmar la solicitud.

---

## 📱 5. Funcionalidades del prototipo

El prototipo contempla las siguientes funcionalidades:

| Funcionalidad | Descripción |
|---|---|
| **Consultar menú** | Visualizar productos, precios y opciones disponibles. |
| **Seleccionar productos** | Agregar productos y cantidades al pedido. |
| **Revisar pedido** | Consultar los productos seleccionados y el total. |
| **Editar pedido** | Modificar cantidades o eliminar productos. |
| **Confirmar pedido** | Enviar la solicitud mediante una acción identificable. |
| **Visualizar estados** | Mostrar procesamiento, errores y confirmaciones. |
| **Recibir retroalimentación** | Informar si el pedido fue recibido correctamente. |

### Recorridos principales

**Recorrido 1 — Confirmación del pedido**

`Menú → Seleccionar productos → Revisar pedido → Confirmar → Pedido recibido`

**Recorrido 2 — Edición del pedido**

`Menú → Seleccionar productos → Revisar pedido → Editar → Revisar nuevamente → Confirmar`

Ambos recorridos deberán implementarse y verificarse en el prototipo navegable.

---

## 🧠 6. Principios de IHC aplicados

| Principio | Aplicación |
|---|---|
| **Gestalt** | Agrupación de productos, información y acciones relacionadas. |
| **Consistencia** | Uso uniforme de botones, tipografía, componentes y navegación. |
| **Accesibilidad** | Controles legibles, contraste adecuado y acciones comprensibles. |
| **Carga cognitiva** | Reducción de información innecesaria y simplificación del recorrido. |
| **Visibilidad del estado del sistema** | Mensajes claros durante el procesamiento y la confirmación. |
| **Prevención de errores** | Revisión y modificación del pedido antes de confirmar. |
| **Retroalimentación** | Comunicación de acciones exitosas, errores y cambios de estado. |

---

## 🔄 7. Metodología de desarrollo

El proyecto se organiza en cinco actividades.

### Fase 1. Refinamiento de wireframes

Se recuperarán los cuatro wireframes desarrollados anteriormente y se verificará su coherencia con los requisitos, sitemap y flujos de usuario.

Se aplicarán mejoras de jerarquía visual, distribución, tipografía, color y componentes.

**Producto:** Cuatro pantallas refinadas, comparación antes/después y tres decisiones de diseño justificadas.

### Fase 2. Prototipo navegable

Se conectarán al menos cuatro pantallas en Figma, implementando dos recorridos completos.

Se configurarán botones, menús, enlaces, opciones de regreso, cancelación y confirmación.

**Producto:** Prototipo interactivo navegable con enlace funcional.

### Fase 3. Estados y microinteracciones

Se representarán los cuatro estados requeridos:

- **Inicial:** interfaz lista para recibir acciones.
- **Procesamiento:** sistema ejecutando una solicitud.
- **Error:** comunicación de una dificultad o validación incorrecta.
- **Éxito:** confirmación de una acción completada.

También se diseñarán al menos tres microinteracciones relacionadas con selección, transición o progreso.

**Producto:** Capturas y descripción de estados, feedback y microinteracciones.

### Fase 4. Prueba cognitiva con usuarios

Se definirán dos tareas representativas y se evaluará el prototipo con al menos dos participantes externos al equipo.

Durante la prueba se registrarán el cumplimiento de las tareas, las dudas y los errores observados, sin indicar a los participantes dónde hacer clic.

**Producto:** Matriz de pruebas, hallazgos y propuestas de mejora.

### Fase 5. Corrección y conclusiones

Se priorizarán los problemas identificados y se corregirán al menos tres hallazgos cuando existan.

Se documentará la comparación entre la versión inicial y la corregida, justificando los cambios.

**Producto:** Prototipo corregido, matriz de mejoras, tres conclusiones e informe PDF.

---

## 👥 8. Equipo de trabajo

| N.º | Integrante | Usuario GitHub | Correo institucional | Responsabilidad |
|:---:|---|---|---|---|
| **1** | Sarco Sailema Viviana Maribel | [@maribelsailema](https://github.com/maribelsailema) | `vsarco7769@uta.edu.ec` | Refinamiento de wireframes |
| **2** | Santana Durán Sebastián Israel | [@Sebaslsd](https://github.com/Sebaslsd) | `ssantana1312@uta.edu.ec` | Prototipado navegable |
| **3** | Pillapa Tubón Wilson Joseph | [@W1LSONN](https://github.com/W1LSONN) | `wpillapa8482@uta.edu.ec` | Estados y microinteracciones |
| **4** | Guachi Aucapiña Alex Fabricio | [@A1EXF6A](https://github.com/A1EXF6A) | `aguachi4414@uta.edu.ec` | Evaluación, correcciones y documentación |

---

## 📋 9. Distribución de actividades

| Issue | Responsable | Actividad | Entregable principal |
|:---:|---|---|---|
| **#1** | Viviana | Refinar cuatro wireframes y justificar decisiones de IHC. | Pantallas refinadas y comparativa |
| **#2** | Sebastián | Construir el prototipo navegable y dos recorridos. | Enlace Figma y documentación de flujos |
| **#3** | Wilson | Diseñar estados, feedback y tres microinteracciones. | Capturas y descripción |
| **#4** | Alex | Ejecutar pruebas, registrar hallazgos, coordinar correcciones y consolidar resultados. | Matriz de pruebas, mejoras y PDF |

> Las actividades requieren colaboración. Los responsables de diseño y prototipado deberán aplicar las correcciones identificadas durante la evaluación.

---

## 📁 10. Estructura del repositorio

```text
Grupo_1_Tutoria_Facil_UTA/
│
├── README.md
│
├── APE4-Fase1/
│   └── 01_requisito_usuario.md
│
└── APE4_Fase2/
    │
    ├── docs/
    │   ├── refinamiento_wireframes.md
    │   ├── decisiones_diseno.md
    │   ├── recorridos_prototipo.md
    │   ├── estados_microinteracciones.md
    │   ├── prueba_cognitiva.md
    │   ├── matriz_mejoras.md
    │   └── conclusiones.md
    │
    ├── wireframes/
    │   ├── originales/
    │   └── refinados/
    │
    ├── prototipo/
    │   └── enlace_figma.md
    │
    ├── evidencias/
    │   ├── estados/
    │   ├── microinteracciones/
    │   ├── pruebas/
    │   └── antes_despues/
    │
    └── resultados/
        └── informe_final.pdf
```

### Organización de archivos

| Ubicación | Contenido |
|---|---|
| `APE4-Fase1/` | Requisitos y documentación previa disponible. |
| `APE4_Fase2/docs/` | Documentación técnica, pruebas, decisiones y conclusiones. |
| `APE4_Fase2/wireframes/` | Cuatro wireframes originales y refinados. |
| `APE4_Fase2/prototipo/` | Enlace al prototipo interactivo en Figma. |
| `APE4_Fase2/evidencias/` | Capturas de estados, microinteracciones, pruebas y comparaciones. |
| `APE4_Fase2/resultados/` | Informe PDF consolidado. |

---

## 🛠️ 11. Herramientas utilizadas

| Herramienta | Utilidad |
|---|---|
| **Figma** | Diseño de interfaces, componentes, conexiones y prototipos interactivos. |
| **GitHub** | Organización del repositorio, Issues y colaboración. |
| **Git / GitHub Desktop** | Control de versiones y sincronización de archivos. |
| **Markdown** | Documentación técnica y académica. |
| **PDF** | Presentación de resultados, evidencias y conclusiones. |

---



## 📚 12. Conclusiones

Las conclusiones definitivas se incorporarán después de realizar la prueba cognitiva y aplicar las correcciones al prototipo.

La evaluación permitirá determinar si los recorridos diseñados son comprensibles, si los estados y mensajes facilitan la interacción y qué decisiones contribuyen a mejorar la experiencia del usuario.

Los resultados y las tres conclusiones finales se documentarán en `APE4_Fase2/docs/conclusiones.md`.

---



**☕ CaféU — Prototipado interactivo, evaluación y mejora UX**

*Proyecto académico enfocado en el diseño centrado en el usuario, la navegación interactiva y la mejora de interfaces mediante pruebas de usabilidad.*