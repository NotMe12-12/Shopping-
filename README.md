# Shopping-
html


<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cửa Hàng Giày</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background-color: #f8f8f8;
        }
        header {
            background: #333;
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .cart {
            font-size: 18px;
        }
        .products {
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }
        .product {
            background: white;
            padding: 15px;
            margin: 10px;
            border-radius: 8px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            width: 200px;
        }
        .product img {
            width: 100%;
            height: 150px; /* Đặt chiều cao cố định để giao diện đẹp hơn */
            border-radius: 5px;
        }
        button {
            background: #ff5733;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            margin-top: 10px;
        }
        button:hover {
            background: #c70039;
        }
    </style>
</head>
<body>
    <header>
        <h1>Cửa Hàng Giày</h1>
        <div class="cart">🛒 Giỏ hàng: <span id="cart-count">0</span> sản phẩm - <span id="cart-total">0</span>đ</div>
    </header>
    <section class="products">
        <div class="product">
            <img src="https://via.placeholder.com/200x150" alt="Giày Thể Thao">
            <h2>Giày Thể Thao</h2>
            <p>Giá: <span class="price">800000</span>đ</p>
            <button onclick="addToCart(800000)">Mua ngay</button>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/200x150" alt="Giày Da Nam">
            <h2>Giày Da Nam</h2>
            <p>Giá: <span class="price">1200000</span>đ</p>
            <button onclick="addToCart(1200000)">Mua ngay</button>
        </div>
    </section>
    <script>
        let cartCount = 0;
        let cartTotal = 0;

        function addToCart(price) {
            cartCount++;
            cartTotal += price;
            document.getElementById("cart-count").innerText = cartCount;
            document.getElementById("cart-total").innerText = cartTotal.toLocaleString('vi-VN');
            alert("Đã thêm vào giỏ hàng!");
        }
    </script>
</body>
</html>



