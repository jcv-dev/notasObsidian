**Integrantes:** Edgar Andrés Vargas, Juan Pablo Escobar Viveros, Juan Camilo Valencia, Manuel Arango 

# 1. ¿Cuáles son las principales fases de la metodología RUP y qué actividades se llevan a cabo en cada una de ellas?
**1. Inicio:**
- **Objetivo:** Establecer las bases del proyecto y definir su alcance.
- **Actividades:**
    - Definir la visión, el alcance y los objetivos del proyecto.
    - Identificar a los interesados y sus necesidades.
    - Establecer un plan de proyecto inicial, incluyendo el cronograma, el presupuesto y los recursos.
    - Establecer el entorno de desarrollo.
    - Definir responsabilidades de miembros.
    - Definir los riesgos del proyecto y las estrategias para mitigarlos.

**2. Elaboración:**
- **Objetivo:** Refinar los requisitos del sistema y diseñar la arquitectura general.
- **Actividades:**
    - Analizar y modelar los requisitos del sistema en detalle.
    - Analizar los riesgos del proyecto.
    - Desarrollar la arquitectura del sistema, incluyendo la asignación de componentes y la definición de interfaces.
    - Diseñar los casos de uso principales.
    - Estimar el tamaño y la complejidad del proyecto.
    - Construir un prototipo inicial del sistema.

**3. Construcción:**
- **Objetivo:** Implementar el sistema y realizar pruebas exhaustivas.
- **Actividades:**
    - Desarrollar los componentes del sistema de acuerdo con el diseño.
    - Realizar pruebas unitarias e integraciones para verificar el correcto funcionamiento del sistema.
    - Corregir errores y defectos encontrados durante las pruebas.
    - Documentar el código y la arquitectura del sistema.
    - Preparar el sistema para su despliegue.

**4. Transición:**
- **Objetivo:** Desplegar el sistema en producción y proporcionar soporte a los usuarios.
- **Actividades:**
    - Instalar y configurar el sistema en el entorno de producción.
    - Capacitar a los usuarios en el uso del sistema.
    - Proporcionar soporte técnico y capacitar a los usuarios.
    - Monitorizar el rendimiento del sistema y realizar correcciones si es necesario.
    - Cerrar el proyecto y realizar una retrospectiva para identificar lecciones aprendidas.

# 2. Describe el enfoque iterativo e incremental de RUP. ¿Cuál es su importancia en el desarrollo de software?
Se caracteriza por dividir el proyecto en ciclos cortos de desarrollo, conocidos como iteraciones. En cada iteración, se completa un conjunto incremental de funcionalidades del sistema, lo que permite obtener retroalimentación temprana y realizar ajustes en el curso del proyecto. Este enfoque es importante porque permite:

- **Reducir de riesgos:** Al dividir el proyecto en iteraciones más pequeñas, se reduce el riesgo de que el proyecto falle.
- **Mejorar calidad:** La retroalimentación temprana permite identificar y corregir errores y defectos en una etapa temprana del proyecto, lo que mejora la calidad del software final.
- **Obtener mayor satisfacción del cliente:** Al involucrar a los interesados y usuarios en el proceso de desarrollo, se aumenta la probabilidad de que el software final cumpla con sus expectativas.
- **Tener más agilidad:** El enfoque iterativo e incremental permite responder rápidamente a los cambios en los requisitos del proyecto.

# 3. Elige un proyecto de desarrollo de software y enumera los roles que estarían involucrados en él según la metodología RUP. ¿Cuáles son las responsabilidades de cada uno de estos roles?
1. **Patrocinador del Proyecto**:
    - Proporcionar la visión general y los objetivos del proyecto.
    - Garantizar la asignación de recursos necesarios.
    - Aprobar el alcance y los hitos del proyecto.
2. **Director del Proyecto**:
    - Dirigir y coordinar todas las actividades del proyecto.
    - Gestionar el equipo y los recursos.
    - Supervisar el cumplimiento de los plazos y presupuestos.
3. **Gerente de Producto**:
    - Definir y priorizar los requisitos del sistema.
    - Mantener la visión del producto y la dirección estratégica.
    - Colaborar con el equipo para asegurar que el producto cumpla con las necesidades del cliente.
4. **Arquitecto de Software**:
    - Diseñar la arquitectura del sistema.
    - Definir estándares y pautas técnicas.
    - Supervisar la implementación para garantizar la integridad arquitectónica.
5. **Analista de Negocios**:
    - Elicitar, analizar y documentar los requisitos del negocio.
    - Colaborar con los interesados para definir casos de uso y escenarios de uso.
    - Validar que el sistema cumpla con los objetivos del negocio.
6. **Diseñador de Interfaz de Usuario (UI/UX Designer)**:
    - Diseñar la interfaz de usuario del sistema.
    - Asegurar la usabilidad y la accesibilidad del sistema.
    - Colaborar con el equipo de desarrollo para implementar el diseño.
7. **Desarrollador de Software**:
    - Implementar las funcionalidades del sistema de acuerdo con los requisitos.
    - Realizar pruebas unitarias y colaborar en pruebas de integración.
    - Mantener y mejorar el código del sistema.
8. **Tester/QA (Aseguramiento de la Calidad)**:
    - Diseñar casos de prueba y realizar pruebas funcionales y de rendimiento.
    - Informar y seguir el seguimiento de los problemas encontrados.
    - Validar que el sistema cumpla con los estándares de calidad definidos.
9. **Usuario Final**:
	- Proporcionar retroalimentación sobre los requisitos y funcionalidades del sistema.
	- Participar en pruebas de aceptación del usuario.
	- Utilizar el sistema en producción y proporcionar comentarios para mejoras futuras.
	- Representar las necesidades y perspectivas de los usuarios finales durante todo el ciclo de desarrollo.

# 4. Selecciona un caso de uso y elabora un diagrama de casos de uso utilizando notación UML. Identifica los actores involucrados, los casos de uso y sus relaciones.

**Casos de Uso:**
1. **Realizar Pedido:**
    - Descripción: Este caso de uso representa el proceso general de realizar un pedido en la tienda online.
    - Actores: Cliente
    - Flujo Principal:
        1. El cliente selecciona los productos que desea comprar.
        2. El cliente agrega los productos seleccionados al carrito de compras.
        3. El cliente procede al proceso de pago.
        4. El cliente confirma el pedido.
    - Flujo Alternativo: Cancelación del Pedido
        1. Si el cliente decide cancelar el pedido en cualquier momento antes de confirmarlo, el pedido se cancela y se regresa a la tienda.