#mariemoi
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Proposition de mariage</title>
<link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@300&display=swap" rel="stylesheet">
<style>
    body {
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        text-align: center;
        background-color: #f5f5f5;
        padding: 50px;
    }
    h1 {
        font-size: 24px;
        margin-bottom: 20px;
        color: #333;
    }
    #message {
        font-size: 18px;
        margin-bottom: 20px;
        color: #555;
    }
    #buttons {
        display: flex;
        justify-content: center;
    }
    button {
        margin: 0 10px;
        padding: 10px 20px;
        font-size: 18px;
        cursor: pointer;
        border: none;
        border-radius: 5px;
        transition: background-color 0.3s ease;
    }
    #yesButton {
        background-color: #4CAF50;
        color: white;
    }
    #yesButton:hover {
        background-color: #45a049;
    }
    #noButton {
        background-color: #f44336;
        color: white;
    }
    #noButton:hover {
        background-color: #d32f2f;
    }
    .poem {
        font-style: italic;
        margin-top: 20px;
        color: #666;
    }
</style>
</head>
<body>
<h1>Proposition de mariage</h1>
<div id="message">Keyllia, veux-tu m'épouser ? <span id="heart">&hearts;</span></div>
<div id="buttons">
    <button id="yesButton" onclick="yesClicked()">Oui</button>
    <button id="noButton" onclick="noClicked()">Non</button>
</div>
<script>
    function yesClicked() {
        // Générateur de poèmes d'amour
        var poems = [
            "Ton amour est comme une rose, belle et épanouie, illuminant ma vie chaque jour.",
            "Dans tes yeux, je trouve la lumière qui guide mes pas et réchauffe mon cœur.",
            "Ton sourire est la clé qui ouvre les portes de mon bonheur, chaque jour un peu plus.",
            "Ta présence est un doux refrain qui berce mon âme et apaise mes craintes.",
            "Dans tes bras, je trouve le refuge où je me sens en sécurité, entouré de ton amour infini."
        ];
        var randomIndex = Math.floor(Math.random() * poems.length);
        var poem = poems[randomIndex];
        var poemElement = document.createElement("div");
        poemElement.className = "poem";
        poemElement.textContent = poem;
        document.body.appendChild(poemElement);
        
        // Masquer l'URL de la page
        window.history.pushState({}, '', '/');
    }
    
    function noClicked() {
        alert("Oh non ! Peut-être une prochaine fois !");
    }
</script>
</body>
</html>
