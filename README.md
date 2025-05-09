#home page
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>CutieCart Home</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  
  
  <style>
    .search-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px 0;
}

.search-input {
  width: 300px;
  padding: 10px 15px;
  border: 2px solid #ffb6c1;
  border-radius: 8px 0 0 8px;
  outline: none;
  font-size: 1rem;
}

.search-btn {
  padding: 10px 15px;
  background-color: #ffb6c1;
  border: none;
  border-radius: 0 8px 8px 0;
  color: rgb(227, 161, 216);
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.3s;
}

.search-btn:hover {
  background-color: #d63384;
}

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Quicksand', sans-serif;
    }

    body {
      background-color: #fff0f5;
      color: #333;
    }

    header {
      background-color: #ffb6c1;
      padding: 20px;
      text-align: center;
      font-family: 'Pacifico', cursive;
      font-size: 2rem;
      color: white;
    }

    nav {
      background-color: #ffe4e1;
      padding: 15px 20px;
      display: flex;
      justify-content: center;
      gap: 20px;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    nav a {
      text-decoration: none;
      color: #d63384;
      font-weight: bold;
      font-size: 1.2rem;
      padding: 10px 15px;
      border-radius: 8px;
      transition: 0.3s ease-in-out;
    }

    nav a:hover {
      background-color: #ffb6c1;
      color: white;
    }

    .product-row {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin: 30px auto;
      flex-wrap: wrap;
    }

    .product {
      background: #fff;
      border-radius: 15px;
      padding: 15px;
      width: 250px;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      text-align: center;
      transition: transform 0.3s ease-in-out;
      position: relative;
      cursor: pointer;
    }

    .product:hover {
      transform: scale(1.05);
    }

    .product img {
      width: 100%;
      border-radius: 10px;
    }

    .product h3 {
      margin: 10px 0;
      color: #d63384;
    }

    .heart {
      position: absolute;
      top: 10px;
      right: 10px;
      font-size: 24px;
      color: #ccc;
      cursor: pointer;
      transition: color 0.3s ease;
    }

    .heart.liked {
      color: red;
    }

    .floating-heart {
      position: absolute;
      font-size: 20px;
      animation: floatUp 1s ease-out forwards;
      color: red;
      pointer-events: none;
    }

    @keyframes floatUp {
      0% { opacity: 1; transform: translateY(0); }
      100% { opacity: 0; transform: translateY(-100px); }
    }

    footer {
      background-color: #ffb6c1;
      text-align: center;
      padding: 20px;
      color: white;
      margin-top: 20px;
    }

    .btn {
      padding: 8px 15px;
      background-color: #ffb6c1;
      border: none;
      border-radius: 8px;
      color: white;
      cursor: pointer;
      margin: 5px;
    }

    #productGallery img {
      width: 50px;
      height: 50px;
      border-radius: 5px;
      cursor: pointer;
      margin: 5px;
    }
  </style>
</head>
<body>

<header>CutieCart</header>

<nav>
  <a href="#home">Home</a>
  <a href="#shop">Shop</a>
  <a href="{% url 'about' %}">About</a>
  <a href="{% url 'cutiecare' %}">CutieCare</a>
  <a href="{% url 'skin_type' %}" style="text-decoration: none; color: #ff69b4; font-weight: bold;">Know Your Skin ✨</a>

  
</nav>
<!-- Add a Search Bar Here -->
<div class="search-container">
  <input type="text" placeholder="Search for products..." class="search-input">
  <button class="search-btn"><i class="fas fa-search"></i></button>
</div>
<section id="shop">
  <div class="product-row">
    <div class="product">
      <i class="fas fa-heart heart"></i>
      <img src="https://innovist.com/cdn/shop/files/First-images-guidelinestoner_46140800-b4a6-4dcd-818a-e20e157fee66.png?v=1741324967" alt="Cute Product 1">
      <h3>GORGEOUS TONNER</h3>
      <p>2000 RS</p>
    </div>
    <div class="product">
      <i class="fas fa-heart heart"></i>
      <img src="https://www.dyou.co/cdn/shop/files/unkissed_1_cd8af7a1-3b8c-4343-9f1b-e71a70f2b587.png?v=1731490987&width=990" alt="Cute Product 2">
      <h3>SUNSCREEN</h3>
      <p>3000 RS</p>
    </div>
  </div>
  <div class="product-row">
    <div class="product">
      <i class="fas fa-heart heart"></i>
      <img src="data:image/jpeg;base64,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" alt="Glow Booster">
      <h3>GLOW BOOSTER</h3>
      <p>4000 RS</p>
    </div>
  </div>
