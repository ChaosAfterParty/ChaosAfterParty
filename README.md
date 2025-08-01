<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub README Grid Layout</title>
    <style>
        body {
            margin: 0;
            padding: 20px;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            background: #0d1117;
            color: white;
        }

        .parent {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            grid-template-rows: repeat(5, 1fr);
            gap: 12px;
            width: 100%;
            max-width: 800px;
            height: 400px;
            margin: 0 auto;
        }

        .grid-item {
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            font-weight: bold;
            position: relative;
            border: 2px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .grid-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
        }

        .grid-item::before {
            content: '';
            position: absolute;
            top: 8px;
            right: 8px;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #f85149;
        }

        .div1 {
            grid-column: span 4 / span 4;
            grid-row: span 2 / span 2;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .div2 {
            grid-column: span 1 / span 1;
            grid-row: span 5 / span 5;
            grid-column-start: 5;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
        }

        .div3 {
            grid-column: span 2 / span 2;
            grid-row: span 3 / span 3;
            grid-row-start: 3;
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
        }

        .div4 {
            grid-column: span 2 / span 2;
            grid-row: span 3 / span 3;
            grid-column-start: 3;
            grid-row-start: 3;
            background: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
            color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 30px;
            font-size: 2.5rem;
            background: linear-gradient(45deg, #667eea, #764ba2, #f093fb, #f5576c);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .description {
            text-align: center;
            margin-bottom: 20px;
            color: #8b949e;
            font-size: 1.1rem;
        }
    </style>
</head>
<body>
    <h1 class="section-title">Project Overview</h1>
    <p class="description">A modern, responsive grid layout for your GitHub README</p>
    
    <div class="parent">
        <div class="grid-item div1">1</div>
        <div class="grid-item div2">2</div>
        <div class="grid-item div3">3</div>
        <div class="grid-item div4">4</div>
    </div>

    <div style="margin-top: 40px; text-align: center; color: #8b949e;">
        <p>✨ Hover over the sections to see the interactive effects ✨</p>
    </div>
</body>
</html>
