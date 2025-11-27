<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Style.Wear.2 - Dyqan Online</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Roboto', sans-serif;
      margin: 0;
      background: #f8f9fa;
    }
    header {
      background: #222;
      color: #fff;
      text-align: center;
      padding: 1rem;
      font-size: 1.8rem;
      font-weight: bold;
    }

    /* Slider */
    .slider {
      position: relative;
      max-width: 100%;
      overflow: hidden;
      height: 350px;
      margin: 20px auto;
      border-radius: 12px;
    }
    .slides {
      display: flex;
      transition: transform 0.6s ease;
    }
    .slide {
      min-width: 100%;
      background-size: cover;
      background-position: center;
    }
    .slider-buttons {
      position: absolute;
      top: 50%;
      width: 100%;
      display: flex;
      justify-content: space-between;
      transform: translateY(-50%);
      padding: 0 10px;
    }
    .slider-buttons button {
      background: rgba(0,0,0,0.4);
      color: #fff;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 50%;
      font-size: 1.2rem;
    }

    /* Products */
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 20px;
    }
    .product-card {
      background: #fff;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      text-align: center;
      padding: 15px;
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease;
    }
    .product-card.show {
      opacity: 1;
      transform: translateY(0);
    }
    .product-card img {
      width: 100%;
      border-radius: 12px;
    }
    .product-card h3 {
      margin: 10px 0 5px 0;
      font-size: 1.2rem;
    }
    .product-card p {
      font-size: 0.9rem;
      color: #555;
      min-height: 40px;
    }
    .product-card .price {
      font-weight: bold;
      margin: 8px 0;
      color: #ff4081;
      font-size: 1.1rem;
    }
    .product-card button {
      background: #ff4081;
      color: #fff;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s;
    }
    .product-card button:hover {
      background: #e73370;
    }

    /* Modal */
    .modal {
      display: none;
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.6);
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }
    .modal-content {
      background: #fff;
      padding: 25px;
      border-radius: 12px;
      max-width: 450px;
      width: 90%;
      text-align: center;
      position: relative;
    }
    .modal-content h2 {
      margin-top: 0;
    }
    .modal-content img {
      width: 80%;
      border-radius: 12px;
      margin-bottom: 10px;
    }
    .modal-content .close {
      position: absolute;
      top: 10px; right: 15px;
      cursor: pointer;
      font-size: 1.4rem;
      font-weight: bold;
      color: #333;
    }
    .modal-content form input[type="text"], 
    .modal-content form input[type="number"] {
      width: 90%;
      padding: 8px;
      margin: 5px 0;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    .modal-content form button {
      background: #ff4081;
      color: #fff;
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 10px;
    }
    .modal-content form button:hover {
      background: #e73370;
    }

    @media(max-width: 600px){
      header { font-size: 1.4rem; }
      .slider { height: 220px; }
    }
  </style>
</head>
<body>

<header>Style.Wear.2</header>

<!-- Slider -->
<div class="slider">
  <div class="slides">
    <div class="slide" style="background-image:url('https://via.placeholder.com/800x350/ff7f7f/333333?text=Trendy+Style+1')"></div>
    <div class="slide" style="background-image:url('https://via.placeholder.com/800x350/7fbfff/333333?text=Trendy+Style+2')"></div>
    <div class="slide" style="background-image:url('https://via.placeholder.com/800x350/7fff7f/333333?text=Trendy+Style+3')"></div>
  </div>
  <div class="slider-buttons">
    <button id="prev">&#10094;</button>
    <button id="next">&#10095;</button>
  </div>
</div>

<!-- Products -->
<div class="products">
  <div class="product-card" data-name="Shirt" data-price="25" data-img="https://via.placeholder.com/200x200">
    <img src="https://via.placeholder.com/200x200" alt="Shirt">
    <h3>Shirt</h3>
    <p>Këmishë e re moderne për çdo stinë</p>
    <div class="price">$25</div>
    <button class="buy-btn">Bli Tani</button>
  </div>
  <div class="product-card" data-name="Sneakers" data-price="60" data-img="https://via.placeholder.com/200x200/7fbfff">
    <img src="https://via.placeholder.com/200x200/7fbfff" alt="Sneakers">
    <h3>Sneakers</h3>
    <p>Këpucë sportive të rehatshme dhe stil</p>
    <div class="price">$60</div>
    <button class="buy-btn">Bli Tani</button>
  </div>
  <div class="product-card" data-name="Jacket" data-price="80" data-img="https://via.placeholder.com/200x200/7fff7f">
    <img src="https://via.placeholder.com/200x200/7fff7f" alt="Jacket">
    <h3>Jacket</h3>
    <p>Xhaketë elegante për ditët e ftohta</p>
    <div class="price">$80</div>
    <button class="buy-btn">Bli Tani</button>
  </div>
</div>

<!-- Modal -->
<div class="modal" id="buyModal">
  <div class="modal-content">
    <span class="close">&times;</span>
    <img src="" alt="Produkt">
    <h2></h2>
    <p class="modal-price"></p>
    <form>
      <input type="text" placeholder="Emri juaj" required>
      <input type="number" placeholder="Sasia" value="1" min="1" required>
      <button type="submit">Bli Tani</button>
    </form>
  </div>
</div>

<script>
  // Slider
  const slides = document.querySelector('.slides');
  const slideCount = document.querySelectorAll('.slide').length;
  let index = 0;

  function showSlide(i){
    slides.style.transform = translateX(${-i * 100}%);
  }

  document.getElementById('next').addEventListener('click', () => {
    index = (index + 1) % slideCount;
    showSlide(index);
  });
  document.getElementById('prev').addEventListener('click', () => {
    index = (index - 1 + slideCount) % slideCount;
    showSlide(index);
  });

  setInterval(() => {
    index = (index + 1) % slideCount;
    showSlide(index);
  }, 4000);

  // Product card animation
  const productCards = document.querySelectorAll('.product-card');
  window.addEventListener('scroll', () => {
    const triggerBottom = window.innerHeight / 5 * 4;
    productCards.forEach(card => {
      const cardTop = card.getBoundingClientRect().top;
      if(cardTop < triggerBottom){
        card.classList.add('show');
      }
    });
  });

  // Modal
  const modal = document.getElementById('buyModal');
  const modalImg = modal.querySelector('img');
  const modalTitle = modal.querySelector('h2');
  const modalPrice = modal.querySelector('.modal-price');
  const buyButtons = document.querySelectorAll('.buy-btn');
  const closeBtn = document.querySelector('.close');

  buyButtons.forEach(btn => {
    btn.addEventListener('click', (e) => {
      const card = e.target.closest('.product-card');
      modalImg.src = card.dataset.img;
      modalTitle.textContent = card.dataset.name;
      modalPrice.textContent = "Çmimi: $" + card.dataset.price;
      modal.style.display = 'flex';
    });
  });

  closeBtn.addEventListener('click', () => modal.style.display = 'none');
  window.addEventListener('click', e => {
    if(e.target == modal) modal.style.display = 'none';
  });

  // Optional: handle form submission
  modal.querySelector('form').addEventListener('submit', (e) => {
    e.preventDefault();
    alert(Porosia për ${modalTitle.textContent} është regjistruar!);
    modal.style.display = 'none';
  });
</script>

</body>
</html>
