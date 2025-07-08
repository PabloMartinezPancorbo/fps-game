<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <title>FPS Arena - Mobile Game</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
            -webkit-touch-callout: none;
            -webkit-user-select: none;
            user-select: none;
        }
        
        body {
            font-family: 'Arial', sans-serif;
            background: #000;
            overflow: hidden;
            touch-action: none;
        }
        
        #gameContainer {
            position: relative;
            width: 100vw;
            height: 100vh;
        }
        
        #gameCanvas {
            width: 100%;
            height: 100%;
            display: block;
        }
        
        /* UI Elements */
        #ui {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 100;
        }
        
        #crosshair {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 24px;
            height: 24px;
            pointer-events: none;
        }
        
        #crosshair::before,
        #crosshair::after {
            content: '';
            position: absolute;
            background: rgba(255, 255, 255, 0.8);
            box-shadow: 0 0 3px rgba(0, 0, 0, 0.5);
        }
        
        #crosshair::before {
            width: 2px;
            height: 12px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        
        #crosshair::after {
            width: 12px;
            height: 2px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        
        /* Stats Display */
        #stats {
            position: absolute;
            top: 10px;
            left: 10px;
            right: 10px;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 10px;
            pointer-events: none;
        }
        
        .stat-item {
            background: rgba(0, 0, 0, 0.7);
            padding: 8px 15px;
            border-radius: 20px;
            color: #fff;
            font-size: 14px;
            font-weight: bold;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.8);
            border: 2px solid rgba(255, 255, 255, 0.2);
        }
        
        .stat-item.health {
            border-color: rgba(255, 68, 68, 0.5);
        }
        
        .stat-item.ammo {
            border-color: rgba(68, 168, 255, 0.5);
        }
        
        .stat-item.score {
            border-color: rgba(255, 215, 0, 0.5);
        }
        
        .stat-item.enemies {
            border-color: rgba(255, 100, 100, 0.5);
        }
        
        /* Start Screen */
        #startScreen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(20, 20, 40, 0.95), rgba(40, 20, 20, 0.95));
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #fff;
            z-index: 200;
            text-align: center;
            padding: 20px;
        }
        
        #startScreen h1 {
            font-size: 48px;
            margin-bottom: 20px;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.8);
            letter-spacing: 3px;
        }
        
        #startButton {
            padding: 15px 40px;
            font-size: 20px;
            background: linear-gradient(135deg, #ff4444, #cc0000);
            color: #fff;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            margin-top: 30px;
            font-weight: bold;
            letter-spacing: 1px;
            box-shadow: 0 4px 15px rgba(255, 68, 68, 0.4);
            transition: all 0.3s ease;
        }
        
        #startButton:active {
            transform: scale(0.95);
            box-shadow: 0 2px 8px rgba(255, 68, 68, 0.4);
        }
        
        /* Game Over Screen */
        #gameOverScreen {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: #fff;
            z-index: 200;
            text-align: center;
            padding: 20px;
        }
        
        #gameOverScreen h2 {
            font-size: 36px;
            margin-bottom: 20px;
            color: #ff4444;
        }
        
        #finalScore {
            font-size: 24px;
            margin-bottom: 30px;
        }
        
        /* Mobile Controls */
        .mobile-controls {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 150;
        }
        
        .joystick-container {
            position: absolute;
            width: 120px;
            height: 120px;
            pointer-events: all;
        }
        
        .joystick-container.left {
            bottom: 30px;
            left: 30px;
        }
        
        .joystick-container.right {
            bottom: 30px;
            right: 30px;
        }
        
        .joystick-base {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            border: 3px solid rgba(255, 255, 255, 0.3);
            position: relative;
        }
        
        .joystick-knob {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.6);
            border: 2px solid rgba(255, 255, 255, 0.8);
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            pointer-events: none;
        }
        
        .action-button {
            position: absolute;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            pointer-events: all;
            transition: all 0.1s ease;
        }
        
        .shoot-button {
            bottom: 180px;
            right: 30px;
            width: 80px;
            height: 80px;
            background: rgba(255, 68, 68, 0.7);
            border: 3px solid rgba(255, 68, 68, 0.9);
            color: white;
            font-size: 18px;
        }
        
        .shoot-button:active {
            background: rgba(255, 100, 100, 0.9);
            transform: scale(0.92);
        }
        
        .reload-button {
            bottom: 180px;
            left: 30px;
            width: 60px;
            height: 60px;
            background: rgba(68, 168, 255, 0.7);
            border: 3px solid rgba(68, 168, 255, 0.9);
            color: white;
            font-size: 16px;
        }
        
        .reload-button:active {
            background: rgba(100, 180, 255, 0.9);
            transform: scale(0.92);
        }
        
        /* Hide mobile controls on desktop */
        @media (hover: hover) and (pointer: fine) {
            .mobile-controls {
                display: none;
            }
        }
        
        /* Debug console for mobile */
        #debugConsole {
            position: absolute;
            bottom: 10px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(0, 0, 0, 0.7);
            color: #0f0;
            font-family: monospace;
            font-size: 10px;
            padding: 5px;
            border-radius: 5px;
            pointer-events: none;
            z-index: 300;
            max-width: 90%;
            text-align: center;
        }
    </style>
