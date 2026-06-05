<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>ProZvon | Обзвоны для CR:MP & SA:MP</title>
    <style>
        :root {
            --bg-gradient-start: #0a0f1e;
            --bg-gradient-end: #0f172a;
            --card-bg-start: #1e293b;
            --card-bg-end: #0f172a;
            --border-color: #334155;
            --text-main: #cbd5e1;
            --text-muted: #94a3b8;
            --text-dark: #0f172a;
            --price-bg: linear-gradient(135deg, #00d4ff, #7c3aed);
            --discount-bg: linear-gradient(135deg, #ffaa00, #ff6600);
            --vk-bg: linear-gradient(135deg, #2787F5, #1a6bc4);
            --payment-bg: rgba(0, 212, 255, 0.1);
        }
        body.light {
            --bg-gradient-start: #f0f4f8;
            --bg-gradient-end: #d9e2ec;
            --card-bg-start: #ffffff;
            --card-bg-end: #f8fafc;
            --border-color: #cbd5e1;
            --text-main: #1e293b;
            --text-muted: #475569;
            --text-dark: #ffffff;
            --price-bg: linear-gradient(135deg, #0f8b9f, #5b2bc7);
            --discount-bg: linear-gradient(135deg, #e69500, #cc5500);
            --vk-bg: linear-gradient(135deg, #1a6bc4, #0f5096);
            --payment-bg: rgba(0, 100, 120, 0.1);
        }
        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, var(--bg-gradient-start), var(--bg-gradient-end));
            padding: 40px 20px;
            min-height: 100vh;
            transition: background 0.3s ease;
        }

        .container { max-width: 800px; margin: 0 auto; }

        .theme-switch {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--card-bg-start);
            border: 1px solid var(--border-color);
            border-radius: 50px;
            padding: 8px 16px;
            cursor: pointer;
            z-index: 1000;
            font-size: 1.2em;
            transition: 0.2s;
            color: var(--text-main);
        }
        .theme-switch:hover { transform: scale(1.05); background: var(--price-bg); color: white; }

        .header { text-align: center; margin-bottom: 30px; }
        .logo {
            font-size: 3em;
            font-weight: 800;
            background: linear-gradient(135deg, #00d4ff 0%, #7c3aed 100%);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 2px;
        }
        .logo span {
            font-size: 0.5em;
            color: var(--text-muted);
            display: block;
        }
        .tagline {
            color: var(--text-muted);
            margin-top: 10px;
            font-size: 0.9em;
            border-top: 1px solid var(--border-color);
            display: inline-block;
            padding-top: 12px;
        }

        .online-counter {
            background: var(--payment-bg);
            border: 1px solid #00d4ff;
            border-radius: 40px;
            padding: 8px 20px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            margin: 15px auto;
            width: fit-content;
        }
        .online-dot {
            width: 10px;
            height: 10px;
            background: #00ff88;
            border-radius: 50%;
            animation: pulse 1.5s infinite;
        }
        @keyframes pulse {
            0% { opacity: 0.5; transform: scale(0.8); }
            100% { opacity: 1; transform: scale(1.2); }
        }
        .online-text { color: var(--text-main); font-size: 0.85em; }

        .discount-banner {
            background: var(--discount-bg);
            border-radius: 20px;
            padding: 12px 20px;
            margin: 20px 0;
            text-align: center;
            color: var(--text-dark);
            font-weight: bold;
            box-shadow: 0 0 20px rgba(255,170,0,0.3);
            animation: glow 2s infinite;
        }
        @keyframes glow {
            0% { box-shadow: 0 0 10px rgba(255,170,0,0.3); }
            50% { box-shadow: 0 0 25px rgba(255,170,0,0.6); }
            100% { box-shadow: 0 0 10px rgba(255,170,0,0.3); }
        }
        .discount-banner span { font-size: 1.3em; }

        .top-contact { text-align: center; margin: 15px 0; }
        .top-vk-link {
            display: inline-block;
            background: var(--vk-bg);
            color: white;
            padding: 10px 25px;
            border-radius: 40px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.2s;
            animation: subtlePulse 2s infinite;
        }
        @keyframes subtlePulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.02); }
            100% { transform: scale(1); }
        }
        .top-vk-link:hover { transform: scale(1.05); animation: none; }

        .counter-block {
            background: linear-gradient(135deg, var(--card-bg-start), var(--card-bg-end));
            border: 1px solid var(--border-color);
            border-radius: 60px;
            padding: 15px 25px;
            margin: 20px auto;
            max-width: 320px;
            text-align: center;
        }
        .counter-number { font-size: 2.8em; font-weight: 800; color: #00d4ff; line-height: 1; }
        .counter-text { color: var(--text-muted); font-size: 0.75em; }

        .service-card {
            background: linear-gradient(135deg, var(--card-bg-start), var(--card-bg-end));
            border: 1px solid var(--border-color);
            padding: 20px;
            margin: 16px 0;
            border-radius: 20px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        .service-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 4px;
            height: 100%;
            background: linear-gradient(135deg, #00d4ff, #7c3aed);
        }
        .service-card:hover { transform: translateY(-3px); border-color: #00d4ff; }
        
        .service-card.hot { border: 1px solid #ffaa00; background: linear-gradient(135deg, #2a1e3a, #1a1528); }
        body.light .service-card.hot { background: linear-gradient(135deg, #fff3e0, #ffe6cc); }
        .hot-badge {
            position: absolute;
            top: 12px;
            right: 12px;
            background: var(--discount-bg);
            color: var(--text-dark);
            font-weight: bold;
            padding: 4px 12px;
            border-radius: 30px;
            font-size: 0.7em;
        }
        .service-card h3 { color: #00d4ff; font-size: 1.25em; margin-bottom: 10px; padding-right: 100px; }
        .service-card p { color: var(--text-main); margin-bottom: 15px; }
        
        .price-block { display: flex; align-items: center; gap: 12px; flex-wrap: wrap; margin-top: 5px; }
        .old-price { color: var(--text-muted); text-decoration: line-through; font-size: 0.9em; }
        .price { background: var(--price-bg); color: white; font-weight: bold; padding: 5px 16px; border-radius: 30px; font-size: 1em; }
        .discount-badge { background: #ffaa00; color: #0f172a; padding: 2px 10px; border-radius: 30px; font-size: 0.7em; font-weight: bold; }

        .order-btn {
            background: rgba(0, 212, 255, 0.15);
            border: 1px solid #00d4ff;
            color: #00d4ff;
            padding: 8px 20px;
            border-radius: 40px;
            font-size: 0.85em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s;
            margin-top: 15px;
            width: 100%;
        }
        .order-btn:hover { background: #00d4ff; color: #0f172a; transform: scale(0.98); }

        .category { margin-top: 30px; margin-bottom: 10px; opacity: 0; transform: translateX(-20px); transition: all 0.5s ease; }
        .category.visible { opacity: 1; transform: translateX(0); }
        .category-title { color: var(--text-muted); font-size: 0.75em; text-transform: uppercase; letter-spacing: 2px; }
        .service-card { opacity: 0; transform: translateY(30px); transition: all 0.6s ease; }
        .service-card.visible { opacity: 1; transform: translateY(0); }

        .guarantee, .reviews, .contact, .security, .daily-tip {
            background: linear-gradient(135deg, var(--card-bg-start), var(--card-bg-end));
            border: 1px solid var(--border-color);
            border-radius: 24px;
            padding: 20px;
            margin: 25px 0;
            text-align: center;
        }
        .guarantee { display: flex; align-items: center; justify-content: center; gap: 15px; flex-wrap: wrap; }
        .guarantee-icon { font-size: 2.5em; }
        .guarantee-text strong { color: #00d4ff; }

        .security-icons { display: flex; justify-content: center; gap: 25px; flex-wrap: wrap; margin-top: 15px; }
        .security-icons span { font-size: 2.2em; filter: grayscale(0.2); transition: 0.2s; }
        .security-text { color: var(--text-muted); font-size: 0.8em; margin-top: 12px; }

        .daily-tip {
            background: linear-gradient(135deg, rgba(0,212,255,0.1), rgba(124,58,237,0.1));
            border: 1px dashed #00d4ff;
        }
        .daily-tip .tip-icon { font-size: 1.5em; margin-bottom: 8px; }
        .daily-tip .tip-text { color: var(--text-main); font-size: 0.9em; font-style: italic; }

        .reviews h3 { color: var(--text-main); margin-bottom: 15px; }
        .review-card {
            background: rgba(255,255,255,0.05);
            padding: 12px;
            border-radius: 16px;
            margin-bottom: 12px;
            text-align: left;
        }
        body.light .review-card { background: rgba(0,0,0,0.05); }
        .review-author { color: #00d4ff; font-weight: bold; }
        .review-text { color: var(--text-main); font-size: 0.85em; font-style: italic; }
        .review-stars { color: #ffaa00; font-size: 0.8em; margin-top: 5px; }

        .contact h3 {
            font-size: 1.4em;
            margin-bottom: 15px;
            background: linear-gradient(135deg, #00d4ff, #7c3aed);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        .contact-item { display: flex; align-items: center; justify-content: center; gap: 12px; margin: 12px 0; flex-wrap: wrap; }
        .contact-item .label { color: var(--text-muted); font-weight: 500; }
        .vk-link {
            background: var(--vk-bg);
            color: white;
            padding: 8px 20px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
        }
        .payment-info {
            background: var(--payment-bg);
            border: 1px dashed #00d4ff;
            border-radius: 40px;
            padding: 8px 16px;
            display: inline-block;
            color: #00d4ff;
            font-size: 0.85em;
        }
        .footer { text-align: center; margin-top: 20px; color: var(--text-muted); font-size: 0.7em; }

        .floating-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: linear-gradient(135deg, #00d4ff, #7c3aed);
            color: white;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8em;
            text-decoration: none;
            box-shadow: 0 5px 20px rgba(0,212,255,0.4);
            z-index: 999;
            transition: all 0.2s;
        }
        .floating-btn:hover { transform: scale(1.1); }

        /* Всплывающее уведомление */
        .notification {
            position: fixed;
            bottom: 100px;
            left: 20px;
            background: linear-gradient(135deg, #1e293b, #0f172a);
            border-left: 4px solid #00d4ff;
            border-radius: 16px;
            padding: 12px 20px;
            color: #cbd5e1;
            font-size: 0.85em;
            z-index: 1000;
            box-shadow: 0 4px 15px rgba(0,0,0,0.3);
            animation: slideIn 0.5s ease, fadeOut 0.5s ease 4s forwards;
            pointer-events: none;
            max-width: 280px;
        }
        .notification span { color: #00d4ff; font-weight: bold; }
        @keyframes slideIn {
            from { opacity: 0; transform: translateX(-50px); }
            to { opacity: 1; transform: translateX(0); }
        }
        @keyframes fadeOut {
            to { opacity: 0; visibility: hidden; }
        }

        .toast {
            position: fixed;
            bottom: 90px;
            right: 20px;
            background: #00d4ff;
            color: #0f172a;
            padding: 8px 16px;
            border-radius: 40px;
            font-size: 0.8em;
            z-index: 1000;
            animation: fadeOut 2s ease forwards;
        }

        @media (max-width: 600px) {
            body { padding: 20px 15px; }
            .logo { font-size: 2.2em; }
            .service-card h3 { font-size: 1em; padding-right: 80px; }
            .counter-number { font-size: 2em; }
        }
    </style>
</head>
<body>
    <div class="theme-switch" id="themeToggle">🌙 Светлая тема</div>

<div class="container">
    <div class="header">
        <div class="logo">
            ProZvon
            <span>Проведем вас на любую должность</span>
        </div>
        <div class="tagline">⚡ Дешёвые и качественные обзвоны для CR:MP / SA:MP проектов ⚡</div>
    </div>

    <div style="display: flex; justify-content: center;">
        <div class="online-counter">
            <div class="online-dot"></div>
            <div class="online-text">👥 4 человека сейчас на сайте</div>
        </div>
    </div>

    <div class="discount-banner">
        🎁 <span>Скидка 20% на все услуги!</span> 🎁<br>
        Промокод: <span style="background:#0f172a; padding:2px 10px; border-radius:30px; color:#ffaa00;">PROZVON20</span>
    </div>

    <div class="top-contact">
        <a href="https://vk.com/im/convo/-239353201?entrypoint=list_all" target="_blank" class="top-vk-link">📱 Связаться сейчас →</a>
    </div>

    <div class="counter-block">
        <div class="counter-number" id="orderCounter">0</div>
        <div class="counter-text">✅ Успешно проведённых обзвонов</div>
    </div>

    <div class="guarantee">
        <div class="guarantee-icon">🛡️</div>
        <div class="guarantee-text"><strong>Гарантия возврата</strong><br>Не прошёл обзвон – вернём деньги</div>
    </div>

    <div class="security">
        <div style="font-size: 1.3em; margin-bottom: 8px;">🔒 Безопасность платежей</div>
        <div class="security-icons">
            <span>💳</span> <span>🛡️</span> <span>🔐</span> <span>✅</span>
        </div>
        <div class="security-text">
            Данные защищены. Оплата через надёжные серверы.<br>
            Никакая информация не передаётся третьим лицам.
        </div>
    </div>

    <!-- СЛУЧАЙНЫЙ СОВЕТ ДНЯ -->
    <div class="daily-tip" id="dailyTip">
        <div class="tip-icon">💡</div>
        <div class="tip-text" id="tipText">Загрузка совета...</div>
    </div>

    <!-- УСЛУГИ -->
    <div class="category"><div class="category-title">▸ АДМИНИСТРАЦИЯ</div></div>
    
    <div class="service-card" data-position="администратора Black Russia" data-price="99">
        <h3>Обзвон на пост администратора Black Russia</h3>
        <p>Полное прохождение собеседования. Гарантия успеха.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice1"></span>
            <span class="price" id="price1">99 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="service-card" data-position="заместителя куратора / куратора Black Russia" data-price="399">
        <h3>Обзвон на пост заместителя куратора / куратора Black Russia</h3>
        <p>Проход в кураторский состав с гарантией.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice2"></span>
            <span class="price" id="price2">399 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="category"><div class="category-title">▸ 🔥 ПОПУЛЯРНОЕ</div></div>
    
    <div class="service-card hot" data-position="агента поддержки Black Russia" data-price="59">
        <div class="hot-badge">🔥 САМАЯ ПОПУЛЯРНАЯ</div>
        <h3>Обзвон на пост агента службы поддержки Black Russia</h3>
        <p>Успешное прохождение вступительного интервью.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice3"></span>
            <span class="price" id="price3">59 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="category"><div class="category-title">▸ ЛИДЕРЫ И СТАРШИЙ СОСТАВ</div></div>

    <div class="service-card" data-position="лидера ГОСС/ОПГ Black Russia" data-price="99">
        <h3>Обзвон на пост лидера ГОСС/ОПГ Black Russia</h3>
        <p>Поможем занять лидерскую позицию.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice4"></span>
            <span class="price" id="price4">99 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="service-card" data-position="СС ГОСС/ОПГ Black Russia" data-price="67">
        <h3>Обзвон на пост СС ГОСС/ОПГ Black Russia</h3>
        <p>Проход в Старший Состав.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice5"></span>
            <span class="price" id="price5">67 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="category"><div class="category-title">▸ ТЕХНИЧЕСКАЯ ПОДДЕРЖКА</div></div>

    <div class="service-card" data-position="технического специалиста Black Russia" data-price="199">
        <h3>Обзвон на пост технического специалиста Black Russia</h3>
        <p>Помощь в прохождении обзвона.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice6"></span>
            <span class="price" id="price6">199 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="category"><div class="category-title">▸ DISCORD</div></div>

    <div class="service-card" data-position="модератора Discord Black Russia" data-price="67">
        <h3>Обзвон на пост модератора Discord Black Russia</h3>
        <p>Поможем пройти отбор в модерацию Discord-сервера.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice7"></span>
            <span class="price" id="price7">67 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать обзвон</button>
    </div>

    <div class="category"><div class="category-title">▸ ДОПОЛНИТЕЛЬНО</div></div>

    <div class="service-card" data-position="изменение личных данных" data-price="67">
        <h3>Изменение личных данных</h3>
        <p>Безопасная смена данных.</p>
        <div class="price-block">
            <span class="old-price" id="oldPrice8"></span>
            <span class="price" id="price8">67 ₽</span>
            <span class="discount-badge">-20%</span>
        </div>
        <button class="order-btn">📞 Заказать услугу</button>
    </div>

    <div class="reviews">
        <h3>⭐ Отзывы наших клиентов</h3>
        <div class="review-card">
            <div class="review-author">Алексей, администратор</div>
            <div class="review-text">"Прошёл с первого раза. Ребята подготовили отлично!"</div>
            <div class="review-stars">★★★★★</div>
        </div>
        <div class="review-card">
            <div class="review-author">Максим, лидер ОПГ</div>
            <div class="review-text">"Помогли занять лидерку за 2 дня. Спасибо ProZvon!"</div>
            <div class="review-stars">★★★★★</div>
        </div>
    </div>

    <div class="contact">
        <h3>📞 СВЯЗЬ С ProZvon</h3>
        <div class="contact-item">
            <span class="label">📱 ВКонтакте:</span>
            <a href="https://vk.com/im/convo/-239353201?entrypoint=list_all" target="_blank" class="vk-link">Написать в сообщество →</a>
        </div>
        <div class="contact-item">
            <span class="label">💳 Оплата:</span>
            <div class="payment-info">💳 Банковская карта РФ / Криптовалюта</div>
        </div>
        <div class="contact-item">✅ Связь в течение 5 минут</div>
    </div>

    <div class="footer">© 2026 ProZvon — Анонимно. Качественно. Быстро.</div>
</div>

<a href="https://vk.com/im/convo/-239353201?entrypoint=list_all" target="_blank" class="floating-btn">💬</a>

<script>
    // Зачёркнутая цена (+20%)
    function setOldPrice(priceElementId, oldPriceElementId, realPrice) {
        const oldPrice = Math.ceil(realPrice * 1.2);
        document.getElementById(oldPriceElementId).innerText = oldPrice + " ₽";
    }
    setOldPrice('price1', 'oldPrice1', 99);
    setOldPrice('price2', 'oldPrice2', 399);
    setOldPrice('price3', 'oldPrice3', 59);
    setOldPrice('price4', 'oldPrice4', 99);
    setOldPrice('price5', 'oldPrice5', 67);
    setOldPrice('price6', 'oldPrice6', 199);
    setOldPrice('price7', 'oldPrice7', 67);
    setOldPrice('price8', 'oldPrice8', 67);

    // Анимация появления
    const animated = document.querySelectorAll('.service-card, .category, .contact, .reviews, .guarantee, .security, .daily-tip, .online-counter, .discount-banner');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) entry.target.classList.add('visible');
        });
    }, { threshold: 0.1 });
    animated.forEach(el => observer.observe(el));

    // Счётчик заказов
    const counterEl = document.getElementById('orderCounter');
    const target = 147;
    let current = 0;
    const inc = target / 100;
    const timer = setInterval(() => {
        current += inc;
        if (current >= target) {
            counterEl.innerText = target;
            clearInterval(timer);
        } else {
            counterEl.innerText = Math.floor(current);
        }
    }, 20);

    // ========== СЛУЧАЙНЫЙ СОВЕТ ДНЯ ==========
    const tips = [
        "💪 Чаще всего заказывают обзвон на пост Агента поддержки — он самый лёгкий!",
        "🎯 Если хочешь стать лидером ОПГ — подготовься к вопросам про экономику фракции.",
        "📝 Администраторов спрашивают про знание правил — учим их с вами.",
        "⚡ Скидка 20% действует ограниченное время! Не упусти.",
        "💬 Связь с нами в течение 5 минут после сообщения.",
        "🛡️ Гарантируем возврат денег, если не пройдёте обзвон.",
        "🔥 Самый быстрый способ — написать нам прямо сейчас в ВК.",
        "📊 147 успешных обзвонов — доверяют уже много игроков."
    ];
    const randomTip = tips[Math.floor(Math.random() * tips.length)];
    document.getElementById('tipText').innerText = randomTip;

    // ========== ВСПЛЫВАЮЩИЕ УВЕДОМЛЕНИЯ О ЗАКАЗАХ ==========
    const names = ["Алексей", "Максим", "Дмитрий", "Артём", "Иван", "Екатерина", "Анна", "Сергей", "Владимир", "Ольга"];
    const services = ["администратора", "агента поддержки", "лидера ОПГ", "технического специалиста", "модератора Discord", "СС ГОСС"];
    
    function showRandomOrder() {
        const randomName = names[Math.floor(Math.random() * names.length)];
        const randomService = services[Math.floor(Math.random() * services.length)];
        
        const notification = document.createElement('div');
        notification.className = 'notification';
        notification.innerHTML = `📢 <span>${randomName}</span> только что заказал обзвон на пост "${randomService}"!`;
        document.body.appendChild(notification);
        
        setTimeout(() => {
            if (notification && notification.remove) notification.remove();
        }, 4500);
    }
    
    // Первое уведомление через 5 секунд, затем каждые 18-25 секунд
    setTimeout(showRandomOrder, 5000);
    setInterval(showRandomOrder, Math.random() * (25000 - 18000) + 18000);

    // Переключение темы
    const toggleBtn = document.getElementById('themeToggle');
    toggleBtn.addEventListener('click', () => {
        document.body.classList.toggle('light');
        if (document.body.classList.contains('light')) {
            toggleBtn.innerHTML = '🌞 Тёмная тема';
        } else {
            toggleBtn.innerHTML = '🌙 Светлая тема';
        }
    });

    // Копирование и переход в чат
    const chatLink = "https://vk.com/im/convo/-239353201?entrypoint=list_all";
    function showToast(msg) {
        let toast = document.createElement('div');
        toast.className = 'toast';
        toast.innerText = msg;
        document.body.appendChild(toast);
        setTimeout(() => toast.remove(), 2000);
    }
    document.querySelectorAll('.order-btn').forEach(btn => {
        btn.addEventListener('click', (e) => {
            const card = btn.closest('.service-card');
            const pos = card.getAttribute('data-position');
            const message = `Привет, хочу купить обзвон на пост "${pos}" (со скидкой 20% по промокоду PROZVON20)`;
            navigator.clipboard.writeText(message).then(() => {
                showToast("✅ Сообщение скопировано! Вставьте (Ctrl+V) в чат VK");
                window.open(chatLink, '_blank');
            }).catch(() => {
                alert("Чат VK откроется. Скопируйте сообщение:\n" + message);
                window.open(chatLink, '_blank');
            });
        });
    });
</script>
</body>
</html>
