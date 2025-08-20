<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
</head>
<body>
    <h1>Can I ask you two questions?</h1>
    
    <p>On a scale from 1 to 10, 1 being not so sure and 10 being absolutely certain, if you died right now how certain are you that you'd go to Heaven?</p>
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
                    <p>If you were a doctor, and I was your healthy looking patient unknowingly riddled with a life threatening disease, would you prescribe me medicine first or show me proof of my disease? Of course, proof of disease or else I wouldn't believe you and agree to the medicine. In the same way, in our brief moment here, I have to try to convince you of a disease plauging you or you won't understand the need for the cure. As it stands right now you think you're a "good" (healthy) person.<br><br>

                    This part is uncomfortable, but crucial to understand the Good News. Are you ready?<br><br><br>


                    1. How many lies have you told in your life? What do we call someone who tells lies? (A liar)
                    2. Have you ever stolen something no matter how small or time from an employer? What do we call someone who steals? (A thief)
                    3. Have you ever lusted or had sex outside of marriage?
                    4. Have you ever taken God's name in vain and used it as a cuss word?<br><br>

                    Now I'm not judging you, but what you've just said is you're a blasphemous, lying, thieving, fornicating, and adulterer at heart. If God judges you based on the 10 Commandments, of which we've only examined 4, on Judgement Day will you be innocent or guilty? (Guilty). Would you go to Heaven or Hell? (Hell). Just stop... and feel the weight of that..<br><br>

                    Now, when Jesus said, "It is finished" before giving up His life on the cross. Why did he say that? Scripture tells us the wages of sin is death (Romans 6:23). A wage is something you earn for your actions. God has told us, what we have earned for our sin is the death sentence. In the same way that a judge in a court of law can legally declare you guiltless from your pile of speeding tickets because someone else paid on your behalf, so God can justly remove the death sentence from your head, so long as you accept Jesus' payment on your behalf. You can accept His payment, or you can pay for it yourself. There are no other options.<br><br>

                    That is why Jesus said, "It is finished." He was declaring for any and all who will accept it, your death sentence is paid on His behalf. You can be declared forgiven and righteous and innocent. Separation from God fully restored.<br><br>

                    If your answer between 0 and 10 was anything besides a 10, you need to know Jesus died for ALL your sins: past, present, and future. Not just 70% of them. All of them.<br>
                    And to the hypothetical why should I let you in question? The correct heart posture and answer is "because JESUS" paid on my behalf. 
                    If your answer was "because I ___" it highlights a foundational misunderstanding of how your sin separates you from your Creator and what it cost Him to pay your fines. You couldn't earn it, you could never do it yourself, you can only accept the free gift for what it is.<br><br>
                    
                    Lord Jesus, if they have read to this point their soul is seeking you, please let your love and peace wash over them. Save them. Right this very minute let them pass from death to life in faith in you, accepting your life laid down for them. Please continue to reveal yourself to them and draw them in with your love and kidness. Amen.</p>
                `;
                resultDiv.innerHTML = message;
            } else {
                alert("Please answer both questions.");
            }
        }
    </script>
    <button onclick="visitGotQuestions()">Visit GotQuestions.org</button>

<script>
    function visitGotQuestions() {
        window.location.href = "https://www.gotquestions.org/";
    }
</script>

</body>
</html>
