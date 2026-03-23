# Metrro-shop<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
    <meta name="theme-color" content="#0a0f1e">
    <meta name="description" content="SkwizyShop - магазин предметов Metro Royale для PUBG Mobile. Низкие цены, быстрая доставка.">
    <meta name="keywords" content="PUBG Mobile, Metro Royale, скины, оружие, сопровождение, донат, SkwizyShop">
    <meta name="author" content="SkwizyShop">
    <meta property="og:title" content="SkwizyShop | Metro Royale магазин">
    <meta property="og:description" content="Покупка предметов и сопровождения для Metro Royale по низким ценам">
    <meta property="og:type" content="website">
    <title>SkwizyShop | Metro Royale — Низкие цены!</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background: radial-gradient(circle at 10% 20%, #0a0f1e, #03060c);
            color: #eef2ff;
            padding: 20px;
            min-height: 100vh;
            font-family: system-ui, -apple-system, 'Segoe UI', 'Poppins', 'Inter', 'Roboto', sans-serif;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
        }

        .header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
            margin-bottom: 24px;
            background: rgba(10, 20, 30, 0.8);
            backdrop-filter: blur(12px);
            border-radius: 2rem;
            padding: 16px 28px;
            border: 1px solid rgba(255, 215, 0, 0.3);
            box-shadow: 0 8px 25px rgba(0,0,0,0.4);
        }

        .logo h1 {
            font-size: clamp(1.5rem, 4vw, 2.2rem);
            background: linear-gradient(135deg, #F5AF19, #f0c45a);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }
        .logo p {
            font-size: 0.75rem;
            color: #b9c7d9;
            margin-top: 4px;
        }

        .sale-badge {
            background: #ff4444;
            color: white;
            font-size: 0.7rem;
            padding: 2px 8px;
            border-radius: 20px;
            margin-left: 8px;
            font-weight: bold;
        }

        .cart-icon {
            background: #11161f;
            padding: 10px 24px;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 12px;
            cursor: pointer;
            transition: all 0.2s;
            border: 1px solid #2a3a44;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        }
        .cart-icon:hover {
            background: #1e2a36;
            transform: translateY(-2px);
            border-color: #f5b81b;
        }
        .cart-count {
            background: #f5b81b;
            color: #0a0c15;
            font-weight: bold;
            border-radius: 30px;
            padding: 2px 12px;
            font-size: 1rem;
            min-width: 32px;
            text-align: center;
        }
        .cart-price {
            font-weight: 600;
            background: #00000066;
            padding: 5px 14px;
            border-radius: 32px;
            font-size: 1rem;
        }

        .support-bar {
            display: flex;
            justify-content: flex-end;
            margin-bottom: 20px;
            gap: 15px;
            flex-wrap: wrap;
        }
        .support-card {
            background: rgba(15, 23, 34, 0.9);
            backdrop-filter: blur(8px);
            padding: 8px 20px;
            border-radius: 60px;
            font-size: 0.85rem;
            border: 1px solid #f5b81b55;
            display: inline-flex;
            align-items: center;
            gap: 10px;
            transition: all 0.2s;
        }
        .support-card:hover {
            border-color: #f5b81b;
            transform: translateY(-1px);
        }
        .phone-num, .card-number {
            font-weight: bold;
            color: #f5c542;
            font-family: monospace;
            font-size: 0.9rem;
            letter-spacing: 0.5px;
        }
        .copy-btn {
            background: #2a3a44;
            border: none;
            padding: 5px 14px;
            border-radius: 40px;
            color: white;
            cursor: pointer;
            font-size: 0.7rem;
            transition: 0.1s;
            font-weight: 500;
        }
        .copy-btn:hover {
            background: #f5b81b;
            color: #000;
            transform: scale(1.02);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 24px;
            margin: 30px 0;
        }

        .product-card {
            background: linear-gradient(145deg, #11171f, #0b1017);
            border-radius: 1.8rem;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid #2a3743;
            cursor: pointer;
            position: relative;
        }
        .product-card:hover {
            transform: translateY(-8px);
            border-color: #f5b81b;
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.6);
        }
        .product-img {
            height: 160px;
            background: #1f2a33;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4.5rem;
            border-bottom: 1px solid #2f3e4a;
            transition: 0.2s;
        }
        .product-card:hover .product-img {
            transform: scale(1.02);
        }
        .product-info {
            padding: 1.2rem;
        }
        .product-title {
            font-size: 1.25rem;
            font-weight: 700;
            margin-bottom: 8px;
        }
        .product-category {
            font-size: 0.7rem;
            text-transform: uppercase;
            background: #1e2a32;
            display: inline-block;
            padding: 3px 12px;
            border-radius: 20px;
            color: #cddcec;
            margin-bottom: 10px;
            letter-spacing: 0.5px;
        }
        .product-desc {
            font-size: 0.85rem;
            color: #b0c4de;
            margin: 10px 0;
            line-height: 1.4;
        }
        .price-block {
            display: flex;
            align-items: baseline;
            gap: 10px;
            margin: 12px 0;
            flex-wrap: wrap;
        }
        .product-price {
            font-size: 1.7rem;
            font-weight: bold;
            color: #f5c542;
        }
        .old-price {
            font-size: 1rem;
            color: #888;
            text-decoration: line-through;
        }
        .discount {
            background: #ff4444;
            padding: 2px 8px;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: bold;
        }
        .btn-add {
            background: #f5b81b;
            border: none;
            width: 100%;
            padding: 12px;
            font-weight: bold;
            font-size: 1rem;
            border-radius: 60px;
            color: #0b0f17;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
        }
        .btn-add:hover {
            background: #ffce4a;
            transform: scale(0.98);
            box-shadow: 0 4px 12px rgba(245,184,27,0.4);
        }

        .cart-modal, .payment-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.92);
            backdrop-filter: blur(10px);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        .cart-modal.active, .payment-modal.active { display: flex; }
        .cart-panel, .payment-panel {
            background: linear-gradient(145deg, #0e141f, #0a0f18);
            width: 90%;
            max-width: 700px;
            max-height: 85vh;
            border-radius: 2rem;
            padding: 1.5rem;
            border: 1px solid #ffd966;
            overflow-y: auto;
            box-shadow: 0 30px 50px rgba(0,0,0,0.6);
        }
        .payment-panel {
            max-width: 500px;
            text-align: center;
        }
        .payment-panel h2 {
            color: #f5c542;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        .payment-amount {
            font-size: 2.5rem;
            font-weight: bold;
            background: #00000055;
            padding: 15px;
            border-radius: 1.5rem;
            margin: 20px 0;
            color: #ffdf8c;
        }
        .payment-card-details {
            background: #071017;
            border-radius: 1.2rem;
            padding: 20px;
            margin: 20px 0;
            border: 1px solid #f5b81b55;
        }
        .payment-card-number {
            font-size: 1.4rem;
            font-family: monospace;
            font-weight: bold;
            letter-spacing: 2px;
            background: #00000066;
            padding: 12px;
            border-radius: 1rem;
            margin: 10px 0;
            color: #ffde9c;
            word-break: break-all;
        }
        .payment-support {
            background: #1a2530;
            border-radius: 1rem;
            padding: 12px;
            margin: 15px 0;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }
        .copy-big-btn, .paid-btn, .close-payment-btn {
            border: none;
            padding: 12px 24px;
            border-radius: 60px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }
        .copy-big-btn { background: #f5b81b; color: #0a0c15; margin-top: 10px; }
        .paid-btn { background: #27ae60; color: white; width: 100%; margin-top: 15px; font-size: 1rem; }
        .close-payment-btn { background: #2c3e44; color: white; margin-top: 12px; width: 100%; }
        .copy-big-btn:hover, .paid-btn:hover, .close-payment-btn:hover { transform: translateY(-2px); filter: brightness(1.05); }

        .cart-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 2px solid #2d3e4e;
            padding-bottom: 15px;
            margin-bottom: 20px;
        }
        .close-cart {
            background: none;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            color: #f0c45a;
            transition: 0.2s;
        }
        .close-cart:hover { transform: scale(1.1); color: #ffd966; }
        .cart-items-list {
            max-height: 45vh;
            overflow-y: auto;
            margin: 15px 0;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: #0a111a;
            margin: 10px 0;
            padding: 12px 15px;
            border-radius: 1.2rem;
            border-left: 4px solid #f5b81b;
            transition: 0.2s;
        }
        .cart-item:hover { background: #0f1722; }
        .item-info h4 { font-size: 1rem; font-weight: 600; }
        .item-info small { font-size: 0.75rem; color: #9aaec2; }
        .item-price { font-weight: bold; color: #f5c542; font-size: 1rem; }
        .item-actions button {
            background: #2c3e44;
            border: none;
            color: white;
            font-weight: bold;
            width: 32px;
            height: 32px;
            border-radius: 30px;
            margin: 0 4px;
            cursor: pointer;
            transition: 0.1s;
        }
        .item-actions button:hover { background: #f5b81b; color: #000; }
        .cart-total {
            text-align: right;
            font-size: 1.5rem;
            border-top: 1px solid #2e4a5a;
            padding-top: 15px;
            margin-top: 10px;
            font-weight: bold;
        }
        .payment-section {
            background: #071017;
            border-radius: 1.5rem;
            padding: 1.2rem;
            margin-top: 20px;
        }
        .pay-methods {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            margin: 15px 0;
        }
        .method-btn {
            background: #1b2a33;
            border: none;
            padding: 8px 18px;
            border-radius: 40px;
            color: white;
            cursor: pointer;
            transition: 0.2s;
            font-size: 0.9rem;
        }
        .method-btn.active {
            background: #f5b81b;
            color: #0a0c15;
            font-weight: bold;
        }
        .method-btn:hover { transform: translateY(-2px); background: #2c4a55; }
        .order-btn {
            background: #27ae60;
            width: 100%;
            padding: 14px;
            font-weight: bold;
            border: none;
            border-radius: 60px;
            font-size: 1.1rem;
            color: white;
            cursor: pointer;
            margin-top: 15px;
            transition: 0.2s;
        }
        .order-btn:hover { background: #2ecc71; transform: translateY(-2px); }
        .toast-msg {
            position: fixed;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            background: #1f2c38e6;
            backdrop-filter: blur(12px);
            padding: 12px 28px;
            border-radius: 60px;
            color: #ffdf8c;
            font-weight: bold;
            z-index: 1200;
            border-left: 4px solid gold;
            pointer-events: none;
            font-size: 0.9rem;
            white-space: nowrap;
        }
        .empty-cart {
            text-align: center;
            padding: 40px 20px;
            color: #9aaec2;
            font-size: 1rem;
        }
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            font-size: 0.8rem;
            opacity: 0.7;
            border-top: 1px solid rgba(245,184,27,0.2);
        }
        
        @media (max-width: 768px) {
            body { padding: 12px; }
            .header { padding: 12px 20px; }
            .products-grid { grid-template-columns: repeat(auto-fill, minmax(280px, 1fr)); gap: 18px; }
            .product-title { font-size: 1.1rem; }
            .product-price { font-size: 1.4rem; }
            .cart-item { flex-wrap: wrap; gap: 10px; }
            .item-actions { margin-left: auto; }
            .toast-msg { white-space: normal; text-align: center; max-width: 90%; font-size: 0.85rem; }
        }
        
        @media (min-width: 1400px) {
            .products-grid { grid-template-columns: repeat(4, 1fr); }
        }
        
        ::-webkit-scrollbar { width: 8px; height: 8px; }
        ::-webkit-scrollbar-track { background: #1e2a32; border-radius: 10px; }
        ::-webkit-scrollbar-thumb { background: #f5b81b; border-radius: 10px; }
        ::-webkit-scrollbar-thumb:hover { background: #ffce4a; }
        
        button, .cart-icon, .product-card, .btn-add {
            cursor: pointer;
            user-select: none;
        }
    </style>
</head>
<body>
<div class="container">
    <div class="support-bar">
        <div class="support-card">
            <span>📞</span> Поддержка: <span class="phone-num">+79997818232</span>
            <button class="copy-btn" data-copy="+79997818232">📋 Копировать</button>
        </div>
        <div class="support-card">
            <span>💳</span> Карта: <span class="card-number">2200701230844117</span>
            <button class="copy-btn" data-copy="2200701230844117">📋 Копировать</button>
        </div>
    </div>

    <div class="header">
        <div class="logo">
            <h1>⚡ SKWIZYSHOP <span style="font-size:0.8rem; background:#ff4444; padding:2px 8px; border-radius:20px;">🔥 СУПЕР ЦЕНЫ</span></h1>
            <p>Metro Royale • Сопровождение • Оружие • Реликвии • До -70%</p>
        </div>
        <div class="cart-icon" id="openCartBtn">
            <span>🛒</span>
            <span class="cart-count" id="cartCount">0</span>
            <span class="cart-price" id="cartTotalPreview">0₽</span>
        </div>
    </div>

    <div class="products-grid" id="productsGrid"></div>
    <footer>© SkwizyShop — официальный трансфер Metro Royale. Мгновенная доставка после подтверждения оплаты. Низкие цены только сегодня!</footer>
</div>

<!-- Корзина -->
<div id="cartModal" class="cart-modal">
    <div class="cart-panel">
        <div class="cart-header">
            <h2>🧾 Ваша корзина</h2>
            <button class="close-cart" id="closeCartBtn">&times;</button>
        </div>
        <div id="cartItemsContainer" class="cart-items-list"></div>
        <div class="cart-total" id="cartTotalAmount">Итого: 0₽</div>
        <div class="payment-section">
            <h3>💳 Способ оплаты</h3>
            <div class="pay-methods" id="payMethodsContainer">
                <button data-method="card" class="method-btn active">💳 Банковская карта</button>
                <button data-method="qiwi" class="method-btn">🟣 QIWI / ЮMoney</button>
                <button data-method="crypto" class="method-btn">₿ USDT / Crypto</button>
            </div>
            <div id="paymentInfoMsg" style="font-size:0.8rem; margin: 8px 0; color:#c0d4f0;">💳 Оплата картой 2200701230844117</div>
            <button class="order-btn" id="checkoutBtn">✅ Оформить заказ</button>
        </div>
    </div>
</div>

<!-- Модалка оплаты -->
<div id="paymentModal" class="payment-modal">
    <div class="payment-panel">
        <h2>💸 ОПЛАТА ЗАКАЗА</h2>
        <p>Для завершения покупки переведите сумму на карту</p>
        <div class="payment-amount" id="paymentAmountDisplay">0 ₽</div>
        <div class="payment-card-details">
            <span>💳 Карта получателя:</span>
            <div class="payment-card-number">2200701230844117</div>
            <button class="copy-big-btn" id="copyCardFromPayment">📋 Скопировать номер карты</button>
        </div>
        <div class="payment-support">
            <span>📞 Поддержка:</span>
            <strong>+79997818232</strong>
            <button class="copy-btn" data-copy="+79997818232" style="background:#1f2a33;">Копировать</button>
        </div>
        <p style="font-size:0.75rem; margin: 10px 0;">После оплаты нажмите "Я оплатил(а)", чтобы подтвердить заказ</p>
        <button class="paid-btn" id="confirmPaymentBtn">✅ Я оплатил(а)</button>
        <button class="close-payment-btn" id="closePaymentBtn">✖️ Закрыть</button>
    </div>
</div>

<div id="toast" class="toast-msg" style="display: none;"></div>

<script>
    (function(){
        // Товары с ПОНИЖЕННЫМИ ЦЕНАМИ! Максимально доступные цены
        const PRODUCTS = [
            // Сопровождение — супер цены!
            { id: 1, name: "👥 Страж Метро", category: "Сопровождение", desc: "Надежный телохранитель. Помогает в рейдах, защищает от рейдеров. 1 рейд", price: 49, oldPrice: 199, icon: "🛡️" },
            { id: 2, name: "🔍 Сталкер Теней", category: "Сопровождение", desc: "Разведчик, сканирует тайники, показывает врагов. 2 рейда", price: 69, oldPrice: 299, icon: "🔍" },
            { id: 3, name: "⚡ Быстрый разносчик", category: "Сопровождение", desc: "Ускоряет сбор лута, переносит ценные предметы", price: 59, oldPrice: 249, icon: "⚡" },
            // Оружие Metro Royale — большие скидки
            { id: 4, name: "MK14 'Легенда Метро'", category: "Оружие", desc: "Снайперская винтовка с бронепробитием, х2 модуль", price: 499, oldPrice: 1290, icon: "🔫" },
            { id: 5, name: "Бронекостюм 'Стальной Шторм'", category: "Снаряжение", desc: "Lv.6 бронежилет + шлем. Максимальная защита", price: 349, oldPrice: 890, icon: "🛡️" },
            { id: 6, name: "Рюкзак 'Сектор 7'", category: "Снаряжение", desc: "Увеличенная вместимость + защита от мародеров", price: 199, oldPrice: 490, icon: "🎒" },
            { id: 7, name: "Аптечка 'Феникс' x5", category: "Расходники", desc: "Мгновенное восстановление HP + адреналин", price: 149, oldPrice: 350, icon: "💊" },
            { id: 8, name: "M762 'Золотой Тигр'", category: "Оружие", desc: "Легендарный скин + повышенный урон по боссам", price: 599, oldPrice: 1590, icon: "🐅" },
            { id: 9, name: "Глушитель 'Тень'", category: "Модули", desc: "Бесшумный выстрел + на 15% больше урона", price: 299, oldPrice: 720, icon: "🔇" },
            { id: 10, name: "Экзощит 'Барьер'", category: "Снаряжение", desc: "Баллистический щит для штурма метро", price: 449, oldPrice: 1100, icon: "🛡️" },
            { id: 11, name: "Реликвия Метро", category: "Контейнер", desc: "Гарантированный легендарный лут + эксклюзивные скины", price: 999, oldPrice: 2490, icon: "🎁" },
            { id: 12, name: "Боеприпасы .300 Магнум x60", category: "Расходники", desc: "Улучшенные патроны для снайперских винтовок", price: 149, oldPrice: 420, icon: "💥" },
            { id: 13, name: "Стимулятор 'Адреналин' x3", category: "Расходники", desc: "Мгновенное восстановление выносливости", price: 99, oldPrice: 280, icon: "💉" }
        ];

        let cart = [];
        let currentPaymentMethod = "card";
        let pendingOrderTotal = 0;

        function loadCart() {
            try {
                const saved = localStorage.getItem("skwizy_cart_v5");
                if(saved) {
                    cart = JSON.parse(saved);
                    if(!Array.isArray(cart)) cart = [];
                }
            } catch(e) { cart = []; }
            cart = cart.filter(item => item && typeof item.id === 'number' && item.quantity > 0);
            updateBadge();
        }

        function saveCart() {
            localStorage.setItem("skwizy_cart_v5", JSON.stringify(cart));
            updateBadge();
        }

        function updateBadge() {
            const count = cart.reduce((s, i) => s + i.quantity, 0);
            const total = cart.reduce((s, i) => s + (i.price * i.quantity), 0);
            document.getElementById('cartCount').innerText = count;
            document.getElementById('cartTotalPreview').innerHTML = total + "₽";
        }

        function getTotal() {
            return cart.reduce((s, i) => s + (i.price * i.quantity), 0);
        }

        function showToast(msg, dur = 2500) {
            const toast = document.getElementById('toast');
            toast.innerText = msg;
            toast.style.display = 'block';
            setTimeout(() => { toast.style.display = 'none'; }, dur);
        }

        function addToCart(product) {
            const existing = cart.find(i => i.id === product.id);
            if(existing) existing.quantity++;
            else cart.push({ id: product.id, name: product.name, price: product.price, quantity: 1 });
            saveCart();
            showToast(`✅ ${product.name.split(' ').slice(0,2).join(' ')} добавлен! Всего ${product.price}₽`, 1500);
            if(document.getElementById('cartModal').classList.contains('active')) renderCartModal();
        }

        function updateQty(id, delta) {
            const idx = cart.findIndex(i => i.id === id);
            if(idx === -1) return;
            const newQty = cart[idx].quantity + delta;
            if(newQty <= 0) cart.splice(idx,1);
            else cart[idx].quantity = newQty;
            saveCart();
            renderCartModal();
            if(cart.length === 0 && document.getElementById('cartModal').classList.contains('active')) renderCartModal();
        }

        function renderCartModal() {
            const container = document.getElementById('cartItemsContainer');
            if(!container) return;
            if(cart.length === 0) {
                container.innerHTML = '<div class="empty-cart">🛒 Корзина пуста. Добавьте товары по супер ценам!</div>';
                document.getElementById('cartTotalAmount').innerHTML = 'Итого: 0₽';
                return;
            }
            let html = '<ul style="list-style:none;">';
            cart.forEach(item => {
                const itemTotal = item.price * item.quantity;
                html += `<li class="cart-item">
                    <div class="item-info"><h4>${item.name}</h4><small>${item.price}₽ × ${item.quantity}</small></div>
                    <div class="item-price">${itemTotal}₽</div>
                    <div class="item-actions">
                        <button class="qty-minus" data-id="${item.id}">−</button>
                        <span style="margin:0 8px;">${item.quantity}</span>
                        <button class="qty-plus" data-id="${item.id}">+</button>
                        <button class="qty-remove" data-id="${item.id}" style="background:#aa2e2e;">🗑</button>
                    </div>
                </li>`;
            });
            html += '</ul>';
            container.innerHTML = html;
            document.getElementById('cartTotalAmount').innerHTML = `Итого: ${getTotal()}₽`;

            document.querySelectorAll('.qty-plus').forEach(btn => btn.onclick = () => updateQty(parseInt(btn.dataset.id), 1));
            document.querySelectorAll('.qty-minus').forEach(btn => btn.onclick = () => updateQty(parseInt(btn.dataset.id), -1));
            document.querySelectorAll('.qty-remove').forEach(btn => btn.onclick = () => {
                const id = parseInt(btn.dataset.id);
                const idx = cart.findIndex(i => i.id === id);
                if(idx !== -1) cart.splice(idx,1);
                saveCart();
                renderCartModal();
                updateBadge();
            });
        }

        function openPaymentModal(amount) {
            pendingOrderTotal = amount;
            document.getElementById('paymentAmountDisplay').innerHTML = `${amount} ₽`;
            document.getElementById('paymentModal').classList.add('active');
        }

        function closePaymentModal() {
            document.getElementById('paymentModal').classList.remove('active');
            pendingOrderTotal = 0;
        }

        function confirmPayment() {
            if(pendingOrderTotal <= 0) {
                showToast("Нет активного заказа для подтверждения", 1500);
                closePaymentModal();
                return;
            }
            cart = [];
            saveCart();
            updateBadge();
            renderCartModal();
            closePaymentModal();
            const cartModal = document.getElementById('cartModal');
            if(cartModal.classList.contains('active')) cartModal.classList.remove('active');
            showToast(`✅ Оплата ${pendingOrderTotal}₽ подтверждена! Предметы доставлены в Metro Royale. Спасибо за покупку!`, 5000);
            pendingOrderTotal = 0;
        }

        function processOrder() {
            if(cart.length === 0) {
                showToast("⚠️ Корзина пуста! Добавьте товары перед заказом.", 2000);
                return;
            }
            const total = getTotal();
            const methodText = currentPaymentMethod === 'card' ? 'Банковская карта' : (currentPaymentMethod === 'qiwi' ? 'QIWI' : 'Криптовалюта');
            document.getElementById('cartModal').classList.remove('active');
            openPaymentModal(total);
            showToast(`💸 Заказ на сумму ${total}₽. Оплатите по реквизитам. Способ: ${methodText}`, 4000);
        }

        function renderProducts() {
            const grid = document.getElementById('productsGrid');
            if(!grid) return;
            grid.innerHTML = '';
            PRODUCTS.forEach(prod => {
                const card = document.createElement('div');
                card.className = 'product-card';
                const discountPercent = prod.oldPrice ? Math.round((1 - prod.price/prod.oldPrice) * 100) : 0;
                card.innerHTML = `
                    <div class="product-img">${prod.icon}</div>
                    <div class="product-info">
                        <div class="product-title">${prod.name}</div>
                        <div class="product-category">${prod.category}</div>
                        <div class="product-desc">${prod.desc}</div>
                        <div class="price-block">
                            <span class="product-price">${prod.price} ₽</span>
                            ${prod.oldPrice ? `<span class="old-price">${prod.oldPrice} ₽</span><span class="discount">-${discountPercent}%</span>` : ''}
                        </div>
                        <button class="btn-add" data-id="${prod.id}">➕ В корзину</button>
                    </div>
                `;
                grid.appendChild(card);
                const btn = card.querySelector('.btn-add');
                btn.addEventListener('click', (e) => {
                    e.stopPropagation();
                    addToCart(prod);
                });
            });
        }

        function initEventListeners() {
            document.getElementById('openCartBtn').onclick = () => { renderCartModal(); document.getElementById('cartModal').classList.add('active'); };
            document.getElementById('closeCartBtn').onclick = () => document.getElementById('cartModal').classList.remove('active');
            document.getElementById('cartModal').onclick = (e) => { if(e.target === document.getElementById('cartModal')) e.target.classList.remove('active'); };
            document.getElementById('checkoutBtn').onclick = processOrder;
            
            document.getElementById('closePaymentBtn').onclick = closePaymentModal;
            document.getElementById('confirmPaymentBtn').onclick = confirmPayment;
            document.getElementById('paymentModal').onclick = (e) => { if(e.target === document.getElementById('paymentModal')) closePaymentModal(); };
            document.getElementById('copyCardFromPayment').onclick = () => {
                navigator.clipboard.writeText('2200701230844117').then(() => showToast('💳 Номер карты скопирован!', 1500));
            };
            
            const methods = document.querySelectorAll('.method-btn');
            methods.forEach(btn => {
                btn.onclick = () => {
                    methods.forEach(m => m.classList.remove('active'));
                    btn.classList.add('active');
                    currentPaymentMethod = btn.dataset.method;
                    const msg = document.getElementById('paymentInfoMsg');
                    if(currentPaymentMethod === 'card') msg.innerHTML = '💳 Оплата картой 2200701230844117. Безопасно и быстро.';
                    else if(currentPaymentMethod === 'qiwi') msg.innerHTML = '🟣 Оплата через QIWI, ЮMoney на карту 2200701230844117. Мгновенное зачисление.';
                    else msg.innerHTML = '₿ Криптовалюта USDT (TRC20/BEP20). Реквизиты уточняйте в поддержке.';
                };
            });
            
            document.querySelectorAll('.copy-btn').forEach(btn => {
                btn.onclick = (e) => {
                    e.stopPropagation();
                    const text = btn.getAttribute('data-copy');
                    if(text) navigator.clipboard.writeText(text).then(() => showToast(`📋 Скопировано: ${text}`, 1200));
                };
            });
        }

        function init() {
            loadCart();
            renderProducts();
            initEventListeners();
            console.log("SkwizyShop — цены снижены! Максимальные скидки до 70%");
        }
        
        init();
    })();
</script>
</body>
</html>
