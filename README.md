# Calculator

- Crear entorno de trabajo utilizando Maven `4.0.0`, Sprint Boot `3.0.3` y Java `17` más otras dependencias utiles encontradas dentro del pom.xml.

- Importar librerías externas __tracer.jar__ de la carpeta _.libs_ a través del __pom.xml__.

- Preparar una arquitectura hexagonal del proyecto con lo que desarollar posteriormente.

- Crar una clase principal ejecutadora del programa en si, un modelo de la estructura de calculadora, una interfaz e implementación sobre la que interactuará con el tracer y el repositorio JPA para la posterior gestión de operaciones registradas, y un controlador que estará escuchando las consultas de suma y resta por sus respectivos end-point.

- Agregar en el application.properties persistencia de datos utilizando H2 como gestor de pruebas, "lo dejé en (create-drop)".

- Implementar nuevas consultas básicas de CRUD para sacar mayor provecho al proyecto. También un paquete para errores personalizados.

- Asignar al puerto 8087 evitando estar utilizándose. Más guardar en la carpeta __.run__ las ejecuciones de Maven para el empaquetado del proyecto a _.jar_ y el Run para el despliegue local desde el IDE.

- Pasar los tests unitarios utilizando JUnit y la librería Mockito.

- Las consultas están construidas con parámetros de entrada, los campos first y second, para introducir el número deseado.

- Adjunto varios ejemplos de consultas tanto con ResponseEntity como del mismo objecto modelo:

ResponseEntity
- http://localhost:8087/api/v1/calculator/add?first=17&second=23
- http://localhost:8087/api/v1/calculator/subtract?first=17&second=23

Objects
- http://localhost:8087/api/v1/calculator/all
- http://localhost:8087/api/v1/calculator/id/1
- http://localhost:8087/api/v1/calculator/remove/1