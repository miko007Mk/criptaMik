# criptaMik
crypts
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Моя Криптовалютная Страница</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
            color: #333;
        }
        header {
            text-align: center;
            padding: 20px;
            background-color: #282c34;
            color: white;
        }
        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }
        .slider {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin: 0 auto;
            overflow: hidden;
        }
        .slides {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }
        .slide {
            min-width: 100%;
            box-sizing: border-box;
        }
        .navigation {
            text-align: center;
            margin-top: 10px;
        }
        .navigation button {
            background-color: #282c34;
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            margin: 5px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #282c34;
            color: white;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>
    <h1>Добро пожаловать на страницу о криптовалюте</h1>
</header>

<div class="container">
    <section>
        <h2>О криптовалюте</h2>
        <p>Криптовалюта — это цифровая или виртуальная валюта, защищенная криптографией, что делает практически невозможным подделку или двойное расходование. Криптовалюты работают на технологии блокчейн — децентрализованной сети, основанной на распределенной бухгалтерской книге.</p>
    </section>

    <div class="slider" id="slider">
        <div class="slides" id="slides">
            <div class="slide">
                <h3>Биткойн (BTC)</h3>
                <p>Первая и самая известная криптовалюта, созданная в 2009 году. Считается цифровым золотом.</p>
            </div>
            <div class="slide">
                <h3>Эфириум (ETH)</h3>
                <p>Платформа для децентрализованных приложений, известная своими смарт-контрактами и токенами ERC-20.</p>
            </div>
            <div class="slide">
                <h3>Лайткоин (LTC)</h3>
                <p>Криптовалюта, созданная как улучшенная версия Биткойна, известная быстрыми транзакциями.</p>
            </div>
        </div>
    </div>

    <div class="navigation">
        <button onclick="prevSlide()">Предыдущий</button>
        <button onclick="nextSlide()">Следующий</button>
    </div>
</div>

<footer>
    <p>Контакты: крипта@пример.com</p>
</footer>

<script>
    let currentSlide = 0;

    function showSlide(index) {
        const slides = document.getElementById('slides');
        const totalSlides = document.getElementsByClassName('slide').length;
        if (index >= totalSlides) {
            currentSlide = 0;
        } else if (index < 0) {
            currentSlide = totalSlides - 1;
        } else {
            currentSlide = index;
        }
        slides.style.transform = 'translateX(' + (-currentSlide * 100) + '%)';
    }

    function nextSlide() {
        showSlide(currentSlide + 1);
    }

    function prevSlide() {
        showSlide(currentSlide - 1);
    }
</script>

</body>
</html>
