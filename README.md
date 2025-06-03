<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Urban Threads - Clothing Brand</title>
  <style>
    * {
      margin: 0; padding: 0; box-sizing: border-box;
      font-family: 'Arial', sans-serif;
    }
    body {
      background: #fff; color: #222; line-height: 1.6;
    }
    .navbar {
      background: #000; color: #fff;
      display: flex; justify-content: space-between;
      align-items: center; padding: 1rem 2rem;
      position: sticky; top: 0; z-index: 999;
    }
    .navbar a {
      color: #fff; text-decoration: none; margin-left: 1.5rem;
    }
    .navbar a:hover {
      color: #f39c12;
    }
    .hero {
      background: url('https://source.unsplash.com/1600x900/?fashion') center/cover no-repeat;
      height: 90vh;
      display: flex; flex-direction: column;
      justify-content: center; align-items: center;
      text-align: center; color: white;
      animation: fadeIn 2s ease;
    }
    .hero h1 {
      font-size: 3rem;
    }
    .btn {
      background: #f39c12; color: white;
      border: none; padding: 0.75rem 1.5rem;
      border-radius: 4px; cursor: pointer;
      margin-top: 1rem; transition: background 0.3s;
    }
    .btn:hover {
      background: #e67e22;
    }
    .filter-bar {
      padding: 2rem; text-align: center;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem; padding: 2rem;
    }
    .product-card {
      border: 1px solid #ddd; padding: 1rem;
      text-align: center; background: #f9f9f9;
      border-radius: 8px;
    }
    .product-card img {
      width: 100%; height: 250px; object-fit: cover;
      border-radius: 8px;
    }
    .cart {
      position: fixed; top: 1rem; right: 1rem;
      background: white; padding: 1rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
      display: none; z-index: 1000;
    }
    footer {
      text-align: center; padding: 1.5rem;
      background: #000; color: #fff;
    }
    form {
      display: flex; flex-direction: column;
      gap: 1rem; max-width: 400px; margin: auto;
    }
    input, textarea {
      padding: 0.75rem; border-radius: 5px;
      border: 1px solid #ccc;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <header class="navbar">
    <h2>Urban Threads</h2>
    <nav>
      <a href="#home">Home</a>
      <a href="#shop">Shop</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home" class="hero">
    <h1>Redefining Street Fashion</h1>
    <p>Trendy, Comfortable, Sustainable</p>
    <a href="#shop" class="btn">Shop Now</a>
  </section>

  <section class="filter-bar">
    <strong>Filter:</strong>
    <button class="btn" onclick="filterProducts('all')">All</button>
    <button class="btn" onclick="filterProducts('hoodie')">Hoodies</button>
    <button class="btn" onclick="filterProducts('jacket')">Jackets</button>
    <button class="btn" onclick="filterProducts('jeans')">Jeans</button>
  </section>

  <section id="shop" class="products">
    <div class="product-card hoodie">
      <img src="https://source.unsplash.com/400x400/?hoodie" alt="Hoodie">
      <h3>Classic Hoodie</h3>
      <p>$45.00</p>
      <button class="btn" onclick="addToCart('Classic Hoodie')">Add to Cart</button>
      <button class="btn" onclick="orderNow('Classic Hoodie')">Order Now</button>
    </div>
    <div class="product-card jacket">
      <img src="https://source.unsplash.com/400x400/?jacket" alt="Jacket">
      <h3>Urban Jacket</h3>
      <p>$70.00</p>
      <button class="btn" onclick="addToCart('Urban Jacket')">Add to Cart</button>
      <button class="btn" onclick="orderNow('Urban Jacket')">Order Now</button>
    </div>
    <div class="product-card jeans">
      <img src="https://source.unsplash.com/400x400/?jeans" alt="Jeans">
      <h3>Denim Jeans</h3>
      <p>$60.00</p>
      <button class="btn" onclick="addToCart('Denim Jeans')">Add to Cart</button>
      <button class="btn" onclick="orderNow('Denim Jeans')">Order Now</button>
    </div>
  </section>

  <section id="about" style="padding:2rem; text-align:center;">
    <h2>About Urban Threads</h2>
    <p>We create modern streetwear that blends comfort with edgy fashion. Sustainable fabrics, bold designs.</p>
  </section>

  <section id="contact" style="padding:2rem; text-align:center;">
    <h2>Contact Us</h2>
    <form>
      <input type="text" name="name" placeholder="Your Name" required />
      <input type="email" name="email" placeholder="Your Email" required />
      <textarea rows="5" name="message" placeholder="Your Message" required></textarea>
      <button type="submit" class="btn">Send Message</button>
    </form>
  </section>

  <section style="padding:2rem; text-align:center;">
    <h2>Payment Options</h2>
    <p><strong>M-Pesa:</strong> Paybill: <b>123456</b> | Account: <b>UrbanThreads</b></p>
    <p><strong>PayPal:</strong></p>
    <form action="https://www.sandbox.paypal.com/cgi-bin/webscr" method="post" target="_blank">
      <input type="hidden" name="cmd" value="_s-xclick" />
      <input type="hidden" name="hosted_button_id" value="DUMMYID123" />
      <input type="submit" value="Pay with PayPal" class="btn" />
    </form>
    <p><strong>Stripe:</strong> (Coming Soon)</p>
  </section>

  <footer>
    <p>&copy; 2025 Urban Threads. All rights reserved.</p>
  </footer>

  <div id="cart" class="cart">
    <h3>Your Cart</h3>
    <ul id="cart-items"></ul>
    <button class="btn" onclick="closeCart()">Close Cart</button>
  </div>

  <script>
    const cartItems = [];
    function addToCart(productName) {
      cartItems.push(productName);
      renderCart();
    }
    function renderCart() {
      const cart = document.getElementById('cart');
      const list = document.getElementById('cart-items');
      list.innerHTML = '';
      cartItems.forEach(item => {
        const li = document.createElement('li');
        li.textContent = item;
        list.appendChild(li);
      });
      cart.style.display = 'block';
    }
    function closeCart() {
      document.getElementById('cart').style.display = 'none';
    }
    function filterProducts(category) {
      const cards = document.querySelectorAll('.product-card');
      cards.forEach(card => {
        if (category === 'all' || card.classList.contains(category)) {
          card.style.display = 'block';
        } else {
          card.style.display = 'none';
        }
      });
    }
    function orderNow(productName) {
      alert('To order "' + productName + '", please contact us via the form or use the payment options below.');
    }
  </script>

</body>
</html>
