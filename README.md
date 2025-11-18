<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RocK Tsunami 2024 - Літній Рок-Фестиваль</title>
    <!-- Підключення Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Налаштування Tailwind для використання яскравих кольорів та градієнтів -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary-neon': '#FF00FF', // Неоновий рожевий
                        'secondary-electric': '#00FFFF', // Електричний блакитний
                        'dark-bg': '#0D0A1F', // Темний фон
                    },
                    backgroundImage: {
                        'hero-gradient': 'linear-gradient(90deg, #FF00FF 0%, #8A2BE2 100%)', // Градієнт для Hero
                        'section-gradient': 'linear-gradient(135deg, #1A1A40 0%, #0D0A1F 100%)',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        /* Стилізація, що додає музичних елементів */
        .music-wave-bg {
            background-image: radial-gradient(rgba(255, 0, 255, 0.2) 1px, transparent 1px),
                              radial-gradient(rgba(0, 255, 255, 0.2) 1px, transparent 1px);
            background-size: 40px 40px;
            background-position: 0 0, 20px 20px;
        }

        /* Додаткові стилі для "інтерактивності" */
        .card-glow:hover {
            box-shadow: 0 0 20px rgba(0, 255, 255, 0.6), 0 0 40px rgba(255, 0, 255, 0.3);
            transform: translateY(-5px);
        }

        /* Стиль для активного елемента FAQ */
        .faq-item[data-open="true"] .faq-answer {
            max-height: 500px;
            padding-bottom: 1.5rem;
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease-in-out, padding-bottom 0.4s ease-in-out;
            padding-bottom: 0;
        }
    </style>
</head>
<body class="bg-dark-bg text-gray-100 font-sans antialiased">

    <!-- Навігація -->
    <header class="sticky top-0 z-50 bg-dark-bg/90 backdrop-blur-sm shadow-xl">
        <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-3xl font-bold bg-clip-text text-transparent bg-hero-gradient">
                RocK Tsunami
            </a>
            <div class="hidden md:flex space-x-6 text-lg">
                <a href="#schedule" class="hover:text-primary-neon transition duration-300">Виступи</a>
                <a href="#artists" class="hover:text-primary-neon transition duration-300">Артисти</a>
                <a href="#map" class="hover:text-primary-neon transition duration-300">Мапа</a>
                <a href="#tickets" class="hover:text-primary-neon transition duration-300">Квитки</a>
                <a href="#gallery" class="hover:text-primary-neon transition duration-300">Галерея</a>
                <a href="#faq" class="hover:text-primary-neon transition duration-300">FAQ</a>
            </div>
            <!-- Кнопка бургер-меню для мобільних пристроїв -->
            <button id="menu-btn" class="md:hidden text-2xl focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>
            </button>
        </nav>
        <!-- Мобільне меню -->
        <div id="mobile-menu" class="hidden md:hidden bg-dark-bg/95">
            <div class="flex flex-col space-y-3 p-4 text-center">
                <a href="#schedule" class="py-2 hover:bg-primary-neon/20 rounded-lg transition duration-300" onclick="closeMenu()">Виступи</a>
                <a href="#artists" class="py-2 hover:bg-primary-neon/20 rounded-lg transition duration-300" onclick="closeMenu()">Артисти</a>
                <a href="#map" class="py-2 hover:bg-primary-neon/20 rounded-lg transition duration-300" onclick="closeMenu()">Мапа</a>
                <a href="#tickets" class="py-2 hover:bg-primary-neon/20 rounded-lg transition duration-300" onclick="closeMenu()">Квитки</a>
                <a href="#gallery" class="py-2 hover:bg-primary-neon/20 rounded-lg transition duration-300" onclick="closeMenu()">Галерея</a>
                <a href="#faq" class="py-2 hover:bg-primary-neon/20 rounded-lg transition duration-300" onclick="closeMenu()">FAQ</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero" class="bg-dark-bg music-wave-bg relative h-screen flex items-center justify-center overflow-hidden">
        <!-- Анімовані елементи - ноти/звукові хвилі (як SVG або псевдоелементи) - тут використаємо іконку та градієнтний фон -->
        <div class="absolute inset-0 bg-hero-gradient opacity-30 mix-blend-screen"></div>

        <div class="container mx-auto text-center z-10 p-6 rounded-xl backdrop-blur-sm">
            <h1 class="text-6xl sm:text-7xl md:text-8xl lg:text-9xl font-extrabold tracking-tight mb-4 leading-tight">
                <span class="bg-clip-text text-transparent bg-gradient-to-r from-primary-neon to-secondary-electric">
                    RocK Tsunami
                </span>
            </h1>
            <p class="text-3xl sm:text-4xl font-light text-white mb-8 italic">
                Найпотужніша хвиля року!
            </p>
            <div class="bg-black/50 p-6 rounded-2xl inline-block shadow-2xl border border-primary-neon/50">
                <h2 class="text-xl sm:text-3xl font-bold mb-2 text-secondary-electric">
                    3 ДНІ ЧИСТОГО РОКУ
                </h2>
                <p class="text-2xl sm:text-4xl font-extrabold text-white">
                    23-25 СЕРПНЯ 2024
                </p>
                <p class="text-lg sm:text-2xl text-gray-300 mt-2">
                    МІСТО КИЇВ, АРТ-ЗАВОД "ПЛАТФОРМА"
                </p>
            </div>
            <a href="#tickets" class="mt-10 inline-block px-12 py-4 text-xl font-bold text-dark-bg rounded-full transition duration-300 transform hover:scale-105 shadow-lg" style="background: linear-gradient(90deg, #00FFFF, #FF00FF);">
                ПРИДБАТИ КВИТКИ
            </a>
        </div>
    </section>

    <!-- Таймлайн виступів (Schedule) -->
    <section id="schedule" class="py-20 bg-section-gradient music-wave-bg">
        <div class="container mx-auto px-4">
            <h2 class="text-5xl font-extrabold text-center mb-16 bg-clip-text text-transparent bg-hero-gradient">
                Таймлайн Виступів
            </h2>

            <div class="space-y-8">
                <!-- День 1 -->
                <div class="bg-dark-bg/70 p-6 rounded-2xl shadow-2xl border border-secondary-electric/30">
                    <h3 class="text-3xl font-bold text-secondary-electric mb-6 text-center">П'ятниця, 23 Серпня - Metal Night</h3>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-lg">
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-primary-neon">18:00</span>
                            <span class="text-white">The Void (UA)</span>
                        </div>
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-primary-neon">19:30</span>
                            <span class="text-white">Iron Heart (PL)</span>
                        </div>
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-primary-neon">21:30</span>
                            <span class="text-white">**Headliner: Chaos Theory (DE)**</span>
                        </div>
                    </div>
                </div>

                <!-- День 2 -->
                <div class="bg-dark-bg/70 p-6 rounded-2xl shadow-2xl border border-primary-neon/30">
                    <h3 class="text-3xl font-bold text-primary-neon mb-6 text-center">Субота, 24 Серпня - Classic Rock</h3>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-lg">
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-secondary-electric">16:00</span>
                            <span class="text-white">Blues Breakers (UA)</span>
                        </div>
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-secondary-electric">18:00</span>
                            <span class="text-white">Echoes of Time (GB)</span>
                        </div>
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-secondary-electric">20:30</span>
                            <span class="text-white">**Headliner: The Ancients (US)**</span>
                        </div>
                    </div>
                </div>

                <!-- День 3 -->
                <div class="bg-dark-bg/70 p-6 rounded-2xl shadow-2xl border border-secondary-electric/30">
                    <h3 class="text-3xl font-bold text-secondary-electric mb-6 text-center">Неділя, 25 Серпня - Alternative & Punk</h3>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-lg">
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-primary-neon">17:00</span>
                            <span class="text-white">Punk Riot (UA)</span>
                        </div>
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-primary-neon">19:00</span>
                            <span class="text-white">Neon Waves (CA)</span>
                        </div>
                        <div class="col-span-1 p-4 bg-gray-900/50 rounded-lg flex items-center justify-between">
                            <span class="font-bold text-primary-neon">21:00</span>
                            <span class="text-white">**Headliner: Digital Decay (FR)**</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Картки артистів -->
    <section id="artists" class="py-20 bg-dark-bg">
        <div class="container mx-auto px-4">
            <h2 class="text-5xl font-extrabold text-center mb-16 bg-clip-text text-transparent bg-hero-gradient">
                Наші Хедлайнери
            </h2>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                <!-- Картка 1 -->
                <div class="card-glow transition duration-500 rounded-3xl overflow-hidden bg-gray-900 shadow-2xl border border-primary-neon/50">
                    <div class="h-64 bg-gray-700 w-full" style="background-image: url('https://placehold.co/600x400/8A2BE2/ffffff?text=Chaos+Theory'); background-size: cover; background-position: center;">
                        <!--  -->
                    </div>
                    <div class="p-6">
                        <h3 class="text-3xl font-bold text-primary-neon mb-2">Chaos Theory (DE)</h3>
                        <p class="text-sm text-secondary-electric mb-4">Деструктивний Метал / П'ятниця</p>
                        <p class="text-gray-300 text-base">
                            Німецькі титани, які розривають світові сцени своєю енергією та технічністю. Їхнє шоу - це чистий хаос, контрольований гітарними рифами, що не залишає шансів на спокій.
                        </p>
                    </div>
                </div>

                <!-- Картка 2 -->
                <div class="card-glow transition duration-500 rounded-3xl overflow-hidden bg-gray-900 shadow-2xl border border-secondary-electric/50">
                    <div class="h-64 bg-gray-700 w-full" style="background-image: url('https://placehold.co/600x400/00FFFF/0D0A1F?text=The+Ancients'); background-size: cover; background-position: center;">
                        <!--  -->
                    </div>
                    <div class="p-6">
                        <h3 class="text-3xl font-bold text-secondary-electric mb-2">The Ancients (US)</h3>
                        <p class="text-sm text-primary-neon mb-4">Легенди Класичного Року / Субота</p>
                        <p class="text-gray-300 text-base">
                            Справжній вінтажний звук з США. Потужний вокал, гітарні соло та хіти, які знає кожне покоління. Вони — жива історія року. Готуйтеся співати хором!
                        </p>
                    </div>
                </div>

                <!-- Картка 3 -->
                <div class="card-glow transition duration-500 rounded-3xl overflow-hidden bg-gray-900 shadow-2xl border border-primary-neon/50">
                    <div class="h-64 bg-gray-700 w-full" style="background-image: url('https://placehold.co/600x400/FF00FF/0D0A1F?text=Digital+Decay'); background-size: cover; background-position: center;">
                        <!--  -->
                    </div>
                    <div class="p-6">
                        <h3 class="text-3xl font-bold text-primary-neon mb-2">Digital Decay (FR)</h3>
                        <p class="text-sm text-secondary-electric mb-4">Альтернативний Панк / Неділя</p>
                        <p class="text-gray-300 text-base">
                            Французький панк-рок із цифровим присмаком. Швидкі ритми, агресивна подача та соціально значущі тексти. Закриють фестиваль зі справжнім бунтом на сцені.
                        </p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Інтерактивна мапа фестивалю (Mock) -->
    <section id="map" class="py-20 bg-section-gradient">
        <div class="container mx-auto px-4">
            <h2 class="text-5xl font-extrabold text-center mb-10 bg-clip-text text-transparent bg-hero-gradient">
                Мапа Фестивалю
            </h2>

            <div class="bg-dark-bg/80 p-6 rounded-2xl shadow-2xl border border-secondary-electric/30">
                <div class="text-center mb-6">
                    <p class="text-xl text-white italic">Натисніть на зони, щоб побачити деталі!</p>
                </div>
                <!-- Макет карти у вигляді SVG/Placeholder, що імітує інтерактивність -->
                <svg viewBox="0 0 800 500" class="w-full h-auto max-w-4xl mx-auto border-4 border-secondary-electric/50 rounded-xl shadow-lg bg-gray-900/70">
                    <!-- Загальний фон -->
                    <rect x="0" y="0" width="800" height="500" fill="#1A1A40" />

                    <!-- Сцена 1 (Main Stage) -->
                    <rect x="50" y="50" width="200" height="80" rx="10" fill="#FF00FF" class="hover:opacity-80 transition duration-300 cursor-pointer" onclick="alert('Головна Сцена: тут відбуваються всі хедлайнерські виступи!')"/>
                    <text x="150" y="95" font-size="20" fill="white" text-anchor="middle" font-weight="bold">ГОЛОВНА СЦЕНА</text>

                    <!-- Фудкорт (Food Court) -->
                    <rect x="600" y="50" width="150" height="150" rx="10" fill="#00FFFF" class="hover:opacity-80 transition duration-300 cursor-pointer" onclick="alert('Food Court: Їжа та напої. Тут є веганські та м\'ясні опції.')"/>
                    <text x="675" y="125" font-size="20" fill="#1A1A40" text-anchor="middle" font-weight="bold">ФУДКОРТ</text>

                    <!-- Кемпінг (Camping) -->
                    <rect x="50" y="250" width="200" height="200" rx="10" fill="#8A2BE2" class="hover:opacity-80 transition duration-300 cursor-pointer" onclick="alert('Кемпінг: Зона для наметів. Вхід лише з квитком на кемпінг.')"/>
                    <text x="150" y="350" font-size="24" fill="white" text-anchor="middle" font-weight="bold">КЕМПІНГ</text>

                    <!-- Арт-зона (Art Zone) -->
                    <circle cx="400" cy="350" r="80" fill="#FF00FF" opacity="0.7" class="hover:opacity-100 transition duration-300 cursor-pointer" onclick="alert('Арт-Зона: Майстер-класи, графіті, інсталяції.')"/>
                    <text x="400" y="355" font-size="20" fill="#1A1A40" text-anchor="middle" font-weight="bold">АРТ-ЗОНА</text>

                    <!-- Точки мерчу (Merch) -->
                    <polygon points="550,400 650,400 650,450 600,480 550,450" fill="#00FFFF" opacity="0.8" class="hover:opacity-100 transition duration-300 cursor-pointer" onclick="alert('Мерч: Футболки, значки та сувеніри гуртів!')"/>
                    <text x="600" y="435" font-size="16" fill="#1A1A40" text-anchor="middle" font-weight="bold">МЕРЧ</text>

                    <!-- Доріжки та позначки -->
                    <line x1="250" y1="90" x2="600" y2="90" stroke="#FFFFFF" stroke-width="5" stroke-linecap="round" stroke-dasharray="10,10"/>
                    <line x1="250" y1="350" x2="320" y2="350" stroke="#FFFFFF" stroke-width="5" stroke-linecap="round"/>

                </svg>
            </div>
        </div>
    </section>

    <!-- Секція "Квитки" -->
    <section id="tickets" class="py-20 bg-dark-bg">
        <div class="container mx-auto px-4">
            <h2 class="text-5xl font-extrabold text-center mb-16 bg-clip-text text-transparent bg-hero-gradient">
                Квитки та Ціни
            </h2>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                <!-- Картка 1: Standard Ticket -->
                <div class="bg-gray-900 rounded-3xl p-8 shadow-2xl border-4 border-secondary-electric/70 transform hover:scale-[1.02] transition duration-500 card-glow">
                    <h3 class="text-4xl font-bold text-secondary-electric mb-2">СТАНДАРТ</h3>
                    <p class="text-gray-400 mb-6">Доступ до всіх сцен та зон фестивалю.</p>
                    <p class="text-5xl font-extrabold text-white mb-6">
                        1800 <span class="text-2xl text-primary-neon">грн</span>
                    </p>
                    <ul class="space-y-3 text-lg text-gray-300 mb-8">
                        <li>✅ 3 дні музики</li>
                        <li>✅ Вхід на Main Stage</li>
                        <li>❌ Доступ до VIP-ложі</li>
                        <li>❌ Зона кемпінгу</li>
                    </ul>
                    <button class="w-full py-3 text-xl font-bold text-dark-bg rounded-xl transition duration-300 transform hover:bg-opacity-90 shadow-lg" style="background: linear-gradient(90deg, #00FFFF, #8A2BE2);">
                        ПРИДБАТИ
                    </button>
                </div>

                <!-- Картка 2: Camping Ticket (Найпопулярніший) -->
                <div class="bg-gray-800 rounded-3xl p-10 shadow-3xl border-4 border-primary-neon transform scale-[1.05] transition duration-500 card-glow relative">
                    <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 bg-primary-neon text-dark-bg font-extrabold text-sm px-4 py-1 rounded-full shadow-lg">
                        POPULAR
                    </div>
                    <h3 class="text-5xl font-extrabold text-primary-neon mb-3">ПОВНИЙ ПАКЕТ</h3>
                    <p class="text-gray-300 mb-6 text-xl">Стандартний квиток + Проживання в Кемпінгу.</p>
                    <p class="text-6xl font-extrabold text-white mb-6">
                        2500 <span class="text-3xl text-secondary-electric">грн</span>
                    </p>
                    <ul class="space-y-3 text-lg text-gray-200 mb-8">
                        <li>✅ 3 дні музики</li>
                        <li>✅ Вхід на Main Stage</li>
                        <li>❌ Доступ до VIP-ложі</li>
                        <li>✅ <span class="font-bold">Місце в зоні Кемпінгу</span></li>
                    </ul>
                    <button class="w-full py-4 text-2xl font-bold text-dark-bg rounded-2xl transition duration-300 transform hover:scale-95 shadow-xl" style="background: linear-gradient(90deg, #FF00FF, #FFC0CB);">
                        ОФОРМИТИ ЗАМОВЛЕННЯ
                    </button>
                </div>

                <!-- Картка 3: VIP Ticket -->
                <div class="bg-gray-900 rounded-3xl p-8 shadow-2xl border-4 border-secondary-electric/70 transform hover:scale-[1.02] transition duration-500 card-glow">
                    <h3 class="text-4xl font-bold text-secondary-electric mb-2">VIP PASS</h3>
                    <p class="text-gray-400 mb-6">Ексклюзивний досвід фестивалю.</p>
                    <p class="text-5xl font-extrabold text-white mb-6">
                        4500 <span class="text-2xl text-primary-neon">грн</span>
                    </p>
                    <ul class="space-y-3 text-lg text-gray-300 mb-8">
                        <li>✅ 3 дні музики</li>
                        <li>✅ Вхід на Main Stage</li>
                        <li>✅ <span class="font-bold">Доступ до VIP-ложі</span></li>
                        <li>✅ Зона кемпінгу</li>
                    </ul>
                    <button class="w-full py-3 text-xl font-bold text-dark-bg rounded-xl transition duration-300 transform hover:bg-opacity-90 shadow-lg" style="background: linear-gradient(90deg, #00FFFF, #8A2BE2);">
                        ПРИДБАТИ
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Галерея з минулорічного фестивалю -->
    <section id="gallery" class="py-20 bg-section-gradient">
        <div class="container mx-auto px-4">
            <h2 class="text-5xl font-extrabold text-center mb-16 bg-clip-text text-transparent bg-hero-gradient">
                Галерея 2023
            </h2>
            <p class="text-center text-xl text-gray-400 mb-8">
                Подивіться, як це було минулого року. Енергія, натовп та справжній рок!
            </p>

            <!-- Responsive Grid Gallery -->
            <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-4 gap-4">
                <div class="aspect-square rounded-xl overflow-hidden shadow-xl hover:shadow-primary-neon/50 hover:scale-105 transition duration-500">
                    <img src="https://placehold.co/600x600/FF00FF/0D0A1F?text=STAGE+LIGHTS" alt="Світло на сцені" class="w-full h-full object-cover">
                </div>
                <div class="aspect-square rounded-xl overflow-hidden shadow-xl hover:shadow-secondary-electric/50 hover:scale-105 transition duration-500">
                    <img src="https://placehold.co/600x600/00FFFF/0D0A1F?text=CROWD+SURFING" alt="Натовп" class="w-full h-full object-cover">
                </div>
                <div class="aspect-square rounded-xl overflow-hidden shadow-xl hover:shadow-primary-neon/50 hover:scale-105 transition duration-500">
                    <img src="https://placehold.co/600x600/8A2BE2/FFFFFF?text=GUITAR+SOLO" alt="Соло на гітарі" class="w-full h-full object-cover">
                </div>
                <div class="aspect-square rounded-xl overflow-hidden shadow-xl hover:shadow-secondary-electric/50 hover:scale-105 transition duration-500">
                    <img src="https://placehold.co/600x600/FF00FF/0D0A1F?text=PYRO+SHOW" alt="Піротехнічне шоу" class="w-full h-full object-cover">
                </div>
                <div class="aspect-square rounded-xl overflow-hidden shadow-xl hover:shadow-secondary-electric/50 hover:scale-105 transition duration-500 hidden sm:block">
                    <img src="https://placehold.co/600x600/00FFFF/0D0A1F?text=CAMPING+VIBE" alt="Кемпінг" class="w-full h-full object-cover">
                </div>
                <div class="aspect-square rounded-xl overflow-hidden shadow-xl hover:shadow-primary-neon/50 hover:scale-105 transition duration-500 hidden sm:block">
                    <img src="https://placehold.co/600x600/8A2BE2/FFFFFF?text=FOOD+COURT" alt="Фудкорт" class="w-full h-full object-cover">
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ та правила фестивалю (Accordion) -->
    <section id="faq" class="py-20 bg-dark-bg">
        <div class="container mx-auto px-4">
            <h2 class="text-5xl font-extrabold text-center mb-16 bg-clip-text text-transparent bg-hero-gradient">
                FAQ та Правила Фестивалю
            </h2>

            <div class="max-w-3xl mx-auto space-y-4">
                <!-- Питання 1 -->
                <div class="faq-item bg-gray-900/70 rounded-xl shadow-xl border border-secondary-electric/20" data-open="false">
                    <button class="faq-toggle w-full flex justify-between items-center p-5 text-xl font-semibold hover:text-primary-neon transition duration-300">
                        <span>Чи можна приносити свою їжу та напої?</span>
                        <span class="text-primary-neon text-2xl transform transition-transform duration-300">
                            +
                        </span>
                    </button>
                    <div class="faq-answer px-5 text-gray-300 text-base">
                        <p>На жаль, приносити власну їжу та алкоголь на територію фестивалю суворо заборонено з міркувань безпеки. Проте, у нас буде великий фудкорт з різноманітними опціями!</p>
                    </div>
                </div>

                <!-- Питання 2 -->
                <div class="faq-item bg-gray-900/70 rounded-xl shadow-xl border border-secondary-electric/20" data-open="false">
                    <button class="faq-toggle w-full flex justify-between items-center p-5 text-xl font-semibold hover:text-primary-neon transition duration-300">
                        <span>Як добратися до Арт-Заводу "Платформа"?</span>
                        <span class="text-primary-neon text-2xl transform transition-transform duration-300">
                            +
                        </span>
                    </button>
                    <div class="faq-answer px-5 text-gray-300 text-base">
                        <p>Локація розташована поруч зі станцією метро "Лісова". Будуть організовані шатл-баси від метро до входу на фестиваль. Також доступна парковка для приватного транспорту.</p>
                    </div>
                </div>

                <!-- Питання 3: Правила -->
                <div class="faq-item bg-gray-900/70 rounded-xl shadow-xl border border-primary-neon/20" data-open="false">
                    <button class="faq-toggle w-full flex justify-between items-center p-5 text-xl font-semibold hover:text-secondary-electric transition duration-300">
                        <span>Основні правила поведінки на фестивалі</span>
                        <span class="text-secondary-electric text-2xl transform transition-transform duration-300">
                            +
                        </span>
                    </button>
                    <div class="faq-answer px-5 text-gray-300 text-base">
                        <ul class="list-disc ml-5 space-y-2">
                            <li>Заборонено проносити зброю та піротехніку.</li>
                            <li>Поважайте простір інших відвідувачів.</li>
                            <li>Сміття викидайте у спеціальні контейнери.</li>
                            <li>Несанкціонована торгівля заборонена.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black py-8">
        <div class="container mx-auto px-4 text-center">
            <h4 class="text-2xl font-bold bg-clip-text text-transparent bg-hero-gradient mb-4">
                RocK Tsunami 2024
            </h4>
            <div class="flex justify-center space-x-6 mb-4">
                <a href="#" class="text-gray-400 hover:text-primary-neon transition duration-300">
                    Facebook
                </a>
                <a href="#" class="text-gray-400 hover:text-primary-neon transition duration-300">
                    Instagram
                </a>
                <a href="#" class="text-gray-400 hover:text-primary-neon transition duration-300">
                    Telegram
                </a>
            </div>
            <p class="text-sm text-gray-500">
                &copy; 2024 RocK Tsunami. Всі права захищено.
            </p>
        </div>
    </footer>

    <!-- JavaScript для інтерактивності (FAQ та меню) -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // JS для мобільного меню
            const menuBtn = document.getElementById('menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');

            menuBtn.addEventListener('click', () => {
                const isHidden = mobileMenu.classList.contains('hidden');
                if (isHidden) {
                    mobileMenu.classList.remove('hidden');
                    menuBtn.innerHTML = '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path></svg>'; // Іконка "X"
                } else {
                    mobileMenu.classList.add('hidden');
                    menuBtn.innerHTML = '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>'; // Іконка бургера
                }
            });

            window.closeMenu = () => {
                mobileMenu.classList.add('hidden');
                menuBtn.innerHTML = '<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path></svg>';
            };

            // JS для FAQ Accordion
            const faqToggles = document.querySelectorAll('.faq-toggle');

            faqToggles.forEach(toggle => {
                toggle.addEventListener('click', () => {
                    const faqItem = toggle.closest('.faq-item');
                    const isOpen = faqItem.getAttribute('data-open') === 'true';
                    const answer = faqItem.querySelector('.faq-answer');
                    const icon = toggle.querySelector('span:last-child');

                    // Закриття всіх інших елементів
                    document.querySelectorAll('.faq-item[data-open="true"]').forEach(openItem => {
                        if (openItem !== faqItem) {
                            openItem.setAttribute('data-open', 'false');
                            openItem.querySelector('.faq-answer').style.maxHeight = null;
                            openItem.querySelector('.faq-answer').style.paddingBottom = null;
                            openItem.querySelector('span:last-child').style.transform = 'rotate(0deg)';
                        }
                    });

                    // Відкриття/закриття поточного елемента
                    if (!isOpen) {
                        faqItem.setAttribute('data-open', 'true');
                        // Встановлюємо висоту для анімації
                        answer.style.maxHeight = answer.scrollHeight + "px";
                        icon.style.transform = 'rotate(45deg)'; // Зміна "+" на "X"
                    } else {
                        faqItem.setAttribute('data-open', 'false');
                        answer.style.maxHeight = null;
                        icon.style.transform = 'rotate(0deg)';
                    }
                });
            });
        });
    </script>

</body>
</html>