</head>
<body>
    <div id="gameContainer">
        <canvas id="gameCanvas"></canvas>
        
        <div id="ui">
            <div id="crosshair"></div>
            <div id="stats">
                <div class="stat-item health">❤️ <span id="health">100</span></div>
                <div class="stat-item ammo">🔫 <span id="ammo">30</span>/30</div>
                <div class="stat-item score">⭐ <span id="score">0</span></div>
                <div class="stat-item enemies">👹 <span id="enemies">5</span></div>
            </div>
        </div>
        
        <div id="startScreen">
            <h1>FPS ARENA</h1>
            <p>Survive waves of enemies in the arena!</p>
            <button id="startButton" type="button">START GAME</button>
            <p style="font-size: 14px; margin-top: 20px; opacity: 0.8;">
                Mobile: Use Touch Controls
            </p>
        </div>
        
        <div id="gameOverScreen">
            <h2>GAME OVER</h2>
            <p id="finalScore">Final Score: 0</p>
            <button id="restartButton" type="button" style="padding: 12px 30px; font-size: 18px; background: #ff4444; color: #fff; border: none; border-radius: 25px; cursor: pointer;">
                PLAY AGAIN
            </button>
        </div>
        
        <!-- Mobile Controls -->
        <div class="mobile-controls">
            <div class="joystick-container left" id="moveJoystick">
                <div class="joystick-base">
                    <div class="joystick-knob" id="moveKnob"></div>
                </div>
            </div>
            
            <div class="joystick-container right" id="lookJoystick">
                <div class="joystick-base">
                    <div class="joystick-knob" id="lookKnob"></div>
                </div>
            </div>
            
            <div class="action-button shoot-button" id="shootButton">FIRE</div>
            <div class="action-button reload-button" id="reloadButton">R</div>
        </div>
        
        <div id="debugConsole"></div>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script>
        // Debug helper
        const debug = (msg) => {
            console.log(msg);
            const debugDiv = document.getElementById('debugConsole');
            if (debugDiv) {
                debugDiv.textContent = msg;
                setTimeout(() => debugDiv.textContent = '', 3000);
            }
        };

        class FPSGame {
            constructor() {
                this.canvas = document.getElementById('gameCanvas');
                this.scene = new THREE.Scene();
                this.camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
                this.renderer = new THREE.WebGLRenderer({ 
                    canvas: this.canvas,
                    antialias: true,
                    alpha: false
                });
                this.clock = new THREE.Clock();
                
                this.gameState = {
                    health: 100,
                    ammo: 30,
                    maxAmmo: 30,
                    score: 0,
                    isPlaying: false,
                    isReloading: false,
                    reloadTime: 2,
                    reloadProgress: 0,
                    wave: 1,
                    enemiesPerWave: 5
                };
                
                this.movement = {
                    forward: false,
                    backward: false,
                    left: false,
                    right: false,
                    speed: 10  // Increased from 5 to 10 for better mobile movement
                };
                
                this.mouse = {
                    x: 0,
                    y: 0,
                    sensitivity: 0.001,
                    mobileSensitivity: 0.02
                };
                
                this.enemies = [];
                this.bullets = [];
                this.particles = [];
                
                // Mobile controls
                this.mobileControls = {
                    moveJoystick: { active: false, x: 0, y: 0 },
                    lookJoystick: { active: false, x: 0, y: 0 },
                    isMobile: true // Force mobile mode
                };
                
                // Player collision
                this.playerRadius = 0.5;
                this.playerHeight = 1.8;
                
                this.reloadInterval = null;
                
                this.init();
            }
            
            init() {
                debug('Initializing game...');
                
                // Setup renderer
                this.renderer.setSize(window.innerWidth, window.innerHeight);
                this.renderer.shadowMap.enabled = true;
                this.renderer.shadowMap.type = THREE.PCFSoftShadowMap;
                this.renderer.setClearColor(0x87CEEB);
                this.renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
                
                // Setup camera
                this.camera.position.set(0, this.playerHeight, 0);
                
                // Create world
                this.createWorld();
                
                // Setup controls
                this.setupControls();
                this.setupMobileControls();
                
                // Window resize handler
                window.addEventListener('resize', () => this.onWindowResize());
                
                // Start button
                document.getElementById('startButton').addEventListener('click', () => this.startGame());
                document.getElementById('restartButton').addEventListener('click', () => this.restartGame());
                
                // Prevent context menu on right click
                this.canvas.addEventListener('contextmenu', (e) => e.preventDefault());
                
                // Start render loop
                this.animate();
                
                debug('Game initialized!');
            }
            
            createWorld() {
                // Ground
                const groundGeometry = new THREE.PlaneGeometry(100, 100);
                const groundMaterial = new THREE.MeshLambertMaterial({ 
                    color: 0x4a4a4a
                });
                const ground = new THREE.Mesh(groundGeometry, groundMaterial);
                ground.rotation.x = -Math.PI / 2;
                ground.receiveShadow = true;
                this.scene.add(ground);
                
                // Walls
                this.createWalls();
                
                // Lighting
                const ambientLight = new THREE.AmbientLight(0x404040, 0.5);
                this.scene.add(ambientLight);
                
                const directionalLight = new THREE.DirectionalLight(0xffffff, 0.8);
                directionalLight.position.set(10, 20, 5);
                directionalLight.castShadow = true;
                directionalLight.shadow.camera.left = -50;
                directionalLight.shadow.camera.right = 50;
                directionalLight.shadow.camera.top = 50;
                directionalLight.shadow.camera.bottom = -50;
                directionalLight.shadow.mapSize.width = 2048;
                directionalLight.shadow.mapSize.height = 2048;
                this.scene.add(directionalLight);
                
                // Fog for atmosphere
                this.scene.fog = new THREE.Fog(0x87CEEB, 10, 100);
            }
            
            createWalls() {
                const wallMaterial = new THREE.MeshLambertMaterial({ color: 0x8B4513 });
                
                // Outer walls
                const walls = [
                    { pos: [0, 5, -50], size: [100, 10, 2] },
                    { pos: [0, 5, 50], size: [100, 10, 2] },
                    { pos: [-50, 5, 0], size: [2, 10, 100] },
                    { pos: [50, 5, 0], size: [2, 10, 100] }
                ];
                
                walls.forEach(wall => {
                    const geometry = new THREE.BoxGeometry(...wall.size);
                    const mesh = new THREE.Mesh(geometry, wallMaterial);
                    mesh.position.set(...wall.pos);
                    mesh.castShadow = true;
                    mesh.receiveShadow = true;
                    mesh.userData.isWall = true;
                    this.scene.add(mesh);
                });
                
                // Cover objects
                const coverMaterial = new THREE.MeshLambertMaterial({ color: 0x654321 });
                const coverPositions = [
                    [-20, 1.5, -20], [20, 1.5, -20], [-20, 1.5, 20], [20, 1.5, 20],
                    [0, 1.5, 0], [-30, 1.5, 0], [30, 1.5, 0], [0, 1.5, -30], [0, 1.5, 30]
                ];
                
                coverPositions.forEach(pos => {
                    const geometry = new THREE.BoxGeometry(3, 3, 3);
                    const box = new THREE.Mesh(geometry, coverMaterial);
                    box.position.set(...pos);
                    box.castShadow = true;
                    box.receiveShadow = true;
                    box.userData.isCover = true;
                    this.scene.add(box);
                });
            }
            
            spawnEnemy() {
                const enemy = new THREE.Group();
                
                // Body
                const bodyGeometry = new THREE.CylinderGeometry(0.3, 0.4, 1.2, 8);
                const bodyMaterial = new THREE.MeshLambertMaterial({ color: 0x2a2a2a });
                const body = new THREE.Mesh(bodyGeometry, bodyMaterial);
                body.position.y = 0.6;
                enemy.add(body);
                
                // Head
                const headGeometry = new THREE.SphereGeometry(0.3, 8, 8);
                const headMaterial = new THREE.MeshLambertMaterial({ color: 0xffdbac });
                const head = new THREE.Mesh(headGeometry, headMaterial);
                head.position.y = 1.5;
                enemy.add(head);
                
                // Helmet
                const helmetGeometry = new THREE.SphereGeometry(0.35, 8, 8);
                const helmetMaterial = new THREE.MeshLambertMaterial({ color: 0x1a1a1a });
                const helmet = new THREE.Mesh(helmetGeometry, helmetMaterial);
                helmet.position.y = 1.6;
                helmet.scale.y = 0.7;
                enemy.add(helmet);
                
                // Arms
                const armGeometry = new THREE.CylinderGeometry(0.1, 0.1, 0.8, 8);
                const armMaterial = new THREE.MeshLambertMaterial({ color: 0x2a2a2a });
                
                const leftArm = new THREE.Mesh(armGeometry, armMaterial);
                leftArm.position.set(-0.4, 0.8, 0);
                leftArm.rotation.z = Math.PI / 6;
                enemy.add(leftArm);
                
                const rightArm = new THREE.Mesh(armGeometry, armMaterial);
                rightArm.position.set(0.4, 0.8, 0);
                rightArm.rotation.z = -Math.PI / 6;
                enemy.add(rightArm);

                
                // Gun
                const gunGroup = new THREE.Group();
                
                const gunBodyGeometry = new THREE.BoxGeometry(0.1, 0.1, 0.6);
                const gunMaterial = new THREE.MeshLambertMaterial({ color: 0x0a0a0a });
                const gunBody = new THREE.Mesh(gunBodyGeometry, gunMaterial);
                gunBody.position.z = -0.3;
                gunGroup.add(gunBody);
                
                const gunBarrelGeometry = new THREE.CylinderGeometry(0.05, 0.05, 0.3, 8);
                const gunBarrel = new THREE.Mesh(gunBarrelGeometry, gunMaterial);
                gunBarrel.rotation.x = Math.PI / 2;
                gunBarrel.position.z = -0.7;
                gunGroup.add(gunBarrel);
                
                gunGroup.position.set(0.3, 0.7, -0.2);
                enemy.add(gunGroup);
                
                // Legs
                const legGeometry = new THREE.CylinderGeometry(0.15, 0.15, 0.8, 8);
                const legMaterial = new THREE.MeshLambertMaterial({ color: 0x1a1a1a });
                
                const leftLeg = new THREE.Mesh(legGeometry, legMaterial);
                leftLeg.position.set(-0.2, -0.4, 0);
                enemy.add(leftLeg);
                
                const rightLeg = new THREE.Mesh(legGeometry, legMaterial);
                rightLeg.position.set(0.2, -0.4, 0);
                enemy.add(rightLeg);
                
                // Position enemy at spawn point
                const side = Math.floor(Math.random() * 4);
                let x, z;
                switch(side) {
                    case 0: x = (Math.random() - 0.5) * 80; z = -45; break;
                    case 1: x = (Math.random() - 0.5) * 80; z = 45; break;
                    case 2: x = -45; z = (Math.random() - 0.5) * 80; break;
                    case 3: x = 45; z = (Math.random() - 0.5) * 80; break;
                }
                
                enemy.position.set(x, 0.8, z);
                
                enemy.userData = {
                    health: 100,
                    maxHealth: 100,
                    speed: 2 + (this.gameState.wave * 0.2),
                    damage: 10,
                    lastShot: 0,
                    shootCooldown: 2000,
                    type: 'enemy',
                    gunGroup: gunGroup
                };
                
                // Enable shadows for all parts
                enemy.traverse((child) => {
                    if (child instanceof THREE.Mesh) {
                        child.castShadow = true;
                        child.receiveShadow = true;
                    }
                });
                
                this.scene.add(enemy);
                this.enemies.push(enemy);
                this.updateEnemyCount();
            }
            
            setupControls() {
                // Keyboard controls for desktop testing
                document.addEventListener('keydown', (e) => {
                    if (!this.gameState.isPlaying) return;
                    
                    switch(e.code) {
                        case 'KeyW': case 'ArrowUp': this.movement.forward = true; break;
                        case 'KeyS': case 'ArrowDown': this.movement.backward = true; break;
                        case 'KeyA': case 'ArrowLeft': this.movement.left = true; break;
                        case 'KeyD': case 'ArrowRight': this.movement.right = true; break;
                        case 'KeyR': this.reload(); break;
                        case 'Space': this.shoot(); break;
                    }
                });
                
                document.addEventListener('keyup', (e) => {
                    switch(e.code) {
                        case 'KeyW': case 'ArrowUp': this.movement.forward = false; break;
                        case 'KeyS': case 'ArrowDown': this.movement.backward = false; break;
                        case 'KeyA': case 'ArrowLeft': this.movement.left = false; break;
                        case 'KeyD': case 'ArrowRight': this.movement.right = false; break;
                    }
                });
            }
            
            setupJoystick(containerId, knobId, onMove, onEnd) {
                const container = document.getElementById(containerId);
                const knob = document.getElementById(knobId);
                let active = false;
                let centerX = 0, centerY = 0;
                
                const getTouch = (e) => {
                    if (e.touches && e.touches.length > 0) {
                        return e.touches[0];
                    } else if (e.changedTouches && e.changedTouches.length > 0) {
                        return e.changedTouches[0];
                    }
                    return e;
                };
                
                const handleStart = (e) => {
                    e.preventDefault();
                    e.stopPropagation();
                    
                    const rect = container.getBoundingClientRect();
                    centerX = rect.left + rect.width / 2;
                    centerY = rect.top + rect.height / 2;
                    
                    active = true;
                    handleMove(e);
                };
                
                const handleMove = (e) => {
                    if (!active) return;
                    e.preventDefault();
                    
                    const touch = getTouch(e);
                    const dx = touch.clientX - centerX;
                    const dy = touch.clientY - centerY;
                    
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    const maxDistance = 40;
                    
                    let normalizedX = dx / maxDistance;
                    let normalizedY = dy / maxDistance;
                    
                    if (distance > maxDistance) {
                        normalizedX = (dx / distance) * 1;
                        normalizedY = (dy / distance) * 1;
                    }
                    
                    const knobX = normalizedX * maxDistance;
                    const knobY = normalizedY * maxDistance;
                    
                    knob.style.transform = `translate(calc(-50% + ${knobX}px), calc(-50% + ${knobY}px))`;
                    
                    onMove(normalizedX, normalizedY);
                };
                
                const handleEnd = (e) => {
                    if (!active) return;
                    e.preventDefault();
                    
                    active = false;
                    knob.style.transform = 'translate(-50%, -50%)';
                    onEnd();
                };
                
                // Touch events
                container.addEventListener('touchstart', handleStart, { passive: false });
                window.addEventListener('touchmove', handleMove, { passive: false });
                window.addEventListener('touchend', handleEnd, { passive: false });
                window.addEventListener('touchcancel', handleEnd, { passive: false });
                
                // Mouse events for testing
                container.addEventListener('mousedown', handleStart);
                window.addEventListener('mousemove', handleMove);
                window.addEventListener('mouseup', handleEnd);
            }
            
            setupMobileControls() {
                debug('Setting up mobile controls');
                
                // Movement joystick
                this.setupJoystick('moveJoystick', 'moveKnob', (x, y) => {
                    this.mobileControls.moveJoystick = { active: true, x, y };
                    debug(`Move: ${x.toFixed(2)}, ${y.toFixed(2)}`);
                }, () => {
                    this.mobileControls.moveJoystick = { active: false, x: 0, y: 0 };
                });
                
                // Look joystick
                this.setupJoystick('lookJoystick', 'lookKnob', (x, y) => {
                    this.mobileControls.lookJoystick = { active: true, x, y };
                }, () => {
                    this.mobileControls.lookJoystick = { active: false, x: 0, y: 0 };
                });
                
                // Shoot button
                const shootButton = document.getElementById('shootButton');
                const shootHandler = (e) => {
                    e.preventDefault();
                    e.stopPropagation();
                    debug('Fire button pressed!');
                    if (this.gameState.isPlaying) {
                        this.shoot();
                    }
                };
                
                shootButton.addEventListener('touchstart', shootHandler, { passive: false });
                shootButton.addEventListener('mousedown', shootHandler);
                shootButton.addEventListener('click', shootHandler);
                
                // Reload button
                const reloadButton = document.getElementById('reloadButton');
                const reloadHandler = (e) => {
                    e.preventDefault();
                    e.stopPropagation();
                    debug('Reload button pressed!');
                    if (this.gameState.isPlaying) {
                        this.reload();
                    }
                };
                
                reloadButton.addEventListener('touchstart', reloadHandler, { passive: false });
                reloadButton.addEventListener('mousedown', reloadHandler);
                reloadButton.addEventListener('click', reloadHandler);
            }
            
            startGame() {
                debug('Starting game...');
                document.getElementById('startScreen').style.display = 'none';
                this.gameState.isPlaying = true;
                
                // Reset game state
                this.gameState.health = 100;
                this.gameState.ammo = 30;
                this.gameState.score = 0;
                this.gameState.wave = 1;
                this.gameState.isReloading = false;
                
                // Reset mouse position
                this.mouse.x = 0;
                this.mouse.y = 0;
                
                // Reset camera position to spawn point
                this.camera.position.set(0, this.playerHeight, 0);
                
                // Clear existing enemies
                this.enemies.forEach(enemy => this.scene.remove(enemy));
                this.enemies = [];
                
                // Clear existing bullets
                this.bullets.forEach(bullet => this.scene.remove(bullet));
                this.bullets = [];
                
                // Spawn initial enemies
                for (let i = 0; i < this.gameState.enemiesPerWave; i++) {
                    setTimeout(() => this.spawnEnemy(), i * 500);
                }
                
                this.updateUI();
                debug('Game started! Use left joystick to move!');
            }
            
            restartGame() {
                document.getElementById('gameOverScreen').style.display = 'none';
                this.startGame();
            }
            
            gameOver() {
                if (!this.gameState.isPlaying) return;
                
                debug('Game Over!');
                this.gameState.isPlaying = false;
                
                // Stop all intervals
                if (this.reloadInterval) {
                    clearInterval(this.reloadInterval);
                    this.reloadInterval = null;
                }
                
                // Clear all enemies and bullets
                this.enemies.forEach(enemy => this.scene.remove(enemy));
                this.enemies = [];
                this.bullets.forEach(bullet => this.scene.remove(bullet));
                this.bullets = [];
                this.particles.forEach(particle => this.scene.remove(particle));
                this.particles = [];
                
                // Show game over screen
                document.getElementById('finalScore').textContent = `Final Score: ${this.gameState.score}`;
                document.getElementById('gameOverScreen').style.display = 'flex';
            }
            
            shoot() {
                if (!this.gameState.isPlaying || this.gameState.ammo <= 0 || this.gameState.isReloading) {
                    return;
                }
                
                debug('BANG!');
                this.gameState.ammo--;
                this.updateUI();
                
                // Create bullet
                const bulletGeometry = new THREE.SphereGeometry(0.1, 8, 8);
                const bulletMaterial = new THREE.MeshBasicMaterial({ 
                    color: 0xffff00,
                    emissive: 0xffff00,
                    emissiveIntensity: 1
                });
                const bullet = new THREE.Mesh(bulletGeometry, bulletMaterial);
                
                // Set bullet position at camera
                bullet.position.copy(this.camera.position);
                
                // Calculate direction
                const direction = new THREE.Vector3(0, 0, -1);
                direction.applyQuaternion(this.camera.quaternion);
                
                bullet.userData = {
                    velocity: direction.multiplyScalar(50),
                    damage: 50,
                    isPlayerBullet: true
                };
                
                this.scene.add(bullet);
                this.bullets.push(bullet);
                
                // Muzzle flash effect
                this.createMuzzleFlash();
            }
            
            reload() {
                if (this.gameState.isReloading || this.gameState.ammo === this.gameState.maxAmmo) return;
                
                debug('Reloading...');
                this.gameState.isReloading = true;
                this.gameState.reloadProgress = 0;
                
                this.reloadInterval = setInterval(() => {
                    this.gameState.reloadProgress += 0.05;
                    this.updateUI();
                    
                    if (this.gameState.reloadProgress >= 1) {
                        this.gameState.ammo = this.gameState.maxAmmo;
                        this.gameState.isReloading = false;
                        this.gameState.reloadProgress = 0;
                        clearInterval(this.reloadInterval);
                        this.reloadInterval = null;
                        this.updateUI();
                        debug('Reload complete!');
                    }
                }, 100);
            }
            
            createMuzzleFlash() {
                const flash = new THREE.PointLight(0xffff00, 2, 5);
                flash.position.copy(this.camera.position);
                this.scene.add(flash);
                
                setTimeout(() => this.scene.remove(flash), 100);
            }
            
            createParticles(position, color, count = 10) {
                for (let i = 0; i < count; i++) {
                    const geometry = new THREE.SphereGeometry(0.1, 4, 4);
                    const material = new THREE.MeshBasicMaterial({ color });
                    const particle = new THREE.Mesh(geometry, material);
                    
                    particle.position.copy(position);
                    
                    particle.userData = {
                        velocity: new THREE.Vector3(
                            (Math.random() - 0.5) * 10,
                            Math.random() * 10,
                            (Math.random() - 0.5) * 10
                        ),
                        lifetime: 1
                    };
                    
                    this.scene.add(particle);
                    this.particles.push(particle);
                }
            }
            
            updatePlayer(delta) {
                const moveSpeed = this.movement.speed * delta;
                
                // Handle movement
                let moveX = 0, moveZ = 0;
                
                // Mobile controls - use joystick input directly
                if (this.mobileControls.moveJoystick.active) {
                    moveX = this.mobileControls.moveJoystick.x * moveSpeed;
                    moveZ = -this.mobileControls.moveJoystick.y * moveSpeed;
                }
                
                if (this.mobileControls.lookJoystick.active) {
                    // Inverted controls - move right to look right, left to look left
                    this.mouse.x += this.mobileControls.lookJoystick.x * this.mouse.mobileSensitivity;
                    // Down on joystick = look down (positive y)
                    this.mouse.y += this.mobileControls.lookJoystick.y * this.mouse.mobileSensitivity;
                    this.mouse.y = Math.max(-Math.PI/2, Math.min(Math.PI/2, this.mouse.y));
                }
                
                // Apply rotation
                this.camera.rotation.order = 'YXZ';
                this.camera.rotation.y = this.mouse.x;
                this.camera.rotation.x = this.mouse.y;
                
                // Calculate movement direction based on camera orientation
                const forward = new THREE.Vector3(0, 0, -1);
                const right = new THREE.Vector3(1, 0, 0);
                
                // Apply camera Y rotation only for movement
                const yQuaternion = new THREE.Quaternion();
                yQuaternion.setFromAxisAngle(new THREE.Vector3(0, 1, 0), this.mouse.x);
                
                forward.applyQuaternion(yQuaternion);
                right.applyQuaternion(yQuaternion);
                
                // New position calculation
                const newPosition = new THREE.Vector3();
                newPosition.copy(this.camera.position);
                newPosition.add(forward.multiplyScalar(moveZ));
                newPosition.add(right.multiplyScalar(moveX));
                
                // Keep player on ground level
                newPosition.y = this.playerHeight;
                
                // Check collision and update position
                if (this.checkPlayerCollision(newPosition)) {
                    this.camera.position.copy(newPosition);
                    
                    // Debug movement
                    if (Math.abs(moveX) > 0.01 || Math.abs(moveZ) > 0.01) {
                        debug(`Moving! Speed: ${moveSpeed.toFixed(2)}`);
                    }
                }
            }
            
            checkPlayerCollision(position) {
                // Check boundaries
                if (Math.abs(position.x) > 48 || Math.abs(position.z) > 48) {
                    return false;
                }
                
                // Check collision with cover objects
                const objects = this.scene.children.filter(child => 
                    child.userData.isCover || child.userData.isWall
                );
                
                for (let obj of objects) {
                    const box = new THREE.Box3().setFromObject(obj);
                    const playerBox = new THREE.Box3().setFromCenterAndSize(
                        position,
                        new THREE.Vector3(this.playerRadius * 2, this.playerHeight, this.playerRadius * 2)
                    );
                    
                    if (box.intersectsBox(playerBox)) {
                        return false;
                    }
                }
                
                return true;
            }

            updateEnemies(delta) {
                const currentTime = Date.now();
                
                this.enemies.forEach((enemy, index) => {
                    if (enemy.userData.health <= 0) {
                        this.scene.remove(enemy);
                        this.enemies.splice(index, 1);
                        this.gameState.score += 100;
                        this.createParticles(enemy.position, 0x2a2a2a, 20);
                        this.updateUI();
                        this.updateEnemyCount();
                        return;
                    }
                    
                    // Move towards player
                    const direction = new THREE.Vector3();
                    direction.subVectors(this.camera.position, enemy.position);
                    direction.y = 0;
                    const distance = direction.length();
                    direction.normalize();
                    
                    // Face player (rotate entire group)
                    const lookAtPos = new THREE.Vector3(
                        this.camera.position.x,
                        enemy.position.y,
                        this.camera.position.z
                    );
                    enemy.lookAt(lookAtPos);
                    
                    // Add slight animation to make enemies feel more alive
                    enemy.position.y = 0.8 + Math.sin(Date.now() * 0.002 + index) * 0.05;
                    
                    // Move if not too close
                    if (distance > 3) {
                        enemy.position.add(direction.multiplyScalar(enemy.userData.speed * delta));
                    }
                    
                    // Shoot at player
                    if (distance < 20 && currentTime - enemy.userData.lastShot > enemy.userData.shootCooldown) {
                        this.enemyShoot(enemy);
                        enemy.userData.lastShot = currentTime;
                    }
                });
                
                // Check if wave complete
                if (this.enemies.length === 0 && this.gameState.isPlaying) {
                    this.nextWave();
                }
            }
            
            enemyShoot(enemy) {
                const bulletGeometry = new THREE.SphereGeometry(0.1, 8, 8);
                const bulletMaterial = new THREE.MeshBasicMaterial({ 
                    color: 0xff0000,
                    emissive: 0xff0000
                });
                const bullet = new THREE.Mesh(bulletGeometry, bulletMaterial);
                
                bullet.position.copy(enemy.position);
                bullet.position.y += 1.2;
                
                // Position bullet at gun tip
                const gunWorldPos = new THREE.Vector3();
                enemy.userData.gunGroup.getWorldPosition(gunWorldPos);
                bullet.position.copy(gunWorldPos);
                bullet.position.z -= 0.5;
                
                const direction = new THREE.Vector3();
                direction.subVectors(this.camera.position, bullet.position);
                direction.normalize();
                
                bullet.userData = {
                    velocity: direction.multiplyScalar(20),
                    damage: enemy.userData.damage,
                    isPlayerBullet: false
                };
                
                this.scene.add(bullet);
                this.bullets.push(bullet);
            }
            
            updateBullets(delta) {
                this.bullets.forEach((bullet, index) => {
                    // Update position
                    bullet.position.add(bullet.userData.velocity.clone().multiplyScalar(delta));
                    
                    // Check boundaries
                    if (Math.abs(bullet.position.x) > 50 || 
                        Math.abs(bullet.position.z) > 50 || 
                        bullet.position.y < 0 || 
                        bullet.position.y > 10) {
                        this.scene.remove(bullet);
                        this.bullets.splice(index, 1);
                        return;
                    }
                    
                    // Check collisions
                    if (bullet.userData.isPlayerBullet) {
                        // Check enemy hits
                        this.enemies.forEach(enemy => {
                            // Check collision with enemy body
                            const distance = bullet.position.distanceTo(enemy.position);
                            if (distance < 1.5) {
                                enemy.userData.health -= bullet.userData.damage;
                                this.createParticles(bullet.position, 0xff0000, 5);
                                
                                // Hit reaction - tilt enemy back slightly
                                enemy.rotation.x = 0.1;
                                setTimeout(() => enemy.rotation.x = 0, 100);
                                
                                this.scene.remove(bullet);
                                this.bullets.splice(index, 1);
                            }
                        });
                    } else {
                        // Check player hit
                        const distance = bullet.position.distanceTo(this.camera.position);
                        if (distance < 1) {
                            this.takeDamage(bullet.userData.damage);
                            this.createParticles(bullet.position, 0xff0000, 5);
                            this.scene.remove(bullet);
                            this.bullets.splice(index, 1);
                        }
                    }
                });
            }
            
            updateParticles(delta) {
                this.particles.forEach((particle, index) => {
                    particle.userData.velocity.y -= 10 * delta; // Gravity
                    particle.position.add(particle.userData.velocity.clone().multiplyScalar(delta));
                    particle.userData.lifetime -= delta;
                    
                    if (particle.userData.lifetime <= 0 || particle.position.y < 0) {
                        this.scene.remove(particle);
                        this.particles.splice(index, 1);
                    }
                });
            }
            
            takeDamage(damage) {
                if (!this.gameState.isPlaying) return;
                
                this.gameState.health -= damage;
                this.gameState.health = Math.max(0, this.gameState.health);
                this.updateUI();
                
                // Red flash effect
                const flash = document.createElement('div');
                flash.style.position = 'absolute';
                flash.style.top = '0';
                flash.style.left = '0';
                flash.style.width = '100%';
                flash.style.height = '100%';
                flash.style.background = 'rgba(255, 0, 0, 0.3)';
                flash.style.pointerEvents = 'none';
                flash.style.zIndex = '90';
                document.getElementById('gameContainer').appendChild(flash);
                
                setTimeout(() => {
                    if (flash && flash.parentNode) {
                        flash.remove();
                    }
                }, 100);
                
                if (this.gameState.health <= 0) {
                    debug('Player died!');
                    this.gameOver();
                }
            }

            nextWave() {
                this.gameState.wave++;
                this.gameState.score += 500 * this.gameState.wave;
                
                // Show wave message
                const waveMsg = document.createElement('div');
                waveMsg.style.position = 'absolute';
                waveMsg.style.top = '50%';
                waveMsg.style.left = '50%';
                waveMsg.style.transform = 'translate(-50%, -50%)';
                waveMsg.style.color = '#fff';
                waveMsg.style.fontSize = '48px';
                waveMsg.style.fontWeight = 'bold';
                waveMsg.style.textShadow = '3px 3px 6px rgba(0,0,0,0.8)';
                waveMsg.style.pointerEvents = 'none';
                waveMsg.style.zIndex = '110';
                waveMsg.textContent = `WAVE ${this.gameState.wave}`;
                document.getElementById('gameContainer').appendChild(waveMsg);
                
                setTimeout(() => waveMsg.remove(), 2000);
                
                // Spawn new enemies
                const enemyCount = this.gameState.enemiesPerWave + this.gameState.wave * 2;
                for (let i = 0; i < enemyCount; i++) {
                    setTimeout(() => this.spawnEnemy(), i * 300);
                }
                
                // Health bonus
                this.gameState.health = Math.min(100, this.gameState.health + 20);
                this.updateUI();
            }
            
            updateUI() {
                document.getElementById('health').textContent = Math.max(0, this.gameState.health);
                document.getElementById('ammo').textContent = this.gameState.ammo;
                document.getElementById('score').textContent = this.gameState.score;
                
                // Update reload button
                const reloadButton = document.getElementById('reloadButton');
                if (this.gameState.isReloading) {
                    reloadButton.textContent = Math.floor(this.gameState.reloadProgress * 100) + '%';
                } else {
                    reloadButton.textContent = 'R';
                }
            }
            
            updateEnemyCount() {
                document.getElementById('enemies').textContent = this.enemies.length;
            }
            
            onWindowResize() {
                this.camera.aspect = window.innerWidth / window.innerHeight;
                this.camera.updateProjectionMatrix();
                this.renderer.setSize(window.innerWidth, window.innerHeight);
            }
            
            animate() {
                requestAnimationFrame(() => this.animate());
                
                const delta = this.clock.getDelta();
                
                if (this.gameState.isPlaying) {
                    this.updatePlayer(delta);
                    this.updateEnemies(delta);
                    this.updateBullets(delta);
                    this.updateParticles(delta);
                }
                
                this.renderer.render(this.scene, this.camera);
            }
        }
        
        // Start game when page loads
        window.addEventListener('load', () => {
            try {
                const game = new FPSGame();
                debug('Game loaded successfully!');
            } catch (error) {
                console.error('Failed to initialize game:', error);
                alert('Failed to start game. Please refresh the page.');
            }
        });
        
        // Prevent scrolling on mobile
        document.addEventListener('touchmove', (e) => {
            if (e.target.closest('.mobile-controls')) {
                e.preventDefault();
            }
        }, { passive: false });
        
        // Prevent double-tap zoom
        let lastTouchEnd = 0;
        document.addEventListener('touchend', (e) => {
            const now = Date.now();
            if (now - lastTouchEnd <= 300) {
                e.preventDefault();
            }
            lastTouchEnd = now;
        }, false);
    </script>
</body>
</html>
