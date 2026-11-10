# My Championship 3.0 — PWA

## Publicación
1. Descomprime esta carpeta.
2. Sube **todo su contenido** a la carpeta donde quieras publicar My Championship 3.0 en GitHub Pages.
3. Mantén juntos `index.html`, `manifest.json`, `service-worker.js` y los dos iconos.
4. Abre la URL publicada y, en Android Chrome, usa el menú ⋮ → Instalar aplicación / Añadir a pantalla principal.

## Datos y compatibilidad
- Se conserva la clave local `myChampionship.v22` para que la actualización lea los mismos datos guardados por 2.2 en el mismo origen.
- No borres la versión anterior hasta comprobar que 3.0 abre correctamente y que tus datos aparecen.
- Exporta un backup JSON antes de actualizar. Los datos permanecen en el almacenamiento local del navegador/dispositivo; no se sincronizan automáticamente entre dispositivos.
- El sistema de puntos, WDC, WCC, mercado de pilotos, reglas de clasificación y resultados existentes se mantienen.

## Novedades 3.0
- Interfaz renovada con estética Motorsport.
- Registro de vuelta rápida en cada sesión de carrera. La VR se muestra en resultados y en las estadísticas por piloto, sin otorgar puntos.
- Formato automático de tiempos `mm:ss.mmm` mientras se escribe, también para la clasificación única.
- Botón para importar una clasificación desde imagen en Q1/Q2/Q3 y Qualifying única. El reconocimiento busca texto por filas, prioriza el nombre del piloto y usa el equipo como apoyo; no depende de colores, tipografías ni del estilo visual del juego.
- La importación no guarda nada automáticamente: los tiempos detectados quedan en los campos editables para revisarlos antes de pulsar Guardar.

## Limitación importante del OCR
La importación de imágenes utiliza la API de reconocimiento de texto local `TextDetector` del navegador, cuando está disponible. El soporte varía según navegador y dispositivo; si el navegador no la incluye, la app avisa y permite seguir introduciendo los tiempos manualmente. No se envían imágenes a un servidor. Para disponer de OCR offline en todos los navegadores haría falta integrar y empaquetar un motor OCR completo y sus modelos, algo que no viene incluido en esta compilación.

## Prueba recomendada
Antes de usarlo en un GP real:
1. Exporta un backup desde tu 2.2.
2. Abre 3.0 en el mismo navegador/origen.
3. Comprueba pilotos, equipos, calendario y resultados.
4. Prueba un tiempo escribiendo `106589` (debe quedar `1:06.589`).
5. Marca una VR en una carrera y comprueba que aparece en resultados/estadísticas y no cambia los puntos.
6. Si `TextDetector` está disponible, prueba la importación con una captura clara y revisa cada fila antes de guardar.


## Indicador de posiciones ganadas/perdidas
En las tablas de resultados de carrera se muestra el cambio entre la posición de salida y la posición final: verde `3 ▲` si ganó tres posiciones, rojo `2 ▼` si perdió dos, y amarillo `—` si mantuvo su posición. Si no existe una clasificación de salida registrada, se muestra `N/D` para no inventar el dato. Para carreras sprint se compara la salida de SR con SQ; para la carrera principal se usa la clasificación correspondiente.
