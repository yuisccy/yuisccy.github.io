<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>人體探險隊：神經與泌尿系統（Mario版）</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC:wght@400;700;900&display=swap');

        body {
            margin: 0;
            padding: 0;
            overflow: hidden;
            background-color: #202028;
            font-family: 'Noto Sans TC', sans-serif;
            touch-action: none;
            user-select: none;
            -webkit-user-select: none;
        }

        #game-container {
            position: relative;
            width: 100vw;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #5c94fc;
        }

        canvas {
            background-color: #5c94fc;
            box-shadow: 0 0 20px rgba(0,0,0,0.5);
            image-rendering: pixelated;
        }

        #ui-layer {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
        }

        #hud {
            position: absolute;
            top: 10px;
            left: 10px;
            color: white;
            font-size: 18px;
            font-weight: bold;
            text-shadow: 2px 2px 0 #000;
            background: rgba(0, 0, 0, 0.5);
            padding: 8px 15px;
            border-radius: 20px;
            pointer-events: auto;
            display: flex;
            gap: 12px;
            border: 2px solid white;
            align-items: center;
            flex-wrap: wrap;
        }

        .hud-item {
            display: flex;
            align-items: center;
            white-space: nowrap;
        }

        .hud-icon {
            margin-right: 5px;
            font-size: 20px;
        }
        
        .divider {
            width: 2px;
            height: 16px;
            background: rgba(255,255,255,0.5);
        }

        /* Warning Message Toast */
        #toast-msg {
            position: absolute;
            top: 80px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(231, 76, 60, 0.9);
            color: white;
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.2em;
            display: none;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            border: 2px solid white;
            z-index: 150;
            animation: shake 0.5s;
        }

        @keyframes shake {
            0% { transform: translateX(-50%) rotate(0deg); }
            25% { transform: translateX(-55%) rotate(-5deg); }
            50% { transform: translateX(-45%) rotate(5deg); }
            75% { transform: translateX(-55%) rotate(-5deg); }
            100% { transform: translateX(-50%) rotate(0deg); }
        }

        .control-btn {
            position: absolute;
            width: 70px;
            height: 70px;
            background: rgba(255, 255, 255, 0.2);
            border: 2px solid rgba(255, 255, 255, 0.5);
            border-radius: 50%;
            pointer-events: auto;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 30px;
            color: white;
            user-select: none;
        }
        
        .control-btn:active {
            background: rgba(255, 255, 255, 0.4);
            transform: scale(0.95);
        }

        #btn-left { bottom: 40px; left: 30px; }
        #btn-right { bottom: 40px; left: 120px; }
        #btn-jump { bottom: 40px; right: 30px; width: 80px; height: 80px; font-size: 24px; }

        /* Quiz Modal */
        #quiz-modal {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: none;
            justify-content: center;
            align-items: center;
            pointer-events: auto;
            z-index: 100;
        }

        .modal-content {
            background: white;
            padding: 25px;
            border-radius: 15px;
            width: 80%;
            max-width: 500px;
            text-align: center;
            border: 5px solid #e67e22;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            animation: popIn 0.3s ease-out;
        }

        @keyframes popIn {
            from { transform: scale(0.8); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        .question-text {
            font-size: 1.4em;
            margin-bottom: 20px;
            color: #333;
            font-weight: bold;
        }

        .category-tag {
            display: inline-block;
            padding: 5px 10px;
            border-radius: 5px;
            color: white;
            font-size: 0.8em;
            margin-bottom: 10px;
        }
        .cat-nervous { background-color: #9b59b6; }
        .cat-urinary { background-color: #3498db; }
        .cat-water { background-color: #1abc9c; } 

        .options-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 10px;
        }

        .option-btn {
            background: #f1f1f1;
            border: 2px solid #ddd;
            padding: 15px;
            border-radius: 10px;
            font-size: 1.1em;
            cursor: pointer;
            transition: all 0.2s;
            text-align: left;
        }

        .option-btn:hover {
            background: #e8f0fe;
            border-color: #5c94fc;
        }

        .feedback-msg {
            margin-top: 15px;
            font-weight: bold;
            font-size: 1.2em;
            min-height: 1.5em;
        }

        .correct { color: #27ae60; }
        .wrong { color: #c0392b; }

        /* Game Over Screen */
        #game-over {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(92, 148, 252, 0.95);
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            pointer-events: auto;
            z-index: 200;
            color: white;
            text-align: center;
        }

        #game-over h1 { font-size: 3em; margin-bottom: 10px; text-shadow: 3px 3px 0 #000; }
        #game-over p { font-size: 1.5em; }
        
        .restart-btn {
            margin-top: 30px;
            padding: 15px 40px;
            font-size: 1.5em;
            background: #2ecc71;
            color: white;
            border: none;
            border-radius: 50px;
            box-shadow: 0 6px 0 #27ae60;
            cursor: pointer;
            font-family: 'Noto Sans TC', sans-serif;
        }
        .restart-btn:active { transform: translateY(4px); box-shadow: 0 2px 0 #27ae60; }

        /* Start Screen */
        #start-screen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: #5c94fc;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            pointer-events: auto;
            z-index: 300;
            color: white;
            text-align: center;
            overflow: hidden;
        }

        #start-screen::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 60px;
            background: repeating-linear-gradient(45deg, #6d4c41, #6d4c41 10px, #5d4037 10px, #5d4037 20px);
            border-top: 5px solid #2ecc71;
        }

        .title-box {
            background: rgba(0, 0, 0, 0.3);
            padding: 30px;
            border-radius: 20px;
            backdrop-filter: blur(5px);
            border: 4px solid white;
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
            margin-bottom: 40px;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }

        #start-screen h1 { 
            font-size: 3em; 
            margin: 0; 
            color: #f1c40f;
            text-shadow: 4px 4px 0 #d35400, -2px -2px 0 #000;
            font-weight: 900;
            letter-spacing: 2px;
            line-height: 1.2;
        }

        #start-screen .subtitle {
            font-size: 1.5em;
            margin-top: 10px;
            color: #fff;
            text-shadow: 2px 2px 0 #000;
        }

        .start-btn {
            padding: 20px 50px;
            font-size: 2em;
            background: #27ae60;
            color: white;
            border: 4px solid #fff;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 8px 0 #1e8449, 0 15px 20px rgba(0,0,0,0.4);
            font-weight: bold;
            transition: transform 0.1s;
            text-shadow: 2px 2px 0 rgba(0,0,0,0.2);
            z-index: 10;
        }

        .start-btn:active {
            transform: translateY(8px);
            box-shadow: 0 0 0 #1e8449, 0 0 10px rgba(0,0,0,0.4);
        }

        .decor {
            position: absolute;
            font-size: 40px;
            opacity: 0.8;
            animation: drift 20s linear infinite;
        }
        
        @keyframes drift {
            from { transform: translateX(-120vw); }
            to { transform: translateX(120vw); }
        }

    </style>
</head>
<body>

    <div id="game-container">
        <canvas id="gameCanvas"></canvas>
        
        <div id="ui-layer">
            <div id="hud">
                <div class="hud-item" style="color: #e74c3c;">
                    <span class="hud-icon">❤️</span> <span id="hp-display">5</span>
                </div>
                <div class="divider"></div>
                <!-- 計時器 -->
                <div class="hud-item" style="color: #fff;">
                    <span class="hud-icon">⏱️</span> <span id="time-display">05:00</span>
                </div>
                <div class="divider"></div>
                <div class="hud-item" style="color: #f1c40f;">
                    <span class="hud-icon">💰</span> <span id="coin-score">0</span>
                </div>
                <div class="divider"></div>
                <div class="hud-item">
                    <span class="hud-icon">📦</span> <span id="score">0</span> / <span id="total-chests">0</span>
                </div>
            </div>

            <!-- Toast Message -->
            <div id="toast-msg"></div>

            <!-- Platformer Controls -->
            <div id="btn-left" class="control-btn">◀</div>
            <div id="btn-right" class="control-btn">▶</div>
            <div id="btn-jump" class="control-btn">跳躍</div>
        </div>

        <!-- Quiz Modal -->
        <div id="quiz-modal">
            <div class="modal-content">
                <div id="quiz-category" class="category-tag">分類</div>
                <div id="quiz-question" class="question-text">題目載入中...</div>
                <div id="quiz-options" class="options-grid"></div>
                <div id="quiz-feedback" class="feedback-msg"></div>
            </div>
        </div>

        <!-- Start Screen -->
        <div id="start-screen">
            <div class="decor" style="top: 10%; animation-duration: 25s; animation-delay: -5s;">☁️</div>
            <div class="decor" style="top: 25%; animation-duration: 35s; animation-delay: -15s;">☁️</div>
            
            <div class="title-box">
                <h1>SUPER<br>BODY ADVENTURE</h1>
                <div class="subtitle">身體大冒險：神經與泌尿系統</div>
            </div>

            <button class="start-btn" onclick="startGame()">PRESS START</button>
            
            <div style="margin-top: 20px; color: white; text-shadow: 1px 1px 0 #000; font-size: 0.9em; z-index: 10;">
                ⭐ 收集金幣 · 🍄 開啟所有寶箱 · 🏆 抵達終點
            </div>
        </div>

        <!-- Game Over Screen -->
        <div id="game-over">
            <h1 id="go-title"></h1>
            <p id="go-msg"></p>
            <p>金幣分數: <span id="final-coins">0</span></p>
            <p>寶箱收集: <span id="final-chests">0</span></p>
            <!-- 修正：改用 JS 重置而非重新整理網頁 -->
            <button class="restart-btn" onclick="resetGame()">再玩一次</button>
        </div>
    </div>

    <script>
        // --- 遊戲數據與問題 ---
        const questions = [
            // 神經系統
            { category: '神經系統', q: '神經系統的「總指揮」是哪一個器官？', options: ['心臟', '腦', '肺'], answer: 1 },
            { category: '神經系統', q: '當我們手碰到熱水立刻縮回來，這叫什麼反應？', options: ['反射動作', '思考動作', '慢動作'], answer: 0 },
            { category: '神經系統', q: '大腦與身體各部位之間傳遞訊息的是？', options: ['血管', '骨骼', '脊髓與神經'], answer: 2 },
            { category: '神經系統', q: '哪一個動作需要大腦思考後才能做？', options: ['膝蓋被敲擊彈起', '瞳孔遇光縮小', '寫數學作業'], answer: 2 },
            { category: '神經系統', q: '按自己的意思去做的行為稱為甚麼動作？', options: ['反射動作', '隨意動作', '無意識動作'], answer: 1 },
            
            // 泌尿系統
            { category: '泌尿系統', q: '人體主要負責過濾血液、製造尿液的器官是？', options: ['胃', '肝臟', '腎臟'], answer: 2 },
            { category: '泌尿系統', q: '尿液製造出來後，會暫時儲存在哪裡？', options: ['膀胱', '輸尿管', '尿道'], answer: 0 },
            { category: '泌尿系統', q: '連接腎臟和膀胱的管子叫做什麼？', options: ['血管', '輸尿管', '腸道'], answer: 1 },
            { category: '泌尿系統', q: '多喝水對哪個系統的健康最重要？', options: ['骨骼系統', '肌肉系統', '泌尿系統'], answer: 2 },
            // 水的功能
            { category: '水的功能', q: '血液的主要成份是甚麼和作用？', options: ['主要成份是血球，負責凝血', '主要成份是水，負責運送養分和氧', '主要成份是鐵，負責造血'], answer: 1 },
            { category: '水的功能', q: '尿液的主要作用是甚麼？', options: ['稀釋體內的廢物，排除多餘的水分', '儲存養分', '製造血液'], answer: 0 },
            { category: '水的功能', q: '水在人體運動時的功用？', options: ['增加肌肉力量', '排出汗以調節體溫', '減少能量消耗'], answer: 1 },
            { category: '水的功能', q: '人體的水份約佔體重的多少百分比？', options: ['30%', '50%', '70%'], answer: 2 },
            { category: '水的功能', q: '下列哪一項不是排出水份的主要方式？', options: ['排尿', '流汗', '吸收養分'], answer: 2 }
        ];

        // --- 遊戲引擎設置 ---
        const canvas = document.getElementById('gameCanvas');
        const ctx = canvas.getContext('2d');
        const scoreEl = document.getElementById('score');
        const coinScoreEl = document.getElementById('coin-score');
        const hpDisplayEl = document.getElementById('hp-display');
        const totalChestsEl = document.getElementById('total-chests');
        const timeDisplayEl = document.getElementById('time-display');
        const toastEl = document.getElementById('toast-msg');
        
        // 控制按鈕
        const btnLeft = document.getElementById('btn-left');
        const btnRight = document.getElementById('btn-right');
        const btnJump = document.getElementById('btn-jump');

        // 遊戲狀態
        let gameState = 'START';
        let chestScore = 0;
        let coinScore = 0;
        let map = [];
        const TILE_SIZE = 50;
        const MAP_COLS = 200; // 地圖長度
        const MAP_ROWS = 14;  // 地圖高度
        
        let chests = [];
        let coins = [];
        let particles = [];
        
        // 計時器相關
        let gameTime = 300; // 300秒 = 5分鐘
        let lastTimeUpdate = 0;

        // 物理常數
        const GRAVITY = 0.5;
        const JUMP_FORCE = -13; 
        const MOVE_SPEED = 6;

        // 玩家設定
        const player = {
            x: 100,
            y: 100,
            width: TILE_SIZE * 0.8,
            height: TILE_SIZE,
            vx: 0,
            vy: 0,
            direction: 1, 
            grounded: false,
            jumpCount: 0, 
            maxJumps: 2,
            hp: 5,       
            maxHp: 5
        };

        // 攝影機
        const camera = { x: 0, y: 0 };

        // --- 初始化與地圖生成 ---
        function initGame() {
            resizeCanvas();
            generateLevel();
            chestScore = 0;
            coinScore = 0;
            player.hp = 5; 
            gameTime = 300; 
            lastTimeUpdate = Date.now();
            updateHUD();
            
            player.x = TILE_SIZE * 2;
            player.y = TILE_SIZE * (MAP_ROWS - 5);
            player.vx = 0;
            player.vy = 0;
        }

        // 新增的重置功能
        function resetGame() {
            document.getElementById('game-over').style.display = 'none';
            initGame();
            gameState = 'PLAYING';
        }

        function generateLevel() {
            map = [];
            chests = [];
            coins = [];
            
            // 階段 1: 初始化與生成地形 (牆壁與地板)
            for(let r=0; r<MAP_ROWS; r++) {
                map.push(new Array(MAP_COLS).fill(0));
            }

            // 地面生成
            for(let c=0; c<10; c++) fillCol(c, MAP_ROWS-2); // 起點平坦

            let groundLevel = MAP_ROWS - 2;
            for(let c=10; c<MAP_COLS-20; c++) {
                // 坑洞
                if (Math.random() < 0.05 && c > 15) { 
                    let gapWidth = Math.floor(Math.random() * 2) + 1; 
                    c += gapWidth;
                    continue;
                }
                // 高度變化
                if (Math.random() < 0.15) {
                    groundLevel += (Math.random() < 0.5 ? -1 : 1);
                    if (groundLevel > MAP_ROWS-1) groundLevel = MAP_ROWS-1;
                    if (groundLevel < MAP_ROWS-5) groundLevel = MAP_ROWS-5;
                }
                fillCol(c, groundLevel);

                // 平台 (注意：這一步會修改 map，但不會放金幣)
                if (Math.random() < 0.25) {
                    let platH = groundLevel - 4;
                    let platLen = Math.floor(Math.random() * 3) + 3; 
                    if (platH > 3) {
                        for(let i=0; i<platLen; i++) {
                            if (c+i < MAP_COLS-20) {
                                map[platH][c+i] = 1; 
                            }
                        }
                    }
                }
            }

            // 終點區域
            for(let c=MAP_COLS-20; c<MAP_COLS; c++) fillCol(c, MAP_ROWS-2);
            fillCol(MAP_COLS-2, MAP_ROWS-10); // 終點牆

            // 階段 2: 生成物件 (根據已確定的地圖放置金幣與寶箱)
            generateEntities();
        }

        function fillCol(col, startRow) {
            for(let r=startRow; r<MAP_ROWS; r++) {
                if(r >= 0 && r < MAP_ROWS && col >= 0 && col < MAP_COLS) {
                    map[r][col] = 1;
                }
            }
        }

        function generateEntities() {
            // 重新遍歷地圖來放置金幣 (確保只放在空氣中)
            for(let c=10; c<MAP_COLS-20; c++) {
                // 掃描這一列，尋找適合放金幣的地方
                for (let r=0; r<MAP_ROWS; r++) {
                    if (map[r][c] === 1) { // 找到地面或平台
                        // 嘗試在上方放金幣
                        if (r-1 >= 0 && map[r-1][c] === 0) { // 上方是空氣
                            // 地面金幣 (低機率)
                            if (Math.random() < 0.05) addCoin(c, r-1);
                            // 平台金幣 (如果是懸空的平台，機率高一點)
                            // 簡單判斷：如果下方很深，可能是平台
                            if (r+1 < MAP_ROWS && map[r+1][c] === 0) {
                                if (Math.random() < 0.4) addCoin(c, r-1);
                            }
                        }
                    }
                }
            }

            // 放置寶箱 (確保所有題目都有寶箱)
            const totalQuestions = questions.length;
            const segment = Math.floor((MAP_COLS - 40) / (totalQuestions + 1)); 
            const shuffledQuestions = [...questions].sort(() => 0.5 - Math.random());
            
            for(let i=0; i<totalQuestions; i++) {
                let centerC = 20 + i * segment + Math.floor(Math.random() * 5);
                if (centerC >= MAP_COLS - 5) centerC = MAP_COLS - 10; 

                // 尋找地面 (從上往下找第一個非空氣方塊)
                let groundR = -1;
                for (let r = 0; r < MAP_ROWS; r++) {
                    if (map[r][centerC] === 1) {
                        groundR = r;
                        break;
                    }
                }

                if (groundR !== -1) {
                    // 放在地面上一格
                    addChest(centerC, groundR - 1, shuffledQuestions[i]);
                } else {
                    // 如果剛好是坑洞，就強制補一個平台
                    let fixR = MAP_ROWS - 4;
                    map[fixR][centerC] = 1;
                    addChest(centerC, fixR - 1, shuffledQuestions[i]);
                }
            }
            totalChestsEl.innerText = chests.length;
        }

        function addCoin(c, r) {
            // 雙重檢查：絕對不放在牆壁裡
            if (map[r][c] !== 0) return;
            
            coins.push({
                x: c * TILE_SIZE + TILE_SIZE/2,
                y: r * TILE_SIZE + TILE_SIZE/2,
                collected: false,
                offset: Math.random() * Math.PI * 2
            });
        }

        function addChest(c, r, question) {
            // 雙重檢查
            if (map[r][c] !== 0) r--; // 如果位置有牆，往上移一格

            chests.push({
                x: c * TILE_SIZE + TILE_SIZE/2,
                y: r * TILE_SIZE + TILE_SIZE/2,
                opened: false,
                question: question
            });
        }

        function updateHUD() {
            scoreEl.innerText = chestScore;
            coinScoreEl.innerText = coinScore;
            hpDisplayEl.innerText = player.hp;

            let m = Math.floor(gameTime / 60);
            let s = Math.floor(gameTime % 60);
            timeDisplayEl.innerText = `${m.toString().padStart(2, '0')}:${s.toString().padStart(2, '0')}`;
            
            if (gameTime <= 30) {
                timeDisplayEl.parentElement.style.color = '#e74c3c';
            } else {
                timeDisplayEl.parentElement.style.color = '#fff';
            }
            
            // 視覺提示：如果還沒收集完，寶箱文字紅色
            if (chestScore < chests.length) {
                scoreEl.parentElement.style.color = '#ffcc00';
            } else {
                scoreEl.parentElement.style.color = '#2ecc71';
            }
        }

        function showToast(msg) {
            toastEl.innerText = msg;
            toastEl.style.display = 'block';
            // 重新觸發動畫
            toastEl.style.animation = 'none';
            toastEl.offsetHeight; /* trigger reflow */
            toastEl.style.animation = 'shake 0.5s';
            
            setTimeout(() => {
                toastEl.style.display = 'none';
            }, 2000);
        }

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        window.addEventListener('resize', resizeCanvas);

        function startGame() {
            document.getElementById('start-screen').style.display = 'none';
            initGame();
            gameState = 'PLAYING';
            requestAnimationFrame(gameLoop);
        }

        // --- 控制 ---
        let keys = { left: false, right: false };

        function handleTouchStart(key) {
            if (gameState !== 'PLAYING') return;
            if (key === 'jump') jump();
            else keys[key] = true;
        }
        function handleTouchEnd(key) {
            if (key !== 'jump') keys[key] = false;
        }

        btnLeft.addEventListener('touchstart', (e) => { e.preventDefault(); handleTouchStart('left'); });
        btnLeft.addEventListener('touchend', (e) => { e.preventDefault(); handleTouchEnd('left'); });
        btnRight.addEventListener('touchstart', (e) => { e.preventDefault(); handleTouchStart('right'); });
        btnRight.addEventListener('touchend', (e) => { e.preventDefault(); handleTouchEnd('right'); });
        btnJump.addEventListener('touchstart', (e) => { e.preventDefault(); handleTouchStart('jump'); });
        
        window.addEventListener('keydown', (e) => {
            if (gameState !== 'PLAYING') return;
            if (e.key === 'ArrowLeft') keys.left = true;
            if (e.key === 'ArrowRight') keys.right = true;
            if (e.key === 'ArrowUp' || e.key === ' ') jump();
        });
        window.addEventListener('keyup', (e) => {
            if (e.key === 'ArrowLeft') keys.left = false;
            if (e.key === 'ArrowRight') keys.right = false;
        });

        function jump() {
            if (player.grounded || player.jumpCount < player.maxJumps) {
                player.vy = JUMP_FORCE;
                player.grounded = false;
                player.jumpCount++;
            }
        }

        // --- 物理更新 ---
        function update() {
            if (gameState !== 'PLAYING') return;

            let now = Date.now();
            if (now - lastTimeUpdate >= 1000) {
                gameTime--;
                lastTimeUpdate = now;
                updateHUD();
                if (gameTime <= 0) {
                    gameOver(false, "時間到！");
                    return;
                }
            }

            // 移動
            if (keys.left) { player.vx = -MOVE_SPEED; player.direction = -1; }
            else if (keys.right) { player.vx = MOVE_SPEED; player.direction = 1; }
            else { player.vx = 0; }

            // 重力
            player.vy += GRAVITY;
            if(player.vy > TILE_SIZE/2) player.vy = TILE_SIZE/2;

            player.x += player.vx;
            checkHorizontalCollision();

            player.y += player.vy;
            player.grounded = false;
            checkVerticalCollision();

            if (player.y > MAP_ROWS * TILE_SIZE + 100) {
                handleFallDamage();
            }

            // 攝影機
            camera.x = player.x - canvas.width * 0.3; 
            camera.x = Math.max(0, camera.x);
            camera.x = Math.min((MAP_COLS * TILE_SIZE) - canvas.width, camera.x);

            const mapHeight = MAP_ROWS * TILE_SIZE;
            if (mapHeight > canvas.height) {
                camera.y = player.y - canvas.height * 0.6;
                camera.y = Math.max(0, camera.y);
                camera.y = Math.min(mapHeight - canvas.height, camera.y);
            } else {
                camera.y = -(canvas.height - mapHeight) / 2;
            }

            checkInteractions();

            // --- 終點檢查 (Win Condition Logic) ---
            if (player.x > (MAP_COLS - 5) * TILE_SIZE) {
                if (chestScore >= chests.length) {
                    gameOver(true); // 成功通關
                } else {
                    // 未收集完寶箱，彈回並提示
                    player.x -= 20; 
                    player.vx = 0;
                    showToast(`還有 ${chests.length - chestScore} 個寶箱沒打開！`);
                }
            }

            updateParticles();
        }

        function handleFallDamage() {
            player.hp--;
            updateHUD();
            
            if (player.hp <= 0) {
                gameOver(false, "體力耗盡！");
            } else {
                respawnPlayer();
            }
        }

        function respawnPlayer() {
            let safeC = Math.floor(player.x / TILE_SIZE) - 4;
            if (safeC < 2) safeC = 2;
            if (safeC > MAP_COLS - 5) safeC = MAP_COLS - 5;
            
            while (safeC > 2 && map[MAP_ROWS-2][safeC] === 0) {
                safeC--;
            }

            player.x = safeC * TILE_SIZE;
            player.y = TILE_SIZE * 2;
            player.vy = 0;
            player.vx = 0;
        }

        function checkInteractions() {
            chests.forEach(chest => {
                if (!chest.opened) {
                    if (checkRectCollide(player, {x: chest.x - TILE_SIZE/2, y: chest.y - TILE_SIZE/2, width: TILE_SIZE, height: TILE_SIZE})) {
                        openChest(chest);
                    }
                }
            });

            coins.forEach(coin => {
                if (!coin.collected) {
                    const dx = player.x + player.width/2 - coin.x;
                    const dy = player.y + player.height/2 - coin.y;
                    if (Math.sqrt(dx*dx + dy*dy) < TILE_SIZE) {
                        collectCoin(coin);
                    }
                }
            });
        }

        function collectCoin(coin) {
            coin.collected = true;
            coinScore += 10;
            updateHUD();
            createSparkles(coin.x, coin.y);
        }

        function checkRectCollide(p, rect) {
            return (p.x < rect.x + rect.width &&
                    p.x + p.width > rect.x &&
                    p.y < rect.y + rect.height &&
                    p.y + p.height > rect.y);
        }

        function getTileAt(x, y) {
            const c = Math.floor(x / TILE_SIZE);
            const r = Math.floor(y / TILE_SIZE);
            if (r < 0 || r >= MAP_ROWS || c < 0 || c >= MAP_COLS) return 0;
            return map[r][c];
        }

        function checkHorizontalCollision() {
            if (player.vx < 0) {
                const leftTop = getTileAt(player.x, player.y + 1);
                const leftBottom = getTileAt(player.x, player.y + player.height - 1);
                if (leftTop === 1 || leftBottom === 1) {
                    player.x = Math.floor(player.x / TILE_SIZE + 1) * TILE_SIZE;
                    player.vx = 0;
                }
            } else if (player.vx > 0) {
                const rightTop = getTileAt(player.x + player.width, player.y + 1);
                const rightBottom = getTileAt(player.x + player.width, player.y + player.height - 1);
                if (rightTop === 1 || rightBottom === 1) {
                    player.x = Math.floor((player.x + player.width) / TILE_SIZE) * TILE_SIZE - player.width;
                    player.vx = 0;
                }
            }
        }

        function checkVerticalCollision() {
            if (player.vy < 0) {
                const topLeft = getTileAt(player.x + 1, player.y);
                const topRight = getTileAt(player.x + player.width - 1, player.y);
                if (topLeft === 1 || topRight === 1) {
                    player.y = Math.floor(player.y / TILE_SIZE + 1) * TILE_SIZE;
                    player.vy = 0;
                }
            } else if (player.vy > 0) {
                const bottomLeft = getTileAt(player.x + 1, player.y + player.height);
                const bottomRight = getTileAt(player.x + player.width - 1, player.y + player.height);
                if (bottomLeft === 1 || bottomRight === 1) {
                    player.y = Math.floor((player.y + player.height) / TILE_SIZE) * TILE_SIZE - player.height;
                    player.vy = 0;
                    player.grounded = true;
                    player.jumpCount = 0;
                }
            }
        }

        // --- 繪圖 ---
        function draw() {
            ctx.fillStyle = '#5c94fc'; 
            ctx.fillRect(0, 0, canvas.width, canvas.height);

            ctx.save();
            ctx.translate(-camera.x, -camera.y);

            const startC = Math.max(0, Math.floor(camera.x / TILE_SIZE));
            const endC = Math.min(MAP_COLS, Math.ceil((camera.x + canvas.width) / TILE_SIZE) + 1);

            for (let r = 0; r < MAP_ROWS; r++) {
                for (let c = startC; c < endC; c++) {
                    if (map[r][c] === 1) drawGround(c * TILE_SIZE, r * TILE_SIZE);
                }
            }

            drawFinishLine((MAP_COLS - 3) * TILE_SIZE, (MAP_ROWS - 5) * TILE_SIZE);

            coins.forEach(c => {
                if(!c.collected && c.x > camera.x - 50 && c.x < camera.x + canvas.width + 50) drawCoin(c);
            });
            chests.forEach(c => {
                if(c.x > camera.x - 50 && c.x < camera.x + canvas.width + 50) drawChest(c);
            });

            drawPlayer();
            drawParticles();

            ctx.restore();
        }

        function drawGround(x, y) {
            ctx.fillStyle = '#654321'; 
            ctx.fillRect(x, y, TILE_SIZE, TILE_SIZE);
            ctx.fillStyle = '#2ecc71'; 
            ctx.fillRect(x, y, TILE_SIZE, 10);
            ctx.fillStyle = '#51361a'; 
            ctx.fillRect(x+10, y+20, 5, 5);
            ctx.fillRect(x+35, y+30, 5, 5);
        }

        function drawCoin(coin) {
            const floatY = Math.sin(Date.now() / 200 + coin.offset) * 5;
            ctx.save();
            ctx.translate(coin.x, coin.y + floatY);
            ctx.beginPath();
            ctx.arc(0, 0, 15, 0, Math.PI * 2);
            ctx.fillStyle = '#f1c40f'; 
            ctx.fill();
            ctx.strokeStyle = '#f39c12';
            ctx.lineWidth = 2;
            ctx.stroke();
            ctx.beginPath();
            ctx.arc(0, 0, 10, 0, Math.PI * 2);
            ctx.strokeStyle = '#ffeaa7';
            ctx.stroke();
            ctx.fillStyle = '#e67e22';
            ctx.font = 'bold 16px Arial';
            ctx.textAlign = 'center';
            ctx.textBaseline = 'middle';
            ctx.fillText('$', 0, 1);
            ctx.restore();
        }

        function drawChest(chest) {
            const x = chest.x - TILE_SIZE/2 + 5;
            const y = chest.y - TILE_SIZE/2 + 5;
            const size = TILE_SIZE - 10;

            if (chest.opened) {
                ctx.fillStyle = '#7f8c8d';
                ctx.fillRect(x, y, size, size);
                ctx.fillStyle = '#95a5a6';
                ctx.fillRect(x+2, y+size/2, size-4, size/2-2);
            } else {
                ctx.fillStyle = '#f1c40f';
                ctx.fillRect(x, y, size, size);
                ctx.strokeStyle = '#d35400';
                ctx.lineWidth = 3;
                ctx.strokeRect(x, y, size, size);
                ctx.fillStyle = '#d35400';
                ctx.fillRect(x+size/2-5, y+size/2-5, 10, 10);
                ctx.fillStyle = '#d35400';
                ctx.font = 'bold 24px Arial';
                ctx.textAlign = 'center';
                ctx.fillText('?', x + size/2, y + size/2 - 5);
            }
        }

        function drawFinishLine(x, y) {
            ctx.fillStyle = '#2c3e50';
            ctx.fillRect(x, y - 100, 10, 250);
            ctx.fillStyle = '#e74c3c';
            ctx.beginPath();
            ctx.moveTo(x + 10, y - 90);
            ctx.lineTo(x + 60, y - 65);
            ctx.lineTo(x + 10, y - 40);
            ctx.fill();
        }

        function drawPlayer() {
            const x = player.x;
            const y = player.y;
            const w = player.width;
            const h = player.height;
            
            ctx.save();
            if (player.direction === -1) {
                ctx.translate(x + w, y);
                ctx.scale(-1, 1);
                ctx.translate(-x, -y);
            }

            // 帽子
            ctx.fillStyle = '#e74c3c';
            ctx.fillRect(x+w*0.2, y, w*0.6, h*0.2);
            ctx.fillRect(x+w*0.1, y+h*0.1, w*0.8, h*0.1);
            
            // 臉
            ctx.fillStyle = '#f1c40f'; 
            ctx.fillRect(x+w*0.15, y+h*0.2, w*0.6, h*0.3);
            ctx.fillStyle = '#51361a';
            ctx.fillRect(x+w*0.55, y+h*0.25, w*0.1, h*0.1); 
            ctx.fillRect(x+w*0.45, y+h*0.4, w*0.3, h*0.1); 

            // 身體
            ctx.fillStyle = '#3498db';
            ctx.fillRect(x+w*0.2, y+h*0.5, w*0.6, h*0.3);
            ctx.fillStyle = '#e74c3c';
            ctx.fillRect(x, y+h*0.5, w*0.2, h*0.3); 
            ctx.fillRect(x+w*0.8, y+h*0.5, w*0.2, h*0.3); 
            
            // 腳
            ctx.fillStyle = '#51361a';
            ctx.fillRect(x+w*0.1, y+h*0.8, w*0.3, h*0.2);
            ctx.fillRect(x+w*0.6, y+h*0.8, w*0.3, h*0.2);
            ctx.restore();
        }

        // --- 特效 ---
        function createParticles(x, y) {
            for(let i=0; i<15; i++) {
                particles.push({
                    x: x, y: y,
                    vx: (Math.random() - 0.5) * 10,
                    vy: (Math.random() - 0.5) * 10,
                    life: 1.0,
                    color: `hsl(${Math.random()*60 + 40}, 100%, 50%)`,
                    type: 'star'
                });
            }
        }

        function createSparkles(x, y) {
            for(let i=0; i<8; i++) {
                particles.push({
                    x: x, y: y,
                    vx: (Math.random() - 0.5) * 5,
                    vy: (Math.random() - 0.5) * 5,
                    life: 0.8,
                    color: '#ffeaa7',
                    type: 'sparkle'
                });
            }
        }
        
        function updateParticles() {
            for(let i=particles.length-1; i>=0; i--) {
                let p = particles[i];
                p.x += p.vx;
                p.y += p.vy;
                p.life -= 0.05;
                if(p.life <= 0) particles.splice(i, 1);
            }
        }
        
        function drawParticles() {
            particles.forEach(p => {
                ctx.globalAlpha = p.life;
                ctx.fillStyle = p.color;
                ctx.beginPath();
                if (p.type === 'sparkle') {
                    ctx.arc(p.x, p.y, 3, 0, Math.PI*2);
                } else {
                    ctx.arc(p.x, p.y, 5, 0, Math.PI*2);
                }
                ctx.fill();
            });
            ctx.globalAlpha = 1.0;
        }

        // --- 遊戲邏輯 ---
        function openChest(chest) {
            keys.left = false;
            keys.right = false;
            player.vx = 0;
            player.vy = 0;
            gameState = 'QUIZ';
            showQuiz(chest);
        }

        function showQuiz(chest) {
            const modal = document.getElementById('quiz-modal');
            const qEl = document.getElementById('quiz-question');
            const optionsEl = document.getElementById('quiz-options');
            const catEl = document.getElementById('quiz-category');
            const feedbackEl = document.getElementById('quiz-feedback');
            
            const qData = chest.question;

            catEl.innerText = qData.category;
            let catClass = 'category-tag ';
            if (qData.category === '神經系統') catClass += 'cat-nervous';
            else if (qData.category === '泌尿系統') catClass += 'cat-urinary';
            else if (qData.category === '水的功能') catClass += 'cat-water';
            
            catEl.className = catClass;

            qEl.innerText = qData.q;
            optionsEl.innerHTML = '';
            feedbackEl.innerText = '';
            
            modal.style.display = 'flex';

            qData.options.forEach((opt, idx) => {
                const btn = document.createElement('button');
                btn.className = 'option-btn';
                btn.innerText = opt;
                btn.onclick = () => checkAnswer(idx, qData.answer, chest);
                optionsEl.appendChild(btn);
            });
        }

        function checkAnswer(selectedIdx, correctIdx, chest) {
            const feedbackEl = document.getElementById('quiz-feedback');
            const options = document.querySelectorAll('.option-btn');
            options.forEach(btn => btn.disabled = true);

            if (selectedIdx === correctIdx) {
                options[selectedIdx].style.background = '#d4edda';
                options[selectedIdx].style.borderColor = '#28a745';
                feedbackEl.innerHTML = '<span class="correct">✅ 答對了！</span>';
                setTimeout(() => closeQuiz(true, chest), 1000);
            } else {
                options[selectedIdx].style.background = '#f8d7da';
                options[selectedIdx].style.borderColor = '#dc3545';
                feedbackEl.innerHTML = '<span class="wrong">❌ 答錯了！扣除 50 金幣</span>';
                
                // 答錯扣分懲罰
                coinScore = Math.max(0, coinScore - 50);
                updateHUD();

                setTimeout(() => {
                    options.forEach(btn => {
                        btn.disabled = false;
                        btn.style.background = '#f1f1f1';
                        btn.style.borderColor = '#ddd';
                    });
                    feedbackEl.innerText = '';
                }, 1500);
            }
        }

        function closeQuiz(success, chest) {
            document.getElementById('quiz-modal').style.display = 'none';
            gameState = 'PLAYING';
            if (success) {
                chest.opened = true;
                chestScore++;
                createParticles(chest.x, chest.y);
                updateHUD();
            }
        }

        function gameOver(isWin, reason = "") {
            gameState = isWin ? 'WIN' : 'LOSE';
            const goScreen = document.getElementById('game-over');
            const goTitle = document.getElementById('go-title');
            const goMsg = document.getElementById('go-msg');
            
            goScreen.style.display = 'flex';
            document.getElementById('final-coins').innerText = coinScore;
            document.getElementById('final-chests').innerText = chestScore;

            if (isWin) {
                goScreen.style.background = 'rgba(92, 148, 252, 0.95)';
                goTitle.innerText = '🎉 抵達終點！';
                goMsg.innerText = '恭喜你完成了這趟人體探險！';
            } else {
                goScreen.style.background = 'rgba(44, 62, 80, 0.95)';
                goTitle.innerText = '💔 挑戰失敗';
                goMsg.innerText = reason ? reason + ' 休息一下再試一次！' : '沒關係，休息一下再試一次！';
            }
        }

        function gameLoop() {
            update();
            draw();
            requestAnimationFrame(gameLoop);
        }
        
        window.onload = function() {
            resizeCanvas();
        };
    </script>
</body>
</html>
