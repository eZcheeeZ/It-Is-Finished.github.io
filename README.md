<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Can I ask you two questions?</h1>
    
    <p>On a scale from 1 to 10, 1 being not so sure and 10 being absolutely certain, how certain are you that you'd go to Heaven if you died right now?</p>
    <input type="range" id="certainty" min="1" max="10" value="5">
    <p id="certaintyLabel">5</p>
    
    <p>If you stood at the gates of Heaven and God asked, "Why should I let you in?" what would you say?</p>
    <textarea id="reason" rows="4" cols="50"></textarea>
    
    <button onclick="checkAnswers()">Submit</button>

    <div id="result"></div>

    <button id="visitButton" onclick="visitGotQuestions()" style="display: none;">Visit GotQuestions.org</button>

    <script>
        const certaintyInput = document.getElementById("certainty");
        const certaintyLabel = document.getElementById("certaintyLabel");
        const visitButton = document.getElementById("visitButton");

        certaintyInput.addEventListener("input", () => {
            certaintyLabel.innerText = certaintyInput.value;
        });

        function checkAnswers() {
            const certainty = certaintyInput.value;
            const reason = document.getElementById("reason").value;

            if (reason !== "") {
                const resultDiv = document.getElementById("result");
                const message = `
                    <p>When a sheep stands in the forest you will think he looks white as snow. But then it starts to snow and the forest becomes snow covered and you see just how dirty he actually is...</p>
                    <!-- (rest of the message) -->
                `;
                resultDiv.innerHTML = message;

                // Show the "Visit GotQuestions.org" button
                visitButton.style.display = "block";
            } else {
                alert("Please answer both questions.");
            }
        }

        function visitGotQuestions() {
            window.location.href = "https://www.gotquestions.org/";
        }
    </script>
</body>
</html>
