# comp4260-Proyecto-Tarea
📌 Proyecto Final de comp4260

Jacob J. Desuza Martinez R00621190 jdesuza1190@arecibointer.edu

🎯 Descripción General

Es una aplicación web de gestión de tareas. Permite a los usuarios interactuar con una interfaz para ver una lista que podras agregar, marcar y eliminar alguna de ellas. Todo el sistema está conectado a una base de datos SQL Server, lo que garantiza que la información no se pierda al cerrar la aplicación.

Esta dirigida a estudiantes y personas que buscan una herramienta sencilla y minimalista para organizar sus actividades diarias.

Ayuda a combatir la falta de organización y el olvido de responsabilidades. Al digitalizar las tareas, elimina la necesidad de notas en papel y permite una gestión rápida desde cualquier navegador.

💭Servicios de Azure Utilizados

1. Azure App Service-Alojamiento de la app web
2. Azure Sql Database-Almacenar los datos del sistema
3. Azure Storage Account-Guardar archivos cargados por usuarios
4. Github-Documentacion y Instrucciones del Proyecto
5. Flask-Puente entre el usuario y la base de datos en la nube.

🧱 Diagrama de Arquitectura

<img width="976" height="467" alt="image" src="https://github.com/user-attachments/assets/281fd2d5-7af8-4319-96f3-c872392bb088" />

⚙️ Despliegue y Configuración

Para ejecutar la aplicación en tu entorno de desarrollo antes del despliegue, sigue estos pasos:

Instalación de dependencias: Debes instalar Flask y PyODBC utilizando un gestor de paquetes, asegurándote de tener instalado el ODBC Driver 18 for SQL Server en tu sistema operativo.

Configuración de variables de entorno: Define localmente las variables SQL_SERVER, SQL_DATABASE, SQL_USERNAME y SQL_PASSWORD para que la aplicación pueda autenticarse sin exponer credenciales en el código.

Ejecución y prueba: Inicia el servidor mediante el comando python app.py, lo cual activará el modo de depuración y creará automáticamente la tabla tasks si no existe en la base de datos vinculada.

Se creó un recurso de Azure SQL Database donde se habilitó el firewall para permitir el acceso desde servicios de Azure y se definió el esquema inicial mediante el script de Python.

Se desplegó la aplicación Flask en un App Service, configurando el entorno de ejecución necesario para procesar las solicitudes HTTP y gestionar las rutas de la aplicación.

En la sección de "Configuration" del App Service, se registraron las claves SQL_SERVER, SQL_DATABASE, SQL_USERNAME y SQL_PASSWORD, permitiendo que el contenedor acceda a la base de datos de forma segura.

💻 Enlace a la Aplicación Desplegada

https://gestiontareas.azurewebsites.net/

💸 Estimación del Costo (Azure Pricing Calculator)

<img width="960" height="510" alt="costo" src="https://github.com/user-attachments/assets/ad5f448c-d6fe-46c0-b938-936d657fe2f7" />
<img width="960" height="510" alt="costo" src="https://github.com/user-attachments/assets/ff14ee1c-f978-4f46-a8d1-b96c9cdec667" />
<img width="960" height="510" alt="costo" src="https://github.com/user-attachments/assets/d7e934b6-3b5f-44f4-8cf2-d6e4fd5199b4" />
<img width="960" height="510" alt="costofinal" src="https://github.com/user-attachments/assets/a7bfd428-17f2-4291-8c3a-ba12b08155a9" />

📁 Capturas del Portal de Azure

DB-Gestion-de-Tareas

AppService

StorageAccount
  
📘 Lecciones Aprendidas

Al hacer el proyecto me enfrente a muchos obstaculos que fueron resuelto rapido, pero el problema mayor fue correr el programa, ya que Azure dice que corre y funciona pero no pasaba nada.  El problema no esta resuelto ya que el problema es la misma applicacion.  Trabajar con servicios cloud  me enseñó la importancia del desacoplamiento, permitiendo que la lógica en Python y la base de datos escalen de forma independiente dentro del ecosistema de Azure. Lo que mejoraria seria integrar un ORM como SQLAlchemy para optimizar la manipulación de datos y mejorar la portabilidad del código entre diferentes entornos.

📚 Repositorio del Código

https://github.com/JansSP07/comp4260-Proyecto-Tarea