</section>

<!-- Modal -->
<div id="productModal" style="display:none;">
  <div style="position:fixed;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.6);z-index:1000;" onclick="closeProductModal()" id="productOverlay"></div>
  <div style="position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);background:white;padding:20px;border-radius:15px;width:320px;z-index:1001;text-align:center;">
    <img id="mainImage" src="" style="width:100%;border-radius:10px;">
    <div id="productGallery"></div>
    <h2 id="modalProdTitle" style="color:#d63384;"></h2>
    <p id="modalProdPrice"></p>
    <p id="modalProdDiscount" style="color:green;"></p>
    <p id="modalProdRating">Rating: ⭐⭐⭐⭐☆</p>
    <p id="modalProdReview">"Amazing product! Highly recommended."</p>
    <div>
      Quantity:
      <button onclick="changeQty(-1)">-</button>
      <span id="qty">1</span>
      <button onclick="changeQty(1)">+</button>
    </div>
    <button onclick="buyNow()" class="btn">Buy Now</button>
    <button onclick="toggleCart()" class="btn">Add to Cart</button>
    <p id="cartMsg" style="color:green;margin-top:10px;display:none;">Item added to cart successfully!</p>
    <button onclick="closeProductModal()" class="btn">Close</button>
  </div>
</div>

<script>
  let currentQty = 1;

  function closeProductModal() {
    document.getElementById("productModal").style.display = "none";
    document.getElementById("cartMsg").style.display = "none";
    currentQty = 1;
    document.getElementById("qty").textContent = currentQty;
  }

  function changeQty(val) {
    currentQty = Math.max(1, currentQty + val);
    document.getElementById("qty").textContent = currentQty;
  }

  function buyNow() {
    alert("Thank you for purchasing!");
  }

  function toggleCart() {
    const msg = document.getElementById("cartMsg");
    msg.textContent = "Item added to cart successfully!";
    msg.style.display = "block";
    setTimeout(() => msg.style.display = "none", 3000);
  }

  document.querySelectorAll('.product').forEach(product => {
    const title = product.querySelector('h3').textContent;
    const priceText = product.querySelector('p')?.textContent || "2000";
    const price = priceText.replace(/[^\d]/g, "") || "2000";
    const discount = "10% OFF";
    const imageSrc = product.querySelector('img')?.src || "https://via.placeholder.com/250";

    product.addEventListener('click', e => {
      if (e.target.classList.contains('btn') || e.target.classList.contains('heart')) return;

      document.getElementById('modalProdTitle').textContent = title;
      document.getElementById('modalProdPrice').textContent = `Price: ₹${price}`;
      document.getElementById('modalProdDiscount').textContent = `Discount: ${discount}`;
      document.getElementById('mainImage').src = imageSrc;

      const gallery = document.getElementById('productGallery');
      gallery.innerHTML = "";
      for (let i = 0; i < 4; i++) {
        const thumb = document.createElement('img');
        thumb.src = imageSrc;
        thumb.onclick = () => document.getElementById('mainImage').src = imageSrc;
        gallery.appendChild(thumb);
      }

      document.getElementById('productModal').style.display = 'block';
    });
  });

  document.querySelectorAll('.heart').forEach(heart => {
    heart.addEventListener('click', e => {
      e.stopPropagation();
      heart.classList.toggle('liked');
      const rect = heart.getBoundingClientRect();
      const floating = document.createElement('div');
      floating.classList.add('floating-heart');
      floating.style.left = `${rect.left + rect.width / 2}px`;
      floating.style.top = `${rect.top}px`;
      floating.innerHTML = '❤️';
      document.body.appendChild(floating);
      setTimeout(() => floating.remove(), 1000);
    });
  });

  document.body.addEventListener('click', function (e) {
    if (e.target.classList.contains('product') || e.target.classList.contains('heart') || e.target.closest('.product')) return;
    const heart = document.createElement('div');
    heart.classList.add('floating-heart');
    heart.style.left = `${e.pageX}px`;
    heart.style.top = `${e.pageY}px`;
    heart.innerHTML = '❤️';
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 1000);
  });
</script>

<footer>
  &copy; 2025 CutieCart look cuter.... All rights reserved.
