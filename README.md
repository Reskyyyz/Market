# Market
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Buy Social Media Services</title>
  <style>
    body { font-family: Arial; background: #f4f4f4; text-align: center; }
    .container { max-width: 600px; margin: auto; background: white; padding: 30px; border-radius: 10px; }
    h1 { color: #333; }
    input, select { width: 100%; padding: 10px; margin: 10px 0; }
    .price { font-weight: bold; font-size: 18px; margin-top: 10px; }
  </style>
</head>
<body>
  <div class="container">
    <h1>Buy Followers, Likes, Views</h1>
    <form id="orderForm">
      <label>Choose Service</label>
      <select id="service" onchange="updatePrice()">
        <option value="followers">Instagram Followers</option>
        <option value="likes">Instagram Likes</option>
        <option value="views">Instagram Views</option>
      </select>

      <label>Quantity</label>
      <input type="number" id="quantity" value="100" min="100">

      <div class="price" id="priceDisplay">$5.00</div>

      <p>Enter your Instagram/TikTok/YouTube link:</p>
      <input type="text" id="link" required>

      <p>Pay below:</p>
      <!-- Replace this with your actual PayPal.me or PayPal Button -->
      <a href="https://www.paypal.com/myaccount/summary" target="_blank">
        <button type="button">Pay with PayPal</button>
      </a>
    </form>
  </div>

  <script>
    function updatePrice() {
      const service = document.getElementById("service").value;
      const quantity = parseInt(document.getElementById("quantity").value);
      let price = 0;

      if (service === "followers") price = quantity * 0.05;
      if (service === "likes") price = quantity * 0.03;
      if (service === "views") price = quantity * 0.01;

      document.getElementById("priceDisplay").innerText = `$${price.toFixed(2)}`;
    }

    document.getElementById("quantity").addEventListener("input", updatePrice);
  </script>
</body>
</html>
