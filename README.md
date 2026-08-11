# RD-3D

Catálogo web de un taller de impresión 3D unipersonal — Diseñamos. Imprimimos. Creamos.

Sitio de una sola página (`index.html`, sin build ni dependencias) con catálogo por secciones, carrito, checkout paso a paso y formulario de pedidos a medida.

## Publicar en GitHub Pages

1. Subí `index.html` (y la carpeta `images/` si ya tenés fotos) a la rama `main`.
2. Andá a **Settings → Pages → Source: `main` / `(root)`**.
3. El sitio queda disponible en `https://rdjoseignacio.github.io/RD3D/`.

## Cargar fotos reales de productos

Los productos están definidos en el array `SECTIONS`, dentro del `<script>` de `index.html`. Por defecto muestran un render esquemático (efecto "plano técnico"). Para reemplazarlo por fotos reales, agregá la propiedad `photos` a cualquier producto:

```js
{
  id:'an-1',
  name:'Cráneo articulado 22 piezas',
  desc:'...',
  sizes:'18 × 13 × 15 cm',
  price:24900,
  photos:['images/craneo-1.jpg','images/craneo-2.jpg','images/craneo-3.jpg']
}
```

Subí las imágenes a una carpeta `images/` al lado de `index.html`. El sitio va a rotar automáticamente entre esas fotos cada 2 segundos, y también se pueden ver en grande haciendo click sobre el producto.

## Mails automáticos (solicitudes y compras)

El sitio usa [Web3Forms](https://web3forms.com) para mandar los mails de "Solicitar pieza" y "Nueva compra" sin necesidad de backend (250 envíos gratis por mes).

1. Entrá a web3forms.com y creá una Access Key gratis con tu mail (`rd.joseignacio@gmail.com`).
2. Pegá esa key en la constante `WEB3FORMS_ACCESS_KEY` al principio del `<script>` de `index.html`.

Mientras esa key esté vacía, el sitio funciona igual pero abre el cliente de correo del usuario (`mailto:`) como respaldo.

## Estructura

- `index.html` — todo el sitio: HTML, CSS y JS en un solo archivo.
- `images/` — fotos de producto (opcional, no incluidas todavía).

## Licencia

Ver [LICENSE.md](./LICENSE.md).
