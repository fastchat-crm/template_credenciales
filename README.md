# GUÍA DE DESARROLLO

Este documento proporciona la información necesaria para configurar y desarrollar el proyecto FastChat CRM.

## Configuración de credenciales

### Para Django (credenciales.json)

El archivo `credenciales.json` debe estar en la raíz del proyecto Django con el siguiente formato:

### Para Node.js (.env)

El archivo `.env` debe estar en la raíz del proyecto Node.js con el siguiente formato:


## TECNOLOGÍAS A USAR

### NVM (PARA MÚLTIPLES VERSIONES DE NODE JS)

#### WINDOWS
https://github.com/coreybutler/nvm-windows/releases/tag/1.2.2

#### UBUNTU
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
source ~/.bashrc
nvm --version
##### Instalar Node.js en su última versión
nvm install node

#### Ahora comprobamos que tengamos Node.js y npm instalados.
node --version | npm --version

### Redis
Redis se utiliza para:
- Almacenamiento en caché
- Gestión de colas de mensajes
- Sesiones de usuario
- Bloqueadores de velocidad (rate limiting)

#### WINDOWS (DOCKER)
docker run --name my-redis -p 6379:6379 -v C:\ruta\a\tus\datos:/data -d redis redis-server --appendonly yes
#### Por ejemplo, si quieres guardar los datos en una carpeta llamada "redis-data" en tu directorio C:
docker run --name my-redis -p 6379:6379 -v C:\redis-data:/data -d redis redis-server --appendonly yes

#### UBUNTU (DOCKER)
Asegúrate de tener Redis instalado:
```bash
# Ubuntu/Debian
sudo apt update
sudo apt install redis-server

# MacOS
brew install redis
```

### Django
Framework principal para el backend en Python:
- Django REST Framework para APIs
- Canales de Django (Django Channels) para WebSockets
- Celery para tareas asíncronas

Instalación:
```bash
pip install -r requirements.txt
```

### Node.js
Utilizado para:
- API de comunicación en tiempo real
- Microservicios independientes
- Gestión de eventos con WebSockets

Instalación:
```bash
npm install
```

## Estructura del proyecto

```
fastchat-crm/
├── fastchatdj/         # Proyecto Django
│
├── fastchatnj/         # Proyecto Node.js
│
├── fastchat-api/       # Microservicios IA FastAPI
│
└── docker/             # Configuración Docker
```

## Comandos útiles

### Django
```bash
# Migraciones
python manage.py makemigrations
python manage.py migrate

# Servidor de desarrollo
python manage.py runserver

# Shell
python manage.py shell
python manage.py sync_whatsapp_sessions

```

### Node.js
```bash
# Desarrollo
npm run dev

# Producción
npm start
```

### FastAPI
```bash
# Servidor de desarrollo
uvicorn main:app --reload
```

### Docker
```bash
# Iniciar todos los servicios
docker-compose up -d

# Reconstruir imágenes
docker-compose build

# Logs
docker-compose logs -f
```
