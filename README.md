<!DOCTYPE html>
<html lang="sq">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Style.Wear.2 - Atlete, Këpucë, Çanta</title>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&display=swap" rel="stylesheet">
<style>
/* Bazik dhe Reset */
* {margin: 0; padding: 0; box-sizing: border-box; font-family: 'Montserrat', sans-serif;}
body {background-color: #f9f9f9; color: #333;}
a {text-decoration: none;}

/* Navbar */
nav {
    background-color: #111;
    color: #fff;
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 100;
}
nav h1 {font-weight: 700; letter-spacing: 1px;}
nav ul {list-style: none; display: flex; gap: 2rem;}
nav ul li a {color: #fff; font-weight: 500;}
nav ul li a:hover {color: #f39c12;}

/* Hero Section */
.hero {
    background: url('https://images.unsplash.com/photo-1618354695050-51e8a6931eb5?auto=format&fit=crop&w=1500&q=80') center/cover no-repeat;
    height: 70vh;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    text-align: center;
}
.hero h2 {
    font-size: 3rem;
    background: rgba(0,0,0,0.5);
    padding: 1rem 2rem;
    border-radius: 10px;
}

/* Slider Produkte Kryesore */
.slider-section {
    margin: 4rem 0;
}
.slider-container {
    position: relative;
    max-width: 1000px;
    margin: 0 auto;
    overflow: hidden;
}
.slider-wrapper {
    display: flex;
    transition: transform 0.5s ease;
}
.slide {
    min-width: 300px;
    margin: 0 1rem;
    cursor: pointer;
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    overflow: hidden;
    text-align: center;
}
.slide img {width: 100%; height: 250px; object-fit: cover;}
.slide h3 {padding: 1rem 0; font-size: 1.2rem;}
.slider-container button.prev,
.slider-container button.next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0,0,0,0.5);
    border: none;
    color: #fff;
    font-size: 2rem;
    padding: 0.5rem 1rem;
    cursor: pointer;
    border-radius: 5px;
    z-index: 10;
}
.slider-container button.prev:hover,
.slider-container button.next:hover {background-color: #f39c12;}
.slider-container button.prev {left: 0;}
.slider-container button.next {right: 0;}

/* Slider Indicator */
.indicators {
    text-align: center;
    margin-top: 1rem;
}
.indicators span {
    display: inline-block;
    width: 12px;
    height: 12px;
    margin: 0 4px;
    background: #ccc;
    border-radius: 50%;
    cursor: pointer;
}
.indicators span.active {background: #f39c12;}

/* Produktet (kategoritë) */
.products {
    padding: 4rem 2rem;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
}
.product-card {
    background-color: #fff;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    cursor: pointer;
    transition: transform 0.3s;
}
.product-card:hover {transform: scale(1.05);}
.product-card img {width: 100%; height: 250px; object-fit: cover;}
.product-card h3 {padding: 1rem; font-size: 1.2rem;}
.product-card p {padding: 0 1rem 1rem; color: #555;}

/* Modal */
.modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left:0; top:0;
    width: 100%; height: 100%;
    background-color: rgba(0,0,0,0.8);
}
.modal-content {
    background-color: #fff;
    margin: 10% auto;
    padding: 2rem;
    border-radius: 10px;
    max-width: 500px;
    text-align: center;
    position: relative;
}
.modal-content img {width:100%; height:auto; border-radius:10px;}
.close {
    position: absolute;
    top: 10px; right: 15px;
    font-size: 28px;
    font-weight: bold;
    color: #333;
    cursor: pointer;
}
.close:hover {color:#f39c12;}
.modal-content h3 {margin-top: 1rem;}
.modal-content p {margin-top: 0.5rem; font-weight:bold;}

/* Footer */
footer {
    background-color: #111;
    color: #fff;
    text-align: center;
    padding: 2rem;
}
footer a {color: #f39c12;}
</style>
</head>
<body>

<!-- Navbar -->
<nav>
    <h1>Style.Wear.2</h1>
    <ul>
        <li><a href="#atlete">Atlete</a></li>
        <li><a href="#kepuce">Këpucë</a></li>
        <li><a href="#canta">Çanta</a></li>
    </ul>
</nav>

<!-- Hero Section -->
<section class="hero">
    <h2>Stili yt, zgjedhja jote</h2>
</section>

<!-- Slider Produkte Kryesore -->
<section class="slider-section">
    <h2 style="text-align:center; margin:2rem 0;">Produkte Kryesore</h2>
    <div class="slider-container">
        <button class="prev">&#10094;</button>
        <div class="slider-wrapper">
            <div class="slide product-card" data-title="Atlete Moderne" data-price="45€" data-img="https://images.unsplash.com/photo-1598970434795-0c54fe7c0642?auto=format&fit=crop&w=500&q=80">
                <img src="https://images.unsplash.com/photo-1598970434795-0c54fe7c0642?auto=format&fit=crop&w=500&q=80">
                <h3>Atlete Moderne</h3>
            </div>
            <div class="slide product-card" data-title="Këpucë Casual" data-price="60€" data-img="https://images.unsplash.com/photo-1618354695050-51e8a6931eb5?auto=format&fit=crop&w=500&q=80">
                <img src="https://images.unsplash.com/photo-1618354695050-51e8a6931eb5?auto=format&fit=crop&w=500&q=80">
                <h3>Këpucë Casual</h3>
            </div>
            <div class="slide product-card" data-title="Çanta Elegante" data-price="75€" data-img="https://images.unsplash.com/photo-1606813902886-0e04eaf7eec3?auto=format&fit=crop&w=500&q=80">
                <img src="https://images.unsplash.com/photo-1606813902886-0e04eaf7eec3?auto=format&fit=crop&w=500&q=80">
                <h3>Çanta Elegante</h3>
            </div>
        </div>
        <button class="next">&#10095;</button>
    </div>
    <div class="indicators">
        <span class="dot active"></span>
        <span class="dot"></span>
        <span class="dot"></span>
    </div>
</section>

<!-- Produkte -->
<section class="products" id="atlete">
    <div class="product-card" data-title="Atlete Moderne" data-price="45€" data-img="https://images.unsplash.com/photo-1598970434795-0c54fe7c0642?auto=format&fit=crop&w=500&q=80">
        <img src="https://images.unsplash.com/photo-1598970434795-0c54fe7c0642?auto=format&fit=crop&w=500&q=80" alt="">
        <h3>Atlete Moderne</h3>
        <p>Ngjyrë e bardhë me dizajn elegant dhe komod.</p>
    </div>
    <div class="product-card" data-title="Këpucë Casual" data-price="60€" data-img="https://images.unsplash.com/photo-1618354695050-51e8a6931eb5?auto=format&fit=crop&w=500&q=80">
        <img src="https://images.unsplash.com/photo-1618354695050-51e8a6931eb5?auto=format&fit=crop&w=500&q=80" alt="">
        <h3>Këpucë Casual</h3>
        <p>Përshtaten me çdo stil të përditshëm.</p>
    </div>
    <div class="product-card" data-title="Çanta Elegante" data-price="75€" data-img="https://images.unsplash.com/photo-1606813902886-0e04eaf7eec3?auto=format&fit=crop&w=500&q=80">
        <img src="https://images.unsplash.com/photo-1606813902886-0e04eaf7eec3?auto=format&fit=crop&w=500&q=80" alt="">
        <h3>Çanta Elegante</h3>
        <p>Dizajn modern për çdo rast.</p>
    </div>
</section>

<!-- Modal -->
<div id="productModal" class="modal">
    <div class="modal-content">
        <span class="close">&times;</span>
        <img id="modalImg" src="" alt="">
        <h3 id="modalTitle"></h3>
        <p id="modalPrice"></p>
    </div>
</div>

<!-- Footer -->
<footer>
    <p>&copy; 2025 Style.Wear.2 | <a href="#">Kontakto</a></p>
</footer>

<script>
// Slider JS
const wrapper = document.querySelector('.slider-wrapper');
const slides = document.querySelectorAll('.slide');
const nextBtn = document.querySelector('.next');
const prevBtn = document.querySelector('.prev');
const dots = document.querySelectorAll('.dot');
let index = 0;

function showSlide(i) {
    const offset = -i * (slides[0].offsetWidth + 16);
    wrapper.style.transform = translateX(${offset}px);
    dots.forEach(dot => dot.classList.remove('active'));
    dots[i].classList.add('active');
}

// Butonat
nextBtn.addEventListener('click', () => { index = (index+1)%slides.length; showSlide(index); resetAutoSlide(); });
prevBtn.addEventListener('click', () => { index = (index-1+slides.length)%slides.length; showSlide(index); resetAutoSlide(); });

// Klikimi tek dot
dots.forEach((dot,i) => { dot.addEventListener('click',()=>{ index=i; showSlide(index); resetAutoSlide(); }); });

// Slider automatik
let autoSlide = setInterval(() => { index=(index+1)%slides.length; showSlide(index); },4000);
function resetAutoSlide() { clearInterval(autoSlide); autoSlide=setInterval(()=>{ index=(index+1)%slides.length; showSlide(index); },4000); }

// Modal JS
const modal = document.getElementById('productModal');
const modalImg = document.getElementById('modalImg');
const modalTitle = document.getElementById('modalTitle');
const modalPrice = document.getElementById('modalPrice');
const closeBtn = document.querySelector('.close');

document.querySelectorAll('.product-card').forEach(card=>{
    card.addEventListener('click',()=>{
        modal.style.display='block';
        modalImg.src=card.dataset.img;
        modalTitle.textContent=card.dataset.title;
        modalPrice.textContent=card.dataset.price;
    });
});
closeBtn.addEventListener('click',()=>{ modal.style.display='none'; });
window.addEventListener('click',(e)=>{ if(e.target===modal){ modal.style.display='none'; } });
</script>
</body>
</html>
