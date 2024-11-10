# se-et-ce
<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice - ce vs se</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }

        .correct {
            color: green;
        }

        .incorrect {
            color: red;
        }

        .analyse {
            color: blue;
        }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["ce", "se", "ce", "se", "ce", "se", "se", "ce", "se", "ce",
                                     "ce", "se", "se", "ce", "ce", "se", "ce", "se", "se", "ce"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));
                let analyse = document.getElementById('analyse' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✔️ Correct";
                    feedback.className = "correct";
                    analyse.innerText = "";
                    score++;
                } else {
                    feedback.innerText = "❌ Incorrect";
                    feedback.className = "incorrect";
                    analyse.innerText = `La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "ce" est un déterminant démonstratif ou un pronom démonstratif (ex : Ce livre est intéressant), tandis que "se" est un pronom réfléchi utilisé devant un verbe pronominal (ex : Il se lave).`;
                    analyse.className = "analyse";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>

<body>
    <h2>Règle : "ce" vs "se"</h2>
    <p>
        - <b>"ce"</b> est un déterminant démonstratif ou un pronom démonstratif. Exemple : "Ce livre est passionnant".<br>
        - <b>"se"</b> est un pronom réfléchi, utilisé avec les verbes pronominaux. Exemple : "Il se réveille tôt le matin".
    </p>

    <h2>Exercice - Complétez avec "ce" ou "se"</h2>

    <!-- Génération des 20 questions -->
    <div id="exercices">
        <p>1. ___ garçon est très intelligent.</p>
        <input type="text" id="reponse1"> <span id="feedback1"></span><br>
        <p id="analyse1"></p><br>

        <p>2. Il ___ prépare pour la fête.</p>
        <input type="text" id="reponse2"> <span id="feedback2"></span><br>
        <p id="analyse2"></p><br>

        <p>3. ___ n'est pas très clair.</p>
        <input type="text" id="reponse3"> <span id="feedback3"></span><br>
        <p id="analyse3"></p><br>

        <p>4. Elle ___ demande si elle a bien fait.</p>
        <input type="text" id="reponse4"> <span id="feedback4"></span><br>
        <p id="analyse4"></p><br>

        <p>5. ___ chien est très amical.</p>
        <input type="text" id="reponse5"> <span id="feedback5"></span><br>
        <p id="analyse5"></p><br>

        <p>6. Il ___ sent mal après l'accident.</p>
        <input type="text" id="reponse6"> <span id="feedback6"></span><br>
        <p id="analyse6"></p><br>

        <p>7. Ils ___ disputent souvent pour rien.</p>
        <input type="text" id="reponse7"> <span id="feedback7"></span><br>
        <p id="analyse7"></p><br>

        <p>8. ___ film était vraiment bien.</p>
        <input type="text" id="reponse8"> <span id="feedback8"></span><br>
        <p id="analyse8"></p><br>

        <p>9. Il ___ fait des amis rapidement.</p>
        <input type="text" id="reponse9"> <span id="feedback9"></span><br>
        <p id="analyse9"></p><br>

        <p>10. ___ n'est pas possible sans efforts.</p>
        <input type="text" id="reponse10"> <span id="feedback10"></span><br>
        <p id="analyse10"></p><br>

        <p>11. ___ livre appartient à ma sœur.</p>
        <input type="text" id="reponse11"> <span id="feedback11"></span><br>
        <p id="analyse11"></p><br>

        <p>12. Il ___ souvient de tout ce qui s'est passé.</p>
        <input type="text" id="reponse12"> <span id="feedback12"></span><br>
        <p id="analyse12"></p><br>

        <p>13. Ils ___ battent pour la victoire.</p>
        <input type="text" id="reponse13"> <span id="feedback13"></span><br>
        <p id="analyse13"></p><br>

        <p>14. ___ moment était parfait.</p>
        <input type="text" id="reponse14"> <span id="feedback14"></span><br>
        <p id="analyse14"></p><br>

        <p>15. ___ n'est pas ce que j'attendais.</p>
        <input type="text" id="reponse15"> <span id="feedback15"></span><br>
        <p id="analyse15"></p><br>

        <p>16. Elle ___ coiffe tous les matins.</p>
        <input type="text" id="reponse16"> <span id="feedback16"></span><br>
        <p id="analyse16"></p><br>

        <p>17. ___ bruit est insupportable.</p>
        <input type="text" id="reponse17"> <span id="feedback17"></span><br>
        <p id="analyse17"></p><br>

        <p>18. Ils ___ cachent derrière la porte.</p>
        <input type="text" id="reponse18"> <span id="feedback18"></span><br>
        <p id="analyse18"></p><br>

        <p>19. ___ qu'il fait est incroyable.</p>
        <input type="text" id="reponse19"> <span id="feedback19"></span><br>
        <p id="analyse19"></p><br>

        <p>20. Elle ___ fâche pour un rien.</p>
        <input type="text" id="reponse20"> <span id="feedback20"></span><br>
        <p id="analyse20"></p><br>
    </div>

    <button onclick="verifier()">Vérifier</button>
    <p id="score"></p>
</body>

</html>
