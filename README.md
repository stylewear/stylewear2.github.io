<!DOCTYPE html>
<html lang="sq">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Style Wear</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap" rel="stylesheet">

    <!-- Font Awesome për ikona -->
    <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }

        body {
            background-color: #f0f2f5;
            color: #333;
            text-align: center;
        }

        header {
            padding: 60px 20px;
            background: linear-gradient(90deg, #ff8a00, #e52e71);
            color: white;
        }

        header h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
        }

        header p {
            font-size: 1.2rem;
        }

        .section-title {
            margin: 50px 0 20px;
            font-size: 1.8rem;
            font-weight: 600;
            color: #333;
        }

        .cards {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            padding: 0 20px;
        }

        .card {
            background-color: white;
            width: 180px;
            height: 180px;
            border-radius: 20px;
            box-shadow: 0 6px 15px rgba(0,0,0,0.1);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.2);
        }

        .card i {
            font-size: 3rem;
            color: #e52e71;
            margin-bottom: 15px;
        }

        .card h3 {
            font-size: 1.2rem;
            font-weight: 600;
        }

        footer {
            margin-top: 60px;
            padding: 20px;
            background-color: #333;
            color: white;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 2rem;
            }
            .card {
                width: 140px;
                height: 140px;
            }
            .card i {
                font-size: 2.2rem;
            }
            .section-title {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <h1>Mirëserdhët në Style Wear</h1>
        <p>Zgjidhni produktin që dëshironi të eksploroni</p>
    </header>

    <h2 class="section-title">Kategoritë</h2>
    <div class="cards">
        <div class="card">
            <i class="fas fa-male"></i>
            <h3>Meshkuj</h3>
        </div>
        <div class="card">
            <i class="fas fa-female"></i>
            <h3>Femra</h3>
        </div>
        <div class="card">
            <i class="fas fa-child"></i>
            <h3>Fëmijë</h3>
        </div>
    </div>

    <h2 class="section-title">Llojet e Këpucëve</h2>
    <div class="cards">
        <div class="card">
            <i class="fas fa-shoe-prints"></i>
            <h3>Class</h3>
        </div>
        <div class="card">
            <i class="fas fa-running"></i>
            <h3>Sportive</h3>
        </div>
        <div class="card">
            <i class="fas fa-bolt"></i>
            <h3>Running</h3>
        </div>
    </div>

    <footer>
        &copy; 2025 Style Wear. Të gjitha të drejtat e rezervuara.
    </footer>

</body>
</html>
