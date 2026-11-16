[README principal.md](https://github.com/user-attachments/files/34921766/README.principal.md)
# Nexus Gaming Store

## Descripción del proyecto

**Nexus Gaming Store** es una aplicación web de comercio electrónico enfocada en la venta de videojuegos digitales. El proyecto permite explorar un catálogo de productos, buscar y filtrar videojuegos, administrar un carrito de compras y completar un proceso de compra de demostración.

La aplicación fue desarrollada con **React** y **Vite**, utilizando componentes reutilizables para organizar la interfaz y `localStorage` del navegador para conservar información entre sesiones.

## Funcionalidades principales

### Catálogo y navegación
- Página de inicio con productos destacados.
- Catálogo con 52 videojuegos precargados.
- Búsqueda de productos.
- Filtro por categoría.
- Paginación del catálogo.
- Visualización de información, precio y stock de cada producto.

### Carrito y compras
- Agregar productos al carrito.
- Modificar y quitar productos del carrito.
- Validación de stock disponible al agregar productos y confirmar la compra.
- Resumen del pedido y cálculo de costos.
- Proceso de checkout de demostración con opciones de tarjeta y transferencia.
- Descuento del inventario después de confirmar una compra.
- Generación de una clave de licencia de ejemplo y registro de la venta en el historial.

### Usuarios y administración
- Registro de cuentas de clientes.
- Inicio de sesión para clientes.
- Acceso de demostración para administrador.
- Panel administrativo para crear, editar y eliminar productos.
- Visualización del inventario y del historial de ventas.

### Otras secciones
- Página de contacto con validación de campos.
- Página de sucursal en Viña del Mar.
- Mapa basado en Leaflet y OpenStreetMap.
- Interfaz adaptable a distintos tamaños de pantalla.
- Carrusel de imágenes en las pantallas de autenticación.

## Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| React 19 | Construcción de interfaces mediante componentes. |
| JavaScript (ES Modules) | Lógica y funcionamiento de la aplicación. |
| Vite | Entorno de desarrollo y compilación. |
| HTML5 | Estructura de la página. |
| CSS3 | Estilos y diseño visual. |
| localStorage | Persistencia local de usuarios, productos, carrito y ventas. |
| Leaflet | Visualización del mapa de la sucursal. |
| OpenStreetMap | Proveedor de mapas. |
| Vitest | Ejecución de pruebas. |
| React Testing Library | Pruebas de componentes e interacción. |
| ESLint | Revisión estática del código. |

## Estructura del proyecto

```text
TiendaNexusGame-master/
└── TiendaNexusGame-master/
    ├── public/
    │   ├── assets/
    │   │   ├── fondo1.jpg
    │   │   ├── fondo2.jpg
    │   │   ├── fondo3.jpg
    │   │   └── fondo4.jpg
    │   ├── img/
    │   ├── favicon.svg
    │   └── icons.svg
    │
    ├── src/
    │   ├── components/
    │   │   ├── AuthCarousel.jsx
    │   │   ├── Footer.jsx
    │   │   ├── Header.jsx
    │   │   ├── ProductCard.jsx
    │   │   └── StoreMap.jsx
    │   │
    │   ├── context/
    │   │   └── AuthContext.jsx
    │   │
    │   ├── data/
    │   │   └── productosIniciales.js
    │   │
    │   ├── lib/
    │   │   └── storage.js
    │   │
    │   ├── pages/
    │   │   ├── Admin.jsx
    │   │   ├── Carrito.jsx
    │   │   ├── Checkout.jsx
    │   │   ├── Contacto.jsx
    │   │   ├── Inicio.jsx
    │   │   ├── Login.jsx
    │   │   ├── LoginAdmin.jsx
    │   │   ├── LoginCliente.jsx
    │   │   ├── LoginUsuario.jsx
    │   │   ├── NoEncontrada.jsx
    │   │   ├── Productos.jsx
    │   │   ├── Registro.jsx
    │   │   └── Sucursal.jsx
    │   │
    │   ├── store/
    │   │   └── tiendaReducer.js
    │   │
    │   ├── App.jsx
    │   ├── index.css
    │   ├── main.jsx
    │   └── styles.css
    │
    ├── test/
    │   ├── 404.test.jsx
    │   ├── auth.test.jsx
    │   ├── contacto.test.jsx
    │   ├── PruebaJasmine.test.jsx
    │   ├── PruebaKarma.test.jsx
    │   ├── setup.js
    │   └── tiendaReducer.test.js
    │
    ├── .gitignore
    ├── eslint.config.js
    ├── index.html
    ├── package.json
    ├── package-lock.json
    └── vite.config.js
```

> `node_modules/` no se incluye en el árbol porque contiene dependencias instaladas automáticamente y no forma parte del código fuente principal.

## Organización del código

- **`src/App.jsx`**: componente principal. Inicializa el almacenamiento local y selecciona la página según la ruta del navegador.
- **`src/main.jsx`**: punto de entrada de React; carga los estilos y monta la aplicación.
- **`src/components/`**: componentes reutilizables como encabezado, pie de página, tarjeta de producto, carrusel y mapa.
- **`src/pages/`**: pantallas principales de la tienda, autenticación, carrito, checkout y administración.
- **`src/context/`**: contexto de autenticación y estado de sesión.
- **`src/data/`**: datos iniciales del catálogo de videojuegos.
- **`src/lib/storage.js`**: funciones para inicializar, consultar y guardar información en `localStorage`, además de utilidades para precios y cantidades.
- **`src/store/tiendaReducer.js`**: lógica de actualización del estado de la tienda, incluyendo acciones de carrito, compra y eliminación de productos.
- **`test/`**: pruebas automatizadas del proyecto.
- **`vite.config.js`**: configuración de Vite y Vitest.

## Requisitos

Antes de ejecutar el proyecto, instala:

- Node.js (se recomienda una versión compatible con Vite 8).
- npm, incluido con Node.js.
- Visual Studio Code u otro editor de código.

## Instalación y ejecución

1. Descarga o clona el repositorio.
2. Abre una terminal en la carpeta del proyecto que contiene `package.json`.
3. Instala las dependencias:

```bash
npm install
```

4. Inicia el servidor de desarrollo:

```bash
npm run dev
```

5. Abre en el navegador la dirección local que indique Vite en la terminal (normalmente `http://localhost:5173`).

## Otros comandos disponibles

Compilar la aplicación para producción:

```bash
npm run build
```

Previsualizar la compilación:

```bash
npm run preview
```

Ejecutar las pruebas en modo interactivo:

```bash
npm run test
```

Ejecutar las pruebas una vez:

```bash
npm run test:run
```

Ejecutar ESLint:

```bash
npm run lint
```

## Rutas principales

La navegación de la aplicación utiliza rutas mediante el fragmento (`#`) de la URL.

| Ruta | Página |
|---|---|
| `#/` | Inicio |
| `#/catalogo` | Catálogo de videojuegos |
| `#/carrito` | Carrito de compras |
| `#/checkout` | Finalizar compra |
| `#/sucursal` | Información de sucursal |
| `#/login` | Acceso de usuario |
| `#/login/cliente` | Acceso de cliente |
| `#/login/admin` | Acceso de administrador |
| `#/registro` | Registro de cliente |
| `#/admin` | Panel administrativo |

## Almacenamiento de datos

El proyecto utiliza `localStorage`, por lo que la información se guarda en el navegador donde se utiliza la aplicación. Entre las claves empleadas se encuentran:

| Clave | Información almacenada |
|---|---|
| `nexus_productos` | Catálogo e inventario de productos. |
| `nexus_carrito` | Productos agregados al carrito. |
| `nexus_usuarios` | Cuentas de clientes registradas. |
| `nexus_usuario_activo` | Sesión del usuario actual. |
| `historialVentas` | Registro de compras realizadas. |

Los datos no se almacenan en una base de datos remota. Si se borran los datos del sitio o se utiliza otro navegador o dispositivo, la información local puede perderse o no estar disponible.

## Acceso de administrador para demostración

La pantalla de acceso administrativo contiene credenciales de prueba definidas directamente en el código:

| Campo | Valor |
|---|---|
| Correo | `admin@nexus.com` |
| Contraseña | `admin123` |
| Token | `12345` (opcional) |

Estas credenciales son únicamente para probar el proyecto. No deben utilizarse en un sistema real.

## Consideraciones de seguridad y alcance

Nexus Gaming Store es un proyecto frontend de demostración. La autenticación y los datos se gestionan en el navegador mediante `localStorage`; por lo tanto, no ofrece las garantías de seguridad de un backend con autenticación y base de datos. Las contraseñas de clientes se guardan en el almacenamiento local sin un sistema de hash en el código revisado.

El checkout simula el flujo de compra y no representa una integración real con una pasarela de pago. Las claves de licencia generadas son de ejemplo y no corresponden a licencias comerciales verificadas.

El mapa de la sucursal necesita conexión a Internet para cargar Leaflet y los recursos de OpenStreetMap.

## Autoría

Proyecto desarrollado como una tienda web de videojuegos digitales, con catálogo, gestión de usuarios, carrito de compras y panel administrativo.
