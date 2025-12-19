<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Christmas Quest 🎄</title>
    <link href="https://fonts.googleapis.com/css2?family=Mountains+of+Christmas:wght@400;700&family=Karla:wght@400;600&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
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
        }

        button:hover {
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
            }

            .container {
                padding: 1rem;
            }

            .button-group {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1><span class="ornament">🎄</span> Christmas Quest <span class="ornament">🎄</span></h1>
            <p class="subtitle">Team Challenge 2024</p>
        </header>

        <!-- Registration Screen -->
        <div id="registrationScreen" class="hidden">
            <div class="card">
                <h2>🎅 Register Your Team</h2>
                <p style="color: var(--silver); margin-bottom: 1.5rem; font-size: 0.95rem;">
                    ⚠️ <strong>Important:</strong> Your team's progress is automatically saved. 
                    Refreshing or closing the page will not reset your answers or penalty timers!
                </p>
                <div class="input-group">
                    <label for="teamName">Team Name</label>
                    <input type="text" id="teamName" placeholder="Enter your team name..." />
                </div>
                <button onclick="registerTeam()">Start Quest</button>
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
                <button class="button-secondary" onclick="resetApp()">Reset</button>
            </div>

            <div class="card">
                <h2>🎁 Your Christmas Tasks</h2>
                <div class="task-list" id="taskList"></div>
            </div>
        </div>
    </div>

    <script>
        const TASKS = [
            {
                id: 1,
                question: "What Christmas carol contains the lyrics 'Strike the harp and join the chorus'?",
                answer: "deck the halls",
                isFinal: false
            },
            {
                id: 2,
                question: "In what country did the tradition of putting up a Christmas tree originate?",
                answer: "germany",
                isFinal: false
            },
            {
                id: 3,
                question: "How many reindeer pull Santa's sleigh (including Rudolph)?",
                answer: "9",
                isFinal: false
            },
            {
                id: 4,
                question: "What is the name of the Grinch's dog?",
                answer: "max",
                isFinal: false
            },
            {
                id: 5,
                question: "In the song '12 Days of Christmas,' what gift is given on the 7th day?",
                answer: "seven swans a-swimming",
                isFinal: false
            },
            {
                id: 6,
                question: "FINAL CHALLENGE: Create a Christmas haiku and share your team's favorite Christmas memory!",
                answer: null, // No wrong answer for final challenge
                isFinal: true
            }
        ];

        let currentTeam = null;
        let completedTasks = [];
        let penaltyTimers = {}; // Track penalty end times for each task

        async function loadTeamData() {
            try {
                const result = await window.storage.get('currentTeam');
                if (result) {
                    currentTeam = JSON.parse(result.value);
                    const tasksResult = await window.storage.get(`tasks_${currentTeam.name}`);
                    if (tasksResult) {
                        completedTasks = JSON.parse(tasksResult.value);
                    }
                    const penaltyResult = await window.storage.get(`penalties_${currentTeam.name}`);
                    if (penaltyResult) {
                        penaltyTimers = JSON.parse(penaltyResult.value);
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
                await window.storage.set('currentTeam', JSON.stringify(currentTeam));
                await window.storage.set(`tasks_${currentTeam.name}`, JSON.stringify(completedTasks));
                await window.storage.set(`penalties_${currentTeam.name}`, JSON.stringify(penaltyTimers));
            } catch (error) {
                console.error('Error saving data:', error);
            }
        }

        async function registerTeam() {
            const teamName = document.getElementById('teamName').value.trim();
            
            if (!teamName) {
                alert('Please enter a team name!');
                return;
            }

            // Check if this team already exists
            try {
                const existingTeamResult = await window.storage.get('currentTeam');
                if (existingTeamResult) {
                    const existingTeam = JSON.parse(existingTeamResult.value);
                    if (existingTeam.name === teamName) {
                        // Team exists, load their data
                        currentTeam = existingTeam;
                        const tasksResult = await window.storage.get(`tasks_${currentTeam.name}`);
                        if (tasksResult) {
                            completedTasks = JSON.parse(tasksResult.value);
                        }
                        const penaltyResult = await window.storage.get(`penalties_${currentTeam.name}`);
                        if (penaltyResult) {
                            penaltyTimers = JSON.parse(penaltyResult.value);
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

            TASKS.forEach((task, index) => {
                const isCompleted = completedTasks.includes(task.id);
                const isUnderPenalty = isTaskUnderPenalty(task.id);
                
                // For regular tasks: only show completed tasks and the next incomplete task
                const taskIndex = regularTasks.findIndex(t => t.id === task.id);
                const shouldShowRegularTask = task.isFinal || isCompleted || taskIndex === firstIncompleteIndex;
                
                if (!shouldShowRegularTask) {
                    return; // Skip this task - don't render it yet
                }

                const isLocked = (task.isFinal && !allRegularCompleted) || isUnderPenalty;
                const isActive = !isCompleted && !isLocked;

                const taskDiv = document.createElement('div');
                taskDiv.className = `task-item ${isCompleted ? 'completed' : ''} ${isActive ? 'active' : ''} ${isLocked ? 'locked' : ''} ${task.isFinal ? 'final-task' : ''}`;
                taskDiv.id = `task_${task.id}`;
                
                let statusClass = isCompleted ? 'completed' : isActive ? 'active' : 'locked';
                let statusText = isCompleted ? '✓ Complete' : isActive ? 'Answer Now' : '🔒 Locked';

                if (isUnderPenalty) {
                    statusText = '⏱️ Penalty';
                }

                if (task.isFinal && allRegularCompleted && !isCompleted) {
                    taskDiv.innerHTML = `
                        <div class="unlocked-badge">✨ UNLOCKED! ✨</div>
                    `;
                }

                taskDiv.innerHTML += `
                    <div class="task-header">
                        <span class="task-number">Task ${task.id}</span>
                        <span class="task-status ${statusClass}">${statusText}</span>
                    </div>
                    <div class="task-question">${task.question}</div>
                `;

                if (isUnderPenalty) {
                    const penaltyDiv = document.createElement('div');
                    penaltyDiv.className = 'penalty-timer';
                    penaltyDiv.id = `penalty_${task.id}`;
                    const remainingSeconds = getRemainingPenaltyTime(task.id);
                    penaltyDiv.innerHTML = `
                        <div style="background: rgba(196, 30, 58, 0.2); border: 2px solid var(--crimson); border-radius: 12px; padding: 1rem; margin-top: 1rem; text-align: center;">
                            <div style="color: var(--crimson); font-weight: 700; font-size: 1.2rem; margin-bottom: 0.5rem;">❌ Wrong Answer!</div>
                            <div style="color: var(--snow); font-size: 0.9rem;">Time remaining: <span id="timer_${task.id}" style="font-weight: 700; color: var(--gold);">${formatTime(remainingSeconds)}</span></div>
                        </div>
                    `;
                    taskDiv.appendChild(penaltyDiv);
                }

                if (isActive) {
                    const answerInput = document.createElement('textarea');
                    answerInput.id = `answer_${task.id}`;
                    answerInput.placeholder = 'Type your answer here...';
                    
                    const submitBtn = document.createElement('button');
                    submitBtn.textContent = task.isFinal ? 'Complete Quest! 🎉' : 'Submit Answer';
                    submitBtn.onclick = () => submitAnswer(task.id);
                    
                    taskDiv.appendChild(answerInput);
                    taskDiv.appendChild(submitBtn);
                }

                if (isCompleted) {
                    const successMsg = document.createElement('div');
                    successMsg.className = 'success-message';
                    successMsg.textContent = task.isFinal ? '🎉 Quest Complete! Congratulations! 🎉' : '✓ Answer submitted successfully!';
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
                alert('Please enter an answer!');
                return;
            }

            const task = TASKS.find(t => t.id === taskId);
            
            // For final task, accept any answer
            if (task.isFinal || task.answer === null) {
                completedTasks.push(taskId);
                
                // Save the answer with timestamp
                try {
                    await window.storage.set(`answer_${currentTeam.name}_${taskId}`, JSON.stringify({
                        answer: answer,
                        timestamp: Date.now()
                    }));
                } catch (error) {
                    console.error('Error saving answer:', error);
                }

                await saveTeamData();
                renderTasks();
                updateProgress();

                setTimeout(() => {
                    alert('🎄 Congratulations! Your team has completed the Christmas Quest! 🎄');
                }, 500);
                return;
            }

            // Check if answer is correct
            const userAnswer = normalizeAnswer(answer);
            const correctAnswer = normalizeAnswer(task.answer);

            if (userAnswer === correctAnswer || userAnswer.includes(correctAnswer) || correctAnswer.includes(userAnswer)) {
                // Correct answer!
                completedTasks.push(taskId);
                
                // Save the answer with timestamp
                try {
                    await window.storage.set(`answer_${currentTeam.name}_${taskId}`, JSON.stringify({
                        answer: answer,
                        timestamp: Date.now()
                    }));
                } catch (error) {
                    console.error('Error saving answer:', error);
                }

                await saveTeamData();
                renderTasks();
                updateProgress();
            } else {
                // Wrong answer - apply 2 minute penalty
                const penaltyEndTime = Date.now() + (2 * 60 * 1000); // 2 minutes from now
                penaltyTimers[taskId] = penaltyEndTime;
                
                // Also save the wrong attempt with timestamp
                try {
                    const attemptsKey = `attempts_${currentTeam.name}_${taskId}`;
                    let attempts = [];
                    try {
                        const attemptsResult = await window.storage.get(attemptsKey);
                        if (attemptsResult) {
                            attempts = JSON.parse(attemptsResult.value);
                        }
                    } catch (e) {}
                    
                    attempts.push({
                        answer: answer,
                        timestamp: Date.now(),
                        penaltyUntil: penaltyEndTime
                    });
                    
                    await window.storage.set(attemptsKey, JSON.stringify(attempts));
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
            if (confirm('Are you sure you want to reset? All progress will be lost!')) {
                try {
                    if (currentTeam) {
                        await window.storage.delete(`tasks_${currentTeam.name}`);
                        await window.storage.delete(`penalties_${currentTeam.name}`);
                        // Delete all answers
                        for (const task of TASKS) {
                            try {
                                await window.storage.delete(`answer_${currentTeam.name}_${task.id}`);
                            } catch (e) {}
                        }
                    }
                    await window.storage.delete('currentTeam');
                } catch (error) {
                    console.error('Error resetting:', error);
                }
                
                currentTeam = null;
                completedTasks = [];
                penaltyTimers = {};
                document.getElementById('teamName').value = '';
                document.getElementById('registrationScreen').classList.remove('hidden');
                document.getElementById('quizScreen').classList.add('hidden');
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
                    const penaltyResult = await window.storage.get(`penalties_${currentTeam.name}`);
                    if (penaltyResult) {
                        const storedPenalties = JSON.parse(penaltyResult.value);
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
