<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <button onclick="checkAnswers()">Submit</button>

    <div id="result"></div>

    <button id="visitButton" onclick="visitGotQuestions()" style="display: none;">Visit GotQuestions.org</button>

    <script>
        function checkAnswers() {
            console.log("checkAnswers function called");

            const resultDiv = document.getElementById("result");
            const message = `
                <p>When a sheep stands in the forest you will think he looks white as snow...</p>
                <!-- (rest of the message) -->
            `;
            resultDiv.innerHTML = message;

            // Show the "Visit GotQuestions.org" button
            document.getElementById("visitButton").style.display = "block";
        }

        function visitGotQuestions() {
            window.location.href = "https://www.gotquestions.org/";
        }
    </script>
</body>
</html>
