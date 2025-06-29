
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crowd Detection Project README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f4;
            color: #333;
        }
        h1, h2, h3 {
            color: #222;
            margin-top: 1em;
        }
        pre {
            background-color: #e8e8e8;
            padding: 10px;
            overflow-x: auto;
            border-radius: 5px;
        }
        code {
            background-color: #eaeaea;
            padding: 2px 4px;
            border-radius: 4px;
        }
        ul {
            padding-left: 20px;
        }
        .box {
            background-color: #fff;
            border: 1px solid #ddd;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            border-radius: 5px;
        }
    </style>
</head>
<body>
    <div class="box">
        <h1>🎯 Crowd Detection Project</h1>
        <p><strong>Описание проекта:</strong> Этот проект представляет собой систему, способную распознавать людей в толпе на видеопотоках или из видеофайлов, используя модель YOLOv8. Проект может быть расширен для анализа плотности толпы и отслеживания движений.</p>
    </div>

    <div class="box">
        <h2>📋 Функционал</h2>
        <ul>
            <li>Обнаружение людей в реальном времени на видео.</li>
            <li>Поддержка различных источников видео (<em>веб-камера</em>, <em>видеофайлы</em>).</li>
            <li>Визуализация ограничивающих рамок вокруг обнаруженных людей.</li>
        </ul>
    </div>

    <div class="box">
        <h2>🚀 Требования</h2>
        <p>Проект требует Python версии 3.8+. Вы также можете установить следующие Python-библиотеки:</p>
        <ul>
            <li><code>opencv-python</code></li>
            <li><code>ultralytics</code></li>
        </ul>
    </div>

    <div class="box">
        <h2>⚙️ Установка</h2>
        <ol>
            <li>
                <p><strong>Клонируйте репозиторий:</strong></p>
                <pre><code>git clone https://github.com/YourUsername/crowd-detection.git
cd crowd-detection</code></pre>
            </li>
            <li>
                <p><strong>Создайте виртуальное окружение (рекомендуется):</strong></p>
                <pre><code>python -m venv venv
source venv/bin/activate  # Для Linux/macOS
# venv\Scripts\activate   # Для Windows</code></pre>
            </li>
            <li>
                <p><strong>Установите зависимости:</strong></p>
                <pre><code>pip install -r requirements.txt</code></pre>
            </li>
            <li>
                <p><strong>Скачайте модель YOLOv8:</strong> Загрузите заранее подготовленную модель <code>yolov8m.pt</code>:</p>
                <p><a href="https://github.com/ultralytics/assets/releases/download/v8.1.0/yolov8m.pt" target="_blank">📥 Скачать yolov8m</a> и разместите модель в корневом каталоге проекта.</p>
            </li>
        </ol>
    </div>

    <div class="box">
        <h2>💻 Использование</h2>
        <h3>Запуск с веб-камеры</h3>
        <pre><code>python detect.py --source 0</code></pre>
        <p>(Где <code>0</code> – индекс вашей веб-камеры.)</p>

        <h3>Запуск с видеофайла</h3>
        <pre><code>python detect.py --source path/to/your/video.mp4</code></pre>
        <p>Замените <code>path/to/your/video.mp4</code> на путь к вашему видеофайлу.</p>

        <h3>Настройка параметров обнаружения</h3>
        <pre><code>python detect.py --source path/to/video.mp4 --conf 0.25 --iou 0.45</code></pre>
        <ul>
            <li><code>--conf</code>: Порог уверенности (по умолчанию 0.25).</li>
            <li><code>--iou</code>: Порог IoU для подавления пересечений (по умолчанию 0.7).</li>
        </ul>
    </div>

    <div class="box">
        <h2>📂 Структура проекта</h2>
        <pre><code>.
├── .gitignore
├── README.md
├── requirements.txt
├── detect.py
├── yolov8m.pt  # YOLOv8 model
</code></pre>
        <ul>
            <li><code>detect.py</code>: Основной скрипт для обнаружения.</li>
            <li><code>requirements.txt</code>: Список зависимостей.</li>
            <li><code>yolov8m.pt</code>: Файл модели YOLOv8.</li>
        </ul>
    </div>

    <div class="box">
        <h2>📜 Лицензия</h2>
        <p>Этот проект распространяется под лицензией MIT. Подробнее смотрите в файле <code>LICENSE</code>.</p>
    </div>
</body>
</html>
