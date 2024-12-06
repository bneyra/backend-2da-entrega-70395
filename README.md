## Comisión 70395 Programación Backend I: Desarrollo Avanzado de Backend ~ NeyraB ~ Segunda entrega

## Descripción del Proyecto

Luego de haber desarrollado el servidor basado en node.Js y Express en la 1er entrega, nos tocará hoy ampliar el proyecto para incluir Hanlebars y WebSocket!

### Nuevos Requisitos

- **Configuración de Handlebars:**
  - Se ha integrado el motor de plantillas Handlebars para renderizar vistas del servidor.
  
- **Configuración de WebSocket:**
  - Se ha instalado y configurado el servidor de `socket.io` para permitir la comunicación en tiempo real entre el servidor y el cliente.
  
- **Nuevas Vistas:**
  - **`home.handlebars`:** Muestra una lista de todos los productos agregados hasta el momento.
  - **`realTimeProducts.handlebars`:** Muestra la lista de productos y se actualiza automáticamente en tiempo real mediante WebSocket.


## Instalación

Sigue estos pasos para clonar el repositorio, instalar las dependencias y ejecutar el proyecto:

1. Clona el repositorio:
    ```sh
    git clone
    ```

2. Navega al directorio del proyecto:
    ```sh
    cd tu-repositorio
    ```

3. Instala las dependencias:
    ```sh
    npm install
    ```

4. Inicia el servidor:
    ```sh
    npm start
    ```

El servidor se ejecutará en `http://localhost:8080`.

## Rutas de Productos

### Base URL: `/api/products/`

(Se mantiene la misma configuración de la primer entrega)

### Base URL: `/api/carts/`

(Se mantiene la misma configuración del primer repositorio)

## Vistas con Handlebars

### Home View

- **Ruta:** `/home`
- **Descripción:** Muestra una lista de todos los productos utilizando la plantilla `home.handlebars`.

### Real-Time Products View

- **Ruta:** `/realtimeproducts`
- **Descripción:** Muestra una lista de productos en tiempo real utilizando la plantilla `realTimeProducts.handlebars`.
- **Características:**
  - Utiliza WebSocket para actualizar automáticamente la lista de productos cuando se crean o eliminan productos.
  - Incluye un formulario para agregar nuevos productos a través de WebSocket.

## Persistencia de la Información

La persistencia de la información se implementa utilizando el file system, con los archivos `productos.json` y `carrito.json` que respaldan la información.

## Ejemplo de Uso

Puedes utilizar Postman o cualquier cliente HTTP para interactuar con las rutas de productos y carritos. La vista en tiempo real y la vista de home están disponibles en el navegador.

### Ejemplo de Uso con WebSocket

Para la vista en tiempo real (`/realtimeproducts`), se puede usar el formulario incluido para agregar nuevos productos. La actualización de la lista de productos se realiza automáticamente gracias a WebSocket.

## Notas Adicionales

- La integración de WebSocket permite que las actualizaciones en la lista de productos se reflejen en tiempo real sin necesidad de recargar la página.
- La vista `home.handlebars` permite ver todos los productos estáticos en la página principal del proyecto.
