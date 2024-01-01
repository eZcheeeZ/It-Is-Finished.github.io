<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gospel Quiz</title>
</head>
<body>
    <h1>Gospel Quiz</h1>
    
    <p>On a scale from 1 to 10, how certain are you that you'd go to Heaven right now?</p>
    <input type="range" id="certainty" min="1" max="10" value="5">
    <p id="certaintyLabel">5</p>
    
    <p>If you stood at the gates of Heaven and God asked, "Why should I let you in?" what would you say?</p>
    <textarea id="reason" rows="4" cols="50"></textarea>
    
    <button onclick="checkAnswers()">Submit</button>

    <div id="result"></div>

    <script>
        const certaintyInput = document.getElementById("certainty");
        const certaintyLabel = document.getElementById("certaintyLabel");

        certaintyInput.addEventListener("input", () => {
            certaintyLabel.innerText = certaintyInput.value;
        });

        function checkAnswers() {
            const certainty = certaintyInput.value;
            const reason = document.getElementById("reason").value;

            if (reason !== "") {
                const resultDiv = document.getElementById("result");
                const message = `
                    <p>When a sheep stands in the forest he looks white as snow. When that same sheep stands in the snow, you can see just how dirty he actually is. In the same way, when we compare ourselves to others, horizontally, we feel righteous. I mean we haven’t done as much evil as people we’ve heard about. That’s us standing in the forest. When we compare ourselves vertically, however, to Gods standard - the mirror of the 10 Commandments, with humility, we finally see just how dirty we are. The 10 Commandments act as a mirror, and a realization that our hearts are wicked and deceitful beyond measure and we are desperately hopeless and in need of saving. Without this foundational understanding, the Gospel message of Jesus that we’ve been inoculated to, doesn’t carry much weight because on the horizontal plane, we aren’t that bad. The Good News of the Gospel has always been, you can be a 10/10 certainty that you will go to Heaven, if your reason in the hypothetical situation God asks, “why should I let you in,” is “because Jesus.” If your answer is “because I” it highlights a misunderstanding of how your sin separates you from God and/or how Jesus legally paid the fine to set you free.</p>
                `;
                resultDiv.innerHTML = message;
            } else {
                alert("Please answer both questions.");
            }
        }
    </script>
</body>
</html>