</footer>
</body>
</html>
<!about page>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>About Us | CutieCart</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&family=Pacifico&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      background: #fff8f4;
      overflow-x: hidden;
      position: relative;
      color: #4b2e2e;
    }

    /* Bubble background */
    .bubble-container {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      overflow: hidden;
      z-index: -1;
    }

    .bubble {
      position: absolute;
      bottom: -100px;
      background: rgba(180, 32, 104, 0.3);
      border-radius: 50%;
      animation: rise 20s infinite ease-in;
    }

    .bubble:nth-child(1) {
      width: 60px;
      height: 60px;
      left: 10%;
      animation-duration: 15s;
    }

    .bubble:nth-child(2) {
      width: 100px;
      height: 100px;
      left: 30%;
      animation-duration: 25s;
    }

    .bubble:nth-child(3) {
      width: 40px;
      height: 40px;
      left: 50%;
      animation-duration: 20s;
    }

    .bubble:nth-child(4) {
      width: 80px;
      height: 80px;
      left: 70%;
      animation-duration: 18s;
    }

    .bubble:nth-child(5) {
      width: 50px;
      height: 50px;
      left: 90%;
      animation-duration: 22s;
    }

    @keyframes rise {
      0% {
        transform: translateY(0) scale(1);
        opacity: 0.6;
      }
      100% {
        transform: translateY(-120vh) scale(1.3);
        opacity: 0;
      }
    }

    header {
      background-color: rgba(255, 227, 227, 0.5);
      padding: 20px;
      text-align: center;
      backdrop-filter: blur(4px);
    }

    header h1 {
      font-family: 'Pacifico', cursive;
      color: #ff6f91;
      font-size: 36px;
      margin: 0;
    }

    section#about {
      max-width: 900px;
      margin: 40px auto;
      padding: 30px;
      color: #4b2e2e;
    }

    section#about h2 {
      color: #ff6f91;
      border-left: 6px solid #ffd6dc;
      padding-left: 10px;
      font-size: 24px;
      margin-bottom: 15px;
    }

    section#about p {
      line-height: 1.8;
      margin-bottom: 20px;
      background: rgba(255, 255, 255, 0); /* fully transparent */
    }

    strong {
      color: #f25378;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 14px;
      color: #aaa;
    }

    footer p {
      margin: 0;
    }
  </style>
</head>
<body>

<!-- BUBBLE BACKGROUND -->
<div class="bubble-container">
  <div class="bubble"></div>
  <div class="bubble"></div>
  <div class="bubble"></div>
  <div class="bubble"></div>
  <div class="bubble"></div>
</div>

<header>
  <h1>CutieCart 🌸</h1>
</header>

<section id="about">
  <h2>About Us</h2>
  <p>
    At <strong>CutieCart</strong>, we believe that true beauty begins with nature. Our products are thoughtfully crafted using ingredients sourced directly from nature’s lap — from organic rose petals and aloe vera to wild turmeric and essential plant oils. We’re passionate about empowering natural beauty and avoiding harsh chemicals or artificial additives.
  </p>
  <p>
    Our journey began with a simple idea: that everyone deserves skincare and beauty products that are both effective and gentle. That’s why each product is designed to enhance your glow naturally — whether it’s a soothing hibiscus hair oil or a refreshing cucumber face mist.
  </p>
  <p>
    We promote a lifestyle where self-care meets sustainability. Every bottle you receive is a step toward loving your skin just the way it is — fresh, radiant, and naturally beautiful. 💕
  </p>

  <h2>Our Mottos</h2>
  <p>
    Launched in <strong>2025</strong>, <strong>CutieCart</strong> was born out of a dream — a dream to celebrate natural beauty in its purest form. Our founders believed that true radiance comes from within, and that nature holds all the secrets to glowing skin and lush hair.
  </p>
  <p>
    At CutieCart, we handpick ingredients that are as kind to your skin as they are to the Earth. Our formulations use natural sources like hibiscus, sandalwood, tulsi, rose, neem, and more — all blended to bring out the best in your beauty. We say no to chemicals, parabens, and cruelty, and yes to clean, green beauty that works.
  </p>
  <p>
    Our mission is simple: to empower every individual to feel confident in their own skin. Whether it's our herbal face packs, fruit-based scrubs, or handmade lip balms, each product is made with love, care, and a whole lot of nature.
  </p>
  <p>
    Join us in celebrating the beauty that blooms naturally. Because at CutieCart, we believe that every person is already beautiful — we’re just here to help it shine through.
  </p>
</section>

<footer>
  <p>© 2025 CutieCart. All rights reserved.</p>
</footer>

