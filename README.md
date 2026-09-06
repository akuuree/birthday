<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Special One ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #ffe6eb;
            color: #333;
            overflow-x: hidden;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            width: 100%;
            max-width: 480px;
            height: 100vh;
            background: #fff0f3;
            position: relative;
            box-shadow: 0 0 20px rgba(255, 105, 180, 0.3);
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
            text-align: center;
            overflow: hidden;
        }

        /* Falling Hearts Background */
        .heart-bg {
            position: absolute;
            top: -10vh;
            color: #ff4d6d;
            font-size: 20px;
            animation: fall linear infinite;
            z-index: 1;
            user-select: none;
        }

        @keyframes fall {
            0% {
                transform: translateY(-10vh) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0.2;
            }
        }

        .screen {
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 100%;
            z-index: 2;
            position: absolute;
            padding: 20px;
            animation: fadeIn 0.8s ease-in-out;
        }

        .screen.active {
            display: flex;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }

        h1, h2, p {
            color: #b7094c;
            margin-bottom: 20px;
        }

        p {
            font-size: 16px;
            line-height: 1.6;
            color: #590d22;
        }

        .box {
            background: #ffb3c6;
            border: 2px dashed #ff4d6d;
            padding: 15px 30px;
            border-radius: 12px;
            font-weight: bold;
            color: #800f2f;
            cursor: pointer;
            margin: 15px 0;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            transition: 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
        }

        .box:hover {
            background: #ff8fa3;
            transform: translateY(-2px);
        }

        .hand-btn {
            font-size: 35px;
            cursor: pointer;
            margin-top: 20px;
            animation: bounce 1.5s infinite;
            background: none;
            border: none;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
            40% {transform: translateY(-10px);}
            60% {transform: translateY(-5px);}
        }

        .points-container {
            max-height: 60vh;
            overflow-y: auto;
            text-align: left;
            padding: 10px;
            width: 100%;
            font-size: 14px;
            color: #590d22;
            background: rgba(255, 255, 255, 0.6);
            border-radius: 10px;
        }

        .points-container ul {
            padding-left: 20px;
        }

        .points-container li {
            margin-bottom: 8px;
        }

        .btn-group {
            display: flex;
            gap: 20px;
            margin-top: 20px;
        }

        .choice-btn {
            padding: 10px 25px;
            font-size: 16px;
            font-weight: bold;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            background: #ff4d6d;
            color: white;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        #no-btn {
            position: relative;
            background: #adb5bd;
        }

        .scrollable-text {
            max-height: 55vh;
            overflow-y: auto;
            padding: 10px;
            font-size: 14px;
            text-align: left;
            background: rgba(255,255,255,0.5);
            border-radius: 10px;
            margin-bottom: 15px;
        }

        /* Cake & Candle CSS */
        .cake-box {
            font-size: 60px;
            cursor: pointer;
            margin: 20px 0;
            position: relative;
        }

        .smoke {
            font-size: 14px;
            color: #d81159;
            font-weight: bold;
            opacity: 0;
            transition: opacity 1s ease;
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            white-space: nowrap;
        }

        .smoke.show {
            opacity: 1;
        }

        .kiss-screen {
            background-image: radial-gradient(#ff758c, #ff7eb3);
        }
    </style>
</head>
<body>

    <div class="container" id="mainContainer">
        <!-- Screen 1: Intro -->
        <div class="screen active" id="screen1">
            <h2>Let's Begin...</h2>
            <p>I am going to introduce a girl who is very important for me.</p>
            <div class="box" onclick="nextScreen(2)">Let's reveal her</div>
        </div>

        <!-- Screen 2: Who is she -->
        <div class="screen" id="screen2">
            <p>Who is she? She is someone...</p>
            <p>She is someone who always comes into my mind whenever I am sad, whenever I am happy, every single time she comes into my mind, she is someone...</p>
            <div class="box" onclick="nextScreen(3)">Let's reveal her</div>
            <p style="margin-top: 15px; font-weight: bold; color: #ff4d6d;">dhappppaaaaaaa itti bhii jali ky haii ladli</p>
            <button class="hand-btn" onclick="nextScreen(3)">👉</button>
        </div>

        <!-- Screen 3: 50 Points why I adore her -->
        <div class="screen" id="screen3">
            <h3>Why I Adore Her</h3>
            <div class="points-container">
                <ul>
                    <li>1. Your smile lights up my entire dark world.</li>
                    <li>2. The way your eyes sparkle when you talk about things you love.</li>
                    <li>3. How purely genuine and kind your heart is.</li>
                    <li>4. You make me feel safe in ways nobody else ever could.</li>
                    <li>5. Your cute little angry face when things don't go your way.</li>
                    <li>6. The comfort I find just sitting next to you in silence.</li>
                    <li>7. How you care for me even when you are stressed yourself.</li>
                    <li>8. The way your voice sounds first thing in the morning.</li>
                    <li>9. Your endless patience with my stupid silly jokes.</li>
                    <li>10. How deeply passionate you get about your feelings.</li>
                    <li>11. The unique way you laugh fills my soul with joy.</li>
                    <li>12. You inspire me to become a better version of myself daily.</li>
                    <li>13. How effortlessly beautiful you look without even trying.</li>
                    <li>14. The fact that you understand my silence without words.</li>
                    <li>15. Your gentle touch heals all my random anxieties.</li>
                    <li>16. How you hold my hand and make everything feel okay.</li>
                    <li>17. Your adorable habit of overthinking that makes me want to squeeze you tight.</li>
                    <li>18. The pure magic hidden inside your softest hugs.</li>
                    <li>19. How completely comfortable I am being my weirdest self around you.</li>
                    <li>20. The warmth of your presence during my coldest days.</li>
                    <li>21. Your sparkling intelligence and sharp observations.</li>
                    <li>22. How fiercely loyal and protective you are of our bond.</li>
                    <li>23. The cute nicknames you give me spontaneously.</li>
                    <li>24. How you listen to my endless rantings with so much attention.</li>
                    <li>25. The tiny details you remember about me that surprise me.</li>
                    <li>26. Your breathtaking beauty that leaves me speechless every time.</li>
                    <li>27. How innocent you look when you fall asleep.</li>
                    <li>28. The strength you carry inside your delicate frame.</li>
                    <li>29. How deeply precious your happiness is to my existence.</li>
                    <li>30. The way you pout when you want something from me.</li>
                    <li>31. How effortlessly you fit into the puzzle pieces of my life.</li>
                    <li>32. Your willingness to fix things when things get rough.</li>
                    <li>33. The cute expressions you make when you are focused.</li>
                    <li>34. How you bring light into my routine and chaotic days.</li>
                    <li>35. The peace that washes over me when you say everything is fine.</li>
                    <li>36. How beautifully honest you are with your emotions.</li>
                    <li>37. The sparkle of mischief in your eyes right before a prank.</li>
                    <li>38. How proud I feel just walking right beside you.</li>
                    <li>39. The safety net of your unconditional love and care.</li>
                    <li>40. How you make every ordinary moment feel like a celebration.</li>
                    <li>41. The soothing melody of your soft sighs.</li>
                    <li>42. Your golden heart that sees the best in everyone.</li>
                    <li>43. How deeply you reside inside my thoughts every single second.</li>
                    <li>44. The way you look at me like I am your entire universe.</li>
                    <li>45. Your sweet vulnerability that shows how much you trust me.</li>
                    <li>46. How perfectly our hands lock together like they were made for it.</li>
                    <li>47. The eternal sweetness you added to my bittersweet life.</li>
                    <li>48. Your gorgeous soul that outshines every standard of beauty.</li>
                    <li>49. Simply because you are *you*, totally irreplaceable.</li>
                    <li>50. Because loving you is the easiest and best thing I've ever done.</li>
                </ul>
                <p style="text-align: center; margin-top: 10px; font-weight: bold;">List will go on and on and on ......</p>
            </div>
            <button class="hand-btn" onclick="nextScreen(4)">👉 Put your hand here</button>
        </div>

        <!-- Screen 4: Heartfelt Message & Love Confession -->
        <div class="screen" id="screen4">
            <div class="scrollable-text">
                <p>Bachhaa ik aap kitta jaade mujhe pyaar krtee pr uk mai kitta jaade krta hu mai vo sbd me express hi nhi kr pata mujhe pata meri ex log ko leke aap bhut insecure feel krti pr bacha aapko pata haiii maii jeetna pyaar krta aapse utna dono me se kbhi kisi se nhii like lgtaa thaa unke bin reh nhii papaunga pr reh liyaa pr aapke binaa raha hi nhii jaata thoda sa aapka tbiyat kharab hota mera jee kharab ho jaata maii didi ya kisi se puchne lgtaa ki aap kaha ho aap theek ho ki nhii appka hlka sa mood change hota mujhe dr lg jaata ki meri bachhi thik hai ya maine hurt kr diya kuch pehle maii itna kuch nhi krtaa thaa hh mnata thaa pr mere gussa aa jati thii mai chhod deta thii pr aapke samne nhh gussa kr pata nh naraz ho pata itti jaade pyaari jo ho aur sundrtaa ka baat kahu to aap unse bhut upr ho beta ji lakh guna upr dil ki sundrta ka baat karu to vo match bhii nhh kr paaye bachha you are mine aur ap meri hi rahogii aur aapka hi hu dw bacha bcuz i love you so so muchh muchh and more than you thought.</p>
                <p style="margin-top: 10px;">A soch to skti hi ho ☺️</p>
            </div>
            <p style="font-weight: bold; margin: 10px 0;">Do you love me?</p>
            <div class="btn-group">
                <button class="choice-btn" onclick="nextScreen(5)">Yes</button>
                <button class="choice-btn" id="no-btn" onmouseover="moveButton()" ontouchstart="moveButton()">No</button>
            </div>
        </div>

        <!-- Screen 5: Extended Love Message -->
        <div class="screen" id="screen5">
            <div class="scrollable-text">
                <p>When I first met you, I had no idea I was gonna get this attached. As the days went by, I could feel myself slowly falling in love with you. I think about you all the time from the moment I wake up to the moment I fall asleep. When I think about you, I realize that you are the one that holds the key to my heart. I know for a fact we are meant for each other.</p>
                <p style="margin-top: 10px;">Seeing your smile literally changes my whole day, Just know I will never let go of you and my feelings will never disappear. I wish I was able to explain how wonderful you are to me, how can just look at you and never get tired of your beauty. How the sounds of your voice gives me butterflies. How hearing your laugh makes me smile I wish I could also tell you how much I love you but you have me loss of words. And even if I could put the words together to tell you these things it wouldn't come anywhere near to show you how much you mean to me. I may not be the most perfect guy or the most amazing but i'll put my all into our relationship. I'll treat you like a queen. I will give reassurance and loyalty and love and care and affection and attention and i'll try to make you feel like you found home. I really want to do my best for youuu!! That's my promise to you!! I love youuu Ik it's a little bit cringe but...</p>
            </div>
            <div class="box" style="margin-top: 5px; padding: 10px 20px;" onclick="nextScreen(6)">Next ➡️</div>
        </div>

        <!-- Screen 6: Cake & Candle -->
        <div class="screen" id="screen6">
            <h3>Make a Wish & Blow the Candle! 🎂</h3>
            <div class="cake-box" onclick="blowCandle()">
                <div class="smoke" id="smokeText">Aalie I love you ❤️</div>
                🍰🕯️
            </div>
            <p style="font-size: 13px; color: #800f2f;">(Tap the cake to blow the candle)</p>
            <div id="afterBlow" style="display: none; margin-top: 15px;">
                <div class="box" onclick="nextScreen(7)">Continue to Birthday Wishes 🎉</div>
            </div>
        </div>

        <!-- Screen 7: Final Birthday Note -->
        <div class="screen" id="screen7">
            <div class="scrollable-text">
                <p>Meri jaaan happy birthday! Like ky hi btau is din ka kb se wait kiya mtlb mai baap nhii bnaa pr aapke papa jeetna khus hue honge usse jaade nhh usse km kukii mere life me aane ka yehii to aik rastaa thaa nhh meri jaan aap paida hue udhr aur jaan me mere rahat mili mere idhr.</p>
                <p style="margin-top: 10px;">Baby ky hi btau mere liye kitta special ho aap, mai to allah bhagwan jesus jaha jo bhii hr jgh sar jhuka aau pr mujhe hr janam bs aap hi aap chahiye to agli bar mere saath bihar me paida hona tujhse bachpan me hi shaadi krunga itta lambaa wait nhii krna pdegaa aapko heheheheh.</p>
                <p style="margin-top: 10px;">Happy birthday meri jaan enjoy karo aur yaad rkhna koii haii jisko aapki bhut fikr haii to khayal rkhna ache se aur moj masti krtee aur merii trh pagalpanti bhii.</p>
            </div>
            <div class="box" onclick="showKisses()" style="background: #ff4d6d; color: white;">
                umaaaaaaaaaaaaaaaah umaaaaaaaaaaaaaah 💋
            </div>
        </div>

        <!-- Screen 8: Kiss Explosion -->
        <div class="screen kiss-screen" id="screen8" style="background: #ffb3c6;">
            <h2 style="color: #fff; text-shadow: 0 2px 5px rgba(0,0,0,0.2);">Forever & Always Yours! ❤️💋</h2>
            <div id="kissContainer" style="font-size: 28px; line-height: 2; margin-top: 20px;">
                💋😘❤️💋😘❤️💋😘❤️💋😘❤️💋😘❤️💋😘❤️
            </div>
            <p style="color: #fff; font-weight: bold; margin-top: 20px;">I Love You So Much, My Everything! ✨</p>
        </div>

    </div>

    <script>
        // Generate Falling Hearts
        const container = document.getElementById('mainContainer');
        for (let i = 0; i < 15; i++) {
            const heart = document.createElement('div');
            heart.classList.add('heart-bg');
            heart.innerHTML = '💖';
            heart.style.left = Math.random() * 100 + '%';
            heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
            heart.style.animationDelay = (Math.random() * 5) + 's';
            container.appendChild(heart);
        }

        // Screen Navigation Logic
        function nextScreen(screenNum) {
            document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
            document.getElementById('screen' + screenNum).classList.add('active');
        }

        // Dodging 'No' Button
        function moveButton() {
            const noBtn = document.getElementById('no-btn');
            const x = Math.random() * 160 - 80;
            const y = Math.random() * 160 - 80;
            noBtn.style.transform = `translate(${x}px, ${y}px)`;
        }

        // Blow Candle Logic
        function blowCandle() {
            document.getElementById('smokeText').classList.add('show');
            document.getElementById('afterBlow').style.display = 'block';
        }

        // Show Final Kisses
        function showKisses() {
            nextScreen(8);
        }
    </script>
</body>
</html>
