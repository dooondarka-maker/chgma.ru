<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Личный кабинет - ЧГМА</title>
    <style>
        :root {
            --primary-blue: #5b82c4;
            --light-blue: #e6eefc;
            --header-blue: #4a6fa5;
            --text-color: #333;
            --border-color: #ccc;
            --green-bg: #e5f6b2;
            --teal-footer: #458b74;
            --sidebar-bg: #f4f6f9;
            --sidebar-active: #ffffff;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, Helvetica, sans-serif;
        }

        body {
            background-color: #f0f2f5;
            color: var(--text-color);
            font-size: 14px;
            line-height: 1.4;
        }

        /* Верхнее меню */
        .top-nav {
            background-color: #f0f2f5;
            padding: 10px 20px;
            display: flex;
            gap: 15px;
            border-bottom: 1px solid #ddd;
            font-size: 13px;
        }
        .top-nav a {
            text-decoration: none;
            color: var(--primary-blue);
        }
        .top-nav a:hover {
            text-decoration: underline;
        }

        /* Основной контейнер */
        .container {
            display: flex;
            max-width: 1400px;
            margin: 0 auto;
            background: #fff;
            min-height: calc(100vh - 100px);
            box-shadow: 0 0 10px rgba(0,0,0,0.05);
        }

        /* Левая колонка */
        .left-sidebar {
            width: 250px;
            background-color: var(--sidebar-bg);
            border-right: 1px solid #ddd;
            flex-shrink: 0;
        }
        .left-sidebar-header {
            background-color: var(--teal-footer);
            color: white;
            padding: 15px;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .left-sidebar ul {
            list-style: none;
        }
        .left-sidebar li {
            border-bottom: 1px solid #e0e0e0;
        }
        .left-sidebar a {
            display: block;
            padding: 12px 15px;
            text-decoration: none;
            color: var(--primary-blue);
            transition: background 0.2s;
        }
        .left-sidebar a:hover {
            background-color: #e2e8f0;
        }

        /* Центральная часть */
        .main-content {
            flex-grow: 1;
            padding: 20px;
            background-color: #fff;
        }
        .breadcrumbs {
            font-size: 12px;
            color: #666;
            margin-bottom: 15px;
        }
        .breadcrumbs a {
            color: var(--primary-blue);
            text-decoration: none;
        }
        .name-banner {
            background-color: var(--green-bg);
            padding: 15px;
            font-weight: bold;
            border: 1px solid #d0e5a0;
            margin-bottom: 20px;
            font-size: 16px;
        }
        .accordion-list {
            display: flex;
            flex-direction: column;
            gap: 5px;
        }
        .accordion-item {
            background-color: var(--light-blue);
            padding: 12px 15px;
            border: 1px solid #c9d9f2;
            cursor: pointer;
            color: #333;
        }
        .accordion-item.active {
            background-color: var(--primary-blue);
            color: white;
            border-color: var(--primary-blue);
        }
        .accordion-item:hover:not(.active) {
            background-color: #dbe7fa;
        }

        /* Правая колонка */
        .right-sidebar {
            width: 350px;
            padding: 20px;
            border-left: 1px solid #eee;
            flex-shrink: 0;
        }
        .info-block {
            margin-bottom: 15px;
            border: 1px solid #ddd;
        }
        .info-header {
            background-color: var(--primary-blue);
            color: white;
            padding: 10px 15px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .info-content {
            padding: 15px;
            background-color: #fff;
            font-size: 13px;
        }
        .info-content p {
            margin-bottom: 8px;
        }
        .info-content .label {
            font-weight: bold;
            color: #444;
        }
        .green-section {
            background-color: var(--green-bg);
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #d0e5a0;
        }
        .balance-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
            font-size: 13px;
        }
        .balance-table th, .balance-table td {
            text-align: left;
            padding: 5px;
            border-bottom: 1px solid #eee;
        }
        .balance-table th {
            font-weight: normal;
            color: #666;
        }

        /* Подвал */
        .footer {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            background-color: var(--teal-footer);
            color: white;
            font-size: 12px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        .footer-support-box {
            background-color: rgba(255,255,255,0.1);
            padding: 15px;
            border-radius: 5px;
            width: fit-content;
        }
        .footer-links {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 10px;
        }
        .footer-links a {
            color: white;
            text-decoration: underline;
        }
        .copyright {
            text-align: center;
            margin-top: 10px;
            color: #ccc;
        }

        /* Иконки-заглушки */
        .icon-plus, .icon-minus {
            font-weight: bold;
            font-family: monospace;
            font-size: 16px;
        }
    </style>
</head>
<body>

    <!-- Верхнее меню -->
    <div class="top-nav">
        <a href="#">Обучение ▼</a>
        <a href="#" style="font-weight: bold; color: #333;">Личный кабинет</a>
        <a href="#">Профилактика ▼</a>
        <a href="#">Language (RU) ▼</a>
        <a href="#" style="margin-left: auto;">Выйти</a>
    </div>

    <!-- Основной макет -->
    <div class="container">
        
        <!-- Левая колонка -->
        <aside class="left-sidebar">
            <div class="left-sidebar-header">
                📌 Личный кабинет
            </div>
            <ul>
                <li><a href="#">Личная информация</a></li>
                <li><a href="#">Анкета ординатора</a></li>
                <li><a href="#">Заказать справку</a></li>
                <li><a href="#">Запись на дисциплины по выбору</a></li>
                <li><a href="#">Запись на производственную практику</a></li>
                <li><a href="#">Обмен сообщениями</a></li>
                <li><a href="#">Портфолио</a></li>
            </ul>
        </aside>

        <!-- Центральная часть -->
        <main class="main-content">
            <div class="breadcrumbs">
                🏠 <a href="#">Главная</a> » Дондоков Айдар Зорикович
            </div>

            <div class="name-banner">
                Дондоков Айдар Зорикович
            </div>

            <div class="accordion-list">
                <div class="accordion-item">Дневник куратора</div>
                <div class="accordion-item">Информация по анкете</div>
                <div class="accordion-item active">Обучение</div>
                <div class="accordion-item">Оплата</div>
                <div class="accordion-item">Тестирования</div>
                <div class="accordion-item">Регистрационные данные</div>
                <div class="accordion-item">Паспортные данные</div>
                <div class="accordion-item">Адреса</div>
                <div class="accordion-item">Семья</div>
                <div class="accordion-item">Работа</div>
                <div class="accordion-item">Образование</div>
                <div class="accordion-item">Индивидуальные достижения</div>
                <div class="accordion-item">Воинская обязанность</div>
                <div class="accordion-item">Медосмотр</div>
                <div class="accordion-item">Библиотека</div>
                <div class="accordion-item">Данные выпускника</div>
            </div>
        </main>

        <!-- Правая колонка -->
        <aside class="right-sidebar">
            
            <!-- Блок Специалитет -->
            <div class="info-block">
                <div class="info-header">
                    <span>➕ Специалитет, 2020</span>
                </div>
            </div>

            <!-- Блок Ординатура -->
            <div class="info-block">
                <div class="info-header">
                    <span>➖ Ординатура, 2026</span>
                </div>
                <div class="info-content">
                    <p><span class="label">№ дела:</span> 277,</p>
                    <p><span class="label">№ зачётной книжки:</span> 54/202601,</p>
                    <p><span class="label">Дата регистрации:</span> 20.07.2026 23:54:14,</p>
                    <p><span class="label">Uid студ билета:</span> 01a09ef9-3e07-7395-82c1-9637e8f7e57b</p>
                </div>
                
                <div class="info-header" style="background-color: #7a9dd4;">
                    <span>➕ Абитуриент</span>
                </div>
                
                <div class="info-content">
                    <p><span class="label">Приказ:</span> №111-о</p>
                    <p><span class="label">Период:</span> 01.09.2026 - 10.09.2026,</p>
                    <p><span class="label">Курс:</span> 1 курс 1 (01) семестр,</p>
                    <p><span class="label">Оплата:</span> 9 444.44,<br>10 дней</p>
                    
                    <p><span class="label">Учебный план:</span><br>Стоматология хирургическая (Стажеры, 2026), 31.08.74, 2026, 2026</p>
                    <p><span class="label">Специальность:</span> Стоматология хирургическая</p>
                    <p><span class="label">Статус:</span> Учится,</p>
                    <p><span class="label">Основа:</span> Внебюджет,</p>
                    <p><span class="label">Форма:</span> Очная</p>

                    <div class="green-section">
                        <p><span class="label">Приказ:</span> №112-о</p>
                        <p><span class="label">Период:</span> 11.09.2026,</p>
                        <p><span class="label">Курс:</span> 1 курс 1 (01) семестр,</p>
                        <p><span class="label">Оплата:</span> 160 555.56 ,<br>5 месяцев, 20 дней</p>
                    </div>

                    <p><span class="label">Учебный план:</span><br>Стоматология хирургическая (Стажеры, 2026), 31.08.74, 2026, 2026 (рейтинг)</p>
                    <p><span class="label">Специальность:</span> Стоматология хирургическая,</p>
                    <p><span class="label">Кафедра:</span> Стоматологии факультета дополнительного профессионального образования</p>
                    <p><span class="label">Статус:</span> Учится,</p>
                    <p><span class="label">Основа:</span> Внебюджет,</p>
                    <p><span class="label">Форма:</span> Очная</p>
                </div>
            </div>

            <!-- Блок Баланс -->
            <div class="info-block">
                <div class="info-header">
                    <span>Баланс</span>
                </div>
                <div class="info-content">
                    <p><span class="label">Должен оплатить</span><br>1 199 202.08</p>
                    <table class="balance-table">
                        <tr>
                            <th>Оплатил</th>
                            <th>Долг</th>
                        </tr>
                        <tr>
                            <td>1 369 303.00</td>
                            <td>-170 100.92</td>
                        </tr>
                    </table>
                </div>
            </div>

            <!-- Блок Приказы -->
            <div class="info-block">
                <div class="info-header">
                    <span>➕ Приказы</span>
                </div>
            </div>

        </aside>
    </div>

    <!-- Подвал -->
    <footer class="footer">
        <div class="footer-support-box">
            <strong>ИСМА 3.4.33</strong><br>
            Разработка и поддержка:<br>
            Информационно-аналитический отдел:<br>
            Тел.: 8 (3022) 32-00-85 (*132)
        </div>
        <div class="footer-support-box" style="margin-top: -5px;">
            <strong>Вы зашли как:</strong><br>
            Дондоков А.З.
        </div>
        
        <div class="footer-links">
            <a href="#">Главная</a>
            <a href="#">Реквизиты учреждения</a>
            <a href="#">Телефонный справочник</a>
        </div>
        
        <div class="copyright">
            Copyright © 2026, ФГБОУ ВО ЧГМА Минздрава России.
        </div>
    </footer>

</body>
</html>