</body>
</html>
#auth page
<!-- templates/gorgeous/auth.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Welcome to CutieCart</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #f5f3f4, #c25f8d);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
        }

        .auth-container {
            background: #fabed6;
            padding: 2rem 2.5rem;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.1);
            width: 400px;
            text-align: center;
            position: relative;
        }

        h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 32px;
            color:rgb(205, 61, 205);
            margin-bottom: 0.5rem;
        }

        .quote {
            font-size: 15px;
            color: #030200;
            font-style:times;
            margin-bottom: 1.5rem;
        }

        input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 10px;
            font-size: 14px;
        }

        button {
            background-color: #fa038ff2;
            color: white;
            padding: 12px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            width: 100%;
            font-size: 16px;
            position: relative;
        }

        button:hover {
            background-color: #c7f0ff;
        }

        .butterfly {
            position: absolute;
            width: 40px;
            height: 40px;
            left: 50%;
            top: -60px;
            transform: translateX(-50%);
            opacity: 0;
            pointer-events: none;
            animation: floatUp 2s forwards;
        }

        @keyframes floatUp {
            0% { transform: translateY(0); opacity: 0; }
            50% { transform: translateY(-15px); opacity: 1; }
            100% { transform: translateY(-30px); opacity: 0; }
        }

        /* Success popup */
        .popup {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #e09ff6;
            color: #f8106d;
            padding: 15px 20px;
            border-radius: 10px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
            font-size: 14px;
            display: none;
            z-index: 999;
        }
    </style>
</head>
<body>
    <div class="popup" id="popup">🦋 Hello beautiful, you are successfully logged in!</div>

    <div class="auth-container">
        <h1>Welcome to CutieCart...</h1>
        <p class="quote">“Your beauty journey starts here...”</p>

        <form method="POST" action="{% url 'handle_auth' %}" id="authForm">
            {% csrf_token %}
            <input type="text" name="username" placeholder="Username" required>
            {% if not login_mode %}
                <input type="email" name="email" placeholder="Email" required>
            {% endif %}
            <input type="password" name="password" placeholder="Password" required>
            <button type="submit">Login / Sign Up</button>
            <img src="https://s3.amazonaws.com/pix.iemoji.com/images/emoji/apple/ios-12/256/butterfly.png" class="butterfly" id="butterfly">
            {% if error %}
                <p style="color: rgb(62, 1, 203);">{{ error }}</p>
            {% endif %}
        </form>
    </div>

    <script>
        const button = document.querySelector('button');
        const butterfly = document.getElementById('butterfly');
        const popup = document.getElementById('popup');

        button.addEventListener('click', () => {
            butterfly.style.opacity = 1;
            butterfly.style.animation = 'floatUp 2s';

            setTimeout(() => {
                butterfly.style.opacity = 0;
            }, 2000);
        });

        // Show success popup after redirect from login/signup
        {% if request.GET.success %}
        window.addEventListener('load', () => {
            popup.style.display = 'block';
            setTimeout(() => {
                popup.style.display = 'none';
            }, 4000);
        });
        {% endif %}
    </script>
</body>
</html>
<! skin care> 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Know Your Skin Type | CutieCart</title>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      background: linear-gradient(to bottom, #ffb6c1, #ffe6f0);
      overflow: hidden;
      position: relative;
      color: #4b2e2e;
    }

    .pink-light {
      position: absolute;
      width: 100px;
      height: 100px;
      background: radial-gradient(circle, rgba(255,192,203,0.5) 0%, rgba(255,182,193,0) 70%);
      border-radius: 50%;
      filter: blur(20px);
      animation: floatLight 20s ease-in-out infinite alternate;
      pointer-events: none;
      z-index: 1;
    }

    @keyframes floatLight {
      0% { transform: translateY(0px) translateX(0px); opacity: 0.4; }
      100% { transform: translateY(60px) translateX(30px); opacity: 0.8; }
    }

    .sparkle {
      position: absolute;
      width: 5px;
      height: 5px;
      background: white;
      border-radius: 50%;
      box-shadow: 0 0 10px #fff;
      animation: sparkle 6s linear infinite;
      pointer-events: none;
    }

    @keyframes sparkle {
      0% { transform: translateY(-10px); opacity: 1; }
      100% { transform: translateY(110vh); opacity: 0; }
    }

    .container {
      position: relative;
      z-index: 2;
      max-width: 600px;
      margin: 80px auto;
      padding: 40px;
      background: rgba(255, 255, 255, 0.3);
      backdrop-filter: blur(10px);
      border-radius: 16px;
      box-shadow: 0 8px 24px rgba(255, 182, 193, 0.3);
    }

    h1 {
      text-align: center;
      color: #ff6f91;
      margin-bottom: 30px;
      font-size: 32px;
    }

    form label {
      display: block;
      margin-bottom: 10px;
      font-weight: 600;
    }

    form select, form input[type="submit"] {
      width: 100%;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ffd6dc;
      margin-bottom: 20px;
      background: #fff0f6;
    }

    form input[type="submit"] {
      background-color: #ff6f91;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s ease;
    }

    form input[type="submit"]:hover {
      background-color: #ff3c72;
    }

    .result-popup {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background: #fff0f6;
      border: 3px solid #ffb6c1;
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 0 20px #ffb6c1;
      z-index: 999;
      text-align: center;
      font-weight: bold;
      color: #d62862;
      font-size: 20px;
    }

    .confetti {
      position: absolute;
      width: 10px;
      height: 10px;
      background-color: #ff6f91;
      animation: confetti-fall 3s linear infinite;
    }

    @keyframes confetti-fall {
      0% {
        transform: rotate(0deg) translateY(-10px);
        opacity: 1;
      }
      100% {
        transform: rotate(360deg) translateY(100vh);
        opacity: 0;
      }
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 14px;
      color: #aaa;
    }
  </style>
