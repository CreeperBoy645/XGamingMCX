# XGamingMCX
<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GamingMC - Usługi Minecraft</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #181818;
            color: #ffffff;
            text-align: center;
            margin: 0;
            padding: 20px;
        }
        h1 {
            color: #00ff00;
        }
        .button {
            background-color: #444444;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
        }
        .button:hover {
            background-color: #555555;
        }
        .hidden {
            display: none;
        }
    </style>
    <script>
        function showOptions(mode) {
            const sections = document.querySelectorAll('div[id]');
            sections.forEach(section => {
                section.classList.add('hidden');
            });
            document.getElementById(mode).classList.remove('hidden');
        }

        function pay(rank, amount, mode) {
            const nick = document.getElementById(`nick${capitalizeFirstLetter(mode)}`).value;
            if (nick === "") {
                alert("Proszę wpisać swój nick z Minecrafta.");
                return;
            }
            const paypalUrl = `https://paypal.me/Gamingmcpl?amount=${amount}`;
            window.open(paypalUrl);
            // Przekierowanie na stronę z usługami
            window.location.href = "https://gamingmc12.wordpress.com/services";
        }

        function capitalizeFirstLetter(string) {
            return string.charAt(0).toUpperCase() + string.slice(1);
        }
    </script>
</head>
<body>

    <h1>Witaj w GamingMC!</h1>
    <p>Oferuję usługi związane z grą Minecraft, takie jak sprzedaż rang i przedmiotów w grze.</p>

    <h2>Nasze Tryby</h2>
    <button class="button" onclick="showOptions('anarchia')">Anarchia SMP</button>
    <button class="button" onclick="showOptions('drop')">Drop SMP</button>
    <button class="button" onclick="showOptions('bedwars')">Bedwars</button>
    <button class="button" onclick="showOptions('survival')">Survival</button>
    <button class="button" onclick="showOptions('oneblock')">Oneblock</button>

    <div id="anarchia" class="hidden">
        <h2>Rangi i pieniądze do Anarchia SMP</h2>
        <div>
            <input type="text" id="nickAnarchia" placeholder="Twój nick z MC" />
        </div>
        <p>Ranga: VIP</p>
        <button class="button" onclick="pay('VIP', 20, 'anarchia')">VIP na ZAWSZE (20 zł)</button>
        
        <p>Ranga: SVIP</p>
        <button class="button" onclick="pay('SVIP', 30, 'anarchia')">SVIP na ZAWSZE (30 zł)</button>
        
        <p>Ranga: Sponsor</p>
        <button class="button" onclick="pay('Sponsor', 50, 'anarchia')">Sponsor na ZAWSZE (50 zł)</button>
        
        <p>Ranga: Elita</p>
        <button class="button" onclick="pay('Elita', 100, 'anarchia')">Elita na ZAWSZE (100 zł)</button>
        
        <p>Ranga: Swagger + Gratis Duży zestaw kluczy</p>
        <button class="button" onclick="pay('Swagger', 200, 'anarchia')">Swagger na ZAWSZE (200 zł)</button>
    </div>

    <div id="drop" class="hidden">
        <h2>Rangi i pieniądze do Drop SMP</h2>
        <div>
            <input type="text" id="nickDrop" placeholder="Twój nick z MC" />
        </div>
        <p>Ranga: VIP</p>
        <button class="button" onclick="pay('VIP', 20, 'drop')">VIP na ZAWSZE (20 zł)</button>
        
        <p>Ranga: SVIP</p>
        <button class="button" onclick="pay('SVIP', 30, 'drop')">SVIP na ZAWSZE (30 zł)</button>
        
        <p>Ranga: Sponsor</p>
        <button class="button" onclick="pay('Sponsor', 50, 'drop')">Sponsor na ZAWSZE (50 zł)</button>
        
        <p>Ranga: Elita</p>
        <button class="button" onclick="pay('Elita', 100, 'drop')">Elita na ZAWSZE (100 zł)</button>
        
        <p>Ranga: Swagger + Gratis Duży zestaw kluczy</p>
        <button class="button" onclick="pay('Swagger', 200, 'drop')">Swagger na ZAWSZE (200 zł)</button>
    </div>

    <div id="bedwars" class="hidden">
        <h2>Rangi i pieniądze do Bedwars</h2>
        <div>
            <input type="text" id="nickBedwars" placeholder="Twój nick z MC" />
        </div>
        <p>Ranga: VIP</p>
        <button class="button" onclick="pay('VIP', 20, 'bedwars')">VIP na ZAWSZE (20 zł)</button>
        
        <p>Ranga: SVIP</p>
        <button class="button" onclick="pay('SVIP', 30, 'bedwars')">SVIP na ZAWSZE (30 zł)</button>
        
        <p>Ranga: Sponsor</p>
        <button class="button" onclick="pay('Sponsor', 50, 'bedwars')">Sponsor na ZAWSZE (50 zł)</button>
        
        <p>Ranga: Elita</p>
        <button class="button" onclick="pay('Elita', 100, 'bedwars')">Elita na ZAWSZE (100 zł)</button>
        
        <p>Ranga: Swagger + Gratis Duży zestaw kluczy</p>
        <button class="button" onclick="pay('Swagger', 200, 'bedwars')">Swagger na ZAWSZE (200 zł)</button>
    </div>

    <div id="survival" class="hidden">
        <h2>Rangi i pieniądze do Survival</h2>
        <div>
            <input type="text" id="nickSurvival" placeholder="Twój nick z MC" />
        </div>
        <p>Ranga: VIP</p>
        <button class="button" onclick="pay('VIP', 20, 'survival')">VIP na ZAWSZE (20 zł)</button>
        
        <p>Ranga: SVIP</p>
        <button class="button" onclick="pay('SVIP', 30, 'survival')">SVIP na ZAWSZE (30 zł)</button>
        
        <p>Ranga: Sponsor</p>
        <button class="button" onclick="pay('Sponsor', 50, 'survival')">Sponsor na ZAWSZE (50 zł)</button>
        
        <p>Ranga: Elita</p>
        <button class="button" onclick="pay('Elita', 100, 'survival')">Elita na ZAWSZE (100 zł)</button>
        
        <p>Ranga: Swagger + Gratis Duży zestaw kluczy</p>
        <button class="button" onclick="pay('Swagger', 200, 'survival')">Swagger na ZAWSZE (200 zł)</button>
    </div>

    <div id="oneblock" class="hidden">
        <h2>Rangi i pieniądze do Oneblock</h2>
        <div>
            <input type="text" id="nickOneblock" placeholder="Twój nick z MC" />
        </div>
        <p>Ranga: VIP</p>
        <button class="button" onclick="pay('VIP', 20, 'oneblock')">VIP na ZAWSZE (20 zł)</button>
        
        <p>Ranga: SVIP</p>
        <button class="button" onclick="pay('SVIP', 30, 'oneblock')">SVIP na ZAWSZE (30 zł)</button>
        
        <p>Ranga: Sponsor</p>
        <button class="button" onclick="pay('Sponsor', 50, 'oneblock')">Sponsor na ZAWSZE (50 zł)</button>
        
        <p>Ranga: Elita</p>
        <button class="button" onclick="pay('Elita', 100, 'oneblock')">Elita na ZAWSZE (100 zł)</button>
        
        <p>Ranga: Swagger + Gratis Duży zestaw kluczy</p>
        <button class="button" onclick="pay('Swagger', 200, 'oneblock')">Swagger na ZAWSZE (200 zł)</button>
    </div>

</body>
</html>
