SaaS Generativo - Aplicación Angular

Este proyecto es una aplicación SaaS que permite optimizar documentos mediante IA. Desarrollado en Angular, con una arquitectura modular y pensado para ser desplegado en contenedores Docker.

🚀 Tecnologías Utilizadas

Angular (Frontend)

TypeScript

TailwindCSS (Para estilos)

Docker (Para contenedores)

Google Cloud Platform (GCP) (Para despliegue)

API Backend (Comunicación con FastAPI o Node.js)

📌 Requisitos Previos

Asegúrate de tener instalados:

Node.js (v18 o superior)

Angular CLI (npm install -g @angular/cli)

Docker (Para contenedores)

Cuenta en Google Cloud Platform (Para el despliegue en GCP, opcional)

📂 Estructura del Proyecto

📦 proyecto-angular
 ┣ 📂 src
 ┃ ┣ 📂 app
 ┃ ┃ ┣ 📂 components  # Componentes reutilizables
 ┃ ┃ ┣ 📂 pages       # Vistas principales (Login, Dashboard)
 ┃ ┃ ┗ 📂 services    # Servicios de conexión con la API
 ┃ ┣ 📂 assets        # Recursos estáticos (imágenes, estilos, etc.)
 ┃ ┗ 📜 main.ts       # Punto de entrada de Angular
 ┣ 📜 package.json    # Dependencias del proyecto
 ┣ 📜 angular.json    # Configuración de Angular
 ┣ 📜 Dockerfile      # Configuración para Docker
 ┗ 📜 README.md       # Documentación

🔧 Instalación y Configuración

1️⃣ Clonar el Repositorio:

git clone https://github.com/tu-usuario/proyecto-angular.git
cd proyecto-angular

2️⃣ Instalar Dependencias:

npm install

3️⃣ Ejecutar en Desarrollo:

ng serve --open

Esto abrirá la aplicación en http://localhost:4200/

🐳 Ejecutar con Docker

1️⃣ Construir la imagen Docker:

docker build -t angular-app .

2️⃣ Ejecutar el contenedor:

docker run -p 8080:80 angular-app

Accede a http://localhost:8080/

☁️ Desplegar en Google Cloud Run

1️⃣ Autenticar con GCP:

gcloud auth configure-docker

2️⃣ Subir la imagen a Google Cloud Artifact Registry:

docker tag angular-app gcr.io/TU_PROYECTO/angular-app
docker push gcr.io/TU_PROYECTO/angular-app

3️⃣ Desplegar en Cloud Run:

gcloud run deploy angular-app \
  --image gcr.io/TU_PROYECTO/angular-app \
  --platform managed \
  --region us-central1 \
  --allow-unauthenticated

🔹 GCP generará una URL pública donde la aplicación estará disponible. 🚀

📌 Autenticación y Seguridad

Actualmente la autenticación no se realiza con Firebase.

Se recomienda utilizar JWT o integración con OAuth2 si se necesita autenticación segura.

Implementar validaciones en los formularios y en la API para proteger los datos.

📋 Próximos Pasos

✅ Mejorar la experiencia UX/UI
✅ Integración con la API
✅ Optimización de rendimiento
✅ Implementación de pruebas unitarias
