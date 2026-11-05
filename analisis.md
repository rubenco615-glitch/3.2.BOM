# Analisis de objetos en JavaScript

## 1. Diferencia entre window y objetos nativos

- window: es un objeto propio del navegador (del BOM). Representa la ventana o pestana y tiene cosas como abrir ventanas, redirigir la pagina o mirar el tamano de pantalla. Si ejecutas JavaScript fuera de un navegador (por ejemplo en Node.js), window no existe.
- Math y JSON: son objetos nativos del propio lenguaje JavaScript. Estan siempre disponibles sin importar donde se ejecute el codigo. Math se usa para operaciones matematicas y JSON para manejar datos en ese formato.
- No es obligatorio escribir window.Math porque en el navegador todo lo global cuelga de window de forma automatica, asi que poner Math.floor() directamente funciona igual y es mas comodo.

## 2. Clasificacion de instrucciones

- window.open(): Pertenece al BOM. Sirve para abrir una nueva ventana o pestana del navegador.
- parseFloat(): Es una funcion nativa de JavaScript. Sirve para convertir un string a numero decimal.
- Math.floor(): Es un metodo de un objeto nativo de JavaScript (Math). Sirve para redondear un numero hacia abajo.
- navigator.userAgent: Pertenece al BOM. Sirve para obtener informacion del navegador y del sistema operativo.

## 3. Objetos y metodos utilizados en la practica

- screen:
  - screen.availWidth y screen.availHeight para sacar el ancho y alto disponible de la pantalla y calcular la posicion para centrar la ventana.

- window:
  - window.open() para lanzar la ventana satelite con las dimensiones y posicion calculadas.
  - window.opener para hacer referencia a la ventana principal desde la secundaria y poder controlarla.
  - window.close() para cerrar la ventana emergente al terminar la cuenta atras.

- navigator:
  - navigator.userAgent para leer los datos del cliente y buscar si usa Windows, Mac o Linux.

- location:
  - location.assign() para cambiar la URL de la ventana principal guardando la entrada en el historial de navegacion.
  - location.replace() para cambiar la URL sustituyendo la pagina actual en el historial sin guardar la anterior.

- Temporizadores:
  - setInterval() para actualizar el texto de la cuenta atras cada 1 segundo.
  - clearInterval() para parar el intervalo cuando la cuenta llega a 0.
  - setTimeout() para esperar 5 segundos antes de cerrar la ventana.
