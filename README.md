![Zona Fit](./logo.png)

# 💪 Zona Fit - Sistema de Gestión para Gimnasio

**Zona Fit** es una aplicación web desarrollada en **Java con Spring Boot** y **JSF (Jakarta Faces)** con soporte de **PrimeFaces**, diseñada para la administración de clientes de un gimnasio. Permite realizar operaciones CRUD (crear, leer, actualizar, eliminar) sobre los registros de clientes, con una interfaz moderna y responsiva.

---

## 🚀 Tecnologías utilizadas

- **Java 21**
- **Spring Boot 3**
- **Jakarta EE (JSF 4.0.2)**
- **PrimeFaces 13 (Jakarta Edition)**
- **Hibernate JPA** (persistencia con base de datos)
- **MySQL** (motor de base de datos)
- **CDI / @ViewScoped** (gestión del ciclo de vida en JSF)
- **Tomcat 10.1.11** (servidor embebido)
- **Maven** (gestión de dependencias)

---

## 📄 Características

- ✅ Listado de clientes con tabla interactiva.
- ➕ Alta de nuevos clientes mediante un modal PrimeFaces.
- 📝 Edición de datos de clientes existentes.
- ❌ Eliminación de registros con feedback visual.
- 📦 Comunicación entre backend (Spring Boot) y frontend (JSF) mediante inyección de dependencias y `@Component`.
- 🔄 Actualización dinámica de la vista con AJAX (PrimeFaces).

---

## 🧠 Estructura principal

### Controlador `IndexControlador.java`

Controlador de vista (`@ViewScoped`) que:
- Carga la lista de clientes desde el servicio (`IClienteServicio`).
- Permite agregar, editar y eliminar clientes.
- Interactúa con la interfaz JSF utilizando `FacesContext` y `PrimeFaces`.

### Vista `index.xhtml`

- Tabla con `p:dataTable` para mostrar los clientes.
- Modal PrimeFaces (`p:dialog`) para agregar o editar clientes.
- Mensajes visuales (`p:messages`) para notificaciones del sistema.
- Botones de acción con integración JSF-PrimeFaces.

---

## 📂 Cómo ejecutar el proyecto

1. Clona este repositorio:
   ```bash
   git clone https://github.com/ivanfr12/ZonaFit-Gym-_web.git

   Abre el proyecto en tu IDE favorito (IntelliJ IDEA, Eclipse).

Asegúrate de tener configurada una base de datos MySQL.

Configura application.properties con tus credenciales de BD.

Ejecuta la aplicación desde ZonaFitWeb.java o mediante Maven:
mvn spring-boot:run
📌 Notas
El sistema está preparado para ser extendido con autenticación y gestión de entrenadores, rutinas o pagos.

Usa anotaciones @PostConstruct, @Autowired, @ViewScoped y @Component para una integración fluida entre Spring Boot y JSF.

🧑‍💻 Autor
Desarrollado por Ivan como parte del programa de formación Java con Alura Latam y Oracle.

📃 Licencia
Este proyecto es de código abierto y está disponible bajo la licencia MIT.
