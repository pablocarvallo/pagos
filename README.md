# Pagos del mes

App personal para llevar la lista de los pagos que hay que hacer cada mes, con un check para marcar los que ya se hicieron. Reemplaza la nota de Notas de iOS con el mismo contenido.

## Qué hace

- **Título del mes**: el título grande (por ejemplo, «Octubre 2026») se toca para cambiarlo. Sugiere el mes actual y el siguiente.
- **Lista de check por secciones**: «A inicios de mes» y «A mitad de mes» vienen creadas. Al tocar un pago se marca como hecho y queda la fecha («Pagado el 3 oct»).
- **Avance**: la tarjeta azul muestra cuántos pagos van hechos y cuántos faltan.
- **Filtro**: «Todos» o solo «Pendientes».
- **Agregar**: la fila «Agregar pago» al final de cada sección.
- **Editar**: el botón Editar permite quitar pagos (con opción de deshacer), subirlos o bajarlos, cambiarles el nombre o la sección, y crear, renombrar o eliminar secciones.
- **Solo este mes**: un pago puede marcarse como de una sola vez (por ejemplo, «Cami noviembre 55.000»); se quita solo al comenzar el mes siguiente.
- **Nuevo mes**: desmarca todos los pagos, propone el título del mes siguiente y guarda el mes que termina en «Meses anteriores», con lo que se pagó y lo que quedó pendiente.
- **Pegar lista**: se copia la lista desde Notas y se pega en la app. Cada línea es un pago; una línea que termina en dos puntos (:) es el nombre de una sección.
- **Respaldo**: copia todos los datos como texto y los restaura desde ahí.

## Instalar en el iPhone

1. La app se publica con GitHub Pages en `https://pablocarvallo.github.io/pagos/`.
2. Abre esa dirección en **Safari** en el iPhone.
3. Toca **Compartir → Agregar a inicio**.
4. Abre la app desde el icono, toca **Pegar lista de Notas** y pega la lista copiada desde la nota.

Se abre como app independiente, con su icono, y funciona sin conexión después de la primera carga.

## Archivos

| Archivo | Uso |
| --- | --- |
| `index.html` | La app completa (HTML, CSS y JavaScript, sin dependencias ni compilación), con el sistema de diseño de las apps domésticas entre las marcas `DS:TOKENS` y `DS:LAYER` |
| `manifest.webmanifest` | Nombre, colores e iconos de la app instalada |
| `sw.js` | Service worker para uso sin conexión |
| `icons/icon-full.svg` | Icono original a pantalla completa (fuente de los PNG) |
| `icons/icon.svg` | Icono con esquinas redondeadas (favicon) |
| `icons/apple-touch-icon.png` | Icono de 180 px para la pantalla de inicio del iPhone |
| `icons/icon-192.png`, `icons/icon-512.png`, `icons/icon-1024.png` | Iconos del manifiesto y archivo de alta resolución |

## Datos

La lista se guarda en `localStorage` del navegador bajo la clave `pagos-del-mes`. El código no incluye ningún pago: la lista solo existe en el iPhone donde se pega, y no se envía nada a ningún servidor.
