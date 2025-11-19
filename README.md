📖 Sistema de Gestión de Revistería Maribel (SGIV-RM)
📌 Resumen del Proyecto
Este repositorio contiene la Base de Datos Relacional maribel_revisteria, diseñada para gestionar el inventario, las transacciones de venta/compra y la auditoría de precios de una revistería con múltiples sucursales.

El proyecto cumple con la Tercera Forma Normal (3NF) y está implementado en MySQL.
🛠️Estructura y Tecnología
Tecnología Utilizada
SGBD: MySQL (8.0+)

Lenguaje: SQL

Control de Versiones: Git / GitHub

Componentes Clave
El diseño se compone de 15 tablas y cumple con los siguientes requisitos de integridad y seguridad:

Normalización: Aplicación estricta de la 3NF para eliminar la redundancia de datos.

Borrado Lógico: Implementado en las tablas publicacion y usuario mediante el campo activo (1=activo, 0=inactivo).

Auditoría: Se utiliza la tabla precio_historial y un Trigger para registrar automáticamente cada cambio de precio en una publicación.

Carga de Datos: El script incluye la carga de más de 100 registros en la tabla detallemovimiento para simular la operación real y probar las consultas jerárquicas.

⚙️Instalación y UsoA. Carga de la Base de DatosAbre tu cliente MySQL (Workbench, DBeaver, línea de comandos).Crea una base de datos con el nombre maribel_revisteria.Ejecuta el script completo maribel_revisteria.sql. Esto creará todas las tablas, insertará los datos de prueba, y establecerá el Trigger.B. Seguridad y Accesos OperativosEl script incluye la creación de un usuario con permisos limitados para operaciones diarias.UsuarioContraseñaPermisosmaribel_DCdc1234SELECT, INSERT, UPDATE, DELETE sobre la BD maribel_revisteria.*
Para conectar: mysql -u maribel_DC -p

Autor
Autor: [Francisco Lucas Arias]

Email: [46525066populorumjujuy.ar]
