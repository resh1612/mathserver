# Ex.05 Design a Website for Server Side Processing
# Date:1.12.2024
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incandescent Bulb Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center; 
            background-color: #dc86f7;
        }

        .container {
            width: 100%;
            max-width: 600px;
            padding: 30px;
            background-color: rgb(230, 89, 248);
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            box-sizing: border-box; /* Ensure padding doesn't overflow */
            transform: translateX(-150px); /* Moves the container 20px to the left */
        }

        h1 {
            font-size: 24px;
            margin-bottom: 20px;
        }

        label {
            font-size: 18px;
            display: block;
            margin-bottom: 8px;
            text-align: center;
        }

        input {
            width: 100%;
            padding: 10px;
            font-size: 16px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }

        button {
            width: 100%;
            padding: 12px;
            font-size: 18px;
            background-color: #46065f;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #f0a58e;
        }

        .result {
            margin-top: 20px;
            font-size: 20px;
            padding: 15px;
            background-color: #e7f3e7;
            border: 1px solid #d4f4d4;
            border-radius: 4px;
            display: none;
        }

        .powerimage {
            right: 20px;
            height: 100%;
            width: 100%;
        }
    </style>
</head>
<body>

<div class="powerimage" alt="powerimage1">
    <img src="powerimage1.jpg" alt="Power Image">
</div>

<div class="container">
    <h1>Incandescent Bulb Power Calculator</h1>

    <form id="calculatorForm">
        <label for="intensity">Enter Intensity (I in Amperes):</label>
        <input type="number" id="intensity" name="intensity" step="any" required>

        <label for="resistance">Enter Resistance (R in Ohms):</label>
        <input type="number" id="resistance" name="resistance" step="any" required>

        <button type="button" onclick="calculatePower()">Calculate Power</button>
    </form>

    <div class="result" id="result">
        Power (P) = <span id="powerResult"></span> Watts
    </div>
</div>

<script>
    function calculatePower() {
        const intensity = parseFloat(document.getElementById("intensity").value);
        const resistance = parseFloat(document.getElementById("resistance").value);

        if (isNaN(intensity) || isNaN(resistance) || intensity <= 0 || resistance <= 0) {
            alert("Please enter valid positive numbers for Intensity and Resistance.");
            return;
        }

        const power = Math.pow(intensity, 2) * resistance;

        document.getElementById("powerResult").innerText = power.toFixed(2);
        document.getElementById("result").style.display = "block";
    }
</script>

</body>
</html>

# SERVER SIDE PROCESSING:
![image](https://github.com/user-attachments/assets/25cf8ef3-b4ec-453a-afa7-4e7936543aa5)

# HOMEPAGE:
![image](https://github.com/user-attachments/assets/7b3f352e-e848-47b1-99ca-e8efb793ab70)

# RESULT:
The program for performing server side processing is completed successfully.
