<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Three.js WebGL Canvas</title>
    <style>
        canvas {
            cursor: grab;
            touch-action: none;
            user-select: none;
        }
    </style>
</head>
<body>
    <canvas id="webglCanvas" width="389" height="563"></canvas>

    <!-- Подключаем three.js -->
 <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r153/three.min.js"></script>

<script>
        const canvas = document.getElementById("webglCanvas");

        // Отключаем контекстное меню
        canvas.oncontextmenu = function (e) {
            e.preventDefault();
        };

        // Инициализируем три.js сцену
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, canvas.width / canvas.height, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ canvas: canvas });
        
        renderer.setSize(canvas.width, canvas.height);
        camera.position.z = 5;

        // Пример добавления куба в сцену
        const geometry = new THREE.BoxGeometry();
        const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
        const cube = new THREE.Mesh(geometry, material);
        scene.add(cube);

        // Анимация
        function animate() {
            requestAnimationFrame(animate);
            cube.rotation.x += 0.01;
            cube.rotation.y += 0.01;
            renderer.render(scene, camera);
        }
        
        animate();
    </script>
</body>
</html>
