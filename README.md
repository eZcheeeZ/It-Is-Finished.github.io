<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gospel Quiz</title>
</head>
<body>
    <h1>Gospel Quiz</h1>
    
    <p>Between 1 and 10, how certain are you that you'd go to Heaven right now?</p>
    <input type="number" id="certainty" min="1" max="10">
    
    <p>If you stood at the gates of Heaven and God asked, "Why should I let you in?" what would you say?</p>
    <textarea id="reason" rows="4" cols="50"></textarea>
    
    <button onclick="checkAnswers()">Submit</button>

    <div id="result"></div>

    <script>
        function checkAnswers() {
            const certainty = document.getElementById("certainty").value;
            const reason = document.getElementById("reason").value;

            if (certainty !== "" && reason !== "") {
                const resultDiv = document.getElementById("result");
                const message = `
                    <p>When a sheep stands in the forest he looks white as snow...</p>
                    <p>The Good News of the Gospel has always been, you can be a 10/10 certainty that you will go to Heaven, if your reason in the hypothetical situation God asks, "Why should I let you in," is "because Jesus." If your answer is "because I" it highlights a misunderstanding of how your sin separates you from God and/or how Jesus legally paid the fine to set you free.</p>
                `;
                resultDiv.innerHTML = message;
            } else {
                alert("Please answer both questions.");
            }
        }
    </script>
</body>
</html>
