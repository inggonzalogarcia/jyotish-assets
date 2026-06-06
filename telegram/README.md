# telegram — bot assets

Binarios que el bot de Telegram (n8n-service / jyotish workflow) usa en runtime
vía `file_id` de Telegram (no por URL). El archivo vive acá **versionado** como
fuente de verdad; el bot referencia el `file_id` (env var), no este archivo.

## `menu-banner.*`

Banner que envía el comando `/menu` (foto + reply keyboard) y que aparece tras el
mensaje de bienvenida de `/start`. Formatos aceptados: `.jpg` / `.jpeg` / `.png` / `.webp`.

### Generar / actualizar el `file_id`

Desde el repo `n8n-service` (sibling de éste):

```powershell
.\auxiliar\get-menu-photo-fileid.ps1 -WriteEnv
```

El script toma por defecto `../jyotish-assets/telegram/menu-banner.*`, lo sube una
sola vez al bot (con `TELEGRAM_BOT_TOKEN`), lee el `file_id` del tamaño más grande y
lo escribe en el `.env` de n8n-service como `TELEGRAM_MENU_PHOTO_FILE_ID`.

> El `file_id` está atado al `TELEGRAM_BOT_TOKEN`. Si se rota el token, re-generar
> corriendo el script de nuevo con la imagen de esta carpeta.
