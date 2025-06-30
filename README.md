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