</head>
<body>

<!-- Background Light and Sparkles -->
<div class="pink-light" style="top: 10%; left: 10%; animation-delay: 0s;"></div>
<div class="pink-light" style="top: 50%; left: 80%; animation-delay: 2s;"></div>
<div class="pink-light" style="top: 70%; left: 30%; animation-delay: 4s;"></div>
<div class="pink-light" style="top: 20%; left: 60%; animation-delay: 1s;"></div>

<!-- Sparkles -->
<script>
  for (let i = 0; i < 40; i++) {
    const sparkle = document.createElement('div');
    sparkle.className = 'sparkle';
    sparkle.style.left = `${Math.random() * 100}%`;
    sparkle.style.animationDuration = `${4 + Math.random() * 3}s`;
    sparkle.style.animationDelay = `${Math.random() * 5}s`;
    document.body.appendChild(sparkle);
  }
</script>

<!-- Main Content -->
<div class="container">
  <h1>✨ Know Your Skin Type ✨</h1>
  <form id="skinForm">
    <label for="oil">Does your skin feel oily after a few hours?</label>
    <select id="oil">
      <option>Yes, very oily</option>
      <option>Somewhat oily</option>
      <option>No, not oily</option>
    </select>

    <label for="dry">Does your skin feel dry or tight?</label>
    <select id="dry">
      <option>Yes, very dry</option>
      <option>Sometimes</option>
      <option>No, it feels balanced</option>
    </select>

    <label for="sensitive">Is your skin sensitive to products or weather?</label>
    <select id="sensitive">
      <option>Yes, very sensitive</option>
      <option>A little sensitive</option>
      <option>No, it's fine</option>
    </select>

    <input type="submit" value="Show My Skin Type 💖" />
  </form>
</div>

<!-- Result Popup -->
<div class="result-popup" id="resultPopup"></div>

<footer>
  <p>© 2025 CutieCart. Glowing with love ✨</p>
</footer>

<script>
  document.getElementById('skinForm').addEventListener('submit', function(e) {
    e.preventDefault();

    const oil = document.getElementById('oil').value;
    const dry = document.getElementById('dry').value;
    const sensitive = document.getElementById('sensitive').value;

    let result = "You have a ";

    if (oil === "Yes, very oily" && dry !== "Yes, very dry") {
      result += "Oily Skin Type 🌟";
    } else if (dry === "Yes, very dry" && oil !== "Yes, very oily") {
      result += "Dry Skin Type 💧";
    } else if (oil === "Somewhat oily" && dry === "Sometimes") {
      result += "Combination Skin Type 🌈";
    } else {
      result += "Normal/Balanced Skin Type 🍃";
    }

    if (sensitive === "Yes, very sensitive") {
      result += " with high sensitivity 🚨";
    } else if (sensitive === "A little sensitive") {
      result += " with some sensitivity ⚠️";
    }

    const popup = document.getElementById('resultPopup');
    popup.innerText = result;
    popup.style.display = 'block';

    // Confetti
    for (let i = 0; i < 50; i++) {
      const confetti = document.createElement('div');
      confetti.className = 'confetti';
      confetti.style.left = `${Math.random() * 100}%`;
      confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 80%, 70%)`;
      confetti.style.animationDuration = `${2 + Math.random() * 2}s`;
      document.body.appendChild(confetti);

      setTimeout(() => confetti.remove(), 4000);
    }

    // Auto-hide popup after 7 seconds
    setTimeout(() => {
      popup.style.display = 'none';
    }, 7000);
  });
</script>

</body>
</html>



