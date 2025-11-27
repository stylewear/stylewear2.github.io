<!DOCTYPE html>
<html lang="sq">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>style.wear.2 - Këpucë & Çanta</title>
<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f5f5f5;
}

/* Header */
header {
    background-color: #ff6f61;
    color: white;
    text-align: center;
    padding: 20px;
}
header h1 { margin: 0; font-size: 2em; }
nav { margin-top: 10px; }
nav a { color: white; text-decoration: none; margin: 0 15px; font-weight: bold; }

/* Produktet */
.products {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px;
}
.product {
    position: relative;
    width: 250px;
    margin: 15px;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    background-color: white;
    cursor: pointer;
}
.product img { width: 100%; display: block; }
.product .info {
    position: absolute;
    bottom: 0;
    width: 100%;
    background: rgba(0,0,0,0.7);
    color: white;
    padding: 15px;
    text-align: center;
}
.product .info h2 { margin: 0 0 5px 0; font-size: 1.1em; }
.product .info p { margin: 0 0 10px 0; font-weight: bold; }
.product .info button {
    background-color: #ff6f61;
    border: none;
    padding: 8px 15px;
    border-radius: 5px;
    color: white;
    cursor: pointer;
}
.product .info button:hover { background-color: #ff3b2e; }

/* Footer */
footer { background-color: #333; color: white; text-align: center; padding: 15px; margin-top: 20px; }

/* Responsive */
@media(max-width:600px){
    .products { flex-direction: column; align-items:center; }
}
</style>
</head>
<body>

<header>
<h1>style.wear.2</h1>
<nav>
<a href="#">Këpucë</a>
<a href="#">Çanta</a>
<a href="#">Kontakti</a>
</nav>
</header>

<section class="products">
    <div class="product">
        <img src="https://via.placeholder.com/250x250.png?text=Këpucë+Sportive" alt="Këpucë Sportive">
        <div class="info"><h2>Këpucë Sportive</h2><p>50€</p><button>Bli Tani</button></div>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/250x250.png?text=Çantë+Modë" alt="Çantë Modë">
        <div class="info"><h2>Çantë Modë</h2><p>35€</p><button>Bli Tani</button></div>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/250x250.png?text=Këpucë+Casual" alt="Këpucë Casual">
        <div class="info"><h2>Këpucë Casual</h2><p>45€</p><button>Bli Tani</button></div>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/250x250.png?text=Çantë+Elegante" alt="Çantë Elegante">
        <div class="info"><h2>Çantë Elegante</h2><p>40€</p><button>Bli Tani</button></div>
    </div>
</section>

<footer>&copy; 2025 style.wear.2 | Të gjitha të drejtat e rezervuara</footer>

</body>
</html>

