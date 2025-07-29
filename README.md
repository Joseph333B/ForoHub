# ForoHub
ForoHub crea y elimina tus topicos 

<h1>ForoHub</h1>

<p>ForoHub es una aplicación web desarrollada en Java usando el framework <strong>Spring Boot</strong>. Su objetivo principal es ofrecer una plataforma de foros donde los usuarios pueden crear y responder a temas relacionados con cursos de programación y desarrollo.</p>

<h2>🛠️ Tecnologías Utilizadas</h2>

<h3>Backend</h3>
<ul>
  <li>Java 24</li>
  <li>Spring Boot</li>
  <li>Spring Security</li>
  <li>Spring Data JPA</li>
  <li>Maven</li>
</ul>

<h3>Base de Datos</h3>
<ul>
  <li>MySQL 8.0</li>
  <li>Flyway (para migraciones)</li>
</ul>

<h3>Testing</h3>
<ul>
  <li>Postman (para pruebas de API REST)</li>
</ul>

<h2>🧩 Estructura del Proyecto</h2>

<h3>Entidades principales</h3>

<h4>Usuario</h4>
<ul>
  <li>Campos: id, nombre, correoElectronico, contrasena</li>
  <li>Relaciones: perfiles (uno o muchos)</li>
</ul>

<h4>Perfil</h4>
<ul>
  <li>Representa el rol del usuario (ejemplo: ROLE_USER)</li>
</ul>

<h4>Topico</h4>
<ul>
  <li>Campos: titulo, mensaje, fechaCreacion, status</li>
  <li>Relaciones: autor (Usuario), curso</li>
</ul>

<h4>Curso</h4>
<ul>
  <li>Campos: nombre, categoria</li>
</ul>

<h4>Respuesta</h4>
<ul>
  <li>Campos: mensaje, topico, fechaCreacion, autor, solucion</li>
</ul>

<h2>🔐 Seguridad y Autenticación</h2>

<ul>
  <li>Autenticación con JWT</li>
  <li>Control de acceso por roles (Spring Security)</li>
  <li>Contraseñas encriptadas con BCrypt</li>
</ul>

<h2>📑 Endpoints Principales</h2>

<h3>Autenticación</h3>
<ul>
  <li><code>POST /auth/registrar</code> – Registrar nuevo usuario</li>
  <li><code>POST /auth/login</code> – Iniciar sesión (retorna JWT)</li>
</ul>

<h3>Gestión de Tópicos</h3>
<ul>
  <li><code>GET /topicos</code> – Obtener todos los temas</li>
  <li><code>POST /topicos</code> – Crear nuevo tema</li>
  <li><code>PUT /topicos/{id}</code> – Editar un tema</li>
  <li><code>DELETE /topicos/{id}</code> – Eliminar tema</li>
</ul>

<h3>Respuestas</h3>
<ul>
  <li><code>POST /topicos/{id}/respuestas</code> – Agregar respuesta a un tema</li>
</ul>

<h2>📁 Base de Datos</h2>

<ul>
  <li>Nombre de la BD: <code>forohub</code></li>
  <li>Tablas: usuario, perfil, topico, curso, respuesta, usuario_perfiles, flyway_schema_history</li>
</ul>

<h2>🧪 Datos de Prueba</h2>

<pre><code>{
  "correoElectronico": "angel@gmail.com",
  "contrasena": "123456"
}
</code></pre>

<h2>🚀 Cómo Ejecutar el Proyecto</h2>
<ol>
  <li>Clona el repositorio.</li>
  <li>Crea una base de datos llamada <code>forohub</code> en MySQL.</li>
  <li>Configura tu <code>application.properties</code> con las credenciales de MySQL.</li>

  <li>Ejecuta con: <code>mvn spring-boot:run</code></li>
  <li>Usa Postman para probar los endpoints.</li>
</ol>

<h2>📌 Notas Finales</h2>
<ul>
  <li>Proyecto en fase de desarrollo.</li>
  <li>Incluye datos precargados para pruebas.</li>
  <li>Ideal para aprender sobre APIs REST seguras con Spring Boot.</li>
</ul>


