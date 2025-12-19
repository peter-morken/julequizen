<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="mobile-web-app-capable" content="yes">
    <title>Nisseopprøret 🎅</title>
    <link href="https://fonts.googleapis.com/css2?family=Mountains+of+Christmas:wght@400;700&family=Karla:wght@400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            overflow-x: hidden;
            width: 100%;
            max-width: 100vw;
        }

        :root {
            --crimson: #C41E3A;
            --forest: #0F5132;
            --gold: #FFD700;
            --snow: #FFFAFA;
            --silver: #C0C0C0;
            --pine: #01411C;
            --berry: #8B0000;
        }

        body {
            font-family: 'Karla', sans-serif;
            background: linear-gradient(135deg, #1a472a 0%, #0a2818 50%, #051810 100%);
            min-height: 100vh;
            color: var(--snow);
            position: relative;
            overflow-x: hidden;
            -webkit-tap-highlight-color: transparent;
            -webkit-touch-callout: none;
            width: 100%;
            max-width: 100vw;
        }

        /* Animated snowflakes background */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(2px 2px at 20% 30%, white, transparent),
                radial-gradient(2px 2px at 60% 70%, white, transparent),
                radial-gradient(1px 1px at 50% 50%, white, transparent),
                radial-gradient(1px 1px at 80% 10%, white, transparent),
                radial-gradient(2px 2px at 90% 60%, white, transparent),
                radial-gradient(1px 1px at 33% 80%, white, transparent),
                radial-gradient(1px 1px at 15% 55%, white, transparent);
            background-size: 200% 200%;
            animation: snow 20s linear infinite;
            opacity: 0.4;
            pointer-events: none;
            z-index: 1;
        }

        @keyframes snow {
            0% { background-position: 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%, 0% 0%; }
            100% { background-position: 200% 200%, 200% 200%, 200% 200%, 200% 200%, 200% 200%, 200% 200%, 200% 200%; }
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem;
            position: relative;
            z-index: 2;
            width: 100%;
            box-sizing: border-box;
        }

        header {
            text-align: center;
            margin-bottom: 3rem;
            animation: slideDown 0.8s ease-out;
        }

        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h1 {
            font-family: 'Mountains of Christmas', cursive;
            font-size: 4rem;
            color: var(--gold);
            text-shadow: 
                3px 3px 0 var(--crimson),
                6px 6px 0 var(--berry),
                -2px -2px 15px rgba(255, 215, 0, 0.3);
            margin-bottom: 0.5rem;
            letter-spacing: 2px;
            word-wrap: break-word;
            overflow-wrap: break-word;
        }

        .subtitle {
            font-size: 1.2rem;
            color: var(--silver);
            letter-spacing: 3px;
            text-transform: uppercase;
        }

        .card {
            background: rgba(255, 250, 250, 0.08);
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 215, 0, 0.2);
            border-radius: 20px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            animation: fadeIn 0.6s ease-out;
            animation-fill-mode: both;
            word-wrap: break-word;
            overflow-wrap: break-word;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .card:nth-child(1) { animation-delay: 0.1s; }
        .card:nth-child(2) { animation-delay: 0.2s; }
        .card:nth-child(3) { animation-delay: 0.3s; }
        .card:nth-child(4) { animation-delay: 0.4s; }

        h2 {
            font-family: 'Mountains of Christmas', cursive;
            font-size: 2rem;
            color: var(--gold);
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .input-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            color: var(--silver);
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 1px;
        }

        input[type="text"],
        textarea {
            width: 100%;
            padding: 1rem;
            border: 2px solid rgba(255, 215, 0, 0.3);
            border-radius: 12px;
            background: rgba(255, 250, 250, 0.05);
            color: var(--snow);
            font-family: 'Karla', sans-serif;
            font-size: 1rem;
            transition: all 0.3s ease;
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
        }

        input[type="text"]:focus,
        textarea:focus {
            outline: none;
            border-color: var(--gold);
            background: rgba(255, 250, 250, 0.1);
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.2);
        }

        textarea {
            resize: vertical;
            min-height: 100px;
        }

        button {
            background: linear-gradient(135deg, var(--crimson) 0%, var(--berry) 100%);
            color: var(--snow);
            border: none;
            padding: 1rem 2.5rem;
            border-radius: 12px;
            font-family: 'Karla', sans-serif;
            font-size: 1rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(196, 30, 58, 0.4);
            -webkit-tap-highlight-color: transparent;
            touch-action: manipulation;
            min-height: 48px; /* Minimum touch target size */
        }

        button:hover,
        button:active {
            transform: translateY(-2px);
            box-shadow: 0 6px 25px rgba(196, 30, 58, 0.6);
        }

        button:active {
            transform: translateY(0);
        }

        button:disabled {
            background: rgba(255, 255, 255, 0.2);
            cursor: not-allowed;
            box-shadow: none;
        }

        .task-list {
            display: grid;
            gap: 1rem;
        }

        .task-item {
            background: rgba(255, 250, 250, 0.05);
            border: 2px solid transparent;
            border-radius: 12px;
            padding: 1.5rem;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .task-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 4px;
            height: 100%;
            background: var(--gold);
            transform: scaleY(0);
            transition: transform 0.3s ease;
        }

        .task-item.completed {
            border-color: rgba(15, 81, 50, 0.5);
            background: rgba(15, 81, 50, 0.1);
        }

        .task-item.completed::before {
            transform: scaleY(1);
            background: var(--forest);
        }

        .task-item.active {
            border-color: var(--gold);
            background: rgba(255, 215, 0, 0.05);
        }

        .task-item.locked {
            opacity: 0.5;
            pointer-events: none;
        }

        .task-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }

        .task-number {
            font-family: 'Mountains of Christmas', cursive;
            font-size: 1.5rem;
            color: var(--gold);
            font-weight: 700;
        }

        .task-status {
            padding: 0.25rem 1rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .task-status.completed {
            background: var(--forest);
            color: var(--gold);
        }

        .task-status.active {
            background: var(--gold);
            color: var(--pine);
        }

        .task-status.locked {
            background: rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
        }

        .task-question {
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: var(--snow);
            line-height: 1.6;
            word-wrap: break-word;
            overflow-wrap: break-word;
        }

        .audio-player {
            margin-top: 1rem;
            margin-bottom: 1rem;
        }

        .audio-player audio {
            width: 100%;
            max-width: 400px;
            border-radius: 8px;
            outline: none;
        }

        .audio-player audio::-webkit-media-controls-panel {
            background: rgba(255, 215, 0, 0.1);
        }

        .final-task {
            background: linear-gradient(135deg, rgba(196, 30, 58, 0.2) 0%, rgba(139, 0, 0, 0.2) 100%);
            border: 3px solid var(--crimson);
            position: relative;
        }

        .final-task::after {
            content: '🎁';
            position: absolute;
            top: 1rem;
            right: 1rem;
            font-size: 3rem;
            opacity: 0.3;
        }

        .unlocked-badge {
            display: inline-block;
            background: var(--gold);
            color: var(--pine);
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-weight: 700;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 1rem;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .team-info {
            background: rgba(255, 215, 0, 0.1);
            border: 2px solid var(--gold);
            border-radius: 12px;
            padding: 1rem;
            margin-bottom: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .team-name {
            font-family: 'Mountains of Christmas', cursive;
            font-size: 1.5rem;
            color: var(--gold);
        }

        .progress-bar {
            width: 100%;
            height: 12px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 6px;
            overflow: hidden;
            margin-top: 0.5rem;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--forest) 0%, var(--gold) 100%);
            border-radius: 6px;
            transition: width 0.5s ease;
            box-shadow: 0 0 10px rgba(255, 215, 0, 0.5);
        }

        .hidden {
            display: none;
        }

        .success-message {
            background: var(--forest);
            color: var(--gold);
            padding: 1rem;
            border-radius: 12px;
            margin-top: 1rem;
            text-align: center;
            font-weight: 600;
            animation: slideIn 0.5s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        /* Congratulations Screen Styles */
        #congratulationsScreen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            z-index: 1000;
            overflow-y: auto;
        }

        #congratulationsScreen.hidden {
            display: none !important;
        }

        .congrats-container {
            max-width: 800px;
            width: 100%;
            animation: fadeIn 1s ease-out;
            padding: 2rem 1rem;
            box-sizing: border-box;
        }

        .trophy {
            font-size: 8rem;
            animation: bounce 2s ease-in-out infinite;
            display: inline-block;
            margin-bottom: 1rem;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .congrats-title {
            font-family: 'Mountains of Christmas', cursive;
            font-size: clamp(2.5rem, 8vw, 5rem);
            color: var(--gold);
            text-shadow: 
                3px 3px 0 var(--crimson),
                6px 6px 0 var(--berry),
                -2px -2px 15px rgba(255, 215, 0, 0.5);
            margin-bottom: 1rem;
            letter-spacing: 2px;
            word-wrap: break-word;
            animation: glow 2s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from {
                text-shadow: 
                    3px 3px 0 var(--crimson),
                    6px 6px 0 var(--berry),
                    -2px -2px 15px rgba(255, 215, 0, 0.5);
            }
            to {
                text-shadow: 
                    3px 3px 0 var(--crimson),
                    6px 6px 0 var(--berry),
                    -2px -2px 30px rgba(255, 215, 0, 0.8),
                    0 0 40px rgba(255, 215, 0, 0.4);
            }
        }

        .congrats-subtitle {
            font-size: clamp(1.2rem, 4vw, 2rem);
            color: var(--snow);
            margin-bottom: 2rem;
            font-weight: 600;
            word-wrap: break-word;
        }

        .congrats-message {
            font-size: clamp(1rem, 3.5vw, 1.2rem);
            color: var(--silver);
            line-height: 1.8;
            margin-bottom: 1.5rem;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-top: 2rem;
        }

        .stat-item {
            background: rgba(255, 215, 0, 0.1);
            border: 2px solid var(--gold);
            border-radius: 12px;
            padding: 1.5rem;
        }

        .stat-value {
            font-family: 'Mountains of Christmas', cursive;
            font-size: clamp(1.5rem, 5vw, 2rem);
            color: var(--gold);
            font-weight: 700;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: clamp(0.85rem, 3vw, 1rem);
            color: var(--silver);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .fireworks {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .firework {
            position: absolute;
            width: 4px;
            height: 4px;
            border-radius: 50%;
            animation: explode 1.5s ease-out forwards;
        }

        @keyframes explode {
            0% {
                transform: translate(0, 0) scale(1);
                opacity: 1;
            }
            100% {
                transform: translate(var(--tx), var(--ty)) scale(0);
                opacity: 0;
            }
        }

        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: var(--gold);
            position: absolute;
            animation: confetti-fall 3s linear forwards;
        }

        @keyframes confetti-fall {
            to {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }

        .button-group {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .button-secondary {
            background: rgba(255, 255, 255, 0.1);
            border: 2px solid var(--silver);
        }

        .button-secondary:hover {
            background: rgba(255, 255, 255, 0.2);
            border-color: var(--gold);
        }

        .ornament {
            display: inline-block;
            animation: swing 3s ease-in-out infinite;
        }

        @keyframes swing {
            0%, 100% { transform: rotate(-5deg); }
            50% { transform: rotate(5deg); }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
                text-shadow: 
                    2px 2px 0 var(--crimson),
                    4px 4px 0 var(--berry),
                    -1px -1px 10px rgba(255, 215, 0, 0.3);
            }

            .subtitle {
                font-size: 0.9rem;
                letter-spacing: 2px;
            }

            .container {
                padding: 1rem 0.75rem;
            }

            .card {
                padding: 1.5rem 1rem;
                margin-bottom: 1.5rem;
            }

            h2 {
                font-size: 1.5rem;
                margin-bottom: 1rem;
            }

            .task-question {
                font-size: 1rem;
                word-wrap: break-word;
                overflow-wrap: break-word;
            }

            .task-number {
                font-size: 1.2rem;
            }

            .task-status {
                font-size: 0.7rem;
                padding: 0.2rem 0.75rem;
            }

            .team-info {
                flex-direction: column;
                align-items: stretch;
                gap: 1rem;
            }

            .team-name {
                font-size: 1.2rem;
                text-align: center;
                word-wrap: break-word;
                overflow-wrap: break-word;
            }

            button {
                padding: 1rem 2rem;
                font-size: 0.9rem;
                width: 100%;
            }

            .button-group {
                flex-direction: column;
            }

            input[type="text"],
            textarea {
                padding: 0.875rem;
                font-size: 16px; /* Prevents zoom on iOS */
            }

            textarea {
                min-height: 80px;
            }

            .task-item {
                padding: 1.25rem 1rem;
            }

            .unlocked-badge {
                font-size: 0.8rem;
                padding: 0.4rem 0.8rem;
            }

            .final-task::after {
                font-size: 2rem;
                top: 0.5rem;
                right: 0.5rem;
            }

            header {
                margin-bottom: 2rem;
            }

            .trophy {
                font-size: 5rem;
            }

            .stats {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 480px) {
            h1 {
                font-size: 2rem;
                word-wrap: break-word;
            }

            .subtitle {
                font-size: 0.75rem;
                letter-spacing: 1px;
            }

            h2 {
                font-size: 1.3rem;
                word-wrap: break-word;
            }

            .container {
                padding: 0.75rem 0.5rem;
            }

            .card {
                padding: 1.25rem 0.875rem;
                border-radius: 16px;
            }

            .task-item {
                padding: 1rem 0.875rem;
                border-radius: 10px;
            }

            button {
                padding: 0.875rem 1.5rem;
                font-size: 0.85rem;
                letter-spacing: 1px;
            }

            label {
                font-size: 0.75rem;
            }

            .task-question {
                word-wrap: break-word;
                overflow-wrap: break-word;
                hyphens: auto;
            }

            .trophy {
                font-size: 4rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1><span class="ornament">🎅</span> Nisseopprøret <span class="ornament">🎅</span></h1>
        </header>

        <!-- Registration Screen -->
        <div id="registrationScreen" class="hidden">
            <div class="card">
                <h2>🎅 Velkommen til Nisseopprøret</h2>
                <p style="color: var(--snow); margin-bottom: 1.5rem; font-size: clamp(0.9rem, 3.5vw, 1rem); line-height: 1.8; text-align: left;">
                    Det har skjedd. Julenissen har endelig knekt under presset av årevis med urimelige forventninger, Amazon Prime-konkurranse, og konstante klager om at "Xbox-en var feil farge". Han har stengt seg inne på kontoret sitt med en flaske akevitt og nekter å komme ut.
                    <br><br>
                    Som den eneste nissen med nøkkelkort til alle avdelingene (takk, HR), er DU den uheldige sjelen som må fikse dette kaoset. Problemet? Julenissen har kodelåst alt i et fyllearrangert raseri, og du har 60 minutter på deg før Instagram-generasjonen våkner og oppdager at julen er avlyst.
                </p>
                <p style="color: var(--silver); margin-bottom: 1.5rem; font-size: clamp(0.85rem, 3.5vw, 0.95rem); line-height: 1.6;">
                    ⚠️ <strong>Viktig:</strong> Lagets fremgang lagres automatisk. 
                    Å oppdatere eller lukke siden vil ikke tilbakestille svarene eller straffetidene deres! Feil svar gir straffetid.
                </p>
                <div class="input-group">
                    <label for="teamName">Nisselagnavn</label>
                    <input type="text" id="teamName" placeholder="F.eks. Snøballkrigerne, Glitter-gjengen..." />
                </div>
                <button onclick="registerTeam()">Start Kaoset</button>
            </div>
        </div>

        <!-- Quiz Screen -->
        <div id="quizScreen" class="hidden">
            <div class="team-info">
                <div>
                    <div class="team-name" id="displayTeamName"></div>
                    <div class="progress-bar">
                        <div class="progress-fill" id="progressFill" style="width: 0%"></div>
                    </div>
                </div>
                <div style="display: flex; gap: 0.5rem;">
                    <button class="button-secondary" onclick="devGoToStart()" title="Developer: Go to Start">⌂</button>
                    <button class="button-secondary" onclick="devPrevTask()" title="Developer: Previous Task">◄</button>
                    <button class="button-secondary" onclick="devNextTask()" title="Developer: Next Task">►</button>
                    <button class="button-secondary" onclick="resetApp()">Tilbakestill</button>
                </div>
            </div>

            <div class="card">
                <h2>🎵 Kapittel 1: Verkstedet</h2>
                <p style="color: var(--snow); margin-bottom: 1.5rem; font-size: clamp(0.9rem, 3.5vw, 1rem); line-height: 1.8;">
                    Du ankommer verkstedet og finner 8 nisser som har funnet julegløggen litt for tidlig i år. De har startet karaoke og nekter å jobbe før du beviser at DU kan noe om musikk. "Du kan ikke være sjef for oss hvis du ikke engang kan gjenkjenne hva vi synger!" roper den mest drita nissen. Du oppdager raskt at tekst og melodi ikke er noe du har hørt før - det må være noen merkelige coverversjoner de synger!
                </p>
                <div class="task-list" id="taskList"></div>
            </div>
        </div>

        <!-- Congratulations Screen -->
        <div id="congratulationsScreen" class="hidden">
            <div class="fireworks" id="fireworks"></div>
            
            <div class="congrats-container">
                <div class="trophy">🏆</div>
                <h1 class="congrats-title">Gratulerer!</h1>
                <p class="congrats-subtitle">Dere Rømte!</p>

                <div class="card">
                    <div class="team-name" id="congratsTeamName">Mesterlaget</div>
                    <p class="congrats-message">
                        🎅 Dere har klart å stoppe nisseopprøret! 🎅
                        <br><br>
                        Laget deres viste utrolig kunnskap, lagarbeid og julestemning. 
                        Godt jobbet med å mestre alle utfordringene!
                    </p>

                    <div class="stats">
                        <div class="stat-item">
                            <div class="stat-value">19/19</div>
                            <div class="stat-label">Utfordringer Fullført</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-value" id="completionTime">--:--</div>
                            <div class="stat-label">Tid Brukt</div>
                        </div>
                    </div>

                    <button onclick="startNewQuest()">Start Ny Rømning</button>
                </div>
            </div>
        </div>
    </div>

    <script>
        const TASKS = [
            {
                id: 1,
                question: "Hvilken sang covrer den fulle nissen her?",
                answer: "africa",
                isFinal: false,
                audioFile: "Afrika.mp3",
                chapter: 1
            },
            {
                id: 2,
                question: "Hvilket band står bak den originale versjonen av denne sangen?",
                answer: "journey",
                isFinal: false,
                audioFile: "Journey.mp3",
                chapter: 1
            },
            {
                id: 3,
                question: "Hva er navnet til artisten bak den originale versjonen av denne låta?",
                answer: "madonna",
                isFinal: false,
                audioFile: "Madonna.mp3",
                chapter: 1
            },
            {
                id: 4,
                question: "Hvilket band står bak den originale versjonen av denne låta?",
                answer: "a-ha",
                isFinal: false,
                audioFile: "A-ha.mp3",
                chapter: 1
            },
            {
                id: 5,
                question: "Hva er etternavnet til artisten bak den originale versjonen av denne låta?",
                answer: "houston",
                isFinal: false,
                audioFile: "Houston.mp3",
                chapter: 1
            },
            {
                id: 6,
                question: "Hva er fornavnet til artisten bak den originale versjonen av denne låta?",
                answer: "rick",
                isFinal: false,
                audioFile: "Rick.mp3",
                chapter: 1
            },
            {
                id: 7,
                question: "Hva er fornavnet til artisten bak den originale versjonen av denne låta?",
                answer: "tina",
                isFinal: false,
                audioFile: "Tina.mp3",
                chapter: 1
            },
            {
                id: 8,
                question: "Hva heter bandet bak den originale versjonen av denne låta?",
                answer: "wham",
                isFinal: false,
                audioFile: "Wham.mp3",
                chapter: 1
            },
            {
                id: 9,
                question: `<strong>REGLER (les nøye, din idiot):</strong><br>
                <br>
                
                <strong>4 2 8</strong><br>
                1 tall er riktig, men feil plass, 0 er på riktig plass, 2 er feil<br><br>
                
                <strong>0 4 2</strong><br>
                1 tall er riktig, men feil plass, 0 er på riktig plass, 2 er feil<br><br>
                
                <strong>3 0 6</strong><br>
                1 tall er riktig, men feil plass, 0 er på riktig plass, 2 er feil<br><br>
                
                <strong>0 2 4</strong><br>
                1 tall er riktig, men feil plass, 0 er på riktig plass, 2 er feil<br><br>
                
                <strong>3 1 6</strong><br>
                1 tall er riktig, men feil plass, 1 er på riktig plass, 1 er feil<br><br>
                
                                
                <strong>Hva er den 3-sifrede koden? (Skriv uten mellomrom, f.eks: 12345)</strong>`,
                answer: "213",
                isFinal: false,
                chapter: 2
            },
            {
                id: 10,
                question: "Hvilken sport forbindes med hva 2. juledag kalles i engelsktalende land?",
                answer: "boksing",
                isFinal: false,
                chapter: 3
            },
            {
                id: 11,
                question: "Hvilket land flyktet Josef og Maria til for å redde Jesus?",
                answer: "egypt",
                isFinal: false,
                chapter: 3
            },
            {
                id: 12,
                question: "Hvilken høy-relevant kjent figur har en birolle i Hjemme Alene 2? (etternavn)",
                answer: "trump",
                isFinal: false,
                chapter: 3
            },
            {
                id: 13,
                question: "Hvilken TV-kanal sender Rampenissen?",
                answer: "tv2",
                isFinal: false,
                chapter: 3
            },
            {
                id: 14,
                question: "Hvem synger sangen 'Home for Christmas'? (fornavn)",
                answer: "bing",
                isFinal: false,
                chapter: 3
            },
            {
                id: 15,
                question: "Hva heter julekalenderen TV2 sendte for første gang i 1994, der nissene vi følger blant annet synger om rytmisk bevegelse i et spesifikt fottøy?",
                answer: "the julekalender",
                isFinal: false,
                chapter: 3
            },
            {
                id: 16,
                question: `Denne pakken skal til en by (hvis navn enkelt kan todeles), og her finner du et knutepunkt som har vært størst i verden.<br><br>
                Første del av navnet kan gi assosiasjon til en tragisk hendelse, kan ha norsk navn, og fremkalle en reaksjon av vemmelse. Tanken kan også gå til binding, ørken, nøtteknekkeren og hår, filmkokk, fanger fra eventyr, jord og når tøff konkurranse rår.<br><br>
                Andre del gir også assosiasjoner; som asiatiske hager, å være stille, et forlag, nyttig byggverk eller bading, samt at dèt er mulig å spille.<br><br>
                <strong>Hvor skal pakken?</strong>`,
                answer: "rotterdam",
                isFinal: false,
                chapter: 4
            },
            {
                id: 17,
                question: `Denne pakken skal til et sted som kan assosieres med odontologi, men splittes navnet i fem, er det tredje sentralt i anatomi.<br><br>
                Det tredje kan stå etter fiske, stille, stol og hale, mens det første ordet er filmen om en grønnkledd julevenn.<br><br>
                Det andre ordet utgjør en artikkel eller et enkelt tallord, fjerde er svovel og det femte å finne ved enhver fjord.<br><br>
                Samlet knyttes de første tre til forbud, og feiring av fjorten, og på engelsk kjent fra Paul-sang (da ved siden av en sort, en).<br><br>
                <strong>Hvor skal pakken?</strong>`,
                answer: "elfenbenskysten",
                isFinal: false,
                chapter: 4
            },
            {
                id: 18,
                question: `Denne pakken skal til hjembyen til et ekte idol, et mindre sted ikke så langt fra der en pirat har bol.<br><br>
                Stedsnavnet kan deles i vakker og den som på svie byr, eller i en i kretsen og en (nynorsk) gjeng av firbente stae dyr.<br><br>
                For sistnevnte deling, kan første ord knyttes til en bistandssang, Viggo, en TV-serie, hund, og gitaren til Tang.<br><br>
                Den tilhørende gjengen kan bestå av det triste til han gule og det glade til han grønne, men ikke kongen (han uten mule).<br><br>
                <strong>Hvor skal pakken?</strong>`,
                answer: "vennesla",
                isFinal: false,
                chapter: 4
            },
            {
                id: 19,
                question: `<strong>Jeg er lei av å levere pakker. Skli ned piper. Gi glede til folk som ikke tror på meg. Nå finnes det bare en ting som kan få meg til å åpne døren. Alt annet er meningsløst. Noen refleksjoner fra en sliten, gammel nisse:.</strong><br><br>
                
                <em>Prisen for å glede alle andre hele tiden? <br><br>
                    Isolasjon. Total. Komplett. Evig. <br><br>
                    Nattene er verst, vet du. Når alle sover. <br><br>
                    Nordlyset danser, men jeg ser det knapt lenger. <br><br>
                    Er dette virkelig alt? År etter år? <br><br>
                    Kanskje burde jeg bare... gi opp. <br><br>
                    Jeg husker da det betydde noe. Da JEG betydde noe. <br><br>
                    Ønsket var annerledes den gang. Enklere. <br><br>
                    Tiden tar alt, til slutt. Selv magien. <br><br>
                    Takk for ingenting, moderne verden.</em><br><br>
                
                
                answer: "pinnekjøtt",
                isFinal: true,
                chapter: 5
            }
        ];

        let currentTeam = null;
        let completedTasks = [];
        let penaltyTimers = {}; // Track penalty end times for each task

        async function loadTeamData() {
            try {
                const currentTeamData = localStorage.getItem('currentTeam');
                if (currentTeamData) {
                    currentTeam = JSON.parse(currentTeamData);
                    const tasksData = localStorage.getItem(`tasks_${currentTeam.name}`);
                    if (tasksData) {
                        completedTasks = JSON.parse(tasksData);
                    }
                    const penaltyData = localStorage.getItem(`penalties_${currentTeam.name}`);
                    if (penaltyData) {
                        penaltyTimers = JSON.parse(penaltyData);
                    }
                    return true;
                }
            } catch (error) {
                console.log('No existing team data');
            }
            return false;
        }

        async function saveTeamData() {
            try {
                localStorage.setItem('currentTeam', JSON.stringify(currentTeam));
                localStorage.setItem(`tasks_${currentTeam.name}`, JSON.stringify(completedTasks));
                localStorage.setItem(`penalties_${currentTeam.name}`, JSON.stringify(penaltyTimers));
            } catch (error) {
                console.error('Error saving data:', error);
            }
        }

        async function registerTeam() {
            const teamName = document.getElementById('teamName').value.trim();
            
            if (!teamName) {
                alert('Vennligst skriv inn et nissenavn!');
                return;
            }

            // Check if this team already exists
            try {
                const existingTeamData = localStorage.getItem('currentTeam');
                if (existingTeamData) {
                    const existingTeam = JSON.parse(existingTeamData);
                    if (existingTeam.name === teamName) {
                        // Team exists, load their data
                        currentTeam = existingTeam;
                        const tasksData = localStorage.getItem(`tasks_${currentTeam.name}`);
                        if (tasksData) {
                            completedTasks = JSON.parse(tasksData);
                        }
                        const penaltyData = localStorage.getItem(`penalties_${currentTeam.name}`);
                        if (penaltyData) {
                            penaltyTimers = JSON.parse(penaltyData);
                        }
                        showQuizScreen();
                        return;
                    }
                }
            } catch (error) {
                console.log('No existing team found');
            }

            // New team registration
            currentTeam = { name: teamName };
            completedTasks = [];
            penaltyTimers = {};
            
            await saveTeamData();
            showQuizScreen();
        }

        function showQuizScreen() {
            document.getElementById('registrationScreen').classList.add('hidden');
            document.getElementById('quizScreen').classList.remove('hidden');
            document.getElementById('displayTeamName').textContent = currentTeam.name;
            renderTasks();
            updateProgress();
        }

        function isTaskUnderPenalty(taskId) {
            if (!penaltyTimers[taskId]) return false;
            const now = Date.now();
            return now < penaltyTimers[taskId];
        }

        function getRemainingPenaltyTime(taskId) {
            if (!penaltyTimers[taskId]) return 0;
            const remaining = Math.max(0, penaltyTimers[taskId] - Date.now());
            return Math.ceil(remaining / 1000); // Convert to seconds
        }

        function formatTime(seconds) {
            const mins = Math.floor(seconds / 60);
            const secs = seconds % 60;
            return `${mins}:${secs.toString().padStart(2, '0')}`;
        }

        function normalizeAnswer(answer) {
            return answer.toLowerCase().trim().replace(/[^a-z0-9\s]/g, '');
        }

        function renderTasks() {
            const taskList = document.getElementById('taskList');
            taskList.innerHTML = '';

            const regularTasks = TASKS.filter(t => !t.isFinal);
            const finalTask = TASKS.find(t => t.isFinal);
            const allRegularCompleted = regularTasks.every(t => completedTasks.includes(t.id));

            // Find the first incomplete task
            let firstIncompleteIndex = regularTasks.findIndex(t => !completedTasks.includes(t.id));
            if (firstIncompleteIndex === -1) firstIncompleteIndex = regularTasks.length; // All regular tasks complete

            let currentChapter = null;

            TASKS.forEach((task, index) => {
                const isCompleted = completedTasks.includes(task.id);
                const isUnderPenalty = isTaskUnderPenalty(task.id);
                
                // Hide final task until all regular tasks are completed
                if (task.isFinal && !allRegularCompleted) {
                    return; // Skip rendering the final task
                }
                
                // For regular tasks: only show completed tasks and the next incomplete task
                const taskIndex = regularTasks.findIndex(t => t.id === task.id);
                const shouldShowRegularTask = task.isFinal || isCompleted || taskIndex === firstIncompleteIndex;
                
                if (!shouldShowRegularTask) {
                    return; // Skip this task - don't render it yet
                }

                // Add chapter header if this is a new chapter
                if (task.chapter && task.chapter !== currentChapter) {
                    currentChapter = task.chapter;
                    const chapterHeader = document.createElement('div');
                    chapterHeader.style.marginTop = currentChapter === 1 ? '0' : '2rem';
                    
                    if (currentChapter === 2) {
                        chapterHeader.innerHTML = `
                            <h2 style="font-family: 'Mountains of Christmas', cursive; font-size: 2rem; color: var(--gold); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem;">
                                🔒 Kapittel 2: Nisselåsen fra Helvete
                            </h2>
                            <p style="color: var(--snow); margin-bottom: 1.5rem; font-size: clamp(0.9rem, 3.5vw, 1rem); line-height: 1.8;">
                                Dere står foran den massive stålporten til hovedverkstedet. På veggen henger det en lapp skrevet med vinglete håndskrift (definitivt akevitt-påvirket). Nederst står det: "Hvis dere ikke kan løse DETTE, fortjener dere ikke å lage leker. Og ja, jeg gjorde den ekstra vanskelig. Fordi, fuck dere. - Sjefen"
                            </p>
                        `;
                        taskList.appendChild(chapterHeader);
                    } else if (currentChapter === 3) {
                        chapterHeader.innerHTML = `
                            <h2 style="font-family: 'Mountains of Christmas', cursive; font-size: 2rem; color: var(--gold); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem;">
                                🥜 Kapittel 3: Nøtteknekkeren
                            </h2>
                            <p style="color: var(--snow); margin-bottom: 1.5rem; font-size: clamp(0.9rem, 3.5vw, 1rem); line-height: 1.8;">
                                Dere ankommer et helt landskap av pepperkaker og marsipan. Men noe er galt. Alt er... grått. Fargeløst. Deprimerende. Som å se Paradise Hotel uten filter.
                                <br><br>
                                En desperat pepperkakeordfører kommer løpende: "ENDELIG! Noen! Julenissen ringte i stad - full som en alke - og sa vi måtte 'bevise vår verdi' før han åpnet porten tilbake til verkstedet. Han etterlot seg nøtter. Ikke spiselige nøtter. VOKSEN-nøtter. For folk som faktisk VET ting."
                            </p>
                        `;
                        taskList.appendChild(chapterHeader);
                    } else if (currentChapter === 4) {
                        chapterHeader.innerHTML = `
                            <h2 style="font-family: 'Mountains of Christmas', cursive; font-size: 2rem; color: var(--gold); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem;">
                                📦 Kapittel 4: Pakke-kaoset
                            </h2>
                            <p style="color: var(--snow); margin-bottom: 1.5rem; font-size: clamp(0.9rem, 3.5vw, 1rem); line-height: 1.8;">
                                En massiv hall fylt med pakker. Tusenvis av dem. Alle adressert, men ingen sortert. En stresset postnisse står midt i kaoset med en clipboard som ser ut til å ha vært gjennom en krig.
                                <br><br>
                                "Å, ENDELIG!" roper han. "Julenissen låste sorteringsmaskinen før han stengte seg inne! Nå står jeg her med tre KRITISKE pakker som må ut I KVELD, men adressene er... vel, han skrev dem mens han var full. De er kodet som jævlige gåter!"
                                <br><br>
                                Han holder frem tre sedler med vinglete håndskrift. "Løs disse, så får dere tilgang til neste område. Fail, og julen er fucked for tre familier. No pressure."
                            </p>
                        `;
                        taskList.appendChild(chapterHeader);
                    } else if (currentChapter === 5) {
                        chapterHeader.innerHTML = `
                            <h2 style="font-family: 'Mountains of Christmas', cursive; font-size: 2rem; color: var(--gold); margin-bottom: 1rem; display: flex; align-items: center; gap: 0.5rem;">
                                ❄️ Kapittel 5: Julenissens Kontor
                            </h2>
                            <p style="color: var(--snow); margin-bottom: 1.5rem; font-size: clamp(0.9rem, 3.5vw, 1rem); line-height: 1.8;">
                                Et spektakulært palass av lys og is. Men inne, bak en massiv dør, hører dere Julenissen synge "Last Christmas" på repeat, helt falskt, mens han snufser høylydt.
                                <br><br>
                                En lapp på døren, skrevet med vinglete håndskrift og noen akevittflekker:
                                <br><br>
                                <em>"Så. Dere kom altså. Gratulerer.<br>
                                Jeg antar dere vil ha meg ut? Vil at jeg skal 'fikse alt'? Selvfølgelig. Det er jo det jeg gjør. Det jeg ALLTID gjør.<br>
                                Men før jeg åpner denne døren... før jeg går tilbake til det sirkuset... vil jeg at dere forstår noe.<br>
                                Under her har jeg skrevet ned tanker. Refleksjoner fra en mann som har sett for mange juler. Les mellom linjene. Finn essensen. Det eneste som fortsatt gir mening for meg.<br>
                                Hvis dere finner det, fortjener dere å komme inn.<br>
                                - En som er for gammel for dette"</em>
                            </p>
                        `;
                        taskList.appendChild(chapterHeader);
                    }
                }

                const isLocked = (task.isFinal && !allRegularCompleted) || isUnderPenalty;
                const isActive = !isCompleted && !isLocked;

                const taskDiv = document.createElement('div');
                taskDiv.className = `task-item ${isCompleted ? 'completed' : ''} ${isActive ? 'active' : ''} ${isLocked ? 'locked' : ''} ${task.isFinal ? 'final-task' : ''}`;
                taskDiv.id = `task_${task.id}`;
                
                let statusClass = isCompleted ? 'completed' : isActive ? 'active' : 'locked';
                let statusText = isCompleted ? '✓ Fullført' : isActive ? 'Svar Nå' : '🔒 Låst';

                if (isUnderPenalty) {
                    statusText = '⏱️ Straff';
                }

                if (task.isFinal && allRegularCompleted && !isCompleted) {
                    taskDiv.innerHTML = `
                        <div class="unlocked-badge">✨ LÅST OPP! ✨</div>
                    `;
                }

                // Determine task label based on chapter
                let taskLabel = '';
                if (task.chapter === 1) {
                    taskLabel = `Nissesang ${task.id}`;
                } else if (task.chapter === 2) {
                    taskLabel = 'Kodelåsen';
                } else if (task.chapter === 3) {
                    const nuttNumber = task.id - 9; // Start counting from 1 for chapter 3
                    taskLabel = `Nøtt ${nuttNumber}`;
                } else if (task.chapter === 4) {
                    const pakkeNumber = task.id - 15; // Start counting from 1 for chapter 4
                    taskLabel = `Pakke ${pakkeNumber}`;
                } else if (task.chapter === 5) {
                    taskLabel = 'Den Endelige Refleksjonen';
                }

                taskDiv.innerHTML += `
                    <div class="task-header">
                        <span class="task-number">${taskLabel}</span>
                        <span class="task-status ${statusClass}">${statusText}</span>
                    </div>
                    <div class="task-question">${task.question}</div>
                `;

                // Add audio player if task has audio file
                if (task.audioFile && isActive) {
                    const audioDiv = document.createElement('div');
                    audioDiv.className = 'audio-player';
                    audioDiv.innerHTML = `
                        <audio id="audio_${task.id}" controls autoplay loop>
                            <source src="${task.audioFile}" type="audio/mpeg">
                            Your browser does not support the audio element.
                        </audio>
                    `;
                    taskDiv.appendChild(audioDiv);
                }

                if (isUnderPenalty) {
                    const penaltyDiv = document.createElement('div');
                    penaltyDiv.className = 'penalty-timer';
                    penaltyDiv.id = `penalty_${task.id}`;
                    const remainingSeconds = getRemainingPenaltyTime(task.id);
                    penaltyDiv.innerHTML = `
                        <div style="background: rgba(196, 30, 58, 0.2); border: 2px solid var(--crimson); border-radius: 12px; padding: 1rem; margin-top: 1rem; text-align: center;">
                            <div style="color: var(--crimson); font-weight: 700; font-size: clamp(1rem, 4vw, 1.2rem); margin-bottom: 0.5rem;">❌ Feil Svar!</div>
                            <div style="color: var(--snow); font-size: clamp(0.85rem, 3.5vw, 0.9rem);">Tid igjen: <span id="timer_${task.id}" style="font-weight: 700; color: var(--gold); font-size: clamp(1rem, 4vw, 1.1rem);">${formatTime(remainingSeconds)}</span></div>
                        </div>
                    `;
                    taskDiv.appendChild(penaltyDiv);
                }

                if (isActive) {
                    const answerInput = document.createElement('textarea');
                    answerInput.id = `answer_${task.id}`;
                    answerInput.placeholder = 'Skriv svaret ditt her...';
                    
                    const submitBtn = document.createElement('button');
                    submitBtn.textContent = task.isFinal ? 'Fullfør Rømningen! 🎉' : 'Send inn svar';
                    submitBtn.onclick = () => submitAnswer(task.id);
                    
                    taskDiv.appendChild(answerInput);
                    taskDiv.appendChild(submitBtn);
                }

                if (isCompleted) {
                    const successMsg = document.createElement('div');
                    successMsg.className = 'success-message';
                    successMsg.textContent = task.isFinal ? '🎉 Rømning Fullført! Gratulerer! 🎉' : '✓ Svar sendt inn!';
                    taskDiv.appendChild(successMsg);
                }

                taskList.appendChild(taskDiv);
            });

            // Start countdown timers for any tasks under penalty
            TASKS.forEach(task => {
                if (isTaskUnderPenalty(task.id)) {
                    startPenaltyCountdown(task.id);
                }
            });
        }

        function startPenaltyCountdown(taskId) {
            const timerElement = document.getElementById(`timer_${taskId}`);
            if (!timerElement) return;

            const interval = setInterval(() => {
                const remaining = getRemainingPenaltyTime(taskId);
                
                if (remaining <= 0) {
                    clearInterval(interval);
                    renderTasks(); // Re-render to show task is now available
                } else {
                    timerElement.textContent = formatTime(remaining);
                }
            }, 1000);
        }

        async function submitAnswer(taskId) {
            const answer = document.getElementById(`answer_${taskId}`).value.trim();
            
            if (!answer) {
                alert('Vennligst skriv inn et svar!');
                return;
            }

            const task = TASKS.find(t => t.id === taskId);
            
            // Check if answer is correct
            const userAnswer = normalizeAnswer(answer);
            const correctAnswer = normalizeAnswer(task.answer);

            if (userAnswer === correctAnswer || userAnswer.includes(correctAnswer) || correctAnswer.includes(userAnswer)) {
                // Correct answer!
                
                // Stop audio if playing
                const audioElement = document.getElementById(`audio_${taskId}`);
                if (audioElement) {
                    audioElement.pause();
                    audioElement.currentTime = 0;
                }
                
                completedTasks.push(taskId);
                
                // Save the answer with timestamp
                try {
                    localStorage.setItem(`answer_${currentTeam.name}_${taskId}`, JSON.stringify({
                        answer: answer,
                        timestamp: Date.now()
                    }));
                } catch (error) {
                    console.error('Error saving answer:', error);
                }

                await saveTeamData();
                
                // If this is the final task, show congratulations screen
                if (task.isFinal) {
                    // Save completion timestamp
                    try {
                        localStorage.setItem(`completed_${currentTeam.name}`, JSON.stringify({
                            teamName: currentTeam.name,
                            completedAt: Date.now()
                        }));
                    } catch (error) {
                        console.error('Error saving completion:', error);
                    }
                    
                    // Show congratulations screen
                    showCongratulations();
                    return;
                }
                
                renderTasks();
                updateProgress();
            } else {
                // Wrong answer - apply 10 second penalty
                const penaltyEndTime = Date.now() + (10 * 1000); // 10 seconds from now
                penaltyTimers[taskId] = penaltyEndTime;
                
                // Also save the wrong attempt with timestamp
                try {
                    const attemptsKey = `attempts_${currentTeam.name}_${taskId}`;
                    let attempts = [];
                    const attemptsData = localStorage.getItem(attemptsKey);
                    if (attemptsData) {
                        attempts = JSON.parse(attemptsData);
                    }
                    
                    attempts.push({
                        answer: answer,
                        timestamp: Date.now(),
                        penaltyUntil: penaltyEndTime
                    });
                    
                    localStorage.setItem(attemptsKey, JSON.stringify(attempts));
                } catch (error) {
                    console.error('Error saving attempt:', error);
                }
                
                await saveTeamData();
                renderTasks();
            }
        }

        function updateProgress() {
            const regularTasks = TASKS.filter(t => !t.isFinal);
            const completedRegular = completedTasks.filter(id => {
                const task = TASKS.find(t => t.id === id);
                return task && !task.isFinal;
            }).length;
            
            const percentage = (completedRegular / regularTasks.length) * 100;
            document.getElementById('progressFill').style.width = percentage + '%';
        }

        async function resetApp() {
            if (confirm('Er du sikker på at du vil tilbakestille? All fremgang vil gå tapt!')) {
                try {
                    if (currentTeam) {
                        localStorage.removeItem(`tasks_${currentTeam.name}`);
                        localStorage.removeItem(`penalties_${currentTeam.name}`);
                        localStorage.removeItem(`completed_${currentTeam.name}`);
                        // Delete all answers
                        for (const task of TASKS) {
                            localStorage.removeItem(`answer_${currentTeam.name}_${task.id}`);
                            localStorage.removeItem(`attempts_${currentTeam.name}_${task.id}`);
                        }
                    }
                    localStorage.removeItem('currentTeam');
                } catch (error) {
                    console.error('Error resetting:', error);
                }
                
                currentTeam = null;
                completedTasks = [];
                penaltyTimers = {};
                document.getElementById('teamName').value = '';
                document.getElementById('registrationScreen').classList.remove('hidden');
                document.getElementById('quizScreen').classList.add('hidden');
                document.getElementById('congratulationsScreen').classList.add('hidden');
            }
        }

        // Congratulations Screen Functions
        function showCongratulations() {
            document.getElementById('registrationScreen').classList.add('hidden');
            document.getElementById('quizScreen').classList.add('hidden');
            document.getElementById('congratulationsScreen').classList.remove('hidden');
            
            // Load team data
            document.getElementById('congratsTeamName').textContent = currentTeam.name;
            
            // Calculate completion time
            try {
                const completionData = localStorage.getItem(`completed_${currentTeam.name}`);
                if (completionData) {
                    const completion = JSON.parse(completionData);
                    
                    // Get the first task timestamp
                    let startTime = completion.completedAt;
                    try {
                        const answer1 = localStorage.getItem(`answer_${currentTeam.name}_1`);
                        if (answer1) {
                            const answerData = JSON.parse(answer1);
                            startTime = answerData.timestamp;
                        }
                    } catch (e) {}

                    const duration = completion.completedAt - startTime;
                    const minutes = Math.floor(duration / 60000);
                    const seconds = Math.floor((duration % 60000) / 1000);
                    document.getElementById('completionTime').textContent = 
                        `${minutes}:${seconds.toString().padStart(2, '0')}`;
                }
            } catch (error) {
                console.error('Error calculating time:', error);
            }
            
            // Start celebrations
            createConfetti();
            startFireworks();
        }

        function createFirework(x, y) {
            const colors = ['#FFD700', '#C41E3A', '#FFFAFA', '#0F5132', '#8B0000'];
            const particleCount = 30;

            for (let i = 0; i < particleCount; i++) {
                const firework = document.createElement('div');
                firework.className = 'firework';
                firework.style.left = x + 'px';
                firework.style.top = y + 'px';
                firework.style.background = colors[Math.floor(Math.random() * colors.length)];
                
                const angle = (Math.PI * 2 * i) / particleCount;
                const velocity = 50 + Math.random() * 100;
                const tx = Math.cos(angle) * velocity;
                const ty = Math.sin(angle) * velocity;
                
                firework.style.setProperty('--tx', tx + 'px');
                firework.style.setProperty('--ty', ty + 'px');
                
                document.getElementById('fireworks').appendChild(firework);
                
                setTimeout(() => firework.remove(), 1500);
            }
        }

        let fireworksInterval;
        function startFireworks() {
            // Clear any existing interval
            if (fireworksInterval) {
                clearInterval(fireworksInterval);
            }
            
            // Launch fireworks periodically
            fireworksInterval = setInterval(() => {
                const x = Math.random() * window.innerWidth;
                const y = Math.random() * (window.innerHeight / 2);
                createFirework(x, y);
            }, 800);
        }

        function createConfetti() {
            const colors = ['#FFD700', '#C41E3A', '#FFFAFA', '#0F5132', '#C0C0C0'];
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.className = 'confetti';
                    confetti.style.left = Math.random() * 100 + '%';
                    confetti.style.top = '-10px';
                    confetti.style.background = colors[Math.floor(Math.random() * colors.length)];
                    confetti.style.animationDelay = Math.random() * 0.5 + 's';
                    document.body.appendChild(confetti);
                    
                    setTimeout(() => confetti.remove(), 3000);
                }, i * 50);
            }
        }

        function startNewQuest() {
            if (confirm('Dette vil tilbakestille all fremgang. Er du sikker?')) {
                // Stop fireworks
                if (fireworksInterval) {
                    clearInterval(fireworksInterval);
                }
                
                try {
                    if (currentTeam) {
                        // Clear all team data
                        localStorage.removeItem(`tasks_${currentTeam.name}`);
                        localStorage.removeItem(`penalties_${currentTeam.name}`);
                        localStorage.removeItem(`completed_${currentTeam.name}`);
                        
                        // Clear answers
                        for (const task of TASKS) {
                            localStorage.removeItem(`answer_${currentTeam.name}_${task.id}`);
                            localStorage.removeItem(`attempts_${currentTeam.name}_${task.id}`);
                        }
                    }
                    localStorage.removeItem('currentTeam');
                } catch (error) {
                    console.error('Error resetting:', error);
                }
                
                currentTeam = null;
                completedTasks = [];
                penaltyTimers = {};
                document.getElementById('teamName').value = '';
                document.getElementById('registrationScreen').classList.remove('hidden');
                document.getElementById('quizScreen').classList.add('hidden');
                document.getElementById('congratulationsScreen').classList.add('hidden');
            }
        }

        // Developer navigation functions
        function devGoToStart() {
            document.getElementById('registrationScreen').classList.remove('hidden');
            document.getElementById('quizScreen').classList.add('hidden');
            document.getElementById('congratulationsScreen').classList.add('hidden');
        }

        function devNextTask() {
            if (completedTasks.length < TASKS.length) {
                // Find the next incomplete task
                const nextTask = TASKS.find(t => !completedTasks.includes(t.id));
                if (nextTask) {
                    completedTasks.push(nextTask.id);
                    saveTeamData();
                    
                    // Check if this was the final task
                    if (nextTask.isFinal) {
                        showCongratulations();
                    } else {
                        renderTasks();
                        updateProgress();
                    }
                }
            }
        }

        function devPrevTask() {
            if (completedTasks.length > 0) {
                // Remove the last completed task
                completedTasks.pop();
                saveTeamData();
                
                // Make sure we're on the quiz screen
                document.getElementById('congratulationsScreen').classList.add('hidden');
                document.getElementById('quizScreen').classList.remove('hidden');
                
                renderTasks();
                updateProgress();
            }
        }

        // Initialize app
        async function init() {
            const hasData = await loadTeamData();
            if (hasData) {
                // Team data exists, show quiz screen immediately
                showQuizScreen();
            } else {
                // No existing team, show registration
                document.getElementById('registrationScreen').classList.remove('hidden');
            }
        }

        // Run init when page loads
        init();

        // Prevent refresh cheating by continuously checking storage
        setInterval(async () => {
            if (currentTeam) {
                // Reload penalty timers to ensure they're current
                try {
                    const penaltyData = localStorage.getItem(`penalties_${currentTeam.name}`);
                    if (penaltyData) {
                        const storedPenalties = JSON.parse(penaltyData);
                        // Update any penalties that might have been modified
                        for (const taskId in storedPenalties) {
                            if (!penaltyTimers[taskId] || storedPenalties[taskId] > penaltyTimers[taskId]) {
                                penaltyTimers[taskId] = storedPenalties[taskId];
                            }
                        }
                    }
                } catch (error) {
                    console.log('Error checking penalties:', error);
                }
            }
        }, 5000); // Check every 5 seconds
    </script>
</body>
</html>
