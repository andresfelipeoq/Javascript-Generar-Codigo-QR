# Javascript-Generar-Codigo-QR
Codigo QR
Puedes crear una aplicación en JavaScript para generar códigos QR utilizando una biblioteca externa llamada "qrcode-generator". Esta biblioteca te permite generar fácilmente códigos QR en tu aplicación web. A continuación, te muestro un ejemplo simple de cómo crear una aplicación de generación de códigos QR en JavaScript:

1. Configuración del proyecto:

   - Crea una carpeta para tu proyecto.
   - Crea un archivo HTML llamado "index.html" y un archivo JavaScript llamado "app.js" en la carpeta.

2. Estructura básica del archivo HTML (index.html):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Generador de Códigos QR</title>
</head>
<body>
    <h1>Generador de Códigos QR</h1>
    <input type="text" id="textInput" placeholder="Texto o enlace">
    <button id="generateQR">Generar QR</button>
    <div id="qrcode"></div>

    <script src="qrcode.min.js"></script>
    <script src="app.js"></script>
</body>
</html>
```

3. Descarga e incluye la biblioteca "qrcode-generator":
   - Descarga la biblioteca "qrcode-generator" desde https://github.com/davidshimjs/qrcodejs o utiliza un CDN.

4. Código JavaScript (app.js):

```javascript
// Obtener elementos del DOM.
const textInput = document.getElementById('textInput');
const generateQRButton = document.getElementById('generateQR');
const qrcode = new QRCode(document.getElementById('qrcode'));

// Manejar el clic en el botón "Generar QR".
generateQRButton.addEventListener('click', () => {
    const text = textInput.value;

    // Generar el código QR.
    qrcode.makeCode(text);
});
```

5. Asegúrate de que la biblioteca "qrcode.min.js" esté en la misma carpeta que tus archivos HTML y JavaScript, o ajusta la ruta al archivo en la etiqueta `<script>` del archivo HTML según corresponda.

Con este código, puedes ingresar un texto o un enlace en el campo de entrada, hacer clic en el botón "Generar QR", y verás el código QR generado en la página. Asegúrate de que la biblioteca "qrcode-generator" esté correctamente configurada en tu proyecto.

Ten en cuenta que este es un ejemplo simple. En una aplicación real, podrías personalizar la apariencia del código QR, guardar los códigos generados, y agregar más funcionalidades según tus necesidades.
