<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ditya Lights & Decore</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Roboto', sans-serif;
    }

    body {
      background-color: #fdfdfd;
      color: #333;
      line-height: 1.6;
    }

    header {
      background: #b30000;
      color: #fff;
      padding: 20px 0;
      text-align: center;
    }

    header h1 {
      font-size: 2.5rem;
    }

    header nav {
      margin-top: 10px;
    }

    header nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
    }

    section {
      padding: 40px 20px;
      max-width: 1200px;
      margin: auto;
    }

    #home {
      background: #ffe6e6;
      text-align: center;
    }

    .product-list {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      justify-content: center;
    }

    .product {
      background: #fff;
      border: 1px solid #ddd;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.05);
      padding: 20px;
      width: 250px;
      text-align: center;
    }

    .product img {
      max-width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 5px;
    }

    #contact {
      background: #f0f0f0;
      text-align: center;
    }

    footer {
      background: #333;
      color: #fff;
      text-align: center;
      padding: 15px 0;
    }

    .pay-section {
      text-align: center;
      margin-top: 30px;
    }

    .pay-button {
      background: #b30000;
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 16px;
      border-radius: 5px;
      cursor: pointer;
    }

    .pay-button:hover {
      background: #8c0000;
    }
  </style>
</head>
<body>
  <header>
    <h1>Ditya Lights & Decore</h1>
    <p>Brighten Your World!</p>
    <nav>
      <a href="#home">Home</a>
      <a href="#products">Products</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="home">
    <h2>Welcome to Ditya Lights & Decore</h2>
    <p>Your one-stop shop for all lighting and electronics needs!</p>
  </section>

  <section id="products">
    <h2 style="text-align:center; margin-bottom: 30px;">Our Products</h2>
    <div class="product-list">
      <div class="product">
        <img src="https://via.placeholder.com/250x180?text=LED+Bulb" alt="LED Bulb">
        <h3>LED Bulb</h3>
        <p>Price: ₹100</p>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/250x180?text=Wall+Light" alt="Wall Light">
        <h3>Wall Light</h3>
        <p>Price: ₹350</p>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/250x180?text=Tube+Light" alt="Tube Light">
        <h3>Tube Light</h3>
        <p>Price: ₹250</p>
      </div>
      <div class="product">
        <img src="https://via.placeholder.com/250x180?text=POP+Light" alt="POP Light">
        <h3>POP Light</h3>
        <p>Price: ₹450</p>
      </div>
    </div>
  </section>

  <section class="pay-section">
    <h2>Pay Now</h2>
    <p>Click below to pay ₹500 for your selected products.</p>
    <button class="pay-button" onclick="payNow()">Pay ₹500</button>
  </section>

  <section id="contact">
    <h2>Contact Us</h2>
    <p>📞 Rohit: 7400602221 / 8959889772</p>
    <p>📍 In front of State Bank of India</p>
    <p>💬 WhatsApp available</p>
  </section>

  <footer>
    <p>&copy; 2025 Ditya Lights & Decore. All rights reserved.</p>
  </footer>

  <script src="https://checkout.razorpay.com/v1/checkout.js"></script>
  <script>
    function payNow() {
      var options = {
        "key": "rzp_test_T1zwYJk2585tqQ", // Replace with your Razorpay test key
        "amount": 5, // 50000 paise = ₹500
        "currency": "INR",
        "name": "Ditya Lights & Decore",
        "description": "Payment for your order",
        "image": "https://via.placeholder.com/100x100?text=Ditya",
        "handler": function (response) {
          alert("Payment Successful. Razorpay ID: " + response.razorpay_payment_id);
        },
        "prefill": {
          "name": "Rakesh",
          "email": "rm5639830@gmail.com",
          "contact": "8871646301"
        },
        "theme": {
          "color": "#b30000"
        }
      };
      var rzp = new Razorpay(options);
      rzp.open();
    }
  </script>
</body>
</html>
