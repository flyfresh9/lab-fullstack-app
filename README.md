# 🚀 Arquitectura Multi-Contenedor Full-Stack con Docker Compose

Laboratorio integrador de infraestructura que despliega un entorno de servidor web Nginx y una base de datos MySQL 8.0, utilizando **variables de entorno (.env)** para la gestión segura de credenciales y **volúmenes nombrados** para la persistencia de datos.

## 🛠️ Tecnologías Utilizadas
* **Docker & Docker Compose**
* **MySQL 8.0**
* **Nginx**
* **Variables de Entorno (`.env`)**

## 🏗️ Arquitectura del Sistema
* **`db` (MySQL 8.0):** Escuchando en el puerto interno `3306` (mapeado a `3307` en el host). Persistencia gestionada vía el volumen `db_data`.
* **`web` (Nginx):** Expuesto en el puerto `8090`. Sirve contenido web estático montado desde la carpeta `./html`.
* **Red Aislada (`red_fullstack`):** Red virtual `bridge` para comunicación inter-contenedor.

## 🚀 Instrucciones de Despliegue

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/flyfresh9/lab-fullstack-app.git](https://github.com/flyfresh9/lab-fullstack-app.git)
   cd lab-fullstack-app