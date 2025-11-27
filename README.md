<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Style.Wear.2 - Premium Sneakers</title>
<style>
  *{margin:0;padding:0;box-sizing:border-box;font-family:'Arial',sans-serif;}
  body{background:#f2f2f2;color:#333;}
  header{background:#fff;padding:20px 40px;display:flex;justify-content:space-between;align-items:center;box-shadow:0 2px 10px rgba(0,0,0,0.1);position:sticky;top:0;z-index:1000;transition:all 0.3s;}
  header h1{font-size:1.8rem;color:#ff6f61;letter-spacing:1px;}
  nav a{margin-left:20px;text-decoration:none;color:#333;font-weight:500;transition:color 0.3s;}
  nav a:hover{color:#ff6f61;}

  /* Hero Section */
  .hero{display:flex;justify-content:center;align-items:center;height:75vh;background:url('https://images.unsplash.com/photo-1618354690322-c0e5e720c9e0?auto=format&fit=crop&w=1950&q=80') center/cover no-repeat;position:relative;color:#fff;text-align:center;flex-direction:column;overflow:hidden;}
  .hero::after{content:"";position:absolute;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.4);}
  .hero h2{position:relative;font-size:3rem;margin-bottom:20px;animation:fadeInDown 1s;}
  .hero p{position:relative;font-size:1.2rem;margin-bottom:30px;animation:fadeInUp 1s;}
  .hero button{position:relative;padding:14px 30px;background:#ff6f61;border:none;color:#fff;font-size:1.1rem;cursor:pointer;border-radius:8px;transition:all 0.3s;animation:fadeIn 1.5s;}
  .hero button:hover{background:#ff4a3d;transform:scale(1.05);}

  @keyframes fadeInDown{from{opacity:0;transform:translateY(-20px);}to{opacity:1;transform:translateY(0);}}
  @keyframes fadeInUp{from{opacity:0;transform:translateY(20px);}to{opacity:1;transform:translateY(0);}}
  @keyframes fadeIn{from{opacity:0;}to{opacity:1;}}

  /* Filter Buttons */
  .filters{text-align:center;margin:30px 0;}
  .filters button{padding:12px 25px;margin:0 10px;border:none;border-radius:50px;background:#fff;cursor:pointer;box-shadow:0 4px 10px rgba(0,0,0,0.1);transition:all 0.3s;font-weight:600;}
  .filters button:hover, .filters button.active{background:#ff6f61;color:#fff;transform:scale(1.05);}

  /* Products */
  .products{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:30px;padding:0 40px 50px;}
  .product-card{background:#fff;border-radius:15px;overflow:hidden;box-shadow:0 8px 20px rgba(0,0,0,0.1);transition:transform 0.5s, box-shadow 0.5s;cursor:pointer;position:relative;}
  .product-card:hover{transform:translateY(-10px) rotateX(5deg);box-shadow:0 12px 30px rgba(0,0,0,0.2);}
  .product-card img{width:100%;height:260px;object-fit:cover;transition:transform 0.5s;}
  .product-card:hover img{transform:scale(1.05);}
  .product-card .content{padding:20px;text-align:center;}
  .product-card h3{margin-bottom:10px;font-size:1.3rem;color:#ff6f61;transition:color 0.3s;}
  .product-card p{font-size:0.95rem;margin-bottom:15px;color:#666;}
  .product-card button{padding:10px 22px;background:#ff6f61;border:none;color:#fff;cursor:pointer;border-radius:50px;transition:all 0.3s;font-weight:600;}
  .product-card button:hover{background:#ff4a3d;transform:scale(1.05);}

  /* Modal */
  .modal{display:none;position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.8);justify-content:center;align-items:center;z-index:2000;animation:fadeIn 0.3s;}
  .modal-content{background:#fff;padding:25px;border-radius:15px;max-width:500px;width:90%;text-align:center;position:relative;animation:scaleUp 0.3s;}
  .modal-content img{width:100%;height:auto;margin-bottom:15px;border-radius:10px;}
  .modal-content h3{color:#ff6f61;margin-bottom:10px;}
  .modal-content p{color:#666;margin-bottom:20px;}
  .modal-content button{padding:12px 25px;background:#ff6f61;border:none;color:#fff;border-radius:50px;cursor:pointer;transition:all 0.3s;font-weight:600;}
  .modal-content button:hover{background:#ff4a3d;transform:scale(1.05);}
  .close{position:absolute;top:10px;right:15px;font-size:1.7rem;cursor:pointer;color:#ff6f61;}

  @keyframes scaleUp{from{transform:scale(0.8);opacity:0;}to{transform:scale(1);opacity:1;}}

  footer{background:#333;color:#fff;padding:40px;text-align:center;}
  footer a{color:#ff6f61;text-decoration:none;margin:0 10px;}
</style>
</head>
<body>

<header>
  <h1>Style.Wear.2</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#products">Sneakers</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<section class="hero" id="home">
  <h2>Step Up Your Game</h2>
  <p>Premium Sneakers & Shoes for Every Style</p>
  <button>Shop Now</button>
</section>

<div class="filters">
  <button class="filter-btn active" data-category="all">All</button>
  <button class="filter-btn" data-category="running">Running</button>
  <button class="filter-btn" data-category="casual">Casual</button>
  <button class="filter-btn" data-category="sport">Sport</button>
</div>

<section class="products" id="products">
  <div class="product-card" data-category="running">
    <img src="https://images.unsplash.com/photo-1618354690322-c0e5e720c9e0?auto=format&fit=crop&w=800&q=80" alt="Air Runner">
    <div class="content">
      <h3>Air Runner</h3>
      <p>Lightweight sneakers for running and casual wear.</p>
      <button>View</button>
    </div>
  </div>
  <div class="product-card" data-category="casual">
    <img src="https://images.unsplash.com/photo-1618354700323-3a4e0d68f1e1?auto=format&fit=crop&w=800&q=80" alt="Urban Kicks">
    <div class="content">
      <h3>Urban Kicks</h3>
      <p>Stylish sneakers perfect for city streets.</p>
      <button>View</button>
    </div>
  </div>
  <div class="product-card" data-category="sport">
    <img src="https://images.unsplash.com/photo-1618354710322-4b1e1c7f7a9b?auto=format&fit=crop&w=800&q=80" alt="Sporty Flex">
    <div class="content">
      <h3>Sporty Flex</h3>
      <p>Comfortable shoes for sports and workouts.</p>
      <button>View</button>
    </div>
  </div>
</section>

<!-- Modal -->
<div class="modal" id="modal">
  <div class="modal-content">
    <span class="close" id="close">&times;</span>
    <img src="" alt="Product Image" id="modal-img">
    <h3 id="modal-title"></h3>
    <p id="modal-desc"></p>
    <button>Add to Cart</button>
  </div>
</div>

<footer id="contact">
  <p>&copy; 2025 Style.Wear.2 | Designed with ❤</p>
  <p>
    <a href="#">Facebook</a> |
    <a href="#">Instagram</a> |
    <a href="#">Twitter</a>
  </p>
</footer>

<script>
  // Filter
  const filterButtons = document.querySelectorAll('.filter-btn');
  const productCards = document.querySelectorAll('.product-card');
  filterButtons.forEach(btn => {
    btn.addEventListener('click', () => {
      document.querySelector('.filter-btn.active').classList.remove('active');
      btn.classList.add('active');
      const category = btn.getAttribute('data-category');
      productCards.forEach(card => {
        card.style.display = (category === 'all' || card.getAttribute('data-category') === category) ? 'block' : 'none';
      });
    });
  });

  // Modal
  const modal = document.getElementById('modal');
  const modalImg = document.getElementById('modal-img');
  const modalTitle = document.getElementById('modal-title');
  const modalDesc = document.getElementById('modal-desc');
  const closeBtn = document.getElementById('close');
  const viewButtons = document.querySelectorAll('.product-card button');

  viewButtons.forEach((btn,i) => {
    btn.addEventListener('click', e => {
      e.stopPropagation();
      const card = btn.closest('.product-card');
      modal.style.display = 'flex';
      modalImg.src = card.querySelector('img').src;
      modalTitle.textContent = card.querySelector('h3').textContent;
      modalDesc.textContent = card.querySelector('p').textContent;
    });
  });

  closeBtn.addEventListener('click', () => modal.style.display='none');
  window.addEventListener('click', e => {if(e.target === modal) modal.style.display='none';});
</script>

</body>
</html>
