Aquí tienes el diseño del programa de gestión de productos para el supermercado JSumbo, organizado y estructurado en formato Markdown para tus estudiantes:

-----

# Gestión de Productos JSumbo: Programa por Consola

El objetivo de este programa es simular la gestión de productos y ventas de un supermercado. Se utilizarán estructuras de datos como listas de diccionarios para los productos y diccionarios para los clientes, aplicando conceptos fundamentales de Python como funciones (con y sin parámetros), manejo de errores y un menú interactivo.

-----

## Estructuras de Datos

### Productos

Se almacenarán en una **lista de diccionarios**. Cada diccionario representará un producto y contendrá la siguiente información:

  * **nombre**: Cadena de texto, máximo 20 caracteres.
  * **codigo**: Cadena de texto, solo números y letras mayúsculas.
  * **cantidad**: Número entero, la cantidad de existencias.

**Ejemplo:**

```python
productos = [
    {"nombre": "Leche", "codigo": "LEC001", "cantidad": 10},
    {"nombre": "Pan", "codigo": "PAN005", "cantidad": 3},
    {"nombre": "Huevos", "codigo": "HUE010", "cantidad": 15}
]
```

-----

### Clientes

Se almacenarán en un **diccionario**. La llave de este diccionario será el nombre del cliente (cadena de texto), y el valor será otro diccionario con la información del cliente:

  * **rut**: Cadena de texto, solo números y la letra 'K' mayúscula.
  * **puntos**: Número entero, la cantidad de puntos acumulados por compras.

**Ejemplo:**

```python
clientes = {
    "Juan Perez": {"rut": "12345678K", "puntos": 5},
    "Maria Lopez": {"rut": "987654321", "puntos": 2}
}
```

-----

## Funcionalidades del Programa

El programa debe ofrecer las siguientes opciones a través de un menú interactivo:

### 1\. Ver todos los productos

  * Mostrará una lista clara de todos los productos disponibles, incluyendo su nombre, código y cantidad en existencia.

-----

### 2\. Registrar Venta (Comprar productos)

  * Se debe solicitar el **nombre del cliente** y su **RUT** (validando que sea solo números y la letra 'K' mayúscula).
  * Si el cliente no existe, se debe registrar automáticamente con 0 puntos.
  * Para cada producto que el cliente desee comprar:
      * Se solicitará el **código del producto** y la **cantidad a comprar**.
      * **Validación de existencias**: Si no hay suficientes productos en stock, el sistema debe avisar que no hay existencias disponibles para la cantidad solicitada.
      * **Actualización de stock**: Si la venta es exitosa, se debe disminuir la cantidad de existencias del producto.
      * **Puntos del cliente**: Por cada producto comprado, se debe agregar 1 punto al cliente.
      * **Alerta de bajo stock**: Si después de una venta, la cantidad de un producto es inferior a 5, el sistema debe emitir un mensaje de advertencia sobre el bajo stock de ese producto.
  * La venta de productos debe continuar hasta que el usuario decida no comprar más.

-----

### 3\. Ver datos de todos los clientes

  * Mostrará una lista de todos los clientes registrados, incluyendo su nombre, RUT y los puntos acumulados.

-----

### 4\. Salir (Presionando 'x')

  * El programa debe terminar únicamente cuando el usuario seleccione esta opción.

-----

## Requisitos de Implementación

### Funciones

Utilizar funciones para modularizar el código, tanto con parámetros como sin ellos. Ejemplos:

  * `mostrar_productos()`
  * `registrar_venta()`
  * `validar_rut(rut)`
  * `actualizar_stock(codigo_producto, cantidad_vendida)`
  * `agregar_puntos(nombre_cliente, puntos)`
  * `mostrar_clientes()`

-----

### Manejo de Errores

Implementar bloques `try-except` para manejar posibles errores, como la entrada de datos incorrectos por parte del usuario (ej. ingresar texto cuando se espera un número, códigos de producto inexistentes, etc.).

-----

### Menú Interactivo

Un bucle principal que presente las opciones al usuario y permita navegar por las diferentes funcionalidades hasta que se elija la opción de salir.

-----

### Validaciones

  * **Nombre de producto**: Máximo 20 caracteres.
  * **Código de producto**: Solo números y letras mayúsculas.
  * **RUT**: Solo números y la letra 'K' mayúscula.
  * **Cantidad de existencias y cantidad a comprar**: Números enteros positivos.

-----

¡Espero que esta organización sea de gran ayuda para tus estudiantes en el desarrollo del programa\! ¿Hay algo más en lo que te pueda ayudar para tus clases?
