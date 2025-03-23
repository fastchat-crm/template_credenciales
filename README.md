# credenciales.json formato para DJANGO
{
  "POSTGRES_HOST": "localhost",
  "POSTGRES_PASSWORD": "1234",
  "POSTGRES_USER": "postgres",
  "POSTGRES_PORT": "5432",
  "POSTGRES_DBNAME": "dbfastchat",
  "USE_SSL": false,
  "DOMINIO_GENERAL": "",
  "SECRET_KEY": "+4gw$y8hn3k2mlkbxn3fk(%qsmm9zd4zak2yh**k9+mz4ri8t5",
  "EMAIL_HOST_USER": "apikey",
  "DEFAULT_FROM_EMAIL": "",
  "EMAIL_HOST_PASSWORD": "",
  "SENDGRID_API_KEY": "",
  "WKHTMLTOPDF_CMD": "/usr/local/bin/wkhtmltopdf",
  "GMAP_API_KEY": "",
  "ADMINS": [
  ],
  "DEBUG": true,
  "CACHES_REDIS": false,
  "WINDOWS": true,
  "ID_GRUPO_CLIENTE": 3,
  "REDIS_HOST": "localhost",
  "REDIS_PORT": "6379 "
}

# .env para NODEJS

REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_CHANNEL_START=start_session
REDIS_CHANNEL_RECEIVE=receive_message
REDIS_CHANNEL_SEND=send_message
MIN_DELAY_MS=1000
MAX_DELAY_MS=3000
SESSION_FILE_PATH=./session.json
