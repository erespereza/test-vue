<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario de Registro</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        form {
            max-width: 400px;
            margin: 0 auto;
        }
        label {
            display: block;
            margin-top: 10px;
        }
        input, select {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            box-sizing: border-box;
        }
        .checkbox {
            display: flex;
            align-items: center;
        }
        .checkbox input {
            width: auto;
            margin-right: 10px;
        }
        button {
            margin-top: 20px;
            padding: 10px;
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>
    <h1>Formulario de Registro</h1>
    <form action="#" method="POST">
        <label for="nombre">Nombre:</label>
        <input type="text" id="nombre" name="nombre" placeholder="Ingresa tu nombre" required>

        <label for="apellido">Apellido:</label>
        <input type="text" id="apellido" name="apellido" placeholder="Ingresa tu apellido" required>

        <label for="cc">Cédula de Ciudadanía (CC):</label>
        <input type="text" id="cc" name="cc" placeholder="Ingresa tu número de cédula" required>

        <label for="materias">Materias:</label>
        <input type="text" id="materias" name="materias" placeholder="Ingresa las materias">

        <div class="checkbox">
            <input type="checkbox" id="documentacion" name="documentacion">
            <label for="documentacion">Documentación entregada</label>
        </div>

        <button type="submit">Enviar</button>
    </form>
</body>
</html>
