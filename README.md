# desenvolvido por: Matheus, Luis, Gabriel.
 <!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora IMC</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }
 
        #calculator {
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            width: 80%;
            max-width: 400px;
        }
 
        label {
            display: block;
            margin-bottom: 10px;
        }
 
        input {
            width: calc(100% - 16px);
            padding: 8px;
            box-sizing: border-box;
            margin-bottom: 20px;
        }
 
        button {
            background-color: #4caf50;
            color: #fff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 4px;
            cursor: pointer;
        }
 
        button:hover {
            background-color: #45a049;
        }
 
        #result {
            font-size: 18px;
            margin-top: 20px;
            color: #333; 
        }
    </style>
</head>
<body>
    <div id="calculator">
        <h2>Calculadora IMC</h2>
        <label for="weight">Peso (kg):</label>
        <input type="number" id="weight" placeholder="Digite seu peso">
 
        <label for="height">Altura (m):</label>
        <input type="number" id="height" placeholder="Digite sua altura">
 
        <button onclick="calculateIMC()">Calcular IMC</button>
 
        <div id="result"></div>
    </div>
 
    <script>
        function calculateIMC() {
            var weight = document.getElementById('weight').value;
            var height = document.getElementById('height').value;
 
            if (weight !== '' && height !== '') {
                var bmi = weight / (height * height);
                displayResult(bmi);
            } else {
                alert('Por favor, preencha todos os campos.');
            }
        }
 
        function displayResult(bmi) {
            var resultDiv = document.getElementById('result');
            resultDiv.innerHTML = 'Seu IMC é: ' + bmi.toFixed(2);
        }
    </script>
</body>
</html>
