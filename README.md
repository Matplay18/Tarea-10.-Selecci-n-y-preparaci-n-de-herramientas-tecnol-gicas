# Tarea 11. Documentación de herramientas tecnológicas seleccionadas

📌 Avance actualizado – julio 2025

Proyecto de tesis:
Desarrollo de una plataforma web accesible para automatizar embudos de marketing digital dirigida a pequeños negocios.

Nombre del prototipo (tentativo):
LeadFunnel Platform
🎯 Objetivo del proyecto

Diseñar y construir una plataforma intuitiva, funcional y completamente en español que permita a pequeños emprendedores crear, gestionar y automatizar embudos de marketing digital. El objetivo es facilitar la captación y seguimiento de leads, sin necesidad de conocimientos técnicos avanzados y con una curva de aprendizaje mínima.
🧠 Reflexión sobre la evolución tecnológica del proyecto

En la etapa inicial del proyecto (junio 2025), el desarrollo comenzó con un enfoque basado en FastAPI y MongoDB, aprovechando la rapidez de desarrollo y la eficiencia de Python para levantar una API RESTful. Sin embargo, tras una evaluación técnica más profunda y validación con casos reales, se decidió migrar a un stack tecnológico más estándar en la industria moderna web: React + Node.js + Express + MongoDB/PostgreSQL.

Esta decisión se fundamenta en los siguientes motivos:

    Mayor compatibilidad con el desarrollo frontend moderno (React).

    Facilidad de encontrar recursos, ejemplos y soporte comunitario.

    Reducción de la complejidad al trabajar en un solo lenguaje (JavaScript/TypeScript).

    Mejor proyección profesional y escalabilidad del proyecto.

    Mayor facilidad para integrar funcionalidades asincrónicas, notificaciones y dashboard interactivo.
⚙️ Stack Tecnológico Actual
Componente	Tecnología	Descripción
🖥️ Frontend	React.js	Biblioteca moderna para interfaces reactivas y SPA
🔄 Backend	Node.js + Express	Servidor eficiente y modular con APIs RESTful
🧠 Base de datos	MongoDB (NoSQL) / PostgreSQL (SQL)	Almacenamiento flexible o estructurado, según necesidad
✉️ Emails	Nodemailer	Envío automatizado de correos
🧪 Testing	Jest / Postman	Validación funcional de endpoints y flujos
🛠️ Dev Tools	Visual Studio Code	Entorno de desarrollo multiplataforma
🌐 Deploy	Netlify / Vercel (Frontend) + Railway / Render (Backend)	Publicación en la nube con CI/CD
🔐 Gestión secreta	dotenv	Configuración de variables seguras
🐙 Control de versiones	Git + GitHub	Historial de cambios y trabajo colaborativo

📁 Estructura actual del proyecto (simplificada)

lead-funnel-platform/
├── frontend/           # React app
│   └── src/
│       ├── components/
│       ├── views/
│       └── App.jsx
├── backend/            # Node + Express API
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   └── server.js
├── README.md
├── .env
├── package.json
└── docker-compose.yml (opcional)

🔧 Pasos para levantar el entorno de desarrollo

    Clonar el repositorio:

Instalar dependencias:

    Para frontend:

cd frontend
npm install

Para backend:

    cd ../backend
    npm install

Configurar variables de entorno (.env en ambos entornos):

    PORT=5000
    MONGO_URI=mongodb://localhost:27017
    DB_NAME=lead_funnel
    JWT_SECRET=tu_clave_secreta

    Ejecutar ambos servidores:

        Frontend: npm start

        Backend: npm run dev

🧱 Arquitectura de Capas Implementada

    Capa de Presentación:
    Interfaces dinámicas en React que permiten a los usuarios configurar formularios, embudos y seguimiento de leads.

    Capa Lógica de Negocio:
    API en Node.js que maneja autenticación, validaciones, reglas y flujos de automatización.

    Capa de Datos:
    Integración con MongoDB o PostgreSQL para persistencia de leads, usuarios y eventos.

    Capa de Comunicación:
    Envío de emails automáticos vía Nodemailer, posibilidad futura de notificaciones push.

    Capa de Control y Seguridad:
    Rutas protegidas, validaciones y cifrado de tokens JWT para sesiones.

✅ Conclusión y proyección

Esta actualización representa una mejora significativa en la calidad, sostenibilidad y alcance del proyecto. Al adoptar tecnologías ampliamente utilizadas como React y Node.js, el desarrollo se vuelve más profesional, escalable y compatible con estándares actuales. Además, la estructuración por capas y el uso de buenas prácticas técnicas refuerzan la calidad del entregable final.



# Tarea-10.-Selecci-n-y-preparaci-n-de-herramientas-tecnol-gicas
Avance de tesis 30/06/2025
# 📊 Lead Funnel Platform (Aun por escoger nombre)

**Proyecto de tesis:** Desarrollo de una plataforma web accesible para automatizar embudos de marketing digital dirigida a pequeños negocios.

---

## 🚀 Objetivo del proyecto

Construir una aplicación web sencilla, en español y funcional, que permita a pequeños emprendedores crear y gestionar embudos de marketing digital para captar leads de manera automatizada, sin necesidad de conocimientos técnicos avanzados.

---

## ⚙️ Tecnologías utilizadas

- 🐍 Backend: **Python 3.10+**, **FastAPI**
- 🧠 Base de datos: **MongoDB**
- 📦 Cliente Mongo: **Motor (asyncio)**
- 📡 Servidor ASGI: **Uvicorn**
- 🔐 Variables de entorno: **python-dotenv**
- 📧 Validación de correos: **email-validator**
- 💻 Entorno de desarrollo: **Visual Studio Code**
- 🐳 (Opcional): Docker para contenedores

---

## 🧩 Estructura del proyecto hasta el momento 

lead-funnel-platform/
│
├── app/
│ ├── init.py
│ ├── main.py # Punto de inicio de la API
│ ├── config.py # Configuración de entorno
│ ├── models.py # Modelos de datos
│ └── routes/
│ └── leads.py # Endpoints para gestión de leads
│
├── .env # Variables de entorno
├── requirements.txt # Librerías instaladas
└── README.md # Este archivo


---

## 🛠️ Instrucciones para levantar el ambiente de desarrollo

### 1. Clonar el repositorio (si aplica)

```bash
cd lead-funnel-platform

2. Crear y activar entorno virtual
En Windows:

python -m venv venv
venv\Scripts\activate


3. Instalar dependencias

pip install -r requirements.txt

Si aún no tienes el archivo requirements.txt, instala manualmente:

pip install fastapi uvicorn motor python-dotenv pydantic[email]

Y luego:

pip freeze > requirements.txt

4. Configurar variables de entorno

Crear un archivo .env en la raíz del proyecto con el siguiente contenido:

MONGO_URI=mongodb://localhost:27017
DATABASE_NAME=lead_funnel_db

    Asegúrate de tener MongoDB instalado y en ejecución local.

5. Ejecutar el servidor FastAPI

Desde la raíz del proyecto, con el entorno virtual activo:

uvicorn app.main:app --reload


📚 Autor

Mateo Freire
Estudiante de Ingeniería de Software
Tesis de pregrado – Plataforma para la automatización de embudos de marketing digital.

Avance fecha 30/06/2025
