# Gestión de inmuebles — ACME Inmobiliaria

Aplicación web para administrar un catálogo de propiedades inmobiliarias:
listado con búsqueda y paginación, alta y edición con validación, y borrado con
confirmación. Hecha con JavaScript puro, sin frameworks ni dependencias.

Los datos viven en el `localStorage` del navegador, así que la aplicación
funciona completa sin backend: se puede abrir y usar de inmediato.

**Demo en vivo:** https://jeshuaperez.github.io/gestion-inmuebles/

## Funcionalidades

**Listado (`index.html`)**

- Búsqueda en tiempo real por tipo, dirección, ciudad o propietario.
- Paginación de 5 registros por página, que se recalcula al filtrar o eliminar
  (si la página actual queda fuera de rango, retrocede sola).
- Estado vacío cuando ningún inmueble coincide con la búsqueda.
- Eliminación con modal de confirmación y aviso de resultado.

**Alta y edición (`edicion-inmueble.html`)**

- Formulario con nueve campos: identificación, matrícula, propietario, tipo,
  departamento, ciudad, dirección, área y valor.
- Validación de campos obligatorios que marca en rojo lo que falta y bloquea el
  guardado hasta corregirlo.
- Notificaciones tipo *toast* al guardar.

## Lo que demuestra este proyecto

- Las cuatro operaciones de un CRUD trabajando sobre una misma fuente de datos.
- Separación entre leer, filtrar, paginar y pintar, en vez de resolver todo
  dentro del manejador de un evento.
- Manejo de casos borde: lista vacía, búsqueda sin resultados y páginas que
  dejan de existir al borrar registros.
- Manipulación del DOM y validación de formularios sin librerías.

## Estructura

```
index.html             Listado, búsqueda, paginación y borrado
inmuebles-lista.js     Lógica del listado
edicion-inmueble.html  Formulario de alta y edición
edicion-inmueble.js    Validación y guardado
styles.css             Estilos de ambas pantallas
```

Los datos se guardan bajo la clave `inmuebles` del `localStorage`.

## Cómo probarlo

No requiere instalación ni servidor:

```bash
git clone https://github.com/JeshuaPerez/gestion-inmuebles.git
cd gestion-inmuebles
```

Abre `index.html` en el navegador. Para empezar de cero, borra la
clave `inmuebles` desde las herramientas de desarrollo (Application →
Local Storage).

## Stack

JavaScript (ES6+) · HTML5 · CSS3 · localStorage

---

Jeshua Pérez · [Portafolio](https://jeshuaperez.github.io/portafolio/) · [GitHub](https://github.com/JeshuaPerez)
