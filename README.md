<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Interest Calculator</title>
    <script>
        function calculateSimpleInterest() {
            // Get values from input fields
            const principal = parseFloat(document.getElementById("principal").value);
            const rate = parseFloat(document.getElementById("rate").value);
            const time = parseFloat(document.getElementById("time").value);
            
            // Validate inputs
            if (isNaN(principal) || isNaN(rate) || isNaN(time)) {
                document.getElementById("result").innerText = "Please enter valid numbers.";
                return;
            }

            // Calculate simple interest
            const interest = (principal * rate * time) / 100;

            // Display the result
            document.getElementById("result").innerText = `The simple interest is: $${interest.toFixed(2)}`;
        }
    </script>
</head>
<body>
    <h1>Simple Interest Calculator</h1>
    <label for="principal">Principal Amount:</label>
    <input type="number" id="principal" required><br><br>

    <label for="rate">Rate of Interest (%):</label>
    <input type="number" id="rate" required><br><br>

    <label for="time">Time Period (years):</label>
    <input type="number" id="time" required><br><br>

    <button onclick="calculateSimpleInterest()">Calculate</button>

    <h2 id="result"></h2>
</body>
</html>
