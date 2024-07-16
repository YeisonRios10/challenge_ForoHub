🗨️ ForoHub
Bienvenidos a ForoHub, un proyecto desafiante y emocionante que he desarrollado como parte de mi aprendizaje en desarrollo backend con Java y Spring Boot. En este proyecto, he implementado un foro completamente funcional donde los usuarios pueden crear, listar y eliminar tópicos, con seguridad basada en JSON Web Tokens (JWT).

🚀 Tecnologías Utilizadas
Java JDK: versión 17 en adelante
Maven: versión 4 en adelante
Spring Boot: versión 3 en adelante
MySQL: versión 8 en adelante
IDE: IntelliJ IDEA (opcional)
📦 Dependencias del Proyecto
Al crear el proyecto con Spring Initializr, he agregado las siguientes dependencias:

Lombok
Spring Web
Spring Boot DevTools
Spring Data JPA
Flyway Migration
MySQL Driver
Validation
Spring Security
⚙️ Configuración del Proyecto
Variables de Entorno
Para mejorar la seguridad y flexibilidad, he utilizado variables de entorno para almacenar las credenciales de la base de datos y el secreto de JWT. Asegúrate de definir estas variables en tu entorno antes de ejecutar la aplicación.

properties
Copiar código
spring.application.name=foro_hub

spring.datasource.url=jdbc:mysql://localhost/foro_hub
spring.datasource.username=root
spring.datasource.password=${DB_PASS}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

server.error.include-stacktrace=never

api.security.secret=${JWT_SECRET}
Base de Datos
He utilizado MySQL para la base de datos. Asegúrate de que MySQL esté instalado y configurado en tu máquina. Puedes cambiar el nombre de la base de datos y la contraseña en las variables de entorno DB_NAME y DB_PASS.

🧪 Pruebas con Insomnia
Para probar los endpoints de nuestra aplicación, he utilizado Insomnia. Aquí les dejo algunos ejemplos de las pruebas realizadas:

Listar Tópicos

Endpoint: GET /localhost:8080/topicos
Descripción: Obtiene una lista de todos los tópicos creados.
Respuesta: Lista de tópicos en formato JSON.
Crear Tópico

Endpoint: POST /localhost:8080/topicos
Descripción: Crea un nuevo tópico. Se requiere autenticación.
Body: JSON con los campos userId, mensaje, curso, y titulo.
Respuesta: Tópico creado con un status 201 (Created).
Autenticación

Endpoint: POST /localhost:8080/auth
Descripción: Autentica un usuario y devuelve un JWT.
Body: JSON con email y password.
Respuesta: JWT en formato Bearer Token.
Eliminar Tópico

Endpoint: DELETE /localhost:8080/topicos/{id}
Descripción: Elimina un tópico por su ID. Se requiere autenticación.
Respuesta: Status 200 (OK).
🗂️ Gestión del Proyecto
Para la gestión del proyecto, he utilizado Trello. He dividido el problema grande en pequeños problemas manejables y los he organizado en tarjetas en mi tablero de Trello. Esto me ha permitido llevar un seguimiento detallado de mi progreso y mantenerme organizado durante todo el desarrollo.

✨ Conclusión
Este proyecto ha sido un desafío muy interesante y una gran oportunidad para aplicar y consolidar mis conocimientos en desarrollo backend con Java y Spring Boot. Estoy emocionado por seguir mejorando y personalizando ForoHub. Si tienes alguna pregunta o sugerencia, no dudes en compartirla. ¡Gracias por visitar mi repositorio!
