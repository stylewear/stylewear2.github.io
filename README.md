<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Style.Wear.2 - Dyqan Premium</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
body {font-family: 'Roboto', sans-serif; margin:0; background:#f8f9fa;}
header {background:#222; color:#fff; text-align:center; padding:1rem; font-size:1.8rem; font-weight:bold; position:sticky; top:0; z-index:100; display:flex; justify-content:space-between; align-items:center;}
header .cart-count {background:#ff4081; color:#fff; border-radius:50%; padding:2px 8px; font-size:0.9rem; margin-left:5px;}
/* Slider */
.slider {position:relative; max-width:100%; overflow:hidden; height:350px; margin:20px auto; border-radius:12px;}
.slides {display:flex; transition:0.6s ease;}
.slide {min-width:100%; background-size:cover; background-position:center;}
.slider-buttons {position:absolute; top:50%; width:100%; display:flex; justify-content:space-between; transform:translateY(-50%); padding:0 10px;}
.slider-buttons button {background:rgba(0,0,0,0.4); color:#fff; border:none; padding:10px; cursor:pointer; border-radius:50%; font-size:1.2rem;}
/* Categories */
.categories {text-align:center; margin:20px 0;}
.categories button {background:#ff4081; color:#fff; border:none; margin:0 5px; padding:8px 15px; border-radius:6px; cursor:pointer;}
.categories button.active {background:#e73370;}
/* Products */
.products {display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; padding:20px;}
.product-card {background:#fff; border-radius:12px; box-shadow:0 4px 8px rgba(0,0,0,0.1); text-align:center; padding:15px; opacity:0; transform:translateY(30px); transition:all 0.6s ease;}
.product-card.show {opacity:1; transform:translateY(0);}
.product-card img {width:100%; border-radius:12px;}
.product-card h3 {margin:10px 0 5px 0; font-size:1.2rem;}
.product-card p {font-size:0.9rem; color:#555; min-height:40px;}
.product-card .price {font-weight:bold; margin:8px 0; color:#ff4081; font-size:1.1rem;}
.product-card button {background:#ff4081; color:#fff; border:none; padding:10px 15px; border-radius:8px; cursor:pointer; transition:0.3s;}
.product-card button:hover {background:#e73370;}
/* Modal */
.modal {display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.6); justify-content:center; align-items:center; z-index:1000;}
.modal-content {background:#fff; padding:25px; border-radius:12px; max-width:500px; width:90%; text-align:center; position:relative;}
.modal-content h2 {margin-top:0;}
.modal-content img {width:80%; border-radius:12px; margin-bottom:10px;}
.modal-content .close {position:absolute; top:10px; right:15px; cursor:pointer; font-size:1.4rem; font-weight:bold; color:#333;}
.modal-content .modal-price {font-weight:bold; margin:10px 0; color:#ff4081;}
.modal-content form input[type="text"], .modal-content form input[type="number"] {width:90%; padding:8px; margin:5px 0; border-radius:6px; border:1px solid #ccc;}
.modal-content form button {background:#ff4081; color:#fff; border:none; padding:10px 15px; border-radius:8px; cursor:pointer; margin-top:10px;}
.modal-content form button:hover {background:#e73370;}
/* Similar products carousel */
.similar-products {display:flex; overflow-x:auto; gap:10px; padding:10px 0;}
.similar-products img {width:80px; border-radius:8px; cursor:pointer; transition:0.3s;}
.similar-products img:hover {transform:scale(1.1);}
.mini-cart {position:fixed; top:80px; right:20px; width:260px; background:#fff; border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.2); padding:15px; z-index:999; max-height:400px; overflow-y:auto;}
.mini-cart h3 {margin-top:0; font-size:1.2rem; color:#ff4081;}
.cart-item {display:flex; justify-content:space-between; margin-bottom:10px; align-items:center;}
.cart-item button {padding:2px 6px; margin-left:5px; border:none; background:#ff4081; color:#fff; border-radius:6px; cursor:pointer;}
.cart-total {font-weight:bold; text-align:right; margin-top:10px;}
#checkoutBtn {background:#ff4081;color:#fff;border:none;padding:8px 12px;border-radius:6px;cursor:pointer;margin-top:10px;}
#checkoutBtn:hover{background:#e73370;}
@media(max-width:600px){header{font-size:1.4rem}.slider{height:220px;}.mini-cart{width:90%; top:70px; right:5%;}}
</style>
</head>
<body>

<header>
  Style.Wear.2
  <div>Cart <span class="cart-count" id="cartCount">0</span></div>
</header>

<div class="slider">
  <div class="slides">
    <div class="slide" style="background-image:url('https://via.placeholder.com/800x350/ff7f7f/333333?text=Promo+1')"></div>
    <div class="slide" style="background-image:url('https://via.placeholder.com/800x350/7fbfff/333333?text=Promo+2')"></div>
    <div class="slide" style="background-image:url('https://via.placeholder.com/800x350/7fff7f/333333?text=Promo+3')"></div>
  </div>
  <div class="slider-buttons">
    <button id="prev">&#10094;</button>
    <button id="next">&#10095;</button>
  </div>
</div>

<div class="categories">
  <button class="category-btn active" data-category="all">Të Gjitha</button>
  <button class="category-btn" data-category="shirt">Shirts</button>
  <button class="category-btn" data-category="jacket">Jackets</button>
  <button class="category-btn" data-category="sneakers">Sneakers</button>
</div>

<div class="products">
  <!-- Shembuj produktesh -->
  <div class="product-card" data-name="Shirt" data-price="25" data-img="https://via.placeholder.com/200x200" data-category="shirt">
    <img src="https://via.placeholder.com/200x200" alt="Shirt">
    <h3>Shirt</h3>
    <p>Këmishë moderne për çdo stinë</p>
    <div class="price">$25</div>
    <button class="buy-btn">Bli Tani</button>
  </div>
  <div class="product-card" data-name="Jacket" data-price="80" data-img="https://via.placeholder.com/200x200/7fff7f" data-category="jacket">
    <img src="https://via.placeholder.com/200x200/7fff7f" alt="Jacket">
    <h3>Jacket</h3>
    <p>Xhaketë elegante për ditët e ftohta</p>
    <div class="price">$80</div>
    <button class="buy-btn">Bli Tani</button>
  </div>
  <div class="product-card" data-name="Sneakers" data-price="60" data-img="https://via.placeholder.com/200x200/7fbfff" data-category="sneakers">
    <img src="https://via.placeholder.com/200x200/7fbfff" alt="Sneakers">
    <h3>Sneakers</h3>
    <p>Këpucë sportive të rehatshme dhe stil</p>
    <div class="price">$60</div>
    <button class="buy-btn">Bli Tani</button>
  </div>
</div>

<div class="modal" id="buyModal">
  <div class="modal-content">
    <span class="close">&times;</span>
    <img src="" alt="Produkt">
    <h2></h2>
    <p class="modal-price"></p>
    <form>
      <input type="text" placeholder="Emri juaj" required>
      <input type="number" placeholder="Sasia" value="1" min="1" required>
      <button type="submit">Shto në Cart</button>
    </form>
    <h4>Produkte të ngjashme:</h4>
    <div class="similar-products"></div>
  </div>
</div>

<div class="mini-cart" id="miniCart">
  <h3>Cart</h3>
  <div class="cart-items"></div>
  <div class="cart-total">Total: $0</div>
  <button id="checkoutBtn">Checkout</button>
</div>

<script>
// Slider
const slides=document.querySelector('.slides');
const slideCount=document.querySelectorAll('.slide').length;
let index=0;
function showSlide(i){ slides.style.transform=translateX(${-i*100}%); }
document.getElementById('next').addEventListener('click',()=>{ index=(index+1)%slideCount; showSlide(index); });
document.getElementById('prev').addEventListener('click',()=>{ index=(index-1+slideCount)%slideCount; showSlide(index); });
setInterval(()=>{ index=(index+1)%slideCount; showSlide(index); },4000);

// Product card animation
const productCards=document.querySelectorAll('.product-card');
window.addEventListener('scroll',()=>{
  const triggerBottom=window.innerHeight/5*4;
  productCards.forEach(card=>{if(card.getBoundingClientRect().top<triggerBottom){card.classList.add('show');}});
});

// Category filter
const categoryBtns=document.querySelectorAll('.category-btn');
categoryBtns.forEach(btn=>{btn.addEventListener('click',()=>{
  categoryBtns.forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  const cat=btn.dataset.category;
  productCards.forEach(card=>{card.style.display=(cat==='all'||card.dataset.category===cat)?'block':'none';});
});});

// Mini-cart + localStorage
const miniCart=document.getElementById('miniCart');
const cartItemsContainer=miniCart.querySelector('.cart-items');
const cartTotalEl=miniCart.querySelector('.cart-total');
const cartCountEl=document.getElementById('cartCount');
const checkoutBtn=document.getElementById('checkoutBtn');
let cart=[];
let savedCart=localStorage.getItem('cart');
if(savedCart){cart=JSON.parse(savedCart); updateCart();}

function saveCart(){localStorage.setItem('cart',JSON.stringify(cart));}
function updateCart(){
  cartItemsContainer.innerHTML=''; let total=0; let totalQty=0;
  cart.forEach((item,index)=>{
    const div=document.createElement('div');
    div.classList.add('cart-item');
    div.innerHTML=`${item.name} x${item.qty} - $${item.price*item.qty} 
    <button data-index="${index}" class="minus">-</button> 
    <button data-index="${index}" class="plus">+</button>`;
    cartItemsContainer.appendChild(div);
    total+=item.price*item.qty;
    totalQty+=item.qty;
  });
  cartTotalEl.textContent=Total: $${total};
  cartCountEl.textContent=totalQty;
  saveCart();
  document.querySelectorAll('.plus').forEach(btn=>{btn.onclick=()=>{cart[btn.dataset.index].qty++;updateCart();}});
  document.querySelectorAll('.minus').forEach(btn=>{btn.onclick=()=>{if(cart[btn.dataset.index].qty>1){cart[btn.dataset.index].qty--;updateCart();}}});
}

// Modal
const modal=document.getElementById('buyModal');
const modalImg=modal.querySelector('img');
const modalTitle=modal.querySelector('h2');
const modalPrice=modal.querySelector('.modal-price');
const similarContainer=modal.querySelector('.similar-products');
const buyButtons=document.querySelectorAll('.buy-btn');
const closeBtn=modal.querySelector('.close');

buyButtons.forEach(btn=>{
  btn.addEventListener('click',e=>{
    const card=e.target.closest('.product-card');
    modalImg.src=card.dataset.img;
    modalTitle.textContent=card.dataset.name;
    modalPrice.textContent="Çmimi: $"+card.dataset.price;
    modal.style.display='flex';
    similarContainer.innerHTML='';
    const cat=card.dataset.category;
    productCards.forEach(c=>{
      if(c.dataset.category===cat && c.dataset.name!==card.dataset.name){
        const img=document.createElement('img');
        img.src=c.dataset.img; img.title=c.dataset.name;
        img.addEventListener('click',()=>{c.querySelector('.buy-btn').click();});
        similarContainer.appendChild(img);
      }
    });
  });
});

closeBtn.addEventListener('click',()=>{modal.style.display='none';});
window.addEventListener('click',e=>{if(e.target==modal) modal.style.display='none';});

modal.querySelector('form').addEventListener('submit',e=>{
  e.preventDefault();
  const qty=parseInt(modal.querySelector('input[type="number"]').value);
  const name=modalTitle.textContent;
  const price=parseInt(modalTitle.nextElementSibling.textContent.replace('Çmimi: $',''));
  const exist=cart.find(item=>item.name===name);
  if(exist){exist.qty+=qty;}else{cart.push({name:name,price:price,qty:qty});}
  updateCart();
  modal.style.display='none';
});

// Checkout
checkoutBtn.addEventListener('click',()=>{
  if(cart.length===0){alert("Cart është bosh!"); return;}
  let content=<h2>Porosia Juaj</h2><ul>;
  let total=0;
  cart.forEach(item=>{content+=<li>${item.name} x${item.qty} - $${item.price*item.qty}</li>; total+=item.price*item.qty;});
  content+=</ul><h3>Total: $${total}</h3>;
  const printWindow=window.open('','PRINT','height=600,width=800');
  printWindow.document.write('<html><head><title>Porosia Juaj</title></head><body>');
  printWindow.document.write(content);
  printWindow.document.write('</body></html>');
  printWindow.document.close();
  printWindow.focus();
  printWindow.print();
});
</script>
</body>
</html>
