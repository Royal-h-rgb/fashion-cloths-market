
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CYPRIANS - Online Clothing Store</title>
<style>
/* ====== General Styles ====== */
body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: url('african.jpg') no-repeat center center fixed;
  background-size: cover;
  color: #fff;
}

/* Overlay for readability */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-color: rgba(0,0,0,0.6);
  z-index: 0;
}

/* ====== Header ====== */
header {
  background-color: rgba(0,0,0,0.5);
  padding: 15px 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
  z-index: 1;
}
header h1 {
  color: #00c6ff;
  font-size: 1.8em;
}
header button {
  background: linear-gradient(45deg, #ff7b00, #ff00a8);
  border: none;
  border-radius: 20px;
  padding: 10px 18px;
  color: #fff;
  cursor: pointer;
  font-weight: 600;
  transition: 0.3s;
}
header button:hover {
  background: linear-gradient(45deg, #ff00a8, #ff7b00);
}

/* ====== Shop Section ====== */
.shop {
  padding: 40px;
  position: relative;
  z-index: 1;
}
.shop h2 {
  text-align: center;
  color: #ffcc00;
  font-size: 2em;
  margin-bottom: 30px;
}
.products {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 25px;
}
.product {
  background-color: rgba(255, 255, 255, 0.15);
  border-radius: 10px;
  width: 220px;
  text-align: center;
  padding: 15px;
  transition: transform 0.3s, box-shadow 0.3s;
}
.product:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 15px rgba(255,255,255,0.3);
}
.product img {
  width: 100%;
  height: 230px;
  object-fit: cover;
  border-radius: 8px;
}
.product h3 {
  color: #00e6ff;
}
.product p {
  font-size: 0.9em;
  color: #ddd;
}
.price {
  color: #ffcc00;
  font-weight: bold;
  margin: 8px 0;
}
.cart-btn {
  margin-top: 8px;
  background: linear-gradient(45deg, #00e6ff, #0077ff);
  border: none;
  border-radius: 20px;
  padding: 8px 20px;
  color: white;
  cursor: pointer;
}
.cart-btn:hover {
  background: linear-gradient(45deg, #0077ff, #00e6ff);
}

/* ====== Modal (Pop-up) ====== */
.modal {
  display: none; /* Hidden by default */
  position: fixed;
  z-index: 5;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
  justify-content: center;
  align-items: center;
}
.modal-content {
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 15px;
  padding: 30px;
  width: 90%;
  max-width: 400px;
  text-align: center;
  box-shadow: 0 0 25px rgba(0,0,0,0.5);
  backdrop-filter: blur(10px);
}
.modal-content h2 {
  color: #ffcc00;
  margin-bottom: 15px;
}
.modal-content input {
  width: 80%;
  padding: 10px;
  margin: 10px 0;
  border: none;
  border-radius: 5px;
  font-size: 1em;
}
.modal-content button {
  padding: 10px 25px;
  background: linear-gradient(45deg, #ff7b00, #ff00a8);
  color: white;
  border: none;
  border-radius: 25px;
  font-size: 1em;
  cursor: pointer;
}
.modal-content button:hover {
  background: linear-gradient(45deg, #ff00a8, #ff7b00);
}
.close {
  position: absolute;
  top: 15px;
  right: 25px;
  color: #fff;
  font-size: 28px;
  cursor: pointer;
}

/* ====== Responsive ====== */
@media (max-width: 600px) {
  .products {
    flex-direction: column;
    align-items: center;
  }
}
</style>
</head>
<body>

<!-- Header -->
<header>
  <h1>ROYAL HACKER</h1>

  <h1>CLEAN WEAR AROUND</h1>  <h1>CYPRIAN HUMBLE company</h1>
  <div>
    <button onclick="openModal('loginModal')">Login</button>
    <button onclick="openModal('signupModal')">Sign Up</button>
  </div>
</header>

<!-- Shop Section -->
<section class="shop">
  <h2>Our Latest Collection</h2>
  <div class="products">
    <div class="product">
      <img src="image1.jpg" alt="Item 1">
      <h3>Classic full-african wear</h3>
      <p>A black African full suit.</p>
      <div class="price">ksh.2500.00</div>
      <button class="cart-btn">Add to Cart</button>
    </div>

    <div class="product">
      <img src="image2.jpg" alt="Item 2">
      <h3>classic T-shirt</h3>
      <p>Stylish cream shirt to complete your outfit.</p>
      <div class="price">ksh.1000.00</div>
      <button class="cart-btn">Add to Cart</button>
    </div>

    <div class="product">
      <img src="image3.jpg" alt="Item 3">
      <h3>Summer outfit</h3>
      <p>full wear to shine with.</p>
      <div class="price">ksh.1045.00</div>
      <button class="cart-btn">Add to Cart</button>
    </div>

    <div class="product">
      <img src="image4.jpg" alt="Item 4">
      <h3>Black cotton shirt</h3>
      <p>Durable and elegant black clothing.</p>
      <div class="price">ksh.1280.00</div>
      <button class="cart-btn">Add to Cart</button>
    </div>

    <div class="product">
      <img src="image5.jpg" alt="Item 5">
      <h3>Hooded wear</h3>
      <p>perfect warmth and comfort clothing.</p>
      <div class="price">ksh.1235.00</div>
      <button class="cart-btn">Add to Cart</button>
    </div>
  </div>
</section>

<!-- Login Modal -->
<div id="loginModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('loginModal')">&times;</span>
    <h2>Login</h2>
    <form id="loginForm">
      <input type="text" placeholder="Username" required><br>
      <input type="password" placeholder="Password" required><br>
      <button type="submit">Login</button>
    </form>
  </div>
</div>

<!-- Signup Modal -->
<div id="signupModal" class="modal">
  <div class="modal-content">
    <span class="close" onclick="closeModal('signupModal')">&times;</span>
    <h2>Create Account</h2>
    <form id="signupForm">
      <input type="text" placeholder="Username" required><br>
      <input type="email" placeholder="Email" required><br>
      <input type="password" placeholder="Password" required><br>
      <button type="submit">Sign Up</button>
    </form>
  </div>
</div>

<script>
// ====== Modal Controls ======
function openModal(id) {
  document.getElementById(id).style.display = "flex";
}
function closeModal(id) {
  document.getElementById(id).style.display = "none";
}
window.onclick = function(e) {
  if (e.target.classList.contains('modal')) {
    e.target.style.display = "none";
  }
};

// ====== Form Handling ======
document.getElementById("loginForm").addEventListener("submit", function(e) {
  e.preventDefault();
  alert("Logged in successfully!");
  closeModal("loginModal");
});
document.getElementById("signupForm").addEventListener("submit", function(e) {
  e.preventDefault();
  alert("Account created successfully!");
  closeModal("signupModal");
});
</script>
</body>
</html>
![african](https://github.com/user-attachments/assets/b8fa6491-6486-43ae-a625-a8e8e2cb4eff)
![image1](https://github.com/user-attachments/assets/9e735ed7-17c8-4f07-882d-286b3646c4b4)
![image2](https://github.com/user-attachments/assets/7402972b-0934-4d2b-8074-d63ba478a295)
![image3](https://github.com/user-attachments/assets/704efbca-da1b-40c2-b257-4e8599bf2eba)
![image4](https://github.com/user-attachments/assets/c981f78d-cf3e-4c84-b97f-93898204521f)
![image5](https://github.com/user-attachments/assets/1329dd89-4435-4359-b34e-94a797030075)


