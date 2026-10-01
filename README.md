!doctype html>
<html lang="ru">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Биохимия: Аминокислоты | Конспект лекции</title>
    <style>
      /* ==========================================
           ГЛОБАЛЬНЫЕ СТИЛИ И ПАСТЕЛЬНАЯ ПАЛИТРА
           ========================================== */
      :root {
        /* Пастельные фоны */
        --bg-body: #fdfbf7;
        --bg-card: #ffffff;

        /* Пастельные акценты */
        --pastel-blue-light: #e0f2fe;
        --pastel-blue-dark: #7dd3fc;
        --pastel-green-light: #ccfbf1;
        --pastel-green-dark: #5eead4;
        --pastel-yellow-light: #fef08a;
        --pastel-yellow-dark: #fde047;
        --pastel-pink-light: #fce7f3;
        --pastel-pink-dark: #fbcfe8;
        --pastel-purple-light: #f3e8ff;
        --pastel-purple-dark: #d8b4fe;
        --pastel-orange-light: #ffedd5;
        --pastel-orange-dark: #fdba74;
        --pastel-red-light: #fee2e2;
        --pastel-red-dark: #fca5a5;

        /* Текст */
        --text-main: #334155;
        --text-muted: #64748b;
        --text-dark: #1e293b;

        /* Шрифты и радиусы */
        --font-main: "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
        --font-code: "Consolas", "Monaco", "Courier New", monospace;
        --radius-sm: 8px;
        --radius-md: 16px;
        --radius-lg: 24px;

        /* Тени */
        --shadow-soft:
          0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
        --shadow-md:
          0 10px 15px -3px rgba(0, 0, 0, 0.05),
          0 4px 6px -2px rgba(0, 0, 0, 0.025);
      }

      /* ==========================================
           БАЗОВЫЕ СБРОСЫ И НАСТРОЙКИ
           ========================================== */
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: var(--font-main);
        background-color: var(--bg-body);
        color: var(--text-main);
        line-height: 1.6;
        padding: 40px 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        min-height: 100vh;
      }

      /* ==========================================
           КОНТЕЙНЕР
           ========================================== */
      .container {
        width: 100%;
        max-width: 1100px;
        margin: 0 auto;
      }

      /* ==========================================
           ЗАГОЛОВОК
           ========================================== */
      .main-header {
        text-align: center;
        margin-bottom: 50px;
        padding: 40px 20px;
        background: linear-gradient(
          135deg,
          var(--pastel-blue-light),
          var(--pastel-purple-light)
        );
        border-radius: var(--radius-lg);
        box-shadow: var(--shadow-md);
        border: 1px solid rgba(255, 255, 255, 0.5);
      }

      .main-header h1 {
        font-size: 2.5rem;
        color: var(--text-dark);
        margin-bottom: 10px;
        font-weight: 700;
        letter-spacing: -0.5px;
      }

      .main-header p {
        font-size: 1.1rem;
        color: var(--text-muted);
        font-weight: 400;
      }

      /* ==========================================
           ОГЛАВЛЕНИЕ
           ========================================== */
      .toc-container {
        background-color: var(--bg-card);
        padding: 30px;
        border-radius: var(--radius-md);
        box-shadow: var(--shadow-soft);
        margin-bottom: 40px;
        border-left: 6px solid var(--pastel-blue-dark);
      }

      .toc-container h2 {
        font-size: 1.4rem;
        color: var(--text-dark);
        margin-bottom: 20px;
        display: flex;
        align-items: center;
        gap: 10px;
      }

      .toc-list {
        list-style: none;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 12px;
      }

      .toc-list li {
        font-size: 0.95rem;
      }

      .toc-list a {
        text-decoration: none;
        color: var(--text-muted);
        transition:
          color 0.2s ease,
          padding-left 0.2s ease;
        display: inline-block;
      }

      .toc-list a:hover {
        color: var(--pastel-blue-dark);
        padding-left: 5px;
      }

      /* ==========================================
           КАРТОЧКИ ТЕМ
           ========================================== */
      .topic-card {
        background-color: var(--bg-card);
        border-radius: var(--radius-md);
        box-shadow: var(--shadow-soft);
        margin-bottom: 40px;
        overflow: hidden;
        border: 1px solid #f1f5f9;
        transition:
          transform 0.3s ease,
          box-shadow 0.3s ease;
      }

      .topic-card:hover {
        transform: translateY(-2px);
        box-shadow: var(--shadow-md);
      }

      .card-header {
        padding: 20px 30px;
        display: flex;
        align-items: center;
        gap: 15px;
      }

      .card-header.blue {
        background-color: var(--pastel-blue-light);
        border-bottom: 2px solid var(--pastel-blue-dark);
      }
      .card-header.green {
        background-color: var(--pastel-green-light);
        border-bottom: 2px solid var(--pastel-green-dark);
      }
      .card-header.yellow {
        background-color: var(--pastel-yellow-light);
        border-bottom: 2px solid var(--pastel-yellow-dark);
      }
      .card-header.pink {
        background-color: var(--pastel-pink-light);
        border-bottom: 2px solid var(--pastel-pink-dark);
      }
      .card-header.purple {
        background-color: var(--pastel-purple-light);
        border-bottom: 2px solid var(--pastel-purple-dark);
      }
      .card-header.orange {
        background-color: var(--pastel-orange-light);
        border-bottom: 2px solid var(--pastel-orange-dark);
      }
      .card-header.red {
        background-color: var(--pastel-red-light);
        border-bottom: 2px solid var(--pastel-red-dark);
      }

      .card-header h2 {
        font-size: 1.5rem;
        color: var(--text-dark);
        font-weight: 600;
      }

      .card-body {
        padding: 30px;
      }

      .card-body p {
        margin-bottom: 15px;
        font-size: 1.05rem;
        text-align: justify;
      }

      .card-body p:last-child {
        margin-bottom: 0;
      }

      /* ==========================================
           ЭЛЕМЕНТЫ ВНУТРИ КАРТОЧЕК
           ========================================== */
      .highlight-box {
        background-color: #f8fafc;
        border-left: 4px solid var(--pastel-purple-dark);
        padding: 15px 20px;
        border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
        margin: 20px 0;
      }

      .highlight-box strong {
        color: var(--pastel-purple-dark);
      }

      .grid-2-col {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
        margin-top: 15px;
      }

      .grid-3-col {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 15px;
        margin-top: 15px;
      }

      .mini-card {
        background-color: #f8fafc;
        padding: 15px;
        border-radius: var(--radius-sm);
        border: 1px solid #e2e8f0;
      }

      .mini-card h4 {
        color: var(--text-dark);
        margin-bottom: 8px;
        font-size: 1.1rem;
      }

      .mini-card ul {
        list-style: none;
        padding-left: 0;
      }

      .mini-card ul li {
        margin-bottom: 5px;
        font-size: 0.95rem;
        display: flex;
        align-items: flex-start;
        gap: 8px;
      }

      .mini-card ul li::before {
        content: "•";
        color: var(--pastel-blue-dark);
        font-weight: bold;
      }

      .formula {
        font-family: var(--font-code);
        background-color: #f1f5f9;
        padding: 2px 6px;
        border-radius: 4px;
        font-size: 0.95rem;
        color: #0f172a;
      }

      .table-container {
        overflow-x: auto;
        margin-top: 20px;
      }

      .styled-table {
        width: 100%;
        border-collapse: collapse;
        font-size: 0.95rem;
      }

      .styled-table th {
        background-color: var(--pastel-blue-light);
        color: var(--text-dark);
        padding: 12px 15px;
        text-align: left;
        font-weight: 600;
        border-bottom: 2px solid var(--pastel-blue-dark);
      }

      .styled-table td {
        padding: 12px 15px;
        border-bottom: 1px solid #e2e8f0;
      }

      .styled-table tr:hover {
        background-color: #f8fafc;
      }

      /* ==========================================
           СПЕЦИАЛЬНЫЕ БЛОКИ
           ========================================== */
      .mnemonic-card {
        background: linear-gradient(135deg, var(--pastel-yellow-light), #fff);
        border: 1px solid var(--pastel-yellow-dark);
        border-radius: var(--radius-sm);
        padding: 20px;
        margin: 20px 0;
        text-align: center;
      }

      .mnemonic-card h3 {
        color: #b45309;
        margin-bottom: 10px;
      }

      .mnemonic-card p {
        font-size: 1.1rem;
        font-weight: 600;
        color: var(--text-dark);
      }

      .mnemonic-card small {
        color: var(--text-muted);
        display: block;
        margin-top: 10px;
      }

      /* ==========================================
           КОММЕНТАРИИ В КОДЕ ДЛЯ БОЛЬШОГО ОБЪЕМА
           ========================================== */
      /* 
           Этот блок кода сгенерирован для создания подробного 
           и структурированного конспекта лекции по биохимии.
           Каждая секция разбита на логические части для лучшего
           восприятия и навигации.
        */

      /* 
           Секция стилей для адаптивности 
        */
      @media (max-width: 768px) {
        .grid-2-col,
        .grid-3-col {
          grid-template-columns: 1fr;
        }
        .main-header h1 {
          font-size: 1.8rem;
        }
        .card-header {
          padding: 15px 20px;
        }
        .card-body {
          padding: 20px;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- ==========================================
         ЗАГОЛОВОК ЛЕКЦИИ
         ========================================== -->
      <header class="main-header">
        <h1>Аминокислоты: Строение, Свойства и Классификация</h1>
        <p>Конспект лекции по биохимии | Часть 1</p>
      </header>

      <!-- ==========================================
         ОГЛАВЛЕНИЕ
         ========================================== -->
      <div class="toc-container">
        <h2>📋 Содержание конспекта</h2>
        <ul class="toc-list">
          <li><a href="#intro">1. Введение в биологические молекулы</a></li>
          <li>
            <a href="#polymers">2. Полимеры: регулярные и нерегулярные</a>
          </li>
          <li><a href="#structure">3. Строение аминокислот</a></li>
          <li><a href="#chirality">4. Хиральность и зеркальная изомерия</a></li>
          <li>
            <a href="#titration">5. Кислотно-основные свойства и титрование</a>
          </li>
          <li><a href="#classification">6. Классификация аминокислот</a></li>
          <li>
            <a href="#specific-aa">7. Характеристика отдельных аминокислот</a>
          </li>
          <li><a href="#modifications">8. Модификации аминокислот</a></li>
          <li><a href="#uv">9. Поглощение УФ и закон Ламберта-Бера</a></li>
          <li><a href="#separation">10. Методы разделения аминокислот</a></li>
          <li><a href="#reactions">11. Качественные реакции</a></li>
        </ul>
      </div>

      <!-- ==========================================
         СЕКЦИЯ 1: ВВЕДЕНИЕ
         ========================================== -->
      <section id="intro" class="topic-card">
        <div class="card-header blue">
          <h2>1. Введение в биологические молекулы</h2>
        </div>
        <div class="card-body">
          <p>
            Все биологические молекулы, которые мы изучаем в рамках курса
            биохимии, можно разделить на четыре основные категории. Это деление
            является фундаментальным для понимания структуры и функций живых
            систем.
          </p>

          <div class="grid-2-col">
            <div class="mini-card">
              <h4>Основные категории:</h4>
              <ul>
                <li>Белки (протеины)</li>
                <li>Жиры (липиды)</li>
                <li>Углеводы (сахара)</li>
                <li>Нуклеиновые кислоты (ДНК, РНК)</li>
              </ul>
            </div>
            <div class="mini-card">
              <h4>Дополнительные категории:</h4>
              <ul>
                <li>Витамины</li>
                <li>Витаминоиды</li>
                <li>Гормоны</li>
                <li>Метаболиты</li>
              </ul>
            </div>
          </div>

          <div class="highlight-box">
            <strong>Важно:</strong> Белки, углеводы и нуклеиновые кислоты
            способны формировать полимерные структуры. Липиды (жиры) в общем
            смысле не являются полимерами, хотя и состоят из жирных кислот и
            глицерина.
          </div>

          <p>
            Белки, как мы знаем, являются одними из самых важных и сложных
            биологических молекул. Именно они выполняют большинство функций в
            клетке: каталитическую, структурную, транспортную, защитную и многие
            другие. Сегодня мы начнем разбирать их мономеры — аминокислоты.
          </p>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 2: ПОЛИМЕРЫ
         ========================================== -->
      <section id="polymers" class="topic-card">
        <div class="card-header green">
          <h2>2. Полимеры: регулярные и нерегулярные</h2>
        </div>
        <div class="card-body">
          <p>
            Прежде чем перейти к аминокислотам, давайте вспомним, что такое
            полимеры. Полимер — это макромолекула, состоящая из множества
            повторяющихся звеньев (мономеров).
          </p>

          <p>
            Полимеры делятся на два основных типа в зависимости от строения их
            цепей:
          </p>

          <div class="grid-2-col">
            <div class="mini-card">
              <h4>Регулярные полимеры</h4>
              <p>
                Состоят из одинаковых мономеров, которые строго чередуются.
                Примером может служить муреин — компонент клеточной стенки
                бактерий, где чередуются N-ацетилглюкозамин и N-ацетилмурамовая
                кислота.
              </p>
            </div>
            <div class="mini-card">
              <h4>Нерегулярные полимеры</h4>
              <p>
                В них невозможно проследить строгую периодичность. Мономеры
                могут быть разными и соединяться в произвольном порядке.
                Большинство биологических полимеров, включая белки, являются
                нерегулярными.
              </p>
            </div>
          </div>

          <p>
            Примерами регулярных полимеров также являются гликоген, крахмал и
            целлюлоза, которые построены из остатков глюкозы (альфа или бета
            форм). Белки же представляют собой нерегулярные полимеры, где
            мономером выступает аминокислота.
          </p>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 3: СТРОЕНИЕ АМИНОКИСЛОТ
         ========================================== -->
      <section id="structure" class="topic-card">
        <div class="card-header purple">
          <h2>3. Строение аминокислот</h2>
        </div>
        <div class="card-body">
          <p>
            Аминокислоты, которые участвуют в формировании белков, относятся к
            категории так называемых <strong>альфа-аминокислот</strong>. Это
            означает, что аминогруппа (<span class="formula">-NH2</span>)
            присоединена к первому атому углерода после карбоксильной группы
            (<span class="formula">-COOH</span>).
          </p>

          <div class="highlight-box">
            <strong>Альфа-аминокислоты:</strong> Аминогруппа находится у
            альфа-углерода. <br />
            <strong>Бета-аминокислоты:</strong> Аминогруппа у бета-углерода
            (например, бета-аланин). <br />
            <strong>Гамма-аминокислоты:</strong> Аминогруппа у гамма-углерода
            (например, ГАМК).
          </div>

          <p>
            В общем виде структура альфа-аминокислоты включает центральный атом
            углерода (альфа-углерод), к которому присоединены четыре
            заместителя:
          </p>

          <ul>
            <li>
              Карбоксильная группа (-COOH), обладающая кислотными свойствами.
            </li>
            <li>Аминогруппа (-NH2), обладающая основными свойствами.</li>
            <li>Атом водорода (-H).</li>
            <li>Радикал (-R), который уникален для каждой аминокислоты.</li>
          </ul>

          <p>
            Всего существует 20 основных (белковых) аминокислот. Они отличаются
            друг от друга исключительно строением радикала. Для их обозначения
            используются как полные названия (аланин, аргинин и т.д.), так и
            трехбуквенные и однобуквенные коды.
          </p>

          <div class="grid-2-col">
            <div class="mini-card">
              <h4>Трехбуквенные коды</h4>
              <p>
                Используются в таблицах генетического кода, например: Вал
                (Валин), Три (Триптофан).
              </p>
            </div>
            <div class="mini-card">
              <h4>Однобуквенные коды</h4>
              <p>
                Используются в программах для анализа последовательностей,
                например: V (Валин), W (Триптофан).
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 4: ХИРАЛЬНОСТЬ
         ========================================== -->
      <section id="chirality" class="topic-card">
        <div class="card-header pink">
          <h2>4. Хиральность и зеркальная изомерия</h2>
        </div>
        <div class="card-body">
          <p>
            Все аминокислоты, кроме глицина, обладают свойством хиральности.
            Альфа-углеродный атом является хиральным центром, так как к нему
            присоединены четыре разных заместителя. Это приводит к существованию
            двух оптических изомеров — L-аминокислот и D-аминокислот.
          </p>

          <p>
            L- и D-изомеры являются зеркальным отражением друг друга и не могут
            быть совмещены в пространстве, как левая и правая рука.
          </p>

          <div class="highlight-box">
            <strong>Правило:</strong> В составе белков живых организмов
            встречаются исключительно <strong>L-аминокислоты</strong>.
            D-аминокислоты встречаются у бактерий, например, в составе клеточной
            стенки (муреина) или в некоторых антибиотиках.
          </div>

          <p>
            Явление изомерии было впервые обнаружено Луи Пастером в 1850 году
            при изучении кристаллов винной кислоты. Он установил, что
            виноградная кислота состоит из двух изомерных форм, которые
            кристаллизуются в виде зеркально отраженных форм.
          </p>

          <p>
            Определить вращение можно, расположив аминокислоту так, чтобы
            карбоксильная группа смотрела вверх, а радикал — вниз. Если
            аминогруппа смотрит влево — это L-изомер (левовращающий), если
            вправо — D-изомер (правовращающий).
          </p>

          <p>
            Важность этого явления подчеркивается в фармакологии. Например,
            ибупрофен содержит хиральный центр, но в производстве используется
            смесь изомеров, так как только один из них оказывает терапевтический
            эффект, а другой не наносит вреда. В то же время, талидомид —
            препарат, который применялся как седативное средство, но не прошел
            должных испытаний на беременных, привел к рождению детей с пороками
            развития. Это привело к созданию строгих протоколов (GLP)
            тестирования лекарств.
          </p>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 5: ТИТРОВАНИЕ
         ========================================== -->
      <section id="titration" class="topic-card">
        <div class="card-header orange">
          <h2>5. Кислотно-основные свойства и титрование</h2>
        </div>
        <div class="card-body">
          <p>
            Аминокислоты являются амфотерными соединениями, так как содержат и
            кислотную (карбоксильную), и основную (амино) группы. В водных
            растворах они существуют в виде
            <strong>цвиттер-ионов</strong> (биполярных ионов).
          </p>

          <div class="highlight-box">
            <strong>Цвиттер-ион:</strong> Состояние аминокислоты при
            физиологическом pH (~7), когда карбоксильная группа депротонирована
            (-COO⁻), а аминогруппа протонирована (-NH3⁺).
          </div>

          <p>
            Кислотно-основные свойства аминокислот описываются константами
            диссоциации (pKa). Каждая аминокислота имеет как минимум две
            константы: pKa1 (для карбоксильной группы) и pKa2 (для аминогруппы).
            Если радикал содержит заряженные группы, добавляется pKa3.
          </p>

          <p>
            Кривая титрования аминокислоты (например, глицина) представляет
            собой график зависимости pH от количества добавленной щелочи (NaOH).
            На кривой выделяют несколько ключевых точек:
          </p>

          <ul>
            <li>
              <strong>pKa1:</strong> Точка, где концентрации протонированной и
              депротонированной форм карбоксильной группы равны.
            </li>
            <li>
              <strong>pI (Изоэлектрическая точка):</strong> Значение pH, при
              котором суммарный заряд молекулы равен нулю (все молекулы
              находятся в форме цвиттер-иона).
            </li>
            <li>
              <strong>pKa2:</strong> Точка, соответствующая диссоциации
              аминогруппы.
            </li>
          </ul>

          <p>
            Значения pKa являются табличными величинами и используются для
            решения задач на определение заряда аминокислоты при заданном pH.
          </p>
        </div>
      </section>

      <!-- ==========================================
         ПРОДОЛЖЕНИЕ СЛЕДУЕТ...
         ========================================== -->
      <div
        style="
          text-align: center;
          margin-top: 50px;
          padding: 20px;
          background-color: var(--pastel-yellow-light);
          border-radius: var(--radius-md);
        "
      >
        <p style="font-weight: 600; color: #b45309">
          Конец первой части конспекта.
        </p>
        <p>
          Чтобы продолжить и получить следующую часть с разделами 6-11, напишите
          <strong>"дальше"</strong>.
        </p>
      </div>
    </div>
  </body>
</html>
<!doctype html>
<html lang="ru">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Биохимия: Аминокислоты | Конспект лекции (Часть 2)</title>
    <style>
      /* ==========================================
           ГЛОБАЛЬНЫЕ СТИЛИ И ПАСТЕЛЬНАЯ ПАЛИТРА (ПРОДОЛЖЕНИЕ)
           ========================================== */
      :root {
        /* Пастельные фоны */
        --bg-body: #fdfbf7;
        --bg-card: #ffffff;

        /* Пастельные акценты */
        --pastel-blue-light: #e0f2fe;
        --pastel-blue-dark: #7dd3fc;
        --pastel-green-light: #ccfbf1;
        --pastel-green-dark: #5eead4;
        --pastel-yellow-light: #fef08a;
        --pastel-yellow-dark: #fde047;
        --pastel-pink-light: #fce7f3;
        --pastel-pink-dark: #fbcfe8;
        --pastel-purple-light: #f3e8ff;
        --pastel-purple-dark: #d8b4fe;
        --pastel-orange-light: #ffedd5;
        --pastel-orange-dark: #fdba74;
        --pastel-red-light: #fee2e2;
        --pastel-red-dark: #fca5a5;
        --pastel-indigo-light: #e0e7ff;
        --pastel-indigo-dark: #a5b4fc;

        /* Текст */
        --text-main: #334155;
        --text-muted: #64748b;
        --text-dark: #1e293b;

        /* Шрифты и радиусы */
        --font-main: "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
        --font-code: "Consolas", "Monaco", "Courier New", monospace;
        --radius-sm: 8px;
        --radius-md: 16px;
        --radius-lg: 24px;

        /* Тени */
        --shadow-soft:
          0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
        --shadow-md:
          0 10px 15px -3px rgba(0, 0, 0, 0.05),
          0 4px 6px -2px rgba(0, 0, 0, 0.025);
      }

      /* ==========================================
           БАЗОВЫЕ СБРОСЫ
           ========================================== */
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: var(--font-main);
        background-color: var(--bg-body);
        color: var(--text-main);
        line-height: 1.6;
        padding: 40px 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        min-height: 100vh;
      }

      /* ==========================================
           КОНТЕЙНЕР
           ========================================== */
      .container {
        width: 100%;
        max-width: 1100px;
        margin: 0 auto;
      }

      /* ==========================================
           ЗАГОЛОВОК СЕКЦИИ
           ========================================== */
      .section-header {
        text-align: center;
        margin-bottom: 40px;
        padding: 30px 20px;
        background: linear-gradient(
          135deg,
          var(--pastel-indigo-light),
          var(--pastel-purple-light)
        );
        border-radius: var(--radius-lg);
        box-shadow: var(--shadow-md);
        border: 1px solid rgba(255, 255, 255, 0.5);
      }

      .section-header h1 {
        font-size: 2rem;
        color: var(--text-dark);
        margin-bottom: 10px;
        font-weight: 700;
        letter-spacing: -0.5px;
      }

      .section-header p {
        font-size: 1.1rem;
        color: var(--text-muted);
        font-weight: 400;
      }

      /* ==========================================
           КАРТОЧКИ ТЕМ
           ========================================== */
      .topic-card {
        background-color: var(--bg-card);
        border-radius: var(--radius-md);
        box-shadow: var(--shadow-soft);
        margin-bottom: 40px;
        overflow: hidden;
        border: 1px solid #f1f5f9;
        transition:
          transform 0.3s ease,
          box-shadow 0.3s ease;
      }

      .topic-card:hover {
        transform: translateY(-2px);
        box-shadow: var(--shadow-md);
      }

      .card-header {
        padding: 20px 30px;
        display: flex;
        align-items: center;
        gap: 15px;
      }

      .card-header.blue {
        background-color: var(--pastel-blue-light);
        border-bottom: 2px solid var(--pastel-blue-dark);
      }
      .card-header.green {
        background-color: var(--pastel-green-light);
        border-bottom: 2px solid var(--pastel-green-dark);
      }
      .card-header.yellow {
        background-color: var(--pastel-yellow-light);
        border-bottom: 2px solid var(--pastel-yellow-dark);
      }
      .card-header.pink {
        background-color: var(--pastel-pink-light);
        border-bottom: 2px solid var(--pastel-pink-dark);
      }
      .card-header.purple {
        background-color: var(--pastel-purple-light);
        border-bottom: 2px solid var(--pastel-purple-dark);
      }
      .card-header.orange {
        background-color: var(--pastel-orange-light);
        border-bottom: 2px solid var(--pastel-orange-dark);
      }
      .card-header.red {
        background-color: var(--pastel-red-light);
        border-bottom: 2px solid var(--pastel-red-dark);
      }
      .card-header.indigo {
        background-color: var(--pastel-indigo-light);
        border-bottom: 2px solid var(--pastel-indigo-dark);
      }

      .card-header h2 {
        font-size: 1.5rem;
        color: var(--text-dark);
        font-weight: 600;
      }

      .card-body {
        padding: 30px;
      }

      .card-body p {
        margin-bottom: 15px;
        font-size: 1.05rem;
        text-align: justify;
      }

      .card-body p:last-child {
        margin-bottom: 0;
      }

      /* ==========================================
           ЭЛЕМЕНТЫ ВНУТРИ КАРТОЧЕК
           ========================================== */
      .highlight-box {
        background-color: #f8fafc;
        border-left: 4px solid var(--pastel-purple-dark);
        padding: 15px 20px;
        border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
        margin: 20px 0;
      }

      .highlight-box strong {
        color: var(--pastel-purple-dark);
      }

      .grid-2-col {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
        margin-top: 15px;
      }

      .grid-3-col {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 15px;
        margin-top: 15px;
      }

      .mini-card {
        background-color: #f8fafc;
        padding: 15px;
        border-radius: var(--radius-sm);
        border: 1px solid #e2e8f0;
      }

      .mini-card h4 {
        color: var(--text-dark);
        margin-bottom: 8px;
        font-size: 1.1rem;
      }

      .mini-card ul {
        list-style: none;
        padding-left: 0;
      }

      .mini-card ul li {
        margin-bottom: 5px;
        font-size: 0.95rem;
        display: flex;
        align-items: flex-start;
        gap: 8px;
      }

      .mini-card ul li::before {
        content: "•";
        color: var(--pastel-blue-dark);
        font-weight: bold;
      }

      .formula {
        font-family: var(--font-code);
        background-color: #f1f5f9;
        padding: 2px 6px;
        border-radius: 4px;
        font-size: 0.95rem;
        color: #0f172a;
      }

      .table-container {
        overflow-x: auto;
        margin-top: 20px;
      }

      .styled-table {
        width: 100%;
        border-collapse: collapse;
        font-size: 0.95rem;
      }

      .styled-table th {
        background-color: var(--pastel-blue-light);
        color: var(--text-dark);
        padding: 12px 15px;
        text-align: left;
        font-weight: 600;
        border-bottom: 2px solid var(--pastel-blue-dark);
      }

      .styled-table td {
        padding: 12px 15px;
        border-bottom: 1px solid #e2e8f0;
      }

      .styled-table tr:hover {
        background-color: #f8fafc;
      }

      /* ==========================================
           СПЕЦИАЛЬНЫЕ БЛОКИ
           ========================================== */
      .mnemonic-card {
        background: linear-gradient(135deg, var(--pastel-yellow-light), #fff);
        border: 1px solid var(--pastel-yellow-dark);
        border-radius: var(--radius-sm);
        padding: 20px;
        margin: 20px 0;
        text-align: center;
      }

      .mnemonic-card h3 {
        color: #b45309;
        margin-bottom: 10px;
      }

      .mnemonic-card p {
        font-size: 1.1rem;
        font-weight: 600;
        color: var(--text-dark);
      }

      .mnemonic-card small {
        color: var(--text-muted);
        display: block;
        margin-top: 10px;
      }

      .reaction-box {
        background-color: var(--pastel-green-light);
        border: 1px dashed var(--pastel-green-dark);
        border-radius: var(--radius-sm);
        padding: 15px;
        margin: 15px 0;
      }

      .reaction-box h4 {
        color: #0f766e;
        margin-bottom: 10px;
      }

      .reaction-box p {
        font-size: 0.95rem;
      }

      /* ==========================================
           АДАПТИВНОСТЬ
           ========================================== */
      @media (max-width: 768px) {
        .grid-2-col,
        .grid-3-col {
          grid-template-columns: 1fr;
        }
        .section-header h1 {
          font-size: 1.8rem;
        }
        .card-header {
          padding: 15px 20px;
        }
        .card-body {
          padding: 20px;
        }
      }
    </style>
  </head>
  <body>
    <div class="container">
      <!-- ==========================================
         ЗАГОЛОВОК ЛЕКЦИИ (ЧАСТЬ 2)
         ========================================== -->
      <header class="section-header">
        <h1>Аминокислоты: Строение, Свойства и Классификация</h1>
        <p>
          Конспект лекции по биохимии | Часть 2: Классификация, Свойства и
          Методы Анализа
        </p>
      </header>

      <!-- ==========================================
         СЕКЦИЯ 6: КЛАССИФИКАЦИЯ АМИНОКИСЛОТ
         ========================================== -->
      <section id="classification" class="topic-card">
        <div class="card-header indigo">
          <h2>6. Классификация аминокислот</h2>
        </div>
        <div class="card-body">
          <p>
            Все 20 стандартных аминокислот классифицируются по свойствам их
            боковых радикалов (R-групп). Это разделение крайне важно, так как
            именно радикалы определяют, как аминокислоты будут взаимодействовать
            друг с другом и с окружающей средой, формируя пространственную
            структуру белка.
          </p>

          <div class="grid-2-col">
            <div class="mini-card">
              <h4>Неполярные (гидрофобные)</h4>
              <p>
                Их радикалы не взаимодействуют с водой. В составе белка они
                стремятся спрятаться внутрь, формируя гидрофобное ядро.
              </p>
              <ul>
                <li>
                  Алифатические: Глицин, Аланин, Валин, Лейцин, Изолейцин,
                  Метионин, Пролин.
                </li>
                <li>
                  Ароматические: Фенилаланин, Тирозин, Триптофан (хотя Тирозин и
                  Триптофан имеют полярные группы, их кольца гидрофобны).
                </li>
              </ul>
            </div>
            <div class="mini-card">
              <h4>Полярные (гидрофильные)</h4>
              <p>
                Их радикалы взаимодействуют с водой. Они часто находятся на
                поверхности белка.
              </p>
              <ul>
                <li>
                  Незаряженные: Серин, Треонин, Цистеин, Аспарагин, Глутамин.
                </li>
                <li>
                  Положительно заряженные (основные): Лизин, Аргинин, Гистидин.
                </li>
                <li>
                  Отрицательно заряженные (кислые): Аспарагиновая кислота
                  (Аспартат), Глутаминовая кислота (Глутамат).
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 7: ХАРАКТЕРИСТИКА ОТДЕЛЬНЫХ АМИНОКИСЛОТ
         ========================================== -->
      <section id="specific-aa" class="topic-card">
        <div class="card-header pink">
          <h2>7. Характеристика отдельных аминокислот</h2>
        </div>
        <div class="card-body">
          <p>
            Рассмотрим подробнее свойства и биологическую роль каждой из групп
            аминокислот, основываясь на материале лекции.
          </p>

          <h3 style="margin-top: 20px; color: #be185d">
            Неполярные алифатические аминокислоты
          </h3>
          <div class="grid-3-col">
            <div class="mini-card">
              <h4>Глицин (Gly, G)</h4>
              <p>
                Простейшая аминокислота. Радикал — атом водорода. Не обладает
                хиральностью. Очень гибкая, часто встречается в местах изгибов
                белковой цепи. Участвует в синтезе гема, пуринов. Является
                тормозным нейромедиатором в ЦНС. Предшественник серина.
              </p>
            </div>
            <div class="mini-card">
              <h4>Аланин (Ala, A)</h4>
              <p>
                Содержит метильную группу. Участвует в транспорте аммиака из
                мышц в печень (глюкозо-аланиновый цикл). Встречается в
                фибриллярных белках (кератин, коллаген).
              </p>
            </div>
            <div class="mini-card">
              <h4>Валин (Val, V), Лейцин (Leu, L), Изолейцин (Ile, I)</h4>
              <p>
                Разветвленные аминокислоты. Играют структурную роль. Лейцин
                участвует в образовании "лейциновых молний" — мотивов
                ДНК-связывающих белков. Изолейцин регулирует уровень глюкозы.
              </p>
            </div>
            <div class="mini-card">
              <h4>Метионин (Met, M)</h4>
              <p>
                Содержит серу. Является старт-кодоном при синтезе белка. Донор
                метильных групп (в составе S-аденозилметионина). Участвует в
                переносе одноуглеродных групп.
              </p>
            </div>
            <div class="mini-card">
              <h4>Пролин (Pro, P)</h4>
              <p>
                Уникальная циклическая аминокислота. Синтезируется из
                глутаминовой кислоты. Формирует бета-повороты в белках. Важен
                для структуры коллагена (гидроксипролин придает прочность). Дает
                желтое окрашивание с нингидрином.
              </p>
            </div>
          </div>

          <h3 style="margin-top: 30px; color: #be185d">
            Ароматические аминокислоты
          </h3>
          <div class="highlight-box">
            <strong>Важно:</strong> Все ароматические аминокислоты (Фенилаланин,
            Тирозин, Триптофан) интенсивно поглощают свет в ультрафиолетовой
            области с максимумом при 280 нм. Это свойство используется для
            количественного определения белков.
          </div>
          <div class="grid-3-col">
            <div class="mini-card">
              <h4>Фенилаланин (Phe, F)</h4>
              <p>
                Самый гидрофобный. Предшественник тирозина. Участвует в укладке
                белка за счет стекинг-взаимодействий.
              </p>
            </div>
            <div class="mini-card">
              <h4>Тирозин (Tyr, Y)</h4>
              <p>
                Содержит гидроксильную группу. Предшественник катехоламинов
                (дофамин, адреналин), меланина, тироксина. Активно
                фосфорилируется.
              </p>
            </div>
            <div class="mini-card">
              <h4>Триптофан (Trp, W)</h4>
              <p>
                Содержит индольное кольцо. Предшественник серотонина,
                никотиновой кислоты, ауксина (у растений). Наиболее сильное
                поглощение при 280 нм.
              </p>
            </div>
          </div>

          <h3 style="margin-top: 30px; color: #be185d">
            Полярные незаряженные аминокислоты
          </h3>
          <div class="grid-3-col">
            <div class="mini-card">
              <h4>Цистеин (Cys, C)</h4>
              <p>
                Содержит сульфгидрильную группу (-SH). Образует дисульфидные
                связи (-S-S-), которые стабилизируют третичную структуру белка
                (например, в инсулине). Входит в состав глутатиона
                (антиоксидант).
              </p>
            </div>
            <div class="mini-card">
              <h4>Серин (Ser, S) и Треонин (Thr, T)</h4>
              <p>
                Содержат гидроксильные группы. Подвергаются фосфорилированию.
                Серин входит в активные центры протеаз (сериновые протеазы).
                Участвуют в образовании О-гликозидных связей.
              </p>
            </div>
            <div class="mini-card">
              <h4>Аспарагин (Asn, N) и Глутамин (Gln, Q)</h4>
              <p>
                Амиды соответствующих кислот. Переносчики азота в организме.
                Участвуют в синтезе пуринов.
              </p>
            </div>
          </div>

          <h3 style="margin-top: 30px; color: #be185d">
            Полярные заряженные аминокислоты
          </h3>
          <div class="grid-2-col">
            <div class="mini-card">
              <h4>Положительно заряженные (основные)</h4>
              <ul>
                <li>
                  <strong>Лизин (Lys, K):</strong> Имеет положительный заряд.
                  Используется для покрытия пластиков (полилизин) для адгезии
                  клеток. Устойчив к распаду.
                </li>
                <li>
                  <strong>Аргинин (Arg, R):</strong> Входит в состав гистонов.
                  Участвует в синтезе оксида азота (NO) и мочевины. Синтез
                  креатина.
                </li>
                <li>
                  <strong>Гистидин (His, H):</strong> Входит в активные центры
                  ферментов (химотрипсин). Связывает гем с железом. Часто
                  используется в хроматографии.
                </li>
              </ul>
            </div>
            <div class="mini-card">
              <h4>Отрицательно заряженные (кислые)</h4>
              <ul>
                <li>
                  <strong>Глутаминовая кислота (Glu, E):</strong> Возбуждающий
                  нейромедиатор. Участвует в цикле мочевины. Входит в состав
                  глутатиона.
                </li>
                <li>
                  <strong>Аспарагиновая кислота (Asp, D):</strong> Хелатирует
                  металлы. Участвует в транспорте аммиака и активном центре
                  сериновых протеаз.
                </li>
              </ul>
            </div>
          </div>

          <div class="mnemonic-card">
            <h3>🧠 Мнемоника для незаменимых аминокислот</h3>
            <p>
              "Лиза Метнула Фен в Трибуну, Трезвый Лейтенант Валялся в Изоляторе
              с Аргентинским Гитаристом"
            </p>
            <small
              >Лизин, Метионин, Фенилаланин, Триптофан, Треонин, Лейцин, Валин,
              Изолейцин, Аргинин, Гистидин.</small
            >
          </div>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 8: МОДИФИКАЦИИ АМИНОКИСЛОТ
         ========================================== -->
      <section id="modifications" class="topic-card">
        <div class="card-header yellow">
          <h2>8. Модификации аминокислот</h2>
        </div>
        <div class="card-body">
          <p>
            Помимо 20 стандартных аминокислот, в организме существуют их
            модифицированные формы, которые выполняют специфические функции. Они
            могут образовываться в результате посттрансляционных модификаций или
            входить в состав небелковых молекул.
          </p>

          <div class="grid-3-col">
            <div class="mini-card">
              <h4>ГАМК (Гамма-аминомасляная кислота)</h4>
              <p>
                Тормозный нейромедиатор ЦНС. Образуется из глутаминовой кислоты.
              </p>
            </div>
            <div class="mini-card">
              <h4>Дофамин</h4>
              <p>
                Нейромедиатор, предшественник адреналина и норадреналина.
                Синтезируется из тирозина.
              </p>
            </div>
            <div class="mini-card">
              <h4>Тироксин</h4>
              <p>Гормон щитовидной железы. Производное тирозина.</p>
            </div>
            <div class="mini-card">
              <h4>Гистамин</h4>
              <p>
                Медиатор аллергических реакций и воспаления. Содержится в тучных
                клетках. Производное гистидина.
              </p>
            </div>
            <div class="mini-card">
              <h4>Гидроксипролин и Гидроксилизин</h4>
              <p>
                Входят в состав коллагена. Придают ему прочность за счет
                дополнительных водородных связей.
              </p>
            </div>
            <div class="mini-card">
              <h4>Селенцистеин</h4>
              <p>
                Входит в состав антиоксидантных белков. Содержит селен вместо
                серы.
              </p>
            </div>
            <div class="mini-card">
              <h4>Пирролизин</h4>
              <p>Производное лизина. Встречается у архей (метаногенов).</p>
            </div>
            <div class="mini-card">
              <h4>D-Аланин</h4>
              <p>Компонент клеточной стенки бактерий.</p>
            </div>
            <div class="mini-card">
              <h4>Формилметионин</h4>
              <p>
                Первая аминокислота в синтезируемых полипептидных цепях у
                бактерий.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 9: ПОГЛОЩЕНИЕ УФ
         ========================================== -->
      <section id="uv" class="topic-card">
        <div class="card-header purple">
          <h2>9. Поглощение УФ и закон Ламберта-Бера</h2>
        </div>
        <div class="card-body">
          <p>
            Ароматические аминокислоты (Фенилаланин, Тирозин, Триптофан)
            способны поглощать ультрафиолетовое излучение с максимумом в области
            280 нм. Это свойство широко используется в биохимических
            лабораториях для определения концентрации белка в растворе.
          </p>

          <div class="highlight-box">
            <strong>Спектрофотометрия:</strong> Метод, основанный на измерении
            интенсивности света, прошедшего через раствор. Чем выше концентрация
            белка, тем больше света он поглощает.
          </div>

          <p>
            Математически это описывается
            <strong>законом Ламберта-Бера</strong>:
          </p>
          <div
            style="
              text-align: center;
              margin: 20px 0;
              font-size: 1.3rem;
              font-family: var(--font-code);
              background: #f1f5f9;
              padding: 15px;
              border-radius: 8px;
            "
          >
            A = ε · c · l
          </div>

          <ul>
            <li><strong>A</strong> — оптическая плотность (поглощение).</li>
            <li>
              <strong>ε</strong> — коэффициент молярной экстинкции (индивидуален
              для каждого вещества).
            </li>
            <li><strong>c</strong> — концентрация вещества.</li>
            <li>
              <strong>l</strong> — толщина поглощающего слоя (обычно 1 см).
            </li>
          </ul>

          <p>
            Для измерения используют кварцевые кюветы, так как пластик может сам
            поглощать УФ-излучение. Метод очень быстрый, но дает грубую оценку
            концентрации, так как разные белки содержат разное количество
            ароматических аминокислот.
          </p>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 10: МЕТОДЫ РАЗДЕЛЕНИЯ
         ========================================== -->
      <section id="separation" class="topic-card">
        <div class="card-header green">
          <h2>10. Методы разделения аминокислот</h2>
        </div>
        <div class="card-body">
          <p>
            Для анализа смесей аминокислот используются различные
            хроматографические и электрофоретические методы.
          </p>

          <div class="grid-2-col">
            <div class="mini-card">
              <h4>Распределительная хроматография (на бумаге)</h4>
              <p>
                Основана на различии в распределении аминокислот между
                неподвижной водной фазой (на бумаге) и подвижной органической
                фазой (растворитель). Растворитель движется по бумаге
                (восходящий или нисходящий метод), увлекая за собой
                аминокислоты. Положение пятен определяется реакцией с
                нингидрином.
              </p>
            </div>
            <div class="mini-card">
              <h4>Электрофорез</h4>
              <p>
                Основан на движении заряженных частиц в электрическом поле.
                Аминокислоты двигаются к аноду (отрицательный заряд) или катоду
                (положительный заряд) в зависимости от их суммарного заряда при
                данном pH. Более мелкие молекулы мигрируют быстрее.
              </p>
            </div>
            <div class="mini-card">
              <h4>Ионообменная хроматография</h4>
              <p>
                Основана на электростатическом взаимодействии. Ионы аминокислот
                связываются с противоположно заряженными группами на носителе
                (смоле). Элюирование (вымывание) происходит с помощью растворов
                с изменяющимся pH или ионной силой.
              </p>
            </div>
            <div class="mini-card">
              <h4>Высокоэффективная жидкостная хроматография (ВЭЖХ)</h4>
              <p>
                Жидкость под высоким давлением движется через колонку,
                заполненную сорбентом. Позволяет быстро и точно разделять
                сложные смеси аминокислот. Существуют различные варианты:
                адсорбционная, распределительная, ионообменная и др.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- ==========================================
         СЕКЦИЯ 11: КАЧЕСТВЕННЫЕ РЕАКЦИИ
         ========================================== -->
      <section id="reactions" class="topic-card">
        <div class="card-header red">
          <h2>11. Качественные реакции на аминокислоты</h2>
        </div>
        <div class="card-body">
          <p>
            Качественные реакции позволяют обнаружить наличие определенных
            аминокислот в растворе или белке. Они делятся на универсальные (на
            все белки/аминокислоты) и специфические (на отдельные аминокислоты).
          </p>

          <div class="grid-2-col">
            <div class="reaction-box">
              <h4>Ксантопротеиновая реакция</h4>
              <p>
                <strong>На что:</strong> Ароматические аминокислоты
                (Фенилаланин, Тирозин, Триптофан).
              </p>
              <p>
                <strong>Суть:</strong> При взаимодействии с азотной кислотой
                (HNO3) образуется желтое окрашивание. При добавлении щелочи
                (NaOH) окраска усиливается и переходит в оранжевую.
              </p>
            </div>
            <div class="reaction-box">
              <h4>Реакция Миллона</h4>
              <p><strong>На что:</strong> Тирозин.</p>
              <p>
                <strong>Суть:</strong> Тирозин дает красное окрашивание при
                взаимодействии с реактивом Миллона (содержит соли ртути).
              </p>
            </div>
            <div class="reaction-box">
              <h4>Реакция Сакагучи</h4>
              <p><strong>На что:</strong> Аргинин.</p>
              <p>
                <strong>Суть:</strong> Аргинин дает красное окрашивание при
                взаимодействии с α-нафтолом в щелочной среде.
              </p>
            </div>
            <div class="reaction-box">
              <h4>Реакция на серу (Цистеин, Метионин)</h4>
              <p><strong>На что:</strong> Серосодержащие аминокислоты.</p>
              <p>
                <strong>Суть:</strong> При добавлении щелочи и ацетата свинца
                образуется черный осадок сульфида свинца (PbS).
              </p>
            </div>
            <div class="reaction-box">
              <h4>Нингидриновая реакция</h4>
              <p>
                <strong>На что:</strong> Универсальная реакция на
                α-аминокислоты.
              </p>
              <p>
                <strong>Суть:</strong> При нагревании с нингидрином образуется
                сине-фиолетовое окрашивание (кроме пролина — желтое).
              </p>
            </div>
            <div class="reaction-box">
              <h4>Реакция на триптофан</h4>
              <p><strong>На что:</strong> Триптофан.</p>
              <p>
                <strong>Суть:</strong> Триптофан дает сине-фиолетовое
                окрашивание при взаимодействии с глиоксиловой кислотой в
                концентрированной серной кислоте.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- ==========================================
         ЗАВЕРШЕНИЕ КОНСПЕКТА
         ========================================== -->
      <div
        style="
          text-align: center;
          margin-top: 50px;
          padding: 30px;
          background-color: var(--pastel-green-light);
          border-radius: var(--radius-md);
          border: 1px solid var(--pastel-green-dark);
        "
      >
        <h2 style="color: #065f46; margin-bottom: 10px">
          🎉 Конспект лекции завершен!
        </h2>
        <p style="color: #047857; font-size: 1.1rem">
          Мы разобрали все основные темы: от строения аминокислот до методов их
          разделения и качественных реакций.
        </p>
        <p style="color: #047857; margin-top: 10px">
          Удачи на семинаре и тестировании! Не забудьте выучить 20 стандартных
          аминокислот.
        </p>
      </div>
    </div>
  </body>
</html>
