<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema de Gestión Hospitalaria</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        #login-section, #dashboard {
            background-color: #fff;
            border: 1px solid #ccc;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            width: 800px;
        }
        #login-section {
            display: block;
        }
        #dashboard {
            display: none;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        table, th, td {
            border: 1px solid #ccc;
            padding: 10px;
            text-align: center;
        }
        th {
            background-color: #f2f2f2;
        }
        #stats {
            display: flex;
            justify-content: space-around;
            margin-bottom: 20px;
        }
        .stat {
            background-color: #f2f2f2;
            padding: 20px;
            border-radius: 5px;
            text-align: center;
            width: 150px;
        }
        .stat span {
            display: block;
            font-size: 24px;
            font-weight: bold;
        }
        #pacientes-lista h3 {
            margin-bottom: 10px;
        }
        input, button {
            width: calc(100% - 20px);
            padding: 10px;
            margin: 10px;
        }
        button {
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <div id="login-section">
        <h2>Inicio de Sesión</h2>
        <input type="text" id="rut" placeholder="RUT">
        <input type="password" id="password" placeholder="Contraseña">
        <button onclick="login()">Ingresar</button>
    </div>

    <div id="dashboard">
        <table>
            <thead>
                <tr>
                    <th>AREA</th>
                    <th>CANTIDAD DE BOX</th>
                    <th>CAMAS DISPONIBLES</th>
                    <th>CAMAS OCUPADAS</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>ATENCIÓN MÉDICA</td>
                    <td>10</td>
                    <td>20</td>
                    <td>0</td>
                </tr>
                <tr>
                    <td>ATENCIÓN ODONTOLÓGICA</td>
                    <td>2</td>
                    <td>6</td>
                    <td>0</td>
                </tr>
                <tr>
                    <td>PROCEDIMIENTOS</td>
                    <td>6</td>
                    <td>12</td>
                    <td>0</td>
                </tr>
                <tr>
                    <td>REANIMACIÓN</td>
                    <td>4</td>
                    <td>0</td>
                    <td>0</td>
                </tr>
            </tbody>
        </table>

        <div id="stats">
            <div class="stat">
                <p>Paciente en Espera</p>
                <span id="pacientes-espera">56</span>
            </div>
            <div class="stat">
                <p>Paciente en Atención</p>
                <span id="pacientes-atencion">34</span>
            </div>
        </div>

        <div id="pacientes-lista">
            <h3>Pacientes</h3>
            <table>
                <thead>
                    <tr>
                        <th>Nombre Paciente</th>
                        <th>Categorización</th>
                        <th>Tiempo de Espera</th>
                        <th>Área</th>
                        <th>BOX</th>
                        <th>Estado</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Gómez Cortés Álvaro Mauricio</td>
                        <td>C2</td>
                        <td>01:00:00 hrs</td>
                        <td>Atención Médica</td>
                        <td>5</td>
                        <td>Atención</td>
                    </tr>
                    <tr>
                        <td>Vega Romero Rosa Alba</td>
                        <td>C1</td>
                        <td>00:30:00 min</td>
                        <td>Atención Médica</td>
                        <td>4</td>
                        <td>Atención</td>
                    </tr>
                    <tr>
                        <td>Nuñez Álvarez Saulo Alberto</td>
                        <td>C1</td>
                        <td>03:00:00 min</td>
                        <td>Atención Médica</td>
                        <td>3</td>
                        <td>Atención</td>
                    </tr>
                    <tr>
                        <td>Ramírez Ovalle Alfonso Rubén</td>
                        <td>C3</td>
                        <td>05:30:00 hrs</td>
                        <td>Atención Médica</td>
                        <td>2</td>
                        <td>Sin Atención</td>
                    </tr>
                    <tr>
                        <td>López Olivares Antonio López</td>
                        <td>C3</td>
                        <td>02:30:00 hrs</td>
                        <td>Atención Médica</td>
                        <td>1</td>
                        <td>Sin Atención</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>

    <script>
        function login() {
            const rut = document.getElementById('rut').value;
            const password = document.getElementById('password').value;

            // Aquí agregar la lógica de autenticación real
            if (rut === "12345678-9" && password === "password") {
                document.getElementById('login-section').style.display = 'none';
                document.getElementById('dashboard').style.display = 'block';
            } else {
                alert("RUT o contraseña incorrectos");
            }
        }
    </script>
</body>
</html>
