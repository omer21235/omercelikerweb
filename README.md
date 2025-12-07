<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>Tıklama Oyunu + Arama</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #clicker {
            margin-top: 30px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }
        #score {
            font-size: 24px;
            margin-top: 20px;
        }
        input {
            padding: 8px;
            font-size: 16px;
        }
    </style>
</head>
<body>

<h1>Arama ve Tıklama Oyunu</h1>

<!-- Arama Kutusu -->
<input id="search" placeholder="Bir şey yaz">
<button onclick="search()">Ara</button>

<!-- Tıklama Oyunu -->
<div id="clicker">
    <h2>Tıklama Oyunu</h2>
    <button onclick="addScore()">Tıkla!</button>
    <div id="score">Skor: 0</div>
</div>

<script>
    // Arama Fonksiyonu
    function search() {
        let input = document.getElementById('search').value.toLowerCase();
        if(input === "discord") {
            window.location.href = "https://discord.com";
        } else if(input === "oyun") {
            // Oyunun olduğu kısma scroll yapabiliriz
            document.getElementById('clicker').scrollIntoView({behavior: "smooth"});
        } else {
            alert("Sonuç bulunamadı");
        }
    }

    // Tıklama Oyunu Fonksiyonu
    let score = 0;
    function addScore() {
        score++;
        document.getElementById('score').innerText = "Skor: " + score;
    }
</script>

</body>
</html>
