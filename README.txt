MY CHAMPIONSHIP - PWA

ESTE PAQUETE YA INCLUYE:
- index.html: la aplicación
- manifest.json: nombre, icono y modo de instalación
- service-worker.js: caché para abrirla sin conexión después de la primera visita
- icon-192.png e icon-512.png: iconos de instalación

IMPORTANTE:
Para que Chrome permita instalarla como aplicación y activar el modo sin conexión,
estos archivos deben estar publicados en una dirección HTTPS (por ejemplo, GitHub Pages).
No abras index.html directamente desde el almacenamiento del teléfono: file:// no permite
registrar el Service Worker ni instalar una PWA.

DATOS:
Los datos se guardan en el almacenamiento del navegador. La versión publicada en HTTPS
usa un almacenamiento distinto del archivo local que abrías antes. Antes de empezar a usar
la PWA, exporta un backup desde la versión local y luego impórtalo en la versión publicada.
No borres la copia local hasta comprobar que el backup se importó correctamente.
