# Sitio web — Institución Educativa Rural Las Palmeras

Sitio estático (HTML y CSS, sin base de datos) pensado para publicarse gratis con GitHub Pages y luego, si se quiere, moverse a un hosting propio con dominio de la institución.

## Estructura de carpetas

```
palmeras/
├── index.html                  Página principal (portada y todas las secciones)
├── assets/
│   ├── css/estilos.css         Todos los estilos del sitio
│   └── img/                    Escudo, bandera y fotografías
│       ├── escudo.png          Escudo con fondo transparente
│       ├── escudo.jpg          Original tal como se recibió
│       └── bandera.jpg
├── documentos/                 Aquí va el manual de convivencia en PDF
└── paginas/                    Para páginas internas futuras
```

## Colores institucionales

Tomados directamente del escudo y de la bandera:

| Color     | Código    | Dónde se usa                                  |
|-----------|-----------|-----------------------------------------------|
| Verde     | `#009640` | Portada, accesos rápidos, botones principales |
| Verde hondo | `#00602C` | Fondos oscuros y encabezados de tabla       |
| Vinotinto | `#8C2631` | Enlaces, títulos de proyectos, manual         |
| Rojo      | `#ED1B24` | Circulares urgentes y franja de la bandera    |
| Negro     | `#101010` | Texto, barra superior y pie de página         |

Si se cambian, se editan una sola vez en `assets/css/estilos.css`, en el bloque `:root` de arriba.

## Qué falta llenar

Todo lo que está marcado con un recuadro amarillo en la página tiene la etiqueta
`<span class="pendiente">`. Se reemplaza el texto y se borra la etiqueta.

Pendientes principales:

1. Misión, visión, historia y principios (tomados del PEI).
2. Significado de los tres colores de la bandera.
3. Nombres de los cuatro docentes responsables de los centros de interés.
4. Listado completo del cuerpo docente.
5. Nombre de la orientadora y sus campañas.
6. Circulares y novedades reales.
7. Las cuatro direcciones de los accesos rápidos (correo, notas, Orienten, Facebook).
8. El PDF del manual, guardado como `documentos/manual-de-convivencia.pdf`.
9. Teléfono y correo reales en la barra superior y el pie de página.

## Fotografías

Las tarjetas de centros de interés y novedades tienen espacio para foto.
Para poner una, se agrega el archivo en `assets/img/` y se edita el `div` así:

```html
<div class="foto" style="background-image:url('assets/img/nombre-foto.jpg')" role="img" aria-label="Descripción de la foto"></div>
```

Recomendación: usar fotos de máximo 1200 píxeles de ancho para que la página
cargue rápido en conexiones rurales. Y para fotos donde aparezcan estudiantes,
tener la autorización de uso de imagen firmada por el acudiente.

## Publicar en GitHub Pages

1. Crear un repositorio nuevo en GitHub, por ejemplo `ier-las-palmeras`.
2. Subir todo el contenido de esta carpeta a la rama `main`.
3. Entrar a **Settings → Pages**.
4. En *Source* elegir **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
5. Guardar. A los pocos minutos el sitio queda en:
   `https://USUARIO.github.io/ier-las-palmeras/`

Cada vez que se suba un cambio, el sitio se actualiza solo.
