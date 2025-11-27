<!DOCTYPE html>
<html lang="sq">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>style.wear.2 - Slider dhe Produktet</title>
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

/* Slider */
.slider {
    position: relative;
    max-width: 800px;
    margin: 20px auto;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}
.slides {
    display: flex;
    transition: transform 0.5s ease-in-out;
}
.slide {
    min-width: 100%;
    position: relative;
}
.slide img {
    width: 100%;
    display: block;
}
.slide .info {
    position: absolute;
    bottom: 0;
    width: 100%;
    background: rgba(0,0,0,0.7);
    color: white;
    padding: 15px;
    text-align: center;
}
.slide .info h2 { margin: 0 0 5px 0; }
.slide .info p { margin: 0 0 10px 0; font-weight: bold; }
.slide .info button {
    background-color: #ff6f61;
    border: none;
    padding: 8px 15px;
    border-radius: 5px;
    color: white;
    cursor: pointer;
}
.slide .info button:hover { background-color: #ff3b2e; }

/* Slider arrows */
.prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    font-size: 2em;
    color: white;
    background: rgba(0,0,0,0.4);
    border: none;
    padding: 5px 10px;
    cursor: pointer;
    border-radius: 5px;
    z-index: 10;
}
.prev { left: 10px; }
.next { right: 10px; }

/* Produktet poshtë sliderit */
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
    cursor: pointer;
    box-shadow: 0 5px 15px rgba(0,0,0,0.1);
    background-color: white;
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

<!-- Slider -->
<div class="slider">
    <div class="slides">
        <div class="slide">
            <img src="https://via.placeholder.com/800x400.png?text=Këpucë+Sportive" alt="Këpucë Sportive">
            <div class="info">
                <h2>Këpucë Sportive</h2>
                <p>50€</p>
                <button>Bli Tani</button>
            </div>
        </div>
        <div class="slide">
            <img src="https://via.placeholder.com/800x400.png?text=Çantë+Modë" alt="Çantë Modë">
            <div class="info">
                <h2>Çantë Modë</h2>
                <p>35€</p>
                <button>Bli Tani</button>
            </div>
        </div>
        <div class="slide">
            <img src="https://via.placeholder.com/800x400.png?text=Këpucë+Casual" alt="Këpucë Casual">
            <div class="info">
                <h2>Këpucë Casual</h2>
                <p>45€</p>
                <button>Bli Tani</button>
            </div>
        </div>
    </div>
    <button class="prev">&#10094;</button>
    <button class="next">&#10095;</button>
</div>

<!-- Produktet poshtë sliderit -->
<section class="products">
    <div class="product">
        <img src="https://via.placeholder.com/250x250.png?text=Çantë+Elegante" alt="Çantë Elegante">
        <div class="info"><h2>Çantë Elegante</h2><p>40€</p><button>Bli Tani</button></div>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/250x250.png?text=Këpucë+Nike" alt="Këpucë Nike">
        <div class="info"><h2>Këpucë Nike</h2><p>60€</p><button>Bli Tani</button></div>
    </div>
</section>

<footer>&copy; 2025 style.wear.2 | Të gjitha të drejtat e rezervuara</footer>

<script>
let index = 0;
const slides = document.querySelectorAll('.slide');

function showSlide(i) {
    slides.forEach((slide, idx) => {
        slide.style.display = (idx === i) ? 'block' : 'none';
    });
}
showSlide(index);

// Navigimi me butonat
document.querySelector('.prev').addEventListener('click', () => {
    index = (index - 1 + slides.length) % slides.length;
    showSlide(index);
});
document.querySelector('.next').addEventListener('click', () => {
    index = (index + 1) % slides.length;
    showSlide(index);
});

// Slider automatik çdo 4 sekonda
setInterval(() => {
    index = (index + 1) % slides.length;
    showSlide(index);
}, 4000);
</script>

</body>
</html>
