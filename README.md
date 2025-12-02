<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Животный мир</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: #f0f8f0;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header styles */
        header {
            background: linear-gradient(135deg, #2d5a27 0%, #4a8c3a 100%);
            color: white;
            padding: 1.5rem 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .logo {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 15px;
            margin-bottom: 10px;
        }

        .logo i {
            font-size: 2.5rem;
        }

        h1 {
            font-size: 2.8rem;
            margin-bottom: 0.5rem;
        }

        .tagline {
            font-size: 1.2rem;
            opacity: 0.9;
        }

        /* Navigation styles */
        nav {
            background-color: #3a7c2f;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }

        nav li {
            margin: 0;
        }

        nav a {
            color: white;
            text-decoration: none;
            padding: 1rem 1.5rem;
            display: inline-block;
            transition: background-color 0.3s;
            font-weight: 500;
        }

        nav a:hover {
            background-color: #2d5a27;
        }

        /* Hero section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 5rem 1rem;
            margin-bottom: 2rem;
        }

        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 1.5rem;
        }

        .btn {
            display: inline-block;
            background-color: #4a8c3a;
            color: white;
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #3a7c2f;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        /* Main content */
        .section-title {
            text-align: center;
            color: #2d5a27;
            margin: 3rem 0 2rem;
            font-size: 2.2rem;
            position: relative;
        }

        .section-title:after {
            content: '';
            position: absolute;
            width: 100px;
            height: 4px;
            background-color: #4a8c3a;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }

        /* Animal categories */
        .animal-categories {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .category {
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s;
        }

        .category:hover {
            transform: translateY(-10px);
        }

        .category-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }

        .category-content {
            padding: 1.5rem;
        }

        .category h3 {
            color: #2d5a27;
            margin-bottom: 0.8rem;
            font-size: 1.5rem;
        }

        .category p {
            color: #555;
            margin-bottom: 1.2rem;
        }

        /* Facts section */
        .facts {
            background-color: #e8f4e8;
            padding: 3rem 1rem;
            margin: 3rem 0;
            border-radius: 12px;
        }

        .facts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .fact-item {
            background-color: white;
            padding: 1.5rem;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.05);
            text-align: center;
        }

        .fact-item i {
            font-size: 2rem;
            color: #4a8c3a;
            margin-bottom: 1rem;
        }

        /* Representatives section */
        .representatives {
            margin: 4rem 0;
        }

        .rep-category {
            margin-bottom: 4rem;
        }

        .rep-category h3 {
            color: #2d5a27;
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #e8f4e8;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .rep-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .rep-card {
            background-color: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s;
            height: 100%;
            display: flex;
            flex-direction: column;
        }

        .rep-card:hover {
            transform: translateY(-5px);
        }

        .rep-img {
            height: 200px;
            background-size: cover;
            background-position: center;
        }

        .rep-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .rep-content h4 {
            color: #2d5a27;
            margin-bottom: 0.8rem;
            font-size: 1.3rem;
        }

        .rep-content p {
            color: #555;
            margin-bottom: 1rem;
            font-size: 0.95rem;
            flex-grow: 1;
        }

        .rep-details {
            display: flex;
            justify-content: space-between;
            margin-top: 1rem;
            font-size: 0.9rem;
            color: #666;
        }

        .rep-details span {
            display: flex;
            align-items: center;
            gap: 5px;
        }

        /* Footer */
        footer {
            background-color: #2d5a27;
            color: white;
            padding: 3rem 0 1.5rem;
            margin-top: 3rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1.2rem;
            font-size: 1.4rem;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section a {
            color: #d0e8d0;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: white;
        }

        .social-icons {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #3a7c2f;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: background-color 0.3s;
        }

        .social-icons a:hover {
            background-color: #4a8c3a;
        }

        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid #3a7c2f;
            font-size: 0.9rem;
            color: #d0e8d0;
        }

        /* Modal styles */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            overflow-y: auto;
        }

        .modal-content {
            background-color: white;
            margin: 30px auto;
            padding: 0;
            width: 95%;
            max-width: 900px;
            border-radius: 12px;
            box-shadow: 0 5px 30px rgba(0, 0, 0, 0.3);
            animation: modalFade 0.3s;
        }

        @keyframes modalFade {
            from {opacity: 0; transform: translateY(-50px);}
            to {opacity: 1; transform: translateY(0);}
        }

        .modal-header {
            background: linear-gradient(135deg, #2d5a27 0%, #4a8c3a 100%);
            color: white;
            padding: 1.5rem;
            border-radius: 12px 12px 0 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .modal-header h2 {
            margin: 0;
            font-size: 1.8rem;
        }

        .close {
            color: white;
            font-size: 2rem;
            font-weight: bold;
            cursor: pointer;
            transition: color 0.3s;
        }

        .close:hover {
            color: #d0e8d0;
        }

        .modal-body {
            padding: 2rem;
            max-height: 80vh;
            overflow-y: auto;
        }

        .modal-img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 1.5rem;
        }

        .modal-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }

        .info-item {
            background-color: #f0f8f0;
            padding: 1rem;
            border-radius: 8px;
        }

        .info-item h4 {
            color: #2d5a27;
            margin-bottom: 0.5rem;
        }

        .modal-examples {
            margin: 2rem 0;
        }

        .examples-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .example-item {
            background-color: #e8f4e8;
            padding: 0.8rem;
            border-radius: 8px;
            text-align: center;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s;
        }

        .example-item:hover {
            background-color: #d4e8d4;
            transform: translateY(-3px);
        }

        .modal-section {
            margin: 2rem 0;
        }

        .modal-section h3 {
            color: #2d5a27;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #e8f4e8;
        }

        .feature-list {
            list-style-type: none;
            margin: 1rem 0;
        }

        .feature-list li {
            padding: 0.5rem 0;
            padding-left: 1.5rem;
            position: relative;
        }

        .feature-list li:before {
            content: "✓";
            color: #4a8c3a;
            font-weight: bold;
            position: absolute;
            left: 0;
        }

        .modal-tabs {
            display: flex;
            border-bottom: 2px solid #e8f4e8;
            margin-bottom: 1.5rem;
            flex-wrap: wrap;
        }

        .tab-button {
            background: none;
            border: none;
            padding: 0.8rem 1.5rem;
            cursor: pointer;
            font-weight: 500;
            color: #555;
            transition: all 0.3s;
            position: relative;
        }

        .tab-button:hover {
            color: #2d5a27;
        }

        .tab-button.active {
            color: #2d5a27;
        }

        .tab-button.active:after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: #4a8c3a;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .animal-characteristics {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .characteristic {
            background-color: #f9fdf9;
            padding: 1rem;
            border-radius: 8px;
            border-left: 4px solid #4a8c3a;
        }

        /* Representative modal styles */
        .rep-modal-content {
            max-width: 700px;
        }

        .rep-detail-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin: 1.5rem 0;
        }

        .rep-detail-item {
            background-color: #f0f8f0;
            padding: 1rem;
            border-radius: 8px;
        }

        .rep-detail-item h4 {
            color: #2d5a27;
            margin-bottom: 0.5rem;
        }

        .rep-feature-list {
            list-style-type: none;
            margin: 1rem 0;
        }

        .rep-feature-list li {
            padding: 0.5rem 0;
            padding-left: 1.5rem;
            position: relative;
        }

        .rep-feature-list li:before {
            content: "•";
            color: #4a8c3a;
            font-weight: bold;
            position: absolute;
            left: 0;
            font-size: 1.5rem;
        }

        /* Responsive design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
            }

            nav a {
                padding: 0.8rem 1rem;
            }

            .hero {
                padding: 3rem 1rem;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .modal-content {
                width: 98%;
                margin: 10px auto;
            }

            .modal-tabs {
                flex-wrap: wrap;
            }

            .tab-button {
                flex: 1;
                min-width: 120px;
                text-align: center;
            }

            .rep-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }

            .rep-detail-grid {
                grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="logo">
                <i class="fas fa-paw"></i>
                <div>
                    <h1>Животный мир</h1>
                    <p class="tagline">Исследуйте удивительное разнообразие животного мира нашей планеты</p>
                </div>
            </div>
        </div>
    </header>

    <!-- Navigation -->
    <nav>
        <div class="container">
            <ul>
                <li><a href="#home"><i class="fas fa-home"></i> Главная</a></li>
                <li><a href="#categories"><i class="fas fa-th"></i> Категории</a></li>
                <li><a href="#representatives"><i class="fas fa-star"></i> Представители</a></li>
                <li><a href="#facts"><i class="fas fa-lightbulb"></i> Интересные факты</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero section -->
    <section class="hero" id="home">
        <div class="container">
            <h2>Удивительный мир животных</h2>
            <p>От крошечных насекомых до гигантских млекопитающих - животный мир нашей планеты поражает своим разнообразием и красотой. Узнайте больше о различных видах животных и их уникальных особенностях.</p>
            <a href="#categories" class="btn">Исследовать мир животных</a>
        </div>
    </section>

    <!-- Main content -->
    <main class="container">
        <h2 class="section-title" id="categories">Категории животных</h2>

        <div class="animal-categories">
            <!-- Млекопитающие -->
            <div class="category">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80')"></div>
                <div class="category-content">
                    <h3>Млекопитающие</h3>
                    <p>Класс позвоночных животных, основными отличительными особенностями которых являются живорождение и вскармливание детёнышей молоком.</p>
                    <button class="btn more-info" data-animal="mammals">Подробнее</button>
                </div>
            </div>

            <!-- Птицы -->
            <div class="category">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1552728089-57bdde30beb3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80')"></div>
                <div class="category-content">
                    <h3>Птицы</h3>
                    <p>Класс теплокровных яйцекладущих позвоночных животных. Представляют собой хорошо обособленную группу.</p>
                    <button class="btn more-info" data-animal="birds">Подробнее</button>
                </div>
            </div>

            <!-- Рептилии -->
            <div class="category">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1579954115545-a95591f28bfc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80')"></div>
                <div class="category-content">
                    <h3>Рептилии</h3>
                    <p>Класс позвоночных животных, кожа которых покрыта роговыми чешуями или щитками.</p>
                    <button class="btn more-info" data-animal="reptiles">Подробнее</button>
                </div>
            </div>

            <!-- Рыбы -->
            <div class="category">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1599487488170-d11ec9c172f0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80')"></div>
                <div class="category-content">
                    <h3>Рыбы</h3>
                    <p>Парафилетическая группа водных позвоночных животных. Обладают жабрами и конечностями в виде плавников.</p>
                    <button class="btn more-info" data-animal="fish">Подробнее</button>
                </div>
            </div>

            <!-- Насекомые -->
            <div class="category">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1565402170291-8491f14678db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80')"></div>
                <div class="category-content">
                    <h3>Насекомые</h3>
                    <p>Класс беспозвоночных членистоногих животных. Насекомые являются самой разнообразной группой животных.</p>
                    <button class="btn more-info" data-animal="insects">Подробнее</button>
                </div>
            </div>

            <!-- Амфибии -->
            <div class="category">
                <div class="category-img" style="background-image: url('https://images.unsplash.com/photo-1559253664-ca249d4608c6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80')"></div>
                <div class="category-content">
                    <h3>Амфибии</h3>
                    <p>Класс позвоночных четвероногих животных, которые могут жить как в воде, так и на суше.</p>
                    <button class="btn more-info" data-animal="amphibians">Подробнее</button>
                </div>
            </div>
        </div>

        <!-- Representatives section -->
        <div class="representatives" id="representatives">
            <h2 class="section-title">Знаменитые представители</h2>

            <!-- Млекопитающие -->
            <div class="rep-category">
                <h3><i class="fas fa-otter"></i> Млекопитающие</h3>
                <div class="rep-grid">
                    <!-- Африканский слон -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Африканский слон</h4>
                            <p>Крупнейшее наземное млекопитающее. Обладает высоким интеллектом, сложной социальной структурой и отличной памятью.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 7 тонн</span>
                                <span><i class="fas fa-ruler"></i> До 4 м</span>
                                <span><i class="fas fa-clock"></i> 60-70 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="elephant">Подробнее</button>
                        </div>
                    </div>

                    <!-- Синий кит -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1574871619173-b8b6f1a926e9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Синий кит</h4>
                            <p>Крупнейшее животное на планете. Питается крилем, фильтруя воду через китовый ус. Издает самые громкие звуки среди животных.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 200 тонн</span>
                                <span><i class="fas fa-ruler"></i> До 33 м</span>
                                <span><i class="fas fa-clock"></i> 80-90 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="whale">Подробнее</button>
                        </div>
                    </div>

                    <!-- Большая панда -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1564349683136-77e08dba1ef7?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Большая панда</h4>
                            <p>Символ Всемирного фонда дикой природы. Питается в основном бамбуком. Находится под угрозой исчезновения.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 70-125 кг</span>
                                <span><i class="fas fa-ruler"></i> 1.2-1.9 м</span>
                                <span><i class="fas fa-clock"></i> 20 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="panda">Подробнее</button>
                        </div>
                    </div>

                    <!-- Гепард -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Гепард</h4>
                            <p>Самое быстрое наземное животное. Может развивать скорость до 110 км/ч. Охотится днем, полагаясь на зрение.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 35-65 кг</span>
                                <span><i class="fas fa-ruler"></i> 1.1-1.5 м</span>
                                <span><i class="fas fa-clock"></i> 10-12 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="cheetah">Подробнее</button>
                        </div>
                    </div>

                    <!-- Дельфин -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Афалина (дельфин)</h4>
                            <p>Один из самых умных морских млекопитающих. Использует эхолокацию для навигации и охоты. Обладает сложной социальной структурой.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 150-650 кг</span>
                                <span><i class="fas fa-ruler"></i> 2-4 м</span>
                                <span><i class="fas fa-clock"></i> 40-50 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="dolphin">Подробнее</button>
                        </div>
                    </div>

                    <!-- Человек -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Человек разумный</h4>
                            <p>Единственный современный вид рода Homo. Обладает развитым сознанием, речью, способностью к абстрактному мышлению и созданию сложных орудий.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 50-100 кг</span>
                                <span><i class="fas fa-ruler"></i> 1.5-1.9 м</span>
                                <span><i class="fas fa-clock"></i> 70-80 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="human">Подробнее</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Птицы -->
            <div class="rep-category">
                <h3><i class="fas fa-dove"></i> Птицы</h3>
                <div class="rep-grid">
                    <!-- Орлан-белохвост -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1596273315327-5f059a42b4c0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Орлан-белохвост</h4>
                            <p>Крупная хищная птица, символ силы и свободы. Обитает near водоемов, питается рыбой и водоплавающими птицами.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 3-7 кг</span>
                                <span><i class="fas fa-ruler"></i> Размах до 2.4 м</span>
                                <span><i class="fas fa-clock"></i> 20-25 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="eagle">Подробнее</button>
                        </div>
                    </div>

                    <!-- Колибри -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1530919424169-4b95c30a00b0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Колибри</h4>
                            <p>Самая маленькая птица в мире. Единственная птица, способная летать назад. Питается нектаром цветов.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 2-20 г</span>
                                <span><i class="fas fa-ruler"></i> 5-22 см</span>
                                <span><i class="fas fa-clock"></i> 3-5 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="hummingbird">Подробнее</button>
                        </div>
                    </div>

                    <!-- Императорский пингвин -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1589561253898-768ab8d6d5e5?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Императорский пингвин</h4>
                            <p>Самый крупный вид пингвинов. Размножается в суровых условиях Антарктики. Самец высиживает яйцо в течение двух месяцев.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 20-45 кг</span>
                                <span><i class="fas fa-ruler"></i> До 1.3 м</span>
                                <span><i class="fas fa-clock"></i> 15-20 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="penguin">Подробнее</button>
                        </div>
                    </div>

                    <!-- Страус -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Африканский страус</h4>
                            <p>Самая крупная птица в мире. Не умеет летать, но отлично бегает. Откладывает самые большие яйца среди птиц.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 90-130 кг</span>
                                <span><i class="fas fa-ruler"></i> До 2.7 м</span>
                                <span><i class="fas fa-clock"></i> 40-45 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="ostrich">Подробнее</button>
                        </div>
                    </div>

                    <!-- Попугай -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Ара (попугай)</h4>
                            <p>Крупный попугай с ярким оперением. Обладает высоким интеллектом, способен имитировать человеческую речь.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 1-1.7 кг</span>
                                <span><i class="fas fa-ruler"></i> 80-95 см</span>
                                <span><i class="fas fa-clock"></i> 50-80 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="parrot">Подробнее</button>
                        </div>
                    </div>

                    <!-- Альбатрос -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Странствующий альбатрос</h4>
                            <p>Птица с самым большим размахом крыльев. Проводит большую часть жизни в полете над океаном. Совершает длительные миграции.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 8-12 кг</span>
                                <span><i class="fas fa-ruler"></i> Размах до 3.5 м</span>
                                <span><i class="fas fa-clock"></i> 50+ лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="albatross">Подробнее</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Рептилии -->
            <div class="rep-category">
                <h3><i class="fas fa-dragon"></i> Рептилии</h3>
                <div class="rep-grid">
                    <!-- Комодский варан -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Комодский варан</h4>
                            <p>Крупнейшая ящерица в мире. Обитает на индонезийских островах. Имеет ядовитый укус и мощные челюсти.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 90 кг</span>
                                <span><i class="fas fa-ruler"></i> До 3 м</span>
                                <span><i class="fas fa-clock"></i> 30 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="komodo">Подробнее</button>
                        </div>
                    </div>

                    <!-- Королевская кобра -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1572977497251-9e05cb47d983?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Королевская кобра</h4>
                            <p>Самая длинная ядовитая змея в мире. Может достигать 5.5 метров в длину. Питается другими змеями.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 6-9 кг</span>
                                <span><i class="fas fa-ruler"></i> До 5.5 м</span>
                                <span><i class="fas fa-clock"></i> 20 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="cobra">Подробнее</button>
                        </div>
                    </div>

                    <!-- Зеленая морская черепаха -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1595521626788-00d2a2f6b730?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Зеленая морская черепаха</h4>
                            <p>Крупная морская черепаха, питающаяся в основном морскими водорослями. Совершает длительные миграции для размножения.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 200 кг</span>
                                <span><i class="fas fa-ruler"></i> До 1.5 м</span>
                                <span><i class="fas fa-clock"></i> 80+ лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="turtle">Подробнее</button>
                        </div>
                    </div>

                    <!-- Гребнистый крокодил -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Гребнистый крокодил</h4>
                            <p>Крупнейший современный крокодил и рептилия. Обитает в солоноватых водах Юго-Восточной Азии и Австралии.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 1000 кг</span>
                                <span><i class="fas fa-ruler"></i> До 7 м</span>
                                <span><i class="fas fa-clock"></i> 70+ лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="crocodile">Подробнее</button>
                        </div>
                    </div>

                    <!-- Хамелеон -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Йеменский хамелеон</h4>
                            <p>Известен способностью менять цвет кожи. Имеет длинный язык для ловли насекомых и независимо движущиеся глаза.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 90-180 г</span>
                                <span><i class="fas fa-ruler"></i> 35-50 см</span>
                                <span><i class="fas fa-clock"></i> 5-8 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="chameleon">Подробнее</button>
                        </div>
                    </div>

                    <!-- Анаконда -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Зеленая анаконда</h4>
                            <p>Одна из самых крупных змей в мире. Обитает в тропических реках Южной Америки. Не ядовита, убивает добычу удушением.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 250 кг</span>
                                <span><i class="fas fa-ruler"></i> До 9 м</span>
                                <span><i class="fas fa-clock"></i> 10-30 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="anaconda">Подробнее</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Рыбы -->
            <div class="rep-category">
                <h3><i class="fas fa-fish"></i> Рыбы</h3>
                <div class="rep-grid">
                    <!-- Китовая акула -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Китовая акула</h4>
                            <p>Самая крупная рыба в мире. Питается планктоном, фильтруя воду через жабры. Совершает длительные миграции.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 34 тонн</span>
                                <span><i class="fas fa-ruler"></i> До 20 м</span>
                                <span><i class="fas fa-clock"></i> 70-100 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="whale_shark">Подробнее</button>
                        </div>
                    </div>

                    <!-- Рыба-клоун -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Рыба-клоун</h4>
                            <p>Известна симбиозом с актиниями. Имеет яркую окраску. Все особи рождаются самцами, некоторые становятся самками.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 250 г</span>
                                <span><i class="fas fa-ruler"></i> 10-18 см</span>
                                <span><i class="fas fa-clock"></i> 6-10 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="clownfish">Подробнее</button>
                        </div>
                    </div>

                    <!-- Пиранья -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Обыкновенная пиранья</h4>
                            <p>Хищная рыба с мощными челюстями и острыми зубами. Обитает в реках Южной Америки. Охотится стаями.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 3.5 кг</span>
                                <span><i class="fas fa-ruler"></i> До 50 см</span>
                                <span><i class="fas fa-clock"></i> 10-25 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="piranha">Подробнее</button>
                        </div>
                    </div>

                    <!-- Скат -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Манта (гигантский скат)</h4>
                            <p>Крупнейший вид скатов. Питается планктоном. Имеет «крылья» размахом до 7 метров. Совершает акробатические прыжки из воды.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 2 тонн</span>
                                <span><i class="fas fa-ruler"></i> Размах до 7 м</span>
                                <span><i class="fas fa-clock"></i> 40-50 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="manta">Подробнее</button>
                        </div>
                    </div>

                    <!-- Рыба-парусник -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Рыба-парусник</h4>
                            <p>Самая быстрая рыба в мире. Может развивать скорость до 110 км/ч. Имеет высокий спинной плавник, похожий на парус.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 100 кг</span>
                                <span><i class="fas fa-ruler"></i> До 3.5 м</span>
                                <span><i class="fas fa-clock"></i> 10-15 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="sailfish">Подробнее</button>
                        </div>
                    </div>

                    <!-- Морской конек -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Морской конек</h4>
                            <p>Необычная рыба с вертикальным положением тела. Самец вынашивает икру в специальной сумке. Плавает медленно, цепляясь хвостом за водоросли.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 200 г</span>
                                <span><i class="fas fa-ruler"></i> 1.5-35 см</span>
                                <span><i class="fas fa-clock"></i> 1-5 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="seahorse">Подробнее</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Насекомые -->
            <div class="rep-category">
                <h3><i class="fas fa-bug"></i> Насекомые</h3>
                <div class="rep-grid">
                    <!-- Бабочка-монарх -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Бабочка-монарх</h4>
                            <p>Известна своей длительной миграцией. Яркая окраска предупреждает хищников о ядовитости. Гусеницы питаются молочаем.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 0.5-1 г</span>
                                <span><i class="fas fa-ruler"></i> Размах 8-10 см</span>
                                <span><i class="fas fa-clock"></i> 2-6 недель</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="monarch">Подробнее</button>
                        </div>
                    </div>

                    <!-- Медоносная пчела -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Медоносная пчела</h4>
                            <p>Важный опылитель растений и производитель меда. Живет сложно организованными колониями с разделением труда.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 0.1 г</span>
                                <span><i class="fas fa-ruler"></i> 1-1.5 см</span>
                                <span><i class="fas fa-clock"></i> Рабочая: 6 недель</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="honeybee">Подробнее</button>
                        </div>
                    </div>

                    <!-- Муравей -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Муравей-листорез</h4>
                            <p>Выращивает грибы на срезанных листьях. Живет огромными колониями с миллионами особей. Имеет сложную социальную организацию.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 1-5 мг</span>
                                <span><i class="fas fa-ruler"></i> 0.3-2 см</span>
                                <span><i class="fas fa-clock"></i> Рабочая: 1-3 года</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="ant">Подробнее</button>
                        </div>
                    </div>

                    <!-- Стрекоза -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Стрекоза</h4>
                            <p>Хищное насекомое с отличным зрением и маневренным полетом. Личинки живут в воде. Охотится на лету, ловя других насекомых.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 0.5-2 г</span>
                                <span><i class="fas fa-ruler"></i> Размах 5-19 см</span>
                                <span><i class="fas fa-clock"></i> 6 месяцев - 7 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="dragonfly">Подробнее</button>
                        </div>
                    </div>

                    <!-- Жук-олень -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Жук-олень</h4>
                            <p>Один из самых крупных жуков Европы. Самец имеет огромные «рога» - видоизмененные верхние челюсти. Личинки развиваются в мертвой древесине.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 10 г</span>
                                <span><i class="fas fa-ruler"></i> До 9 см</span>
                                <span><i class="fas fa-clock"></i> 3-5 недель</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="stag_beetle">Подробнее</button>
                        </div>
                    </div>

                    <!-- Богомол -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Богомол</h4>
                            <p>Хищное насекомое с хватательными передними конечностями. Известен тем, что самка часто поедает самца после спаривания. Мастер маскировки.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 2-10 г</span>
                                <span><i class="fas fa-ruler"></i> 4-15 см</span>
                                <span><i class="fas fa-clock"></i> 6-12 месяцев</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="mantis">Подробнее</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Амфибии -->
            <div class="rep-category">
                <h3><i class="fas fa-frog"></i> Амфибии</h3>
                <div class="rep-grid">
                    <!-- Лягушка-голиаф -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Лягушка-голиаф</h4>
                            <p>Самая крупная лягушка в мире. Обитает в реках Западной Африки. Не издает звуков, так как не имеет голосового мешка.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 3.3 кг</span>
                                <span><i class="fas fa-ruler"></i> До 32 см</span>
                                <span><i class="fas fa-clock"></i> 15 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="goliath_frog">Подробнее</button>
                        </div>
                    </div>

                    <!-- Огненная саламандра -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Огненная саламандра</h4>
                            <p>Ярко окрашенная хвостатая амфибия. Выделяет ядовитый секрет через кожные железы. Активна ночью, днем прячется во влажных укрытиях.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 20-50 г</span>
                                <span><i class="fas fa-ruler"></i> 15-25 см</span>
                                <span><i class="fas fa-clock"></i> 20-30 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="salamander">Подробнее</button>
                        </div>
                    </div>

                    <!-- Аксолотль -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Аксолотль</h4>
                            <p>Личинка амбистомы, способная к размножению (неотения). Обладает удивительной способностью регенерации конечностей и органов.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 60-300 г</span>
                                <span><i class="fas fa-ruler"></i> 15-45 см</span>
                                <span><i class="fas fa-clock"></i> 10-15 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="axolotl">Подробнее</button>
                        </div>
                    </div>

                    <!-- Древолаз -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Ужасный листолаз (древолаз)</h4>
                            <p>Одна из самых ядовитых лягушек в мире. Яркая окраска предупреждает хищников об опасности. Яд используется индейцами для стрел.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 2-6 г</span>
                                <span><i class="fas fa-ruler"></i> 4-6 см</span>
                                <span><i class="fas fa-clock"></i> 10-15 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="poison_frog">Подробнее</button>
                        </div>
                    </div>

                    <!-- Жаба-ага -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Жаба-ага</h4>
                            <p>Крупная ядовитая жаба. Была интродуцирована во многие регионы для борьбы с вредителями, но сама стала инвазивным видом.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> До 2.6 кг</span>
                                <span><i class="fas fa-ruler"></i> До 25 см</span>
                                <span><i class="fas fa-clock"></i> 10-15 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="cane_toad">Подробнее</button>
                        </div>
                    </div>

                    <!-- Тритон -->
                    <div class="rep-card">
                        <div class="rep-img" style="background-image: url('https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80')"></div>
                        <div class="rep-content">
                            <h4>Обыкновенный тритон</h4>
                            <p>Хвостатая амфибия, часть жизни проводит в воде, часть на суше. Весной у самцов появляется яркий гребень для привлечения самок.</p>
                            <div class="rep-details">
                                <span><i class="fas fa-weight"></i> 3-12 г</span>
                                <span><i class="fas fa-ruler"></i> 7-11 см</span>
                                <span><i class="fas fa-clock"></i> 6-14 лет</span>
                            </div>
                            <button class="btn rep-detail-btn" data-rep="newt">Подробнее</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Facts section -->
        <div class="facts" id="facts">
            <h2 class="section-title">Интересные факты о животных</h2>
            <div class="facts-grid">
                <div class="fact-item">
                    <i class="fas fa-brain"></i>
                    <h3>Умные дельфины</h3>
                    <p>Дельфины имеют один из самых высоких коэффициентов энцефализации (относительный размер мозга) среди животных.</p>
                </div>

                <div class="fact-item">
                    <i class="fas fa-heartbeat"></i>
                    <h3>Сердце кита</h3>
                    <p>Сердце синего кита весит около 600 кг и размером с небольшой автомобиль.</p>
                </div>

                <div class="fact-item">
                    <i class="fas fa-eye"></i>
                    <h3>Зрение стрекозы</h3>
                    <p>Стрекозы имеют почти 360-градусное зрение и могут обнаруживать цвета и поляризованный свет.</p>
                </div>

                <div class="fact-item">
                    <i class="fas fa-running"></i>
                    <h3>Быстрые гепарды</h3>
                    <p>Гепард может разгоняться до 110 км/ч за 3 секунды, что быстрее большинства спортивных автомобилей.</p>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Животный мир</h3>
                    <p>Исследуйте удивительное разнообразие животного мира нашей планеты. Узнайте больше о различных видах животных и их уникальных особенностях.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>

                <div class="footer-section">
                    <h3>Категории животных</h3>
                    <ul>
                        <li><a href="#categories">Млекопитающие</a></li>
                        <li><a href="#categories">Птицы</a></li>
                        <li><a href="#categories">Рептилии</a></li>
                        <li><a href="#categories">Рыбы</a></li>
                        <li><a href="#categories">Насекомые</a></li>
                    </ul>
                </div>

                <div class="footer-section">
                    <h3>Контакты</h3>
                    <ul>
                        <li><i class="fas fa-envelope"></i> info@animalworld.ru</li>
                        <li><i class="fas fa-phone"></i> +7 (495) 123-45-67</li>
                        <li><i class="fas fa-map-marker-alt"></i> Москва, ул. Природная, д. 10</li>
                    </ul>
                </div>
            </div>

            <div class="copyright">
                <p>&copy; 2023 Животный мир. Все права защищены.</p>
            </div>
        </div>
    </footer>

    <!-- Modal window for animal categories -->
    <div id="animalModal" class="modal">
        <div class="modal-content">
            <div class="modal-header">
                <h2 id="modalTitle">Млекопитающие</h2>
                <span class="close">&times;</span>
            </div>
            <div class="modal-body">
                <!-- Tabs -->
                <div class="modal-tabs">
                    <button class="tab-button active" data-tab="overview">Обзор</button>
                    <button class="tab-button" data-tab="characteristics">Характеристики</button>
                    <button class="tab-button" data-tab="examples">Представители</button>
                    <button class="tab-button" data-tab="facts">Факты</button>
                </div>

                <!-- Tab contents -->
                <div id="tab-overview" class="tab-content active">
                    <img id="modalImage" src="https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Млекопитающие" class="modal-img">
                    <p id="modalDescription">Описание животного.</p>

                    <div class="modal-info">
                        <div class="info-item">
                            <h4>Количество видов</h4>
                            <p id="modalSpeciesCount">Более 5500</p>
                        </div>
                        <div class="info-item">
                            <h4>Среда обитания</h4>
                            <p id="modalHabitat">Различные среды обитания</p>
                        </div>
                        <div class="info-item">
                            <h4>Размеры</h4>
                            <p id="modalSize">От 3 см до 30 м</p>
                        </div>
                        <div class="info-item">
                            <h4>Продолжительность жизни</h4>
                            <p id="modalLifespan">От 1 года до 200 лет</p>
                        </div>
                    </div>

                    <div class="modal-section">
                        <h3>Основные особенности</h3>
                        <ul id="modalFeatures" class="feature-list">
                            <!-- Features will be added by JavaScript -->
                        </ul>
                    </div>
                </div>

                <div id="tab-characteristics" class="tab-content">
                    <div class="modal-section">
                        <h3>Характеристики класса</h3>
                        <div id="modalCharacteristics" class="animal-characteristics">
                            <!-- Characteristics will be added by JavaScript -->
                        </div>
                    </div>
                </div>

                <div id="tab-examples" class="tab-content">
                    <div class="modal-section">
                        <h3>Примеры представителей</h3>
                        <p>Нажмите на любого представителя, чтобы узнать о нем подробнее:</p>
                        <div id="modalExamples" class="examples-list">
                            <!-- Examples will be added by JavaScript -->
                        </div>
                    </div>
                </div>

                <div id="tab-facts" class="tab-content">
                    <div class="modal-section">
                        <h3>Интересные факты</h3>
                        <p id="modalFact">Интересный факт о животном.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal window for representatives -->
    <div id="repModal" class="modal">
        <div class="modal-content rep-modal-content">
            <div class="modal-header">
                <h2 id="repModalTitle">Африканский слон</h2>
                <span class="close rep-close">&times;</span>
            </div>
            <div class="modal-body">
                <img id="repModalImage" src="https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="Представитель" class="modal-img">

                <p id="repModalDescription">Описание представителя.</p>

                <div class="rep-detail-grid">
                    <div class="rep-detail-item">
                        <h4>Научное название</h4>
                        <p id="repScientificName">Loxodonta africana</p>
                    </div>
                    <div class="rep-detail-item">
                        <h4>Семейство</h4>
                        <p id="repFamily">Слоновые</p>
                    </div>
                    <div class="rep-detail-item">
                        <h4>Вес</h4>
                        <p id="repWeight">До 7 тонн</p>
                    </div>
                    <div class="rep-detail-item">
                        <h4>Длина</h4>
                        <p id="repLength">До 4 м</p>
                    </div>
                    <div class="rep-detail-item">
                        <h4>Продолжительность жизни</h4>
                        <p id="repLifespan">60-70 лет</p>
                    </div>
                    <div class="rep-detail-item">
                        <h4>Среда обитания</h4>
                        <p id="repHabitat">Саванны и леса Африки</p>
                    </div>
                </div>

                <div class="modal-section">
                    <h3>Особенности</h3>
                    <ul id="repFeatures" class="rep-feature-list">
                        <!-- Features will be added by JavaScript -->
                    </ul>
                </div>

                <div class="modal-section">
                    <h3>Интересные факты</h3>
                    <p id="repInterestingFacts">Интересные факты о представителе.</p>
                </div>

                <div class="modal-section">
                    <h3>Охранный статус</h3>
                    <p id="repConservation">Информация об охранном статусе.</p>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Данные для модальных окон категорий
        const animalData = {
            mammals: {
                title: "Млекопитающие",
                image: "https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
                description: "Млекопитающие — класс позвоночных животных, основными отличительными особенностями которых являются живорождение (за исключением инфракласса клоачных) и вскармливание детёнышей молоком. Млекопитающие распространены почти по всей Земле и встречаются во всех экосистемах: на суше, в морях, океанах, пресных водоёмах, в воздухе. Они играют важную роль в пищевых цепях и оказывают значительное влияние на экосистемы.",
                speciesCount: "Более 5500 видов",
                habitat: "Практически все среды обитания: леса, степи, пустыни, горы, океаны, реки, озера, воздушное пространство",
                size: "От 3-4 см (землеройка) до 30 м (синий кит)",
                lifespan: "От 1 года (некоторые грызуны) до 200+ лет (гренландский кит)",
                features: [
                    "Вскармливание детенышей молоком",
                    "Наличие волосяного покрова (шерсти)",
                    "Четырехкамерное сердце",
                    "Теплокровность (эндотермия)",
                    "Диафрагма для дыхания",
                    "Сложное поведение и развитый мозг",
                    "Дифференцированные зубы"
                ],
                characteristics: [
                    {title: "Температура тела", value: "Постоянная (гомойотермные)"},
                    {title: "Дыхание", value: "Легочное, с диафрагмой"},
                    {title: "Кровеносная система", value: "Замкнутая, 4-камерное сердце"},
                    {title: "Нервная система", value: "Высокоразвитая, большой мозг"},
                    {title: "Размножение", value: "Половое, живорождение (кроме яйцекладущих)"},
                    {title: "Покровы тела", value: "Кожа с волосяным покровом, железами"}
                ],
                examples: ["Африканский слон", "Синий кит", "Большая панда", "Гепард", "Дельфин", "Человек"],
                fact: "Единственные млекопитающие, способные к полёту — летучие мыши. Они используют эхолокацию для навигации в темноте. У дельфинов и китов эхолокация также развита, но используется под водой."
            },
            birds: {
                title: "Птицы",
                image: "https://images.unsplash.com/photo-1552728089-57bdde30beb3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
                description: "Птицы — класс теплокровных яйцекладущих позвоночных животных, представляющий собой хорошо обособленную группу, одним из наиболее характерных признаков представителей которой является покров из перьев, предохраняющий тело от неблагоприятных изменений температуры и играющий важную роль при полёте. Птицы освоили практически все экосистемы Земли, от Арктики до Антарктики.",
                speciesCount: "Более 10 000 видов",
                habitat: "Практически все экосистемы от Арктики до Антарктики: леса, степи, пустыни, горы, побережья, открытый океан",
                size: "От 5 см (колибри) до 2.8 м (страус)",
                lifespan: "От 2-3 лет (мелкие воробьиные) до 70+ лет (орлы, попугаи, альбатросы)",
                features: [
                    "Покров из перьев",
                    "Передние конечности преобразованы в крылья",
                    "Клюв без зубов",
                    "Облегченный скелет с полыми костями",
                    "Высокий уровень метаболизма",
                    "Сложное поведение, включая пение и миграции",
                    "Откладка яиц с твердой скорлупой"
                ],
                characteristics: [
                    {title: "Температура тела", value: "Постоянная (40-44°C)"},
                    {title: "Дыхание", value: "Легочное, с воздушными мешками"},
                    {title: "Кровеносная система", value: "Замкнутая, 4-камерное сердце"},
                    {title: "Органы чувств", value: "Отличное зрение, слух, у некоторых - обоняние"},
                    {title: "Размножение", value: "Яйцекладущие, забота о потомстве"},
                    {title: "Пищеварение", value: "Быстрое, с желудком и мускульным желудком"}
                ],
                examples: ["Орлан-белохвост", "Колибри", "Императорский пингвин", "Страус", "Попугай", "Альбатрос"],
                fact: "Колибри — единственные птицы, способные летать назад. Их крылья могут совершать до 80 взмахов в секунду. Некоторые виды колибри мигрируют на расстояние до 5000 км."
            },
            reptiles: {
                title: "Рептилии",
                image: "https://images.unsplash.com/photo-1579954115545-a95591f28bfc?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
                description: "Рептилии (пресмыкающиеся) — класс позвоночных животных, кожа которых покрыта роговыми чешуями или щитками. Рептилии распространены на всех материках, кроме Антарктиды. Большинство рептилий — наземные животные, но некоторые живут в воде. Рептилии — холоднокровные животные, их активность зависит от температуры окружающей среды. Они включают четыре современных отряда: чешуйчатые (ящерицы и змеи), черепахи, крокодилы и клювоголовые (гаттерия).",
                speciesCount: "Более 11 000 видов",
                habitat: "Преимущественно тёплые регионы: пустыни, тропические леса, саванны, реки, озера, моря (морские черепахи, морские змеи)",
                size: "От 1.6 см (карликовый геккон) до 7 м (сетчатый питон, гребнистый крокодил)",
                lifespan: "От 2-3 лет (мелкие ящерицы) до 150+ лет (галапагосские черепахи)",
                features: [
                    "Холоднокровность (эктотермия)",
                    "Кожа покрыта роговыми чешуями или щитками",
                    "Легочное дыхание",
                    "Яйцекладущие с кожистой или известковой скорлупой",
                    "Трехкамерное сердце (у крокодилов четырехкамерное)",
                    "Развитые органы чувств",
                    "Многие виды способны к автотомии (отбрасыванию хвоста)"
                ],
                characteristics: [
                    {title: "Температура тела", value: "Зависит от окружающей среды (пойкилотермные)"},
                    {title: "Дыхание", value: "Легочное, у водных - дополнительное кожное"},
                    {title: "Кровеносная система", value: "3-камерное сердце (4-камерное у крокодилов)"},
                    {title: "Покровы", value: "Сухая кожа с роговыми чешуями, линька"},
                    {title: "Размножение", value: "Яйцекладущие, некоторые яйцеживородящие"},
                    {title: "Органы чувств", value: "Хорошее зрение, обоняние, терморецепция у змей"}
                ],
                examples: ["Комодский варан", "Королевская кобра", "Зеленая морская черепаха", "Гребнистый крокодил", "Хамелеон", "Анаконда"],
                fact: "Некоторые виды змей могут обходиться без пищи до двух лет благодаря медленному метаболизму. Змеиная кожа не растягивается, поэтому они сбрасывают ее целиком (линяют) по мере роста."
            },
            fish: {
                title: "Рыбы",
                image: "https://images.unsplash.com/photo-1599487488170-d11ec9c172f0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
                description: "Рыбы — парафилетическая группа водных позвоночных животных. Обладают жабрами и конечностями в виде плавников. Рыбы населяют солёные и пресные водоёмы по всей планете: от высокогорных водоёмов до глубинных впадин Мирового океана. Рыбы играют важную роль в большинстве водных экосистем как составляющая пищевых цепей. Они представляют собой наиболее древнюю и разнообразную группу позвоночных.",
                speciesCount: "Более 35 000 видов",
                habitat: "Моря, океаны, реки, озера, пруды, ручьи, подземные воды, высокогорные водоемы",
                size: "От 7.9 мм (Paedocypris progenetica) до 20 м (китовая акула)",
                lifespan: "От нескольких недель (некоторые виды карпозубых) до 100+ лет (осетр, окунь)",
                features: [
                    "Жабры для дыхания в воде",
                    "Плавники для передвижения",
                    "Чешуя (у большинства видов)",
                    "Холоднокровность (за редким исключением)",
                    "Боковая линия - орган чувств",
                    "Плавательный пузырь (у большинства костистых)",
                    "Наружное или внутреннее оплодотворение"
                ],
                characteristics: [
                    {title: "Температура тела", value: "Зависит от окружающей среды (пойкилотермные)"},
                    {title: "Дыхание", value: "Жаберное, некоторые имеют дополнительные органы"},
                    {title: "Кровеносная система", value: "Замкнутая, 2-камерное сердце"},
                    {title: "Покровы", value: "Кожа со слизью и чешуей (или без)"},
                    {title: "Органы чувств", value: "Боковая линия, обоняние, зрение, электрорецепция"},
                    {title: "Размножение", value: "Чаще наружное оплодотворение, икрометание"}
                ],
                examples: ["Китовая акула", "Рыба-клоун", "Пиранья", "Манта", "Рыба-парусник", "Морской конек"],
                fact: "Рыба-парусник — самая быстрая рыба в мире, способная развивать скорость до 110 км/ч. Некоторые виды рыб могут менять пол в течение жизни в зависимости от социальных условий."
            },
            insects: {
                title: "Насекомые",
                image: "https://images.unsplash.com/photo-1565402170291-8491f14678db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
                description: "Насекомые — класс беспозвоночных членистоногих животных. Насекомые являются самой разнообразной группой животных на Земле, включающей более 1 миллиона описанных видов, что составляет более половины всех известных живых организмов. Насекомые освоили все среды обитания: наземно-воздушную, водную и почвенную. Они играют ключевую роль в функционировании экосистем как опылители, разрушители органики, звенья пищевых цепей.",
                speciesCount: "Более 1 000 000 видов (оценивается до 10 млн)",
                habitat: "Практически все среды обитания по всей планете, кроме морских глубин",
                size: "От 0.139 мм (перепончатокрылые) до 57 см (палочник)",
                lifespan: "От 1 дня (подёнки) до 50 лет (королевы термитов)",
                features: [
                    "Тело разделено на голову, грудь и брюшко",
                    "Три пары ног (6 ног)",
                    "Одна пара усиков (антенн)",
                    "Обычно две пары крыльев (у большинства)",
                    "Хитиновый экзоскелет",
                    "Развитие с метаморфозом (полным или неполным)",
                    "Фасеточные глаза"
                ],
                characteristics: [
                    {title: "Дыхание", value: "Трахейное, через дыхальца"},
                    {title: "Кровеносная система", value: "Открытая, спинной сосуд"},
                    {title: "Нервная система", value: "Окологлоточное кольцо, брюшная нервная цепочка"},
                    {title: "Размножение", value: "Половое, часто партеногенез"},
                    {title: "Органы чувств", value: "Фасеточные глаза, усики, сенсиллы"},
                    {title: "Пищеварение", value: "Разные типы в зависимости от пищи"}
                ],
                examples: ["Бабочка-монарх", "Медоносная пчела", "Муравей", "Стрекоза", "Жук-олень", "Богомол"],
                fact: "Муравьи никогда не спят. Вместо этого у них есть циклы покоя и активности, которые длятся около 8 минут. Колония муравьев может содержать миллионы особей и функционировать как суперорганизм с разделением труда."
            },
            amphibians: {
                title: "Амфибии",
                image: "https://images.unsplash.com/photo-1559253664-ca249d4608c6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80",
                description: "Амфибии или земноводные — класс позвоночных четвероногих животных, которые могут жить как в воде, так и на суше. Амфибии занимают промежуточное положение между рыбами и настоящими наземными позвоночными. Для большинства амфибий характерно наличие личиночной стадии развития в воде с жаберным дыханием и взрослой стадии на суше с лёгочным дыханием. Они включают три современных отряда: бесхвостые (лягушки, жабы), хвостатые (саламандры, тритоны) и безногие (червяги).",
                speciesCount: "Более 8000 видов",
                habitat: "Влажные места вблизи водоемов: болота, пруды, реки, тропические леса, некоторые в засушливых регионах",
                size: "От 7.7 мм (лягушка Paedophryne amauensis) до 1.8 м (китайская гигантская саламандра)",
                lifespan: "От 1-2 лет (некоторые лягушки) до 55+ лет (японская исполинская саламандра)",
                features: [
                    "Голая кожа с железами, выделяющая слизь",
                    "Холоднокровность",
                    "Двойное дыхание: легкие и кожа (у личинок жабры)",
                    "Развитие с метаморфозом (у большинства)",
                    "Откладка икры в воду (у большинства)",
                    "Четыре конечности (кроме безногих)",
                    "Трехкамерное сердце"
                ],
                characteristics: [
                    {title: "Температура тела", value: "Зависит от окружающей среды (пойкилотермные)"},
                    {title: "Дыхание", value: "Легочное, кожное, у личинок жаберное"},
                    {title: "Кровеносная система", value: "Замкнутая, 3-камерное сердце"},
                    {title: "Покровы", value: "Голая кожа с слизистыми и ядовитыми железами"},
                    {title: "Размножение", value: "Чаще наружное оплодотворение в воде"},
                    {title: "Органы чувств", value: "Боковая линия у личинок, хорошее обоняние"}
                ],
                examples: ["Лягушка-голиаф", "Огненная саламандра", "Аксолотль", "Древолаз", "Жаба-ага", "Тритон"],
                fact: "Некоторые виды лягушек могут выживать после замерзания. Они вырабатывают глицерин, который действует как антифриз, защищая их клетки. Весной они оттаивают и возвращаются к нормальной жизни."
            }
        };

        // Данные для представителей (все 36 представителей)
        const representativesData = {
            // Млекопитающие (6)
            elephant: {
                title: "Африканский слон",
                image: "https://images.unsplash.com/photo-1557050543-4d5f4e07ef46?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Африканский слон — крупнейшее наземное млекопитающее на планете. Обитает в саваннах и лесах Африки. Обладает высоким интеллектом, сложной социальной структурой и отличной памятью. Слоны живут семейными группами под руководством старшей самки (матриарха).",
                scientificName: "Loxodonta africana",
                family: "Слоновые (Elephantidae)",
                weight: "До 7 тонн",
                length: "До 4 метров в высоту",
                lifespan: "60-70 лет в дикой природе",
                habitat: "Саванны, леса и болота Африки к югу от Сахары",
                features: [
                    "Самые большие уши среди животных",
                    "Хобот - универсальный орган для дыхания, обоняния, хватания, питья",
                    "Бивни - удлиненные резцы, растут всю жизнь",
                    "Сложная социальная структура и эмоциональная жизнь",
                    "Отличная память, могут помнить места и других слонов десятилетиями"
                ],
                interestingFacts: "Слоны - единственные млекопитающие, кроме человека, которые могут узнавать себя в зеркале. Они также оплакивают своих умерших сородичей и навещают места, где умерли их родственники. Слоны могут общаться друг с другом на низких частотах, неслышимых для человека, на расстоянии до 10 км.",
                conservation: "Уязвимый вид (VU). Основные угрозы: браконьерство ради бивней, потеря среды обитания, конфликты с человеком. Популяция сократилась на 30% за последние 10 лет."
            },
            whale: {
                title: "Синий кит",
                image: "https://images.unsplash.com/photo-1574871619173-b8b6f1a926e9?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Синий кит — крупнейшее животное, когда-либо существовавшее на Земле. Питается в основном крилем, фильтруя воду через китовый ус. Издает самые громкие звуки среди животных, которые могут распространяться на сотни километров под водой.",
                scientificName: "Balaenoptera musculus",
                family: "Полосатиковые (Balaenopteridae)",
                weight: "До 200 тонн",
                length: "До 33 метров",
                lifespan: "80-90 лет",
                habitat: "Все океаны мира, от тропиков до полярных вод",
                features: [
                    "Сердце размером с небольшой автомобиль",
                    "Язык весит как слон (до 4 тонн)",
                    "Новорожденный детеныш весит 2-3 тонны",
                    "Питается крилем, потребляя до 4 тонн в день",
                    "Издает звуки громкостью до 188 децибел"
                ],
                interestingFacts: "Синий кит настолько огромен, что человек может проплыть по его артериям. Новорожденный китенок прибавляет в весе около 90 кг в день. Несмотря на свои размеры, синие киты питаются одними из самых маленьких морских существ — крилем.",
                conservation: "Вымирающий вид (EN). Популяция сократилась на 90% из-за китобойного промысла в XX веке. Сейчас охраняется международным правом, но численность восстанавливается медленно."
            },
            panda: {
                title: "Большая панда",
                image: "https://images.unsplash.com/photo-1564349683136-77e08dba1ef7?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Большая панда — символ Всемирного фонда дикой природы (WWF) и охраны природы в целом. Несмотря на принадлежность к отряду хищных, питается в основном бамбуком. Имеет уникальную черно-белую окраску, которая помогает маскироваться в заснеженных и теневых местах обитания.",
                scientificName: "Ailuropoda melanoleuca",
                family: "Медвежьи (Ursidae)",
                weight: "70-125 кг",
                length: "1.2-1.9 метра",
                lifespan: "20 лет в дикой природе, до 30 в неволе",
                habitat: "Горные леса центрального Китая на высоте 1200-3900 м",
                features: [
                    "«Шестой палец» — видоизмененная кость запястья для хватания бамбука",
                    "Питается бамбуком на 99%, хотя пищеварительная система хищника",
                    "Проводит 10-16 часов в день за едой",
                    "Новорожденный детеныш весит всего 100-200 грамм",
                    "Имеет самые мощные зубы среди медведей"
                ],
                interestingFacts: "Детеныш панды рождается слепым и почти голым, размером примерно с пачку масла. Панды — одиночки, встречаются только в брачный период. Несмотря на милый внешний вид, большие панды могут быть опасны и обладают значительной силой.",
                conservation: "Уязвимый вид (VU). Благодаря усилиям по сохранению, популяция медленно растет. Основные угрозы: разрушение среды обитания, низкая рождаемость, фрагментация популяции."
            },
            cheetah: {
                title: "Гепард",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Гепард — самое быстрое наземное животное, способное развивать скорость до 110 км/ч. Отличается стройным телом, длинными ногами и не втягивающимися когтями, которые обеспечивают лучшее сцепление с землей при беге.",
                scientificName: "Acinonyx jubatus",
                family: "Кошачьи (Felidae)",
                weight: "35-65 кг",
                length: "1.1-1.5 метра",
                lifespan: "10-12 лет в дикой природе",
                habitat: "Саванны и полупустыни Африки и Ирана",
                features: [
                    "Специальные «слезные дорожки» от глаз к пасти для защиты от солнца",
                    "Гибкий позвоночник для увеличения длины шага при беге",
                    "Не втягивающиеся когти для лучшего сцепления",
                    "Охотится днем, полагаясь на зрение, а не на обоняние",
                    "Может разгоняться до 75 км/ч за 2 секунды"
                ],
                interestingFacts: "Гепард — единственная большая кошка, которая не может рычать. Вместо этого они издают звуки, похожие на птичье чириканье. При беге гепард проводит до 50% времени в воздухе, отрываясь от земли.",
                conservation: "Уязвимый вид (VU). Популяция сокращается из-за потери среды обитания, конфликтов с человеком и низкого генетического разнообразия. В мире осталось менее 7000 особей."
            },
            dolphin: {
                title: "Афалина (дельфин)",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Афалина — один из самых умных морских млекопитающих. Использует сложную систему эхолокации для навигации и охоты. Обладает развитой социальной структурой и сложными формами коммуникации.",
                scientificName: "Tursiops truncatus",
                family: "Дельфиновые (Delphinidae)",
                weight: "150-650 кг",
                length: "2-4 метра",
                lifespan: "40-50 лет",
                habitat: "Умеренные и тропические моря по всему миру",
                features: [
                    "Высокоразвитый мозг с сложной корой",
                    "Эхолокация для обнаружения добычи и навигации",
                    "Сложная социальная структура с индивидуальными «именами»",
                    "Способность к самопознанию и решению сложных задач",
                    "Использует морские губки как инструменты для добычи пищи"
                ],
                interestingFacts: "Дельфины спят с одним открытым глазом, чтобы следить за опасностью. Они дают друг другу индивидуальные «имена» — уникальные свисты. Дельфины могут узнавать себя в зеркале и проявляют альтруистическое поведение, помогая раненым сородичам.",
                conservation: "Вызывающий наименьшие опасения (LC). Основные угрозы: попадание в рыболовные сети, загрязнение океанов, шумовое загрязнение от судов. Некоторые локальные популяции находятся под угрозой."
            },
            human: {
                title: "Человек разумный",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Человек — единственный современный вид рода Homo. Обладает развитым сознанием, речью, способностью к абстрактному мышлению и созданию сложных орудий. Единственный вид, создавший цивилизацию и глобальную культуру.",
                scientificName: "Homo sapiens",
                family: "Гоминиды (Hominidae)",
                weight: "50-100 кг",
                length: "1.5-1.9 метра",
                lifespan: "70-80 лет (в развитых странах)",
                habitat: "Все континенты и экосистемы, включая искусственные среды",
                features: [
                    "Прямохождение и развитый большой палец",
                    "Самый развитый мозг относительно размера тела",
                    "Сложная речь и языковые способности",
                    "Способность к абстрактному мышлению и планированию",
                    "Создание и использование сложных инструментов"
                ],
                interestingFacts: "Человек — единственный вид, который может плакать от эмоций. У нас самый длинный период детства среди млекопитающих. Человеческий мозг потребляет 20% энергии тела, составляя лишь 2% от его веса.",
                conservation: "Не находится под угрозой. Популяция превышает 8 миллиардов особей. Однако деятельность человека угрожает многим другим видам и экосистемам планеты."
            },

            // Птицы (6)
            eagle: {
                title: "Орлан-белохвост",
                image: "https://images.unsplash.com/photo-1596273315327-5f059a42b4c0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Орлан-белохвост — крупная хищная птица, символ силы и свободы. Обитает near водоемов, где охотится на рыбу и водоплавающих птиц. Имеет мощный клюв и когти, отличное зрение, позволяющее видеть добычу с большой высоты.",
                scientificName: "Haliaeetus albicilla",
                family: "Ястребиные (Accipitridae)",
                weight: "3-7 кг",
                length: "До 1 метра, размах крыльев до 2.4 метра",
                lifespan: "20-25 лет в дикой природе",
                habitat: "Побережья, крупные озера и реки Евразии",
                features: [
                    "Мощный крючковатый клюв для разрывания добычи",
                    "Острое зрение — в 3-4 раза лучше человеческого",
                    "Белый хвост у взрослых особей (отсюда название)",
                    "Мощные лапы с острыми когтями",
                    "Строит огромные гнезда до 2 метров в диаметре"
                ],
                interestingFacts: "Орланы образуют пары на всю жизнь. Они строят самые большие гнезда среди птиц, которые используют много лет подряд, каждый год достраивая их. Орлан может поднять в воздух добычу весом до 5 кг.",
                conservation: "Вызывающий наименьшие опасения (LC). Численность восстановилась после запрета ДДТ в 1970-х годах. В некоторых регионах все еще редок и охраняется."
            },
            hummingbird: {
                title: "Колибри",
                image: "https://images.unsplash.com/photo-1530919424169-4b95c30a00b0?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Колибри — самые маленькие птицы в мире. Единственные птицы, способные летать назад. Питаются нектаром цветов, играя важную роль в опылении. Обладают невероятно быстрым метаболизмом и должны питаться каждые 10-15 минут.",
                scientificName: "Trochilidae (семейство, более 350 видов)",
                family: "Колибри (Trochilidae)",
                weight: "2-20 грамм",
                length: "5-22 см",
                lifespan: "3-5 лет в дикой природе",
                habitat: "Америка — от Аляски до Огненной Земли",
                features: [
                    "Способность зависать в воздухе и летать во всех направлениях",
                    "Крылья совершают 50-80 взмахов в секунду",
                    "Сердце бьется 500-1200 раз в минуту",
                    "Длинный тонкий клюв для добычи нектара",
                    "Яркое оперение с металлическим блеском"
                ],
                interestingFacts: "Некоторые виды колибри мигрируют на огромные расстояния — рубиновогорлый колибри преодолевает 800 км над Мексиканским заливом без остановки. Во время полета сердце колибри бьется с частотой до 1200 ударов в минуту, а ночью они впадают в оцепенение, замедляя метаболизм.",
                conservation: "Большинство видов не находятся под угрозой, но некоторые редкие виды уязвимы из-за потери среды обитания. Все виды охраняются законом в США и многих других странах."
            },
            penguin: {
                title: "Императорский пингвин",
                image: "https://images.unsplash.com/photo-1589561253898-768ab8d6d5e5?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Императорский пингвин — самый крупный вид пингвинов и единственный, который размножается в суровых условиях антарктической зимы. Самец высиживает яйцо в течение двух месяцев, не питаясь и выдерживая температуры до -60°C.",
                scientificName: "Aptenodytes forsteri",
                family: "Пингвиновые (Spheniscidae)",
                weight: "20-45 кг",
                length: "До 1.3 метра",
                lifespan: "15-20 лет в дикой природе",
                habitat: "Антарктида и прилегающие воды",
                features: [
                    "Густое оперение и слой жира для защиты от холода",
                    "Способность нырять на глубину до 500 метров",
                    "Задерживает дыхание на 20 минут",
                    "Самцы высиживают яйца, собираясь в плотные группы для тепла",
                    "Плавает со скоростью до 6-9 км/ч"
                ],
                interestingFacts: "Императорские пингвины — рекордсмены по глубине погружения среди птиц. Они могут нырять на глубину более 500 метров. Во время высиживания яиц самцы теряют до 50% веса. Пингвины образуют «детские сады», где оставляют птенцов, пока добывают пищу.",
                conservation: "Близкий к уязвимому положению (NT). Основные угрозы: изменение климата, сокращение площади морского льда, уменьшение количества криля — основной пищи пингвинов."
            },
            ostrich: {
                title: "Африканский страус",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Страус — самая крупная птица в мире, не умеющая летать, но отлично бегающая. Имеет длинные мощные ноги, которые позволяют развивать скорость до 70 км/ч. Откладывает самые большие яйца среди птиц.",
                scientificName: "Struthio camelus",
                family: "Страусовые (Struthionidae)",
                weight: "90-130 кг",
                length: "До 2.7 метра",
                lifespan: "40-45 лет",
                habitat: "Саванны и полупустыни Африки",
                features: [
                    "Двупалые ноги с мощными когтями для бега и защиты",
                    "Крупные глаза (диаметр 5 см) — самые большие среди наземных животных",
                    "Отсутствие киля на грудине (не летает)",
                    "Яйца весом до 1.5 кг",
                    "Питается растениями, семенами, иногда мелкими животными"
                ],
                interestingFacts: "Глаза страуса больше, чем его мозг. Страусы могут бегать со скоростью до 70 км/ч, делая шаги длиной 3-5 метров. Вопреки мифу, страусы не прячут голову в песок — они припадают к земле, чтобы стать менее заметными.",
                conservation: "Вызывающий наименьшие опасения (LC). Широко распространен в Африке. Разводится на фермах по всему миру ради мяса, кожи и перьев."
            },
            parrot: {
                title: "Ара (попугай)",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Ара — крупный попугай с ярким оперением, обитающий в тропических лесах Центральной и Южной Америки. Обладает высоким интеллектом, способен имитировать человеческую речь и решать сложные задачи.",
                scientificName: "Ara (род, 8 видов)",
                family: "Попугаевые (Psittacidae)",
                weight: "1-1.7 кг",
                length: "80-95 см",
                lifespan: "50-80 лет",
                habitat: "Тропические леса Центральной и Южной Америки",
                features: [
                    "Мощный изогнутый клюв для раскалывания орехов",
                    "Зигодактильные лапы (2 пальца вперед, 2 назад) для лазания",
                    "Яркое оперение с металлическим блеском",
                    "Высокий интеллект, способность к имитации звуков",
                    "Моногамны, образуют пары на всю жизнь"
                ],
                interestingFacts: "Ара могут доживать до 80 лет в неволе. Они обладают интеллектом 4-летнего ребенка и могут решать сложные задачи. Попугаи — единственные птицы, которые едят, держа пищу в лапе. Клюв ара настолько силен, что может расколоть кокосовый орех.",
                conservation: "Многие виды находятся под угрозой из-за потери среды обитания и незаконной торговли. Сине-желтый ара — уязвимый вид (VU), гиацинтовый ара — вымирающий (EN)."
            },
            albatross: {
                title: "Странствующий альбатрос",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Странствующий альбатрос — птица с самым большим размахом крыльев среди современных птиц. Проводит большую часть жизни в полете над океаном, совершая длительные миграции и преодолевая тысячи километров без отдыха.",
                scientificName: "Diomedea exulans",
                family: "Альбатросовые (Diomedeidae)",
                weight: "8-12 кг",
                length: "Размах крыльев до 3.5 метров",
                lifespan: "50+ лет",
                habitat: "Открытый океан Южного полушария",
                features: [
                    "Самый большой размах крыльев среди птиц",
                    "Способность парить часами без взмахов крыльев",
                    "Трубчатые ноздри для выведения соли из организма",
                    "Моногамны, образуют пары на всю жизнь",
                    "Сложные брачные танцы"
                ],
                interestingFacts: "Альбатросы могут спать в полете. Они преодолевают до 1000 км в день и могут облететь земной шар за 46 дней. Молодые альбатросы проводят первые 5-10 лет жизни в непрерывном полете над океаном, прежде чем вернуться на сушу для размножения.",
                conservation: "Уязвимый вид (VU). Основные угрозы: попадание в рыболовные сети, пластиковое загрязнение океана, изменение климата. Популяция сокращается во всем ареале."
            },

            // Рептилии (6)
            komodo: {
                title: "Комодский варан",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Комодский варан — крупнейшая ящерица в мире, достигающая 3 метров в длину и 90 кг веса. Обитает на нескольких индонезийских островах. Является активным хищником, охотящимся на оленей, кабанов и даже буйволов. Имеет ядовитые железы и бактерии в слюне.",
                scientificName: "Varanus komodoensis",
                family: "Варановые (Varanidae)",
                weight: "До 90 кг",
                length: "До 3 метров",
                lifespan: "30 лет в дикой природе",
                habitat: "Тропические леса и саванны индонезийских островов Комодо, Ринка, Флорес и Гили-Мотанг",
                features: [
                    "Мощные челюсти с загнутыми назад зубами",
                    "Ядовитые железы в нижней челюсти",
                    "Острое обоняние, может учуять добычу за 5 км",
                    "Развитый интеллект среди рептилий",
                    "Может бегать со скоростью до 20 км/ч на короткие дистанции"
                ],
                interestingFacts: "Комодские вараны могут съесть до 80% своего веса за один прием пищи. Их слюна содержит более 50 видов бактерий, которые вызывают заражение крови у укушенной жертвы. Вараны — каннибалы, молодые особи живут на деревьях, чтобы избежать быть съеденными взрослыми.",
                conservation: "Уязвимый вид (VU). Обитает на ограниченной территории. Основные угрозы: сокращение добычи из-за браконьерства, природные катастрофы, туризм. Охраняется в национальном парке Комодо."
            },
            cobra: {
                title: "Королевская кобра",
                image: "https://images.unsplash.com/photo-1572977497251-9e05cb47d983?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Королевская кобра — самая длинная ядовитая змея в мире, достигающая 5.5 метров. Обитает в тропических лесах Южной и Юго-Восточной Азии. Питается в основном другими змеями, включая ядовитых. При угрозе поднимает переднюю часть тела и расширяет капюшон.",
                scientificName: "Ophiophagus hannah",
                family: "Аспидовые (Elapidae)",
                weight: "6-9 кг",
                length: "До 5.5 метров",
                lifespan: "20 лет в дикой природе",
                habitat: "Тропические леса, бамбуковые заросли, мангровые болота Южной и Юго-Восточной Азии",
                features: [
                    "Самый длинный среди ядовитых змей",
                    "Питается преимущественно другими змеями",
                    "Может поднимать до 1/3 тела над землей",
                    "Нейротоксический яд, поражающий нервную систему",
                    "Единственная змея, строящая гнездо для яиц"
                ],
                interestingFacts: "Королевская кобра — единственная змея, которая строит гнездо для откладывания яиц и охраняет его до вылупления детенышей. Один укус содержит достаточно яда, чтобы убить 20 человек или даже слона. Несмотря на устрашающую репутацию, королевская кобра редко нападает на человека, предпочитая избегать встреч.",
                conservation: "Уязвимый вид (VU). Популяция сокращается из-за уничтожения лесов и незаконной торговли. Охраняется во многих странах ареала, но браконьерство продолжает оставаться проблемой."
            },
            turtle: {
                title: "Зеленая морская черепаха",
                image: "https://images.unsplash.com/photo-1595521626788-00d2a2f6b730?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Зеленая морская черепаха — крупная морская черепаха, питающаяся в основном морскими водорослями и травой. Совершает длительные миграции между местами кормежки и гнездования. Получила название из-за зеленого цвета жира, а не панциря.",
                scientificName: "Chelonia mydas",
                family: "Морские черепахи (Cheloniidae)",
                weight: "До 200 кг",
                length: "До 1.5 метров",
                lifespan: "80+ лет",
                habitat: "Тропические и субтропические моря по всему миру",
                features: [
                    "Обтекаемый панцирь для эффективного плавания",
                    "Передние ласты превращены в ласты для плавания",
                    "Может задерживать дыхание на несколько часов",
                    "Самки возвращаются для кладки яиц на тот же пляж, где родились",
                    "Питается в основном морской растительностью"
                ],
                interestingFacts: "Зеленые черепахи могут проплывать тысячи километров между местами кормежки и гнездования. Они обладают «магнитным компасом», который помогает им ориентироваться в океане. Температура песка, в котором инкубируются яйца, определяет пол детенышей: в теплом песке рождаются самки, в прохладном — самцы.",
                conservation: "Вымирающий вид (EN). Основные угрозы: сбор яиц, браконьерство, запутывание в рыболовных сетях, загрязнение океана, разрушение пляжей для гнездования. Охраняется международными соглашениями."
            },
            crocodile: {
                title: "Гребнистый крокодил",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Гребнистый крокодил — крупнейший современный крокодил и рептилия. Обитает в солоноватых водах Юго-Восточной Азии и Австралии. Является вершиной пищевой цепи в своей экосистеме. Обладает самым сильным укусом среди всех животных.",
                scientificName: "Crocodylus porosus",
                family: "Крокодиловые (Crocodylidae)",
                weight: "До 1000 кг",
                length: "До 7 метров",
                lifespan: "70+ лет",
                habitat: "Мангровые болота, дельты рек, прибрежные воды Юго-Восточной Азии и Северной Австралии",
                features: [
                    "Самый сильный укус среди животных — до 340 атмосфер",
                    "Четырехкамерное сердце (уникально среди рептилий)",
                    "Может жить в соленой воде благодаря специальным железам",
                    "Сложное родительское поведение — охраняет гнездо и помогает детенышам",
                    "Может проплывать до 1000 км по морю"
                ],
                interestingFacts: "Гребнистый крокодил обладает самым сильным укусом в животном мире — сила укуса превышает 340 атмосфер. Они могут выпрыгивать из воды почти всем телом, чтобы схватить добычу с низко свисающих ветвей. Крокодилы плачут не от эмоций, а для выведения избытка соли из организма.",
                conservation: "Вызывающий наименьшие опасения (LC). Популяция стабильна в Австралии, но сокращается в некоторых частях Азии из-за браконьерства и потери среды обитания."
            },
            chameleon: {
                title: "Йеменский хамелеон",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Йеменский хамелеон — известен способностью менять цвет кожи в зависимости от настроения, температуры и окружения. Имеет длинный язык для ловли насекомых и независимо движущиеся глаза, что позволяет смотреть в двух направлениях одновременно.",
                scientificName: "Chamaeleo calyptratus",
                family: "Хамелеоновые (Chamaeleonidae)",
                weight: "90-180 г",
                length: "35-50 см",
                lifespan: "5-8 лет",
                habitat: "Горные районы Йемена и Саудовской Аравии",
                features: [
                    "Способность менять цвет кожи за несколько секунд",
                    "Независимо движущиеся глаза на 180° по горизонтали и 90° по вертикали",
                    "Язык длиннее тела для ловли добычи",
                    "Цепкий хвост для лазания по деревьям",
                    "Зигодактильные лапы для удобного хватания веток"
                ],
                interestingFacts: "Хамелеоны меняют цвет не только для маскировки, но и для коммуникации, регулирования температуры и выражения эмоций. Их язык ускоряется со скоростью 0-100 км/ч за 1/100 секунды. Глаза хамелеона могут смотреть в разные стороны одновременно, что дает им 360-градусный обзор.",
                conservation: "Вызывающий наименьшие опасения (LC). Популяция стабильна. Широко разводится в неволе как домашнее животное."
            },
            anaconda: {
                title: "Зеленая анаконда",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Зеленая анаконда — одна из самых крупных змей в мире. Обитает в тропических реках Южной Америки. Не ядовита, убивает добычу удушением, обвиваясь вокруг жертвы и сжимая ее. Проводит большую часть времени в воде.",
                scientificName: "Eunectes murinus",
                family: "Ложноногие (Boidae)",
                weight: "До 250 кг",
                length: "До 9 метров",
                lifespan: "10-30 лет",
                habitat: "Тропические реки, болота и затопленные леса Южной Америки",
                features: [
                    "Самая тяжелая змея в мире",
                    "Ноздри и глаза расположены на верхней части головы для плавания",
                    "Не ядовита, убивает добычу удушением",
                    "Может оставаться под водой до 10 минут",
                    "Самки значительно крупнее самцов"
                ],
                interestingFacts: "Анаконда — самая тяжелая змея в мире, хотя и не самая длинная (рекорд длины принадлежит сетчатому питону). Самки могут съедать самцов после спаривания. Новорожденные анаконды длиной около 70 см полностью самостоятельны и могут плавать и охотиться сразу после рождения.",
                conservation: "Не оценен (NE). Популяция стабильна, но точных данных нет из-за труднодоступности мест обитания. Основные угрозы: уничтожение тропических лесов, охота ради кожи."
            },

            // Рыбы (6)
            whale_shark: {
                title: "Китовая акула",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Китовая акула — самая крупная рыба в мире. Питается планктоном, фильтруя воду через жабры. Совершает длительные миграции через океаны. Несмотря на размеры, совершенно безопасна для человека.",
                scientificName: "Rhincodon typus",
                family: "Китовые акулы (Rhincodontidae)",
                weight: "До 34 тонн",
                length: "До 20 метров",
                lifespan: "70-100 лет",
                habitat: "Теплые тропические и субтропические моря по всему миру",
                features: [
                    "Самая крупная рыба в мире",
                    "Питается планктоном, фильтруя воду через жабры",
                    "Уникальный пятнистый узор на коже, индивидуальный для каждой особи",
                    "До 3000 мелких зубов, не используемых для питания",
                    "Может нырять на глубину до 1800 метров"
                ],
                interestingFacts: "У каждой китовой акулы уникальный узор пятен на коже, как отпечатки пальцев у человека. Они могут фильтровать до 6000 литров воды в час. Несмотря на размеры, китовые акулы — медленные пловцы, их скорость обычно не превышает 5 км/ч.",
                conservation: "Вымирающий вид (EN). Основные угрозы: столкновения с судами, незаконный промысел, изменение климата, туризм. Охраняется международными соглашениями."
            },
            clownfish: {
                title: "Рыба-клоун",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Рыба-клоун — известна симбиозом с актиниями. Имеет яркую окраску с белыми полосами. Живет небольшими группами с четкой иерархией. Все особи рождаются самцами, некоторые становятся самками.",
                scientificName: "Amphiprioninae (подсемейство, 30 видов)",
                family: "Помацентровые (Pomacentridae)",
                weight: "До 250 г",
                length: "10-18 см",
                lifespan: "6-10 лет",
                habitat: "Коралловые рифы Индийского и Тихого океанов",
                features: [
                    "Симбиоз с актиниями — защита в обмен на очистку и пищу",
                    "Слизь на коже защищает от жгучих клеток актинии",
                    "Все рождаются самцами, доминирующая особь становится самкой",
                    "Яркая окраска с 3 белыми полосами",
                    "Живет группами с одной самкой и несколькими самцами"
                ],
                interestingFacts: "После гибели самки самый крупный самец в группе меняет пол и становится новой самкой. Рыбы-клоуны издают щелкающие и хлопающие звуки для общения. Они никогда не уплывают далеко от своей актинии, максимальное расстояние — 1-2 метра.",
                conservation: "Большинство видов не находятся под угрозой, но некоторые уязвимы из-за разрушения коралловых рифов. Популярны в аквариумистике, что создает давление на дикие популяции."
            },
            piranha: {
                title: "Обыкновенная пиранья",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Пиранья — хищная рыба с мощными челюстями и острыми треугольными зубами. Обитает в реках Южной Америки. Охотится стаями, хотя большую часть времени питается падалью, фруктами и семенами. Репутация «свирепого хищника» сильно преувеличена.",
                scientificName: "Pygocentrus nattereri",
                family: "Пираньевые (Serrasalmidae)",
                weight: "До 3.5 кг",
                length: "До 50 см",
                lifespan: "10-25 лет",
                habitat: "Реки и озера Южной Америки, особенно бассейн Амазонки",
                features: [
                    "Мощные челюсти с острыми треугольными зубами",
                    "Охотится стаями, особенно в сухой сезон",
                    "Отличное обоняние для обнаружения крови",
                    "Красное брюхо у взрослых особей",
                    "Может издавать звуки, похожие на лай"
                ],
                interestingFacts: "Пираньи редко нападают на здоровых крупных животных, предпочитая больных, раненых или уже мертвых. Их зубы настолько остры, что индейцы используют их как ножницы и бритвы. Во время сухого сезона, когда вода отступает, пираньи могут нападать на все, что движется в воде.",
                conservation: "Вызывающий наименьшие опасения (LC). Популяция стабильна. Иногда рассматривается как вредитель, конкурирующий с промысловыми видами рыб."
            },
            manta: {
                title: "Манта (гигантский скат)",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Манта — крупнейший вид скатов с размахом «крыльев» до 7 метров. Питается планктоном, фильтруя воду через жабры. Совершает акробатические прыжки из воды. Обладает самым крупным мозгом среди рыб.",
                scientificName: "Mobula birostris",
                family: "Орляковые скаты (Myliobatidae)",
                weight: "До 2 тонн",
                length: "Размах до 7 метров",
                lifespan: "40-50 лет",
                habitat: "Тропические и субтропические моря по всему миру",
                features: [
                    "Самый крупный мозг относительно размера тела среди рыб",
                    "Питается планктоном, фильтруя воду через жабры",
                    "Прыгает из воды, возможно, для коммуникации или избавления от паразитов",
                    "Имеет «рога» — головные плавники для направления пищи в рот",
                    "У каждой особи уникальный рисунок на брюхе"
                ],
                interestingFacts: "Манты — единственные рыбы, которые могут узнавать себя в зеркале, что свидетельствует о самосознании. Они посещают «станции очистки», где мелкие рыбы чистят их кожу от паразитов. Манты рожают всего одного детеныша раз в 2-3 года после 12-13 месяцев беременности.",
                conservation: "Уязвимый вид (VU). Основные угрозы: целевой промысел ради жаберных пластин (используются в традиционной медицине), случайный вылов, столкновения с судами, изменение климата."
            },
            sailfish: {
                title: "Рыба-парусник",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Рыба-парусник — самая быстрая рыба в мире, способная развивать скорость до 110 км/ч. Имеет высокий спинной плавник, похожий на парус, который может складывать при быстром плавании. Охотится на стаи мелких рыб.",
                scientificName: "Istiophorus platypterus",
                family: "Парусниковые (Istiophoridae)",
                weight: "До 100 кг",
                length: "До 3.5 метров",
                lifespan: "10-15 лет",
                habitat: "Тропические и субтропические воды всех океанов",
                features: [
                    "Самый быстрый морской обитатель — до 110 км/ч",
                    "Высокий спинной плавник («парус»), складывающийся при быстром плавании",
                    "Длинное заостренное рыло («копье») для оглушения добычи",
                    "Способность менять цвет при возбуждении",
                    "Охотится, координируя действия в группах"
                ],
                interestingFacts: "Парусник может менять цвет, становясь ярко-голубым с полосами при возбуждении. При быстром плавании они складывают парус в специальную выемку на спине для уменьшения сопротивления. Парусники охотятся группами, окружая косяки рыб и по очереди атакуя их.",
                conservation: "Вызывающий наименьшие опасения (LC). Популяция стабильна. Популярный объект спортивной рыбалки, что регулируется квотами и правилами catch-and-release (поймал-отпустил)."
            },
            seahorse: {
                title: "Морской конек",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Морской конек — необычная рыба с вертикальным положением тела и головой, напоминающей лошадиную. Самец вынашивает икру в специальной сумке на брюхе. Плавает медленно, цепляясь хвостом за водоросли.",
                scientificName: "Hippocampus (род, 54 вида)",
                family: "Игловые (Syngnathidae)",
                weight: "До 200 г",
                length: "1.5-35 см в зависимости от вида",
                lifespan: "1-5 лет",
                habitat: "Тропические и умеренные моря, коралловые рифы, водорослевые заросли",
                features: [
                    "Самец вынашивает яйца в специальной сумке",
                    "Тело покрыто костными пластинками вместо чешуи",
                    "Цепкий хвост для прикрепления к водорослям",
                    "Независимо движущиеся глаза",
                    "Трубчатый рот для всасывания мелких ракообразных"
                ],
                interestingFacts: "Морские коньки — единственные животные, у которых самец беременеет и рожает. Они образуют моногамные пары и каждое утро исполняют брачный танец. Морские коньки настолько медленно плавают, что считаются самыми медленными рыбами в мире.",
                conservation: "Многие виды уязвимы из-за разрушения среды обитания, сбора для традиционной медицины и аквариумистики. Признаны нуждающимися в охране международными соглашениями."
            },

            // Насекомые (6)
            monarch: {
                title: "Бабочка-монарх",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Бабочка-монарх — известна своей эпической миграцией из Канады и США в Мексику. Яркая окраска предупреждает хищников о ядовитости. Гусеницы питаются молочаем, накапливая ядовитые сердечные гликозиды.",
                scientificName: "Danaus plexippus",
                family: "Нимфалиды (Nymphalidae)",
                weight: "0.5-1 г",
                length: "Размах крыльев 8-10 см",
                lifespan: "2-6 недель (летние поколения), 6-8 месяцев (мигрирующие)",
                habitat: "Северная Америка, мигрирует между Канадой/США и Мексикой",
                features: [
                    "Яркая оранжево-черно-белая окраска",
                    "Мигрирует на тысячи километров",
                    "Ядовита для большинства хищников",
                    "Использует солнце как компас для навигации",
                    "Зимует огромными скоплениями на деревьях"
                ],
                interestingFacts: "Мигрирующее поколение монархов живет в 8 раз дольше, чем летние поколения. Они никогда не были в местах зимовки, но находят их по врожденной программе. Одно дерево в Мексике может быть покрыто десятками тысяч бабочек.",
                conservation: "Находится на грани исчезновения (CR). Популяция сократилась на 80% за последние 20 лет. Основные угрозы: потеря молочая (кормового растения), изменение климата, использование пестицидов."
            },
            honeybee: {
                title: "Медоносная пчела",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Медоносная пчела — важный опылитель растений и производитель меда. Живет сложно организованными колониями с разделением труда. Обладает уникальным «танцевальным» языком для передачи информации о местонахождении пищи.",
                scientificName: "Apis mellifera",
                family: "Настоящие пчелы (Apidae)",
                weight: "0.1 г",
                length: "1-1.5 см",
                lifespan: "Рабочая пчела: 6 недель летом, королева: 2-5 лет",
                habitat: "Практически все регионы мира, кроме крайнего севера",
                features: [
                    "Сложная социальная организация с разделением труда",
                    "«Танец» для указания направления и расстояния до источника пищи",
                    "Производство меда из нектара",
                    "Жало с зазубринами (рабочие пчелы)",
                    "Способность регулировать температуру в улье"
                ],
                interestingFacts: "Чтобы произвести 1 кг меда, пчелы должны посетить около 4 миллионов цветков и пролететь расстояние, равное 4 оборотам вокруг Земли. Пчелы общаются с помощью танца: круглый танец означает пищу рядом, виляющий — дальнюю пищу с указанием направления. У пчел 5 глаз: 2 сложных и 3 простых.",
                conservation: "Зависит от человека. Дикие популяции сокращаются из-за клещей, пестицидов, потери среды обитания. Пчеловодство поддерживает численность домашних пчел."
            },
            ant: {
                title: "Муравей-листорез",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Муравей-листорез — выращивает грибы на срезанных листьях. Живет огромными колониями с миллионами особей. Имеет сложную социальную организацию с кастами разных размеров и функций. Создает подземные «фермы» грибов.",
                scientificName: "Atta (род, 47 видов)",
                family: "Муравьи (Formicidae)",
                weight: "1-5 мг",
                length: "0.3-2 см в зависимости от касты",
                lifespan: "Рабочий: 1-3 года, королева: 10-20 лет",
                habitat: "Тропические леса Центральной и Южной Америки",
                features: [
                    "Выращивает грибы на пережеванных листьях",
                    "Сложная кастовая система с разными размерами особей",
                    "Крупные солдаты с мощными челюстями для защиты",
                    "Создает подземные гнезда с камерами для грибных садов",
                    "Симбиоз с бактериями для защиты грибов от паразитов"
                ],
                interestingFacts: "Муравьи-листорезы создают самые сложные социальные структуры после человека. Их подземные гнезда могут достигать 8 метров в глубину и занимать площадь до 50 м². Муравьи используют антибиотики, производимые симбиотическими бактериями, для защиты своих грибных садов.",
                conservation: "Не находятся под угрозой. Муравьи-листорезы считаются вредителями сельского хозяйства в некоторых регионах, так как могут уничтожать целые плантации за несколько дней."
            },
            dragonfly: {
                title: "Стрекоза",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Стрекоза — хищное насекомое с отличным зрением и маневренным полетом. Личинки (наяды) живут в воде и также являются хищниками. Охотится на лету, ловя других насекомых. Имеет почти 360-градусное зрение.",
                scientificName: "Anisoptera (подотряд, около 3000 видов)",
                family: "Разные семейства стрекоз",
                weight: "0.5-2 г",
                length: "Размах крыльев 5-19 см",
                lifespan: "6 месяцев - 7 лет (большая часть жизни как личинка)",
                habitat: "Водоемы и их окрестности по всему миру, кроме Антарктиды",
                features: [
                    "Почти 360-градусное зрение",
                    "Две пары независимо движущихся крыльев",
                    "Личинки (наяды) живут в воде и дышат жабрами",
                    "Хищник, ловит добычу на лету",
                    "Может летать во всех направлениях, включая назад"
                ],
                interestingFacts: "Стрекозы — одни из самых древних насекомых, их предки жили 300 миллионов лет назад и имели размах крыльев до 75 см. Они ловят 95% предложенной добычи, что делает их самыми успешными хищниками в животном мире. Стрекозы могут летать со скоростью до 50 км/ч.",
                conservation: "Многие виды уязвимы из-за загрязнения и осушения водоемов. Стрекозы — индикаторы чистоты воды, их присутствие свидетельствует о здоровой водной экосистеме."
            },
            stag_beetle: {
                title: "Жук-олень",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Жук-олень — один из самых крупных жуков Европы. Самец имеет огромные «рога» - видоизмененные верхние челюсти, используемые в боях за самок. Личинки развиваются в мертвой древесине в течение 3-7 лет.",
                scientificName: "Lucanus cervus",
                family: "Рогачи (Lucanidae)",
                weight: "До 10 г",
                length: "До 9 см (с «рогами»)",
                lifespan: "Взрослый жук: 3-5 недель, личинка: 3-7 лет",
                habitat: "Старые лиственные леса Европы, особенно с дубами",
                features: [
                    "У самцов огромные «рога» - видоизмененные мандибулы",
                    "Личинки развиваются в гниющей древесине 3-7 лет",
                    "Взрослые жуки питаются древесным соком",
                    "Самцы дерутся за самок, поднимая противников и сбрасывая с деревьев",
                    "Летают преимущественно в сумерках"
                ],
                interestingFacts: "Жуки-олени — самые крупные жуки Европы. Их «рога» на самом деле являются гипертрофированными верхними челюстями. Бои самцов за самок больше похожи на ритуальные поединки и редко заканчиваются серьезными травмами. Личинки могут достигать длины 10 см.",
                conservation: "Уязвимый вид (VU) в Европе. Основные угрозы: вырубка старых лесов, удаление мертвой древесины, использование пестицидов. Охраняется законодательством ЕС."
            },
            mantis: {
                title: "Богомол",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Богомол — хищное насекомое с хватательными передними конечностями. Известен тем, что самка часто поедает самца после спаривания. Мастер маскировки, некоторые виды имитируют цветы или листья. Обладает стереоскопическим зрением.",
                scientificName: "Mantodea (отряд, около 2400 видов)",
                family: "Разные семейства богомолов",
                weight: "2-10 г",
                length: "4-15 см",
                lifespan: "6-12 месяцев",
                habitat: "Тропические и умеренные регионы по всему миру",
                features: [
                    "Хватательные передние конечности с шипами",
                    "Стереоскопическое зрение (трехмерное)",
                    "Самка часто поедает самца после спаривания",
                    "Отличная маскировка, некоторые виды имитируют растения",
                    "Может поворачивать голову на 180 градусов"
                ],
                interestingFacts: "Богомолы — единственные насекомые, которые могут поворачивать голову на 180 градусов. Они обладают стереоскопическим зрением, что редко среди насекомых. Самка поедает самца не всегда, а только если голодна — это обеспечивает питательными веществами для развития яиц.",
                conservation: "Большинство видов не находятся под угрозой. Некоторые тропические виды популярны в качестве домашних питомцев, что может создавать давление на дикие популяции."
            },

            // Амфибии (6)
            goliath_frog: {
                title: "Лягушка-голиаф",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Лягушка-голиаф — самая крупная лягушка в мире. Обитает в быстрых реках Западной Африки. Не издает звуков, так как не имеет голосового мешка. Питается насекомыми, ракообразными, рыбой и мелкими черепахами.",
                scientificName: "Conraua goliath",
                family: "Настоящие лягушки (Ranidae)",
                weight: "До 3.3 кг",
                length: "До 32 см (без учета вытянутых ног)",
                lifespan: "15 лет",
                habitat: "Быстрые реки с водопадами в Камеруне и Экваториальной Гвинее",
                features: [
                    "Самая крупная лягушка в мире",
                    "Не имеет голосового мешка, поэтому не издает звуков",
                    "Мощные задние ноги для плавания в быстрых реках",
                    "Строит собственные бассейны для размножения, перемещая камни",
                    "Прыгает на расстояние до 3 метров"
                ],
                interestingFacts: "Лягушка-голиаф строит собственные бассейны для размножения, перемещая камни весом до 2 кг. Она может прыгать на расстояние до 3 метров. Несмотря на размеры, голиафы очень пугливы и при малейшей опасности ныряют в воду.",
                conservation: "Вымирающий вид (EN). Популяция сократилась на 50% за последние 15 лет. Основные угрозы: охота ради мяса, разрушение среды обитания, загрязнение рек, сбор для торговли домашними животными."
            },
            salamander: {
                title: "Огненная саламандра",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Огненная саламандра — ярко окрашенная хвостатая амфибия с черно-желтым узором. Выделяет ядовитый секрет через кожные железы. Активна ночью, днем прячется во влажных укрытиях. Живородящая, рождает полностью сформированных личинок.",
                scientificName: "Salamandra salamandra",
                family: "Саламандровые (Salamandridae)",
                weight: "20-50 г",
                length: "15-25 см",
                lifespan: "20-30 лет",
                habitat: "Влажные леса Европы, особенно возле чистых ручьев",
                features: [
                    "Яркая предостерегающая окраска (апосематизм)",
                    "Выделяет ядовитый секрет саламандрин через кожные железы",
                    "Живородящая, рождает 20-40 личинок",
                    "Личинки развиваются в воде 3-5 месяцев",
                    "Ночной образ жизни, днем прячется под камнями и бревнами"
                ],
                interestingFacts: "В Средневековье считалось, что саламандры могут жить в огне, отсюда название «огненная». На самом деле они просто прятались в дровах, которые затем бросали в огонь. Яд саламандры может вызывать судороги и повышенное давление у мелких животных, но для человека не смертелен.",
                conservation: "Вызывающий наименьшие опасения (LC). Популяция стабильна, но локально сокращается из-за разрушения лесов, загрязнения воды и дорожной смертности."
            },
            axolotl: {
                title: "Аксолотль",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Аксолотль — личинка амбистомы, способная к размножению (неотения). Обитает только в озере Сочимилько в Мексике. Обладает удивительной способностью регенерации конечностей, органов и даже частей мозга без образования рубцов.",
                scientificName: "Ambystoma mexicanum",
                family: "Амбистомовые (Ambystomatidae)",
                weight: "60-300 г",
                length: "15-45 см",
                lifespan: "10-15 лет",
                habitat: "Каналы озера Сочимилько в Мехико, Мексика",
                features: [
                    "Неотения — способность размножаться на личиночной стадии",
                    "Феноменальная регенерация конечностей, органов, частей мозга",
                    "Наружные жабры в виде пушистых веточек",
                    "Может дышать жабрами, легкими и через кожу",
                    "Разнообразные цветовые морфы в неволе"
                ],
                interestingFacts: "Аксолотль может регенерировать практически любую часть тела, включая конечности, хвост, спинной мозг и даже части мозга. Они остаются в личиночной стадии всю жизнь, но могут превратиться во взрослую амбистому при определенных условиях. В дикой природе осталось менее 1000 особей.",
                conservation: "Находящийся на грани исчезновения (CR) в дикой природе. Основные угрозы: загрязнение и осушение каналов Сочимилько, интродукция хищных рыб. Широко разводится в лабораториях и как домашнее животное."
            },
            poison_frog: {
                title: "Ужасный листолаз (древолаз)",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Ужасный листолаз — одна из самых ядовитых лягушек в мире. Яркая окраска предупреждает хищников об опасности. Яд используется индейцами для стрел. Получает яд из пищи (муравьев и клещей), в неволе становится неядовитым.",
                scientificName: "Phyllobates terribilis",
                family: "Древолазы (Dendrobatidae)",
                weight: "2-6 г",
                length: "4-6 см",
                lifespan: "10-15 лет",
                habitat: "Тропические леса на тихоокеанском побережье Колумбии",
                features: [
                    "Один из самых ядовитых животных в мире",
                    "Яркая предостерегающая окраска (апосематизм)",
                    "Яд батрахотоксин на коже, смертельный для человека",
                    "Получает яд из пищи, в неволе теряет ядовитость",
                    "Сложное родительское поведение, самец переносит головастиков на спине"
                ],
                interestingFacts: "Яда одной лягушки достаточно, чтобы убить 10 взрослых людей. Индейцы эмбера используют яд для охотничьих стрел — одна отравленная стрела может сохранять эффективность до 2 лет. Интересно, что в неволе, на другой диете, древолазы теряют ядовитость.",
                conservation: "Находящийся под угрозой исчезновения (EN). Основные угрозы: разрушение тропических лесов, незаконный сбор для торговли домашними животными. Охраняется колумбийским законодательством."
            },
            cane_toad: {
                title: "Жаба-ага",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Жаба-ага — крупная ядовитая жаба. Была интродуцирована во многие регионы для борьбы с вредителями сельского хозяйства, но сама стала инвазивным видом, наносящим ущерб местным экосистемам. Имеет ядовитые железы за глазами.",
                scientificName: "Rhinella marina",
                family: "Жабы (Bufonidae)",
                weight: "До 2.6 кг",
                length: "До 25 см",
                lifespan: "10-15 лет",
                habitat: "Изначально Центральная и Южная Америка, интродуцирована в Австралию, Флориду, Филиппины и другие регионы",
                features: [
                    "Крупные ядовитые железы (паротиды) за глазами",
                    "Всеядность — ест практически все, что помещается в рот",
                    "Высокая плодовитость — до 30 000 яиц за кладку",
                    "Выносливость к разным условиям среды",
                    "Яд буфотоксин, опасный для многих животных"
                ],
                interestingFacts: "Жабы-ага были завезены в Австралию в 1935 году для борьбы с жуками, повреждающими сахарный тростник. Вместо этого они распространились по всему континенту, уничтожая местных животных, которые не имеют иммунитета к их яду. Сейчас их численность в Австралии оценивается в 200 миллионов особей.",
                conservation: "Вызывающий наименьшие опасения (LC) как вид, но рассматривается как инвазивный во многих регионах. В Австралии проводятся программы по контролю численности."
            },
            newt: {
                title: "Обыкновенный тритон",
                image: "https://images.unsplash.com/photo-1546182990-dffeafbe841d?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80",
                description: "Обыкновенный тритон — хвостатая амфибия, часть жизни проводит в воде, часть на суше. Весной у самцов появляется яркий гребень для привлечения самок. Зимует на суше в укрытиях. Личинки развиваются в воде.",
                scientificName: "Lissotriton vulgaris",
                family: "Саламандровые (Salamandridae)",
                weight: "3-12 г",
                length: "7-11 см",
                lifespan: "6-14 лет",
                habitat: "Леса, парки, сады с водоемами в Европе и Западной Азии",
                features: [
                    "У самцов весной появляется брачный гребень на спине",
                    "Двойной образ жизни: вода (весна-лето) и суша (осень-зима)",
                    "Яркое оранжевое брюхо с черными пятнами",
                    "Личинки с наружными жабрами развиваются в воде",
                    "Может регенерировать утраченные конечности и хвост"
                ],
                interestingFacts: "Тритоны обладают впечатляющей способностью к регенерации — они могут восстанавливать утраченные конечности, хвост, части глаз и даже сердца. Во время брачного периода самцы исполняют сложный танец перед самками, виляя хвостом и демонстрируя гребень. Тритоны зимуют на суше, зарывшись в землю или спрятавшись в трухлявых пнях.",
                conservation: "Вызывающий наименьшие опасения (LC). Популяция стабильна, но локально может сокращаться из-за осушения водоемов, загрязнения и фрагментации среды обитания."
            }
        };

        // Получаем элементы DOM
        const animalModal = document.getElementById("animalModal");
        const modalTitle = document.getElementById("modalTitle");
        const modalImage = document.getElementById("modalImage");
        const modalDescription = document.getElementById("modalDescription");
        const modalSpeciesCount = document.getElementById("modalSpeciesCount");
        const modalHabitat = document.getElementById("modalHabitat");
        const modalSize = document.getElementById("modalSize");
        const modalLifespan = document.getElementById("modalLifespan");
        const modalFeatures = document.getElementById("modalFeatures");
        const modalCharacteristics = document.getElementById("modalCharacteristics");
        const modalExamples = document.getElementById("modalExamples");
        const modalFact = document.getElementById("modalFact");
        const closeBtn = document.querySelector(".close");

        const repModal = document.getElementById("repModal");
        const repModalTitle = document.getElementById("repModalTitle");
        const repModalImage = document.getElementById("repModalImage");
        const repModalDescription = document.getElementById("repModalDescription");
        const repScientificName = document.getElementById("repScientificName");
        const repFamily = document.getElementById("repFamily");
        const repWeight = document.getElementById("repWeight");
        const repLength = document.getElementById("repLength");
        const repLifespan = document.getElementById("repLifespan");
        const repHabitat = document.getElementById("repHabitat");
        const repFeatures = document.getElementById("repFeatures");
        const repInterestingFacts = document.getElementById("repInterestingFacts");
        const repConservation = document.getElementById("repConservation");
        const repCloseBtn = document.querySelector(".rep-close");

        const moreInfoButtons = document.querySelectorAll(".more-info");
        const repDetailButtons = document.querySelectorAll(".rep-detail-btn");
        const tabButtons = document.querySelectorAll(".tab-button");
        const tabContents = document.querySelectorAll(".tab-content");

        // Функция для открытия модального окна категории
        function openAnimalModal(animalType) {
            const animal = animalData[animalType];

            // Заполняем общую информацию
            modalTitle.textContent = animal.title;
            modalImage.src = animal.image;
            modalDescription.textContent = animal.description;
            modalSpeciesCount.textContent = animal.speciesCount;
            modalHabitat.textContent = animal.habitat;
            modalSize.textContent = animal.size;
            modalLifespan.textContent = animal.lifespan;
            modalFact.textContent = animal.fact;

            // Заполняем вкладку "Обзор"
            modalFeatures.innerHTML = "";
            animal.features.forEach(feature => {
                const li = document.createElement("li");
                li.textContent = feature;
                modalFeatures.appendChild(li);
            });

            // Заполняем вкладку "Характеристики"
            modalCharacteristics.innerHTML = "";
            animal.characteristics.forEach(char => {
                const charDiv = document.createElement("div");
                charDiv.className = "characteristic";
                charDiv.innerHTML = `<h4>${char.title}</h4><p>${char.value}</p>`;
                modalCharacteristics.appendChild(charDiv);
            });

            // Заполняем вкладку "Представители"
            modalExamples.innerHTML = "";
            animal.examples.forEach(example => {
                const exampleItem = document.createElement("div");
                exampleItem.className = "example-item";
                exampleItem.textContent = example;

                // Добавляем обработчик для открытия информации о представителе
                exampleItem.addEventListener("click", function() {
                    // Ищем соответствующие данные о представителе
                    for (const key in representativesData) {
                        if (representativesData[key].title === example) {
                            openRepModal(key);
                            closeModal(animalModal);
                            break;
                        }
                    }
                });

                modalExamples.appendChild(exampleItem);
            });

            // Активируем первую вкладку
            switchTab('overview');

            // Показываем модальное окно
            animalModal.style.display = "block";
            document.body.style.overflow = "hidden";
        }

        // Функция для открытия модального окна представителя
        function openRepModal(repId) {
            const rep = representativesData[repId];

            // Заполняем информацию о представителе
            repModalTitle.textContent = rep.title;
            repModalImage.src = rep.image;
            repModalDescription.textContent = rep.description;
            repScientificName.textContent = rep.scientificName;
            repFamily.textContent = rep.family;
            repWeight.textContent = rep.weight;
            repLength.textContent = rep.length;
            repLifespan.textContent = rep.lifespan;
            repHabitat.textContent = rep.habitat;
            repInterestingFacts.textContent = rep.interestingFacts;
            repConservation.textContent = rep.conservation;

            // Заполняем особенности
            repFeatures.innerHTML = "";
            rep.features.forEach(feature => {
                const li = document.createElement("li");
                li.textContent = feature;
                repFeatures.appendChild(li);
            });

            // Показываем модальное окно
            repModal.style.display = "block";
            document.body.style.overflow = "hidden";
        }

        // Функция для переключения вкладок
        function switchTab(tabName) {
            // Деактивируем все кнопки вкладок
            tabButtons.forEach(button => {
                button.classList.remove("active");
            });

            // Скрываем все содержимое вкладок
            tabContents.forEach(content => {
                content.classList.remove("active");
            });

            // Активируем выбранную кнопку вкладки
            const activeButton = document.querySelector(`.tab-button[data-tab="${tabName}"]`);
            if (activeButton) {
                activeButton.classList.add("active");
            }

            // Показываем выбранное содержимое вкладки
            const activeContent = document.getElementById(`tab-${tabName}`);
            if (activeContent) {
                activeContent.classList.add("active");
            }
        }

        // Функция для закрытия модального окна
        function closeModal(modalElement) {
            modalElement.style.display = "none";
            document.body.style.overflow = "auto";
        }

        // Добавляем обработчики событий на кнопки "Подробнее" для категорий
        moreInfoButtons.forEach(button => {
            button.addEventListener("click", function() {
                const animalType = this.getAttribute("data-animal");
                openAnimalModal(animalType);
            });
        });

        // Добавляем обработчики событий на кнопки "Подробнее" для представителей
        repDetailButtons.forEach(button => {
            button.addEventListener("click", function() {
                const repId = this.getAttribute("data-rep");
                openRepModal(repId);
            });
        });

        // Добавляем обработчики событий на кнопки вкладок
        tabButtons.forEach(button => {
            button.addEventListener("click", function() {
                const tabName = this.getAttribute("data-tab");
                switchTab(tabName);
            });
        });

        // Закрытие модальных окон при клике на крестик
        closeBtn.addEventListener("click", () => closeModal(animalModal));
        repCloseBtn.addEventListener("click", () => closeModal(repModal));

        // Закрытие модальных окон при клике вне их области
        window.addEventListener("click", function(event) {
            if (event.target === animalModal) {
                closeModal(animalModal);
            }
            if (event.target === repModal) {
                closeModal(repModal);
            }
        });

        // Закрытие модальных окон при нажатии клавиши Escape
        document.addEventListener("keydown", function(event) {
            if (event.key === "Escape") {
                if (animalModal.style.display === "block") {
                    closeModal(animalModal);
                }
                if (repModal.style.display === "block") {
                    closeModal(repModal);
                }
            }
        });

        // Плавная прокрутка к якорным ссылкам
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();

                const targetId = this.getAttribute('href');
                if(targetId === '#') return;

                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Добавление эффекта при наведении на кнопки
        document.querySelectorAll('.btn').forEach(button => {
            button.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-3px)';
            });

            button.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0)';
            });
        });

        // Анимация при загрузке страницы
        window.addEventListener('DOMContentLoaded', () => {
            document.body.style.opacity = '0';
            document.body.style.transition = 'opacity 0.5s';

            setTimeout(() => {
                document.body.style.opacity = '1';
            }, 100);
        });
    </script>
</body>
</html>
