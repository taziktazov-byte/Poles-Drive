<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Poles Drive — Продажа автомобилей</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;900&family=Montserrat:wght@400;700;900&display=swap" rel="stylesheet">
  <script src="https://unpkg.com/lucide@latest"></script>
  <style>
    /* --- ОБЩИЕ СТИЛИ И ПЕРЕМЕННЫЕ --- */
    :root {
      --bg-main: #14AE5C;
      --bg-header: #016435;
      --bg-darker: #014d28;
      --bg-card: #f0f9f4;
      --bg-circle: #d4f0e2;
      --text-gray: #666;
      --text-dark: #333;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--bg-main);
      color: var(--text-dark);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button {
      cursor: pointer;
      border: none;
      background: none;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      width: 100%;
      padding: 0 16px;
    }

    /* --- ШАПКА САЙТА --- */
    header {
      background-color: var(--bg-header);
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    }

    .header-top {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 12px 0;
    }

    .logo-container {
      display: flex;
      align-items: center;
      gap: 12px;
      cursor: pointer;
    }

    .logo-circle {
      width: 32px;
      height: 32px;
      background-color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .logo-circle i {
      color: var(--bg-header);
    }

    .logo-text {
      color: white;
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      font-size: 20px;
      letter-spacing: 0.15em;
    }

    .logo-text span {
      font-weight: 900;
    }

    nav {
      display: flex;
      gap: 24px;
    }

    .nav-link {
      color: rgba(255, 255, 255, 0.8);
      font-size: 14px;
      font-weight: 500;
      transition: color 0.2s;
    }

    .nav-link:hover, .nav-link.active {
      color: white;
      font-weight: 700;
    }

    .header-actions {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .header-actions button {
      color: rgba(255, 255, 255, 0.8);
      transition: color 0.2s;
    }

    .header-actions button:hover {
      color: white;
    }

    /* --- ОСНОВНОЙ КОНТЕНТ (СТРАНИЦЫ) --- */
    main {
      flex: 1;
      padding: 24px 0;
    }

    .page {
      display: none;
    }

    .page.active {
      display: block;
    }

    .white-card {
      background: white;
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
    }

    /* Сетка автомобилей */
    .cars-title-block {
      background: white;
      padding: 12px 20px;
      border-radius: 16px;
      margin-bottom: 16px;
      font-weight: 700;
      text-align: center;
      font-size: 18px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .cars-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 20px;
    }

    .car-card {
      background: white;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 4px 6px rgba(0,0,0,0.05);
      display: flex;
      flex-direction: column;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .car-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 10px 20px rgba(0,0,0,0.15);
    }

    .car-card-img {
      position: relative;
      width: 100%;
      height: 180px;
    }

    .car-card-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .car-card-info {
      padding: 16px;
      flex: 1;
      display: flex;
      flex-direction: column;
    }

    .car-card-tags {
      font-size: 12px;
      color: var(--text-gray);
      line-height: 1.4;
      margin-bottom: 8px;
    }

    .car-card-price {
      font-size: 20px;
      font-weight: 900;
      color: var(--bg-header);
      margin-bottom: 4px;
    }

    .car-card-title {
      font-size: 16px;
      font-weight: 700;
      margin-bottom: 8px;
    }

    /* --- СТРАНИЦА ПОИСКА (3 КОЛОНКИ) --- */
    .search-grid {
      display: grid;
      grid-template-columns: 250px 1fr 300px;
      gap: 24px;
      align-items: start;
    }

    @media (max-width: 1024px) {
      .search-grid {
        grid-template-columns: 1fr;
      }
    }

    /* Левая колонка: Марки */
    .brands-list {
      display: flex;
      flex-direction: column;
      gap: 8px;
      margin-top: 12px;
    }

    .brand-item {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 10px 12px;
      border-radius: 8px;
      font-size: 14px;
      text-align: left;
      transition: all 0.2s;
    }

    .brand-item:hover {
      background-color: var(--bg-card);
    }

    .brand-item.active {
      background-color: var(--bg-header);
      color: white;
      font-weight: 600;
    }

    .brand-item .dot {
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background-color: var(--text-gray);
    }

    .brand-item.active .dot {
      background-color: white;
    }

    .btn-all-brands {
      margin-top: 12px;
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 20px;
      font-size: 14px;
      text-align: center;
      transition: background 0.2s;
    }

    .btn-all-brands:hover {
      background-color: #f5f5f5;
    }

    /* Правая колонка: Фильтры */
    .filters-title {
      font-weight: 700;
      text-transform: uppercase;
      font-size: 14px;
      letter-spacing: 0.05em;
      margin-bottom: 16px;
      text-align: center;
    }

    .filter-group {
      margin-bottom: 16px;
    }

    .filter-group label {
      display: block;
      font-size: 12px;
      font-weight: 600;
      margin-bottom: 6px;
    }

    .range-inputs {
      display: flex;
      gap: 8px;
    }

    .range-inputs input {
      width: 100%;
      padding: 8px;
      border: 1px solid #e0e0e0;
      border-radius: 8px;
      font-size: 13px;
      background: #f9f9f9;
    }

    .filter-select {
      width: 100%;
      padding: 8px;
      border: 1px solid #e0e0e0;
      border-radius: 8px;
      font-size: 13px;
      background: #f9f9f9;
    }

    .btn-reset {
      width: 100%;
      padding: 12px;
      border: 1px solid #ccc;
      border-radius: 12px;
      font-weight: 600;
      margin-top: 8px;
      transition: background 0.2s;
    }

    .btn-reset:hover {
      background: #f5f5f5;
    }

    /* --- СТРАНИЦА ПОДРОБНО --- */
    .detail-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      flex-wrap: wrap;
      gap: 12px;
      margin-bottom: 16px;
    }

    .detail-title h1 {
      color: white;
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      font-size: 30px;
    }

    .detail-meta {
      display: flex;
      gap: 12px;
      align-items: center;
      color: rgba(255,255,255,0.8);
      font-size: 14px;
      margin-top: 4px;
    }

    .rating {
      color: #fde047;
      display: flex;
      align-items: center;
      gap: 4px;
    }

    .detail-price-box {
      text-align: right;
      color: white;
    }

    .detail-price-main {
      font-family: 'Montserrat', sans-serif;
      font-weight: 900;
      font-size: 36px;
    }

    .detail-grid {
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 24px;
    }

    @media (max-width: 1024px) {
      .detail-grid {
        grid-template-columns: 1fr;
      }
    }

    /* Галерея подробно */
    .carousel-wrapper {
      position: relative;
      aspect-ratio: 16/9;
      border-radius: 16px;
      overflow: hidden;
    }

    .carousel-wrapper img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .carousel-btn {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      width: 40px;
      height: 40px;
      background: rgba(0,0,0,0.5);
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .carousel-btn:hover { background: rgba(0,0,0,0.7); }
    .btn-prev { left: 12px; }
    .btn-next { right: 12px; }

    .carousel-counter {
      position: absolute;
      bottom: 12px;
      right: 12px;
      background: rgba(0,0,0,0.5);
      color: white;
      padding: 4px 8px;
      border-radius: 12px;
      font-size: 12px;
    }

    .badge-verified {
      position: absolute;
      top: 12px;
      left: 12px;
      background: #22c55e;
      color: white;
      padding: 4px 12px;
      border-radius: 12px;
      font-size: 12px;
      font-weight: 700;
    }

    .thumbnails {
      display: flex;
      gap: 8px;
      margin-top: 12px;
      overflow-x: auto;
    }

    .thumb {
      width: 80px;
      height: 56px;
      border-radius: 8px;
      overflow: hidden;
      opacity: 0.6;
      border: 2px solid transparent;
    }

    .thumb.active {
      opacity: 1;
      border-color: var(--bg-header);
    }

    .thumb img { width: 100%; height: 100%; object-fit: cover; }

    /* Характеристики подробно */
    .section-title {
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      font-size: 18px;
      margin-bottom: 16px;
    }

    .specs-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 16px;
    }

    @media (max-width: 640px) {
      .specs-grid { grid-template-columns: repeat(2, 1fr); }
    }

    .spec-pill {
      background-color: var(--bg-card);
      border-radius: 12px;
      padding: 12px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }

    .spec-icon-box {
      width: 36px;
      height: 36px;
      border-radius: 50%;
      background: var(--bg-circle);
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 8px;
    }

    .spec-icon-box i { color: var(--bg-header); }
    .spec-label { font-size: 12px; color: var(--text-gray); margin-bottom: 2px; }
    .spec-value { font-size: 14px; font-weight: 700; }
    .desc-text { font-size: 14px; line-height: 1.6; color: #444; }
    .desc-text p + p { margin-top: 12px; }

    .full-specs-group { margin-bottom: 24px; }
    .group-title {
      font-size: 14px;
      font-weight: 700;
      text-transform: uppercase;
      color: var(--bg-header);
      border-bottom: 1px solid var(--bg-circle);
      padding-bottom: 8px;
      margin-bottom: 12px;
    }

    .row-spec {
      display: flex;
      justify-content: space-between;
      padding: 8px;
      font-size: 14px;
    }
    .row-spec:nth-child(odd) { background: #f9f9f9; border-radius: 4px; }
    .row-key { color: var(--text-gray); }
    .row-val { font-weight: 500; text-align: right; }

    .sticky-sidebar {
      display: flex;
      flex-direction: column;
      gap: 20px;
      position: sticky;
      top: 16px;
    }

    .action-box-price {
      font-size: 30px;
      font-weight: 900;
      color: var(--bg-header);
      border-bottom: 1px solid #e6f4ec;
      padding-bottom: 16px;
      margin-bottom: 16px;
    }

    .actions-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .btn-action-primary {
      width: 100%;
      background: var(--bg-header);
      color: white;
      font-weight: 700;
      padding: 14px;
      border-radius: 12px;
      font-size: 16px;
    }

    .btn-action-secondary {
      width: 100%;
      border: 2px solid var(--bg-header);
      color: var(--bg-header);
      background: var(--bg-card);
      font-weight: 700;
      padding: 14px;
      border-radius: 12px;
      font-size: 16px;
    }

    .btn-action-text {
      width: 100%;
      border: 1px solid #e0e0e0;
      color: #444;
      font-weight: 600;
      padding: 12px;
      border-radius: 12px;
      font-size: 14px;
    }

    .trust-badges {
      margin-top: 16px;
      display: flex;
      flex-direction: column;
      gap: 8px;
      font-size: 12px;
      color: var(--text-gray);
    }
    .badge-item { display: flex; align-items: center; gap: 8px; }
    .badge-item i { color: var(--bg-header); }

    .seller-header { display: flex; gap: 12px; align-items: center; margin-bottom: 16px; }
    .seller-avatar {
      width: 56px;
      height: 56px;
      background: var(--bg-header);
      color: white;
      font-weight: 700;
      font-size: 20px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .seller-name { font-weight: 700; }
    .seller-status { font-size: 12px; color: var(--text-gray); }
    .seller-rating { font-size: 12px; display: flex; align-items: center; gap: 4px; color: var(--text-gray); margin-top: 4px;}

    .seller-info-row { display: flex; gap: 8px; font-size: 14px; color: var(--text-gray); margin-bottom: 8px; }
    .seller-info-row i { color: var(--bg-header); }
    .seller-footer { border-top: 1px solid #e6f4ec; padding-top: 16px; margin-top: 16px; font-size: 12px; color: #aaa; }

    .map-placeholder {
      background-color: #e6f4ec;
      height: 160px;
      border-radius: 12px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
    .map-placeholder i { color: var(--bg-header); margin-bottom: 8px; }

    .safety-tip {
      background-color: #fff8e1;
      padding: 16px;
      border-radius: 16px;
      display: flex;
      gap: 12px;
      font-size: 12px;
      color: #555;
      line-height: 1.5;
    }
    .safety-tip i { color: #f59e0b; }

    /* --- СТРАНИЦА: ПОДАТЬ ОБЪЯВЛЕНИЕ --- */
    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
      margin-top: 16px;
    }
    @media(max-width: 768px) { .form-grid { grid-template-columns: 1fr; } }
    
    .form-group {
      display: flex;
      flex-direction: column;
      gap: 6px;
    }
    .form-group label {
      font-size: 14px;
      font-weight: 600;
    }
    .form-input {
      width: 100%;
      border: 1px solid #ccc;
      border-radius: 10px;
      padding: 12px;
      font-size: 14px;
      outline: none;
    }
    .form-input:focus { border-color: var(--bg-main); }
    
    .btn-green {
      background: var(--bg-header);
      color: white;
      font-weight: 700;
      padding: 14px 28px;
      border-radius: 12px;
      font-size: 15px;
      margin-top: 16px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    /* --- СТРАНИЦА: О НАC --- */
    .about-header {
      background: var(--bg-card);
      padding: 32px;
      border-radius: 20px;
      margin-bottom: 24px;
      text-align: center;
    }
    .about-grid {
      display: grid;
      grid-template-columns: 2fr 1fr;
      gap: 24px;
    }
    @media(max-width: 768px) { .about-grid { grid-template-columns: 1fr; } }
    .contact-item {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 16px;
    }
    .contact-icon {
      width: 40px;
      height: 40px;
      background: var(--bg-circle);
      color: var(--bg-header);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    /* --- СТРАНИЦЫ ПОЛИТИКИ И УСЛОВИЙ --- */
    .legal-content {
      max-width: 900px;
      margin: 0 auto;
    }
    .legal-content h1 {
      font-family: 'Montserrat', sans-serif;
      font-weight: 900;
      color: var(--bg-header);
      font-size: 28px;
      margin-bottom: 16px;
    }
    .legal-content h2 {
      font-family: 'Montserrat', sans-serif;
      font-weight: 700;
      font-size: 20px;
      margin-top: 24px;
      margin-bottom: 12px;
      color: var(--bg-header);
    }
    .legal-content p, .legal-content li {
      font-size: 15px;
      line-height: 1.7;
      color: #444;
      margin-bottom: 12px;
    }
    .legal-content ul {
      padding-left: 24px;
      margin-bottom: 16px;
    }

    /* --- ПОДВАЛ (FOOTER) --- */
    footer {
      background-color: var(--bg-header);
      color: white;
      margin-top: 40px;
      padding: 32px 0 20px 0;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 2fr repeat(3, 1fr);
      gap: 32px;
      margin-bottom: 32px;
    }

    @media (max-width: 768px) {
      .footer-grid { grid-template-columns: 1fr; }
    }

    .footer-title { font-weight: 700; font-size: 14px; margin-bottom: 12px; color: rgba(255,255,255,0.9); }
    .footer-links { list-style: none; display: flex; flex-direction: column; gap: 8px; }
    .footer-links button, .footer-links a { 
      font-size: 14px; 
      color: rgba(255,255,255,0.55); 
      transition: color 0.2s; 
      text-align: left;
      padding: 0;
      background: none;
      border: none;
      cursor: pointer;
    }
    .footer-links button:hover, .footer-links a:hover { color: white; }

    .footer-bottom {
      border-top: 1px solid rgba(255, 255, 255, 0.15);
      padding-top: 20px;
      display: flex;
      justify-content: space-between;
      font-size: 12px;
      color: rgba(255,255,255,0.4);
      flex-wrap: wrap;
      gap: 12px;
    }

    /* --- МОДАЛЬНЫЕ ОКНА --- */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.55);
      z-index: 100;
      display: none;
      align-items: center;
      justify-content: center;
      padding: 16px;
    }

    .modal-overlay.active { display: flex; }

    .modal-card {
      background: white;
      border-radius: 22px;
      width: 100%;
      max-width: 440px;
      padding: 24px;
      position: relative;
      box-shadow: 0 25px 50px -12px rgba(0,0,0,0.25);
    }

    .modal-close { position: absolute; top: 16px; right: 16px; color: #aaa; }
    .modal-close:hover { color: #333; }

    .modal-card h2 { font-family: 'Montserrat', sans-serif; font-weight: 700; font-size: 20px; margin-bottom: 4px; }
    .modal-subtitle { font-size: 14px; color: var(--text-gray); margin-bottom: 20px; }

    .modal-form { display: flex; flex-direction: column; gap: 12px; }
    .modal-form input, .modal-form textarea, .modal-form select {
      width: 100%;
      border: 1px solid var(--bg-circle);
      border-radius: 12px;
      padding: 12px;
      font-size: 14px;
      outline: none;
    }

    .phone-box {
      background: var(--bg-card);
      padding: 16px;
      border-radius: 12px;
      margin-bottom: 12px;
    }
    .phone-number { font-size: 24px; font-weight: 900; color: var(--bg-header); font-family: 'Montserrat', sans-serif; }
    .btn-call {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--bg-header);
      color: white;
      padding: 10px 24px;
      border-radius: 12px;
      font-weight: 700;
      margin-top: 12px;
    }

    .success-state { text-align: center; padding: 24px 0; display: none; }
    .success-icon {
      width: 64px;
      height: 64px;
      border-radius: 50%;
      background: var(--bg-circle);
      color: var(--bg-header);
      display: flex;
      align-items: center;
      justify-content: center;
      margin: 0 auto 12px auto;
    }

    /* Виджет чата */
    .widget-chat {
      position: fixed;
      bottom: 80px;
      right: 20px;
      background: white;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      width: 280px;
      padding: 16px;
      z-index: 90;
      border: 1px solid #e0e0e0;
    }
    .widget-header { display: flex; align-items: center; gap: 10px; margin-bottom: 12px; position: relative;}
    .widget-avatar { width: 40px; height: 40px; border-radius: 50%; object-fit: cover; }
    .widget-name { font-size: 13px; font-weight: 700; }
    .widget-msg { background: #f0f0f0; padding: 8px 12px; border-radius: 12px; font-size: 12px; margin-bottom: 12px; }
    .widget-input-box { display: flex; border: 1px solid #ccc; border-radius: 20px; padding: 4px 12px; align-items: center; }
    .widget-input-box input { border: none; outline: none; font-size: 12px; flex: 1; }
    .widget-close { position: absolute; top: 0; right: 0; color: #ccc; }

    /* Стили для модалки выбора марок */
    .brand-modal-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 16px;
    }
    .brand-modal-btn {
      padding: 8px 16px;
      border-radius: 20px;
      border: 1px solid #ccc;
      font-size: 14px;
      background: #f9f9f9;
      transition: 0.2s;
    }
    .brand-modal-btn:hover {
      background: var(--bg-header);
      color: white;
      border-color: var(--bg-header);
    }
  </style>
</head>
<body>

  <header>
    <div class="container header-top">
      <div class="logo-container" onclick="switchPage('main', document.getElementById('link-main'))">
        <div class="logo-circle">
          <i data-lucide="car" size="18"></i>
        </div>
        <span class="logo-text">POLES <span>DRIVE</span></span>
      </div>
      
      <nav>
        <a href="#" id="link-main" class="nav-link active" onclick="switchPage('main', this)">Список авто</a>
        <a href="#" id="link-search" class="nav-link" onclick="switchPage('search', this)">Поиск авто</a>
        <a href="#" id="link-my-ads" class="nav-link" onclick="switchPage('my-ads', this)">Мои объявления</a>
      </nav>

      <div class="header-actions">
        <button><i data-lucide="share-2" size="20"></i></button>
        <button id="likeBtn" onclick="toggleLike()"><i data-lucide="heart" size="20" id="heartIcon"></i></button>
      </div>
    </div>
  </header>

  <main class="container">

    <!-- СТРАНИЦА: ГЛАВНАЯ -->
    <section id="page-main" class="page active">
      <div class="cars-title-block">
        <span>Рекомендуемые вам авто</span>
        <button class="btn-all-brands" style="margin:0; width:auto; padding:6px 16px;" onclick="switchPage('search', document.getElementById('link-search'))">Открыть поиск</button>
      </div>
      <div class="cars-grid" id="main-random-grid">
        </div>
    </section>

    <!-- СТРАНИЦА: ПОИСК -->
    <section id="page-search" class="page">
      <div class="search-grid">
        
        <aside class="white-card">
          <h3 style="font-size: 14px; font-weight: 700; color: #555;">МАРКИ АВТОМОБИЛЕЙ</h3>
          <div class="brands-list" id="brands-list-left">
            <!-- кнопки будут динамически добавлены из JavaScript -->
          </div>
          <button class="btn-all-brands" onclick="openBrandModal()">Показать все</button>
        </aside>

        <div class="cars-main">
          <div class="cars-title-block" id="selected-brand-title">BMW</div>
          <div class="cars-grid" id="search-cars-grid">
            </div>
        </div>

        <aside class="white-card">
          <div class="filters-title">Фильтры</div>
          
          <div class="filter-group">
            <label>Год выпуска</label>
            <div class="range-inputs">
              <input type="number" placeholder="От" value="1990">
              <input type="number" placeholder="До" value="2026">
            </div>
          </div>

          <div class="filter-group">
            <label>Пробег (км)</label>
            <div class="range-inputs">
              <input type="number" placeholder="От" value="0">
              <input type="number" placeholder="До" value="400000">
            </div>
          </div>

          <div class="filter-group">
            <label>Коробка передач</label>
            <select class="filter-select">
              <option>Любая</option>
              <option>АКПП (Автомат)</option>
              <option>РКПП (Механика)</option>
            </select>
          </div>

          <div class="filter-group">
            <label>Объем двигателя (л)</label>
            <div class="range-inputs">
              <input type="number" placeholder="От" value="1.0">
              <input type="number" placeholder="До" value="6.0">
            </div>
          </div>

          <div class="filter-group">
            <label>Цена (р.)</label>
            <div class="range-inputs">
              <input type="number" placeholder="От" value="0">
              <input type="number" placeholder="До" value="500000">
            </div>
          </div>

          <button class="btn-reset" onclick="alert('Фильтры успешно применены')">Применить фильтры</button>
        </aside>

      </div>
    </section>

    <!-- СТРАНИЦА: ДЕТАЛЬНЫЙ ПРОСМОТР -->
    <section id="page-detail" class="page">
      <div class="detail-header">
        <div class="detail-title">
          <h1 id="det-title">Toyota Camry 2.5 AT, 2019</h1>
          <div class="detail-meta">
            <span style="display:flex; align-items:center; gap:4px;"><i data-lucide="map-pin" size="14"></i> Пинск, Брестская область</span>
            <span class="rating">
              <i data-lucide="star" size="13" fill="currentColor"></i>
              <i data-lucide="star" size="13" fill="currentColor"></i>
              <i data-lucide="star" size="13" fill="currentColor"></i>
              <i data-lucide="star" size="13" fill="currentColor"></i>
              <i data-lucide="star" size="13"></i>
              <span style="color:white; opacity:0.7; margin-left:4px;">4.6 (12 отзывов)</span>
            </span>
            <span style="opacity:0.6;" id="det-id">ID: #482910</span>
          </div>
        </div>
        <div class="detail-price-box">
          <div class="detail-price-main" id="det-price">1 490 000 ₽</div>
          <div style="opacity:0.7; font-size:14px;">Доступно в автокредит / рассрочку</div>
        </div>
      </div>

      <div class="detail-grid">
        <div style="display:flex; flex-direction:column; gap:20px;">
          <div class="white-card" style="padding:0; overflow:hidden;">
            <div class="carousel-wrapper">
              <img id="main-carousel-img" src="" alt="Auto">
              <button class="carousel-btn btn-prev" onclick="changeImage(-1)"><i data-lucide="chevron-left"></i></button>
              <button class="carousel-btn btn-next" onclick="changeImage(1)"><i data-lucide="chevron-right"></i></button>
              <div class="carousel-counter" id="carousel-counter-text">1 / 3</div>
              <div class="badge-verified">ПРОВЕРЕНО POLES</div>
            </div>
            <div class="thumbnails" id="thumb-container"></div>
          </div>

          <div class="white-card">
            <h2 class="section-title">Основные характеристики</h2>
            <div class="specs-grid">
              <div class="spec-pill"><div class="spec-icon-box"><i data-lucide="calendar"></i></div><span class="spec-label">Год выпуска</span><span class="spec-value" id="det-spec-year">2019</span></div>
              <div class="spec-pill"><div class="spec-icon-box"><i data-lucide="gauge"></i></div><span class="spec-label">Пробег</span><span class="spec-value" id="det-spec-mileage">87 450 км</span></div>
              <div class="spec-pill"><div class="spec-icon-box"><i data-lucide="settings"></i></div><span class="spec-label">Двигатель</span><span class="spec-value" id="det-spec-engine">2.5л</span></div>
              <div class="spec-pill"><div class="spec-icon-box"><i data-lucide="fuel"></i></div><span class="spec-label">Трансмиссия</span><span class="spec-value" id="det-spec-trans">Автомат</span></div>
            </div>
          </div>

          <div class="white-card">
            <h2 class="section-title">Описание владельца</h2>
            <div class="desc-text" id="det-description">
              <p>Описание загружается...</p>
            </div>
          </div>
        </div>

        <div class="sticky-sidebar">
          <div class="white-card">
            <div class="action-box-price" id="det-side-price">1 490 000 ₽</div>
            <div class="actions-list">
              <button class="btn-action-primary" onclick="openModal('buy')"><i data-lucide="shopping-cart" style="display:inline; vertical-align:middle; margin-right:6px;"></i> Купить автомобиль</button>
              <button class="btn-action-secondary" onclick="openModal('phone')"><i data-lucide="phone" style="display:inline; vertical-align:middle; margin-right:6px;"></i> Получить номер</button>
              <button class="btn-action-text" onclick="openModal('msg')"><i data-lucide="message-square" style="display:inline; vertical-align:middle; margin-right:6px;"></i> Написать владельцу</button>
            </div>
          </div>

          <div class="white-card">
            <h3 class="section-title" style="font-size:16px;">Продавец</h3>
            <div class="seller-header">
              <div class="seller-avatar">PD</div>
              <div>
                <div class="seller-name">Иван Пинский</div>
                <div class="seller-status">Частное лицо</div>
              </div>
            </div>
            <div class="seller-info-row"><i data-lucide="map-pin" size="14"></i> <span>РБ, Брестская область, Пинск</span></div>
          </div>

          <div class="safety-tip">
            <i data-lucide="alert-circle" size="18"></i>
            <p>Никогда не отправляйте предоплату. Встречайтесь в безопасных местах для полной юридической и технической проверки.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- СТРАНИЦА: МОИ ОБЪЯВЛЕНИЯ -->
    <section id="page-my-ads" class="page">
      <div class="cars-title-block">
        <span>Мои активные объявления</span>
        <button class="btn-green" style="margin:0; padding:8px 16px; font-size:13px;" onclick="switchPage('add-ad')">
          <i data-lucide="plus" size="14"></i> Подать объявление
        </button>
      </div>
      <div class="cars-grid" id="my-ads-grid">
        </div>
    </section>

    <!-- СТРАНИЦА: ПОДАТЬ ОБЪЯВЛЕНИЕ -->
    <section id="page-add-ad" class="page">
      <div class="white-card">
        <h2 class="section-title" style="font-size:22px; margin-bottom:8px;">Подать новое объявление</h2>
        <p style="color:var(--text-gray); font-size:14px; margin-bottom:24px;">Заполните все технические параметры вашего транспортного средства для публикации на платформе Poles Drive.</p>
        
        <form onsubmit="handleFormSubmit(event)">
          <div class="form-grid">
            <div class="form-group">
              <label>Марка авто</label>
              <select class="form-input" id="form-brand" required>
                <option value="BMW">BMW</option>
                <option value="Geely">Geely</option>
                <option value="Lada">Lada</option>
                <option value="Kia">Kia</option>
                <option value="Skoda">Skoda</option>
                <option value="Mercedes-Benz">Mercedes-Benz</option>
                <option value="Dodge">Dodge</option>
                <option value="Toyota">Toyota</option>
              </select>
            </div>
            <div class="form-group">
              <label>Модель и комплектация</label>
              <input type="text" class="form-input" id="form-title" placeholder="Например: X6M F96" required>
            </div>
            <div class="form-group">
              <label>Год выпуска</label>
              <input type="number" class="form-input" id="form-year" placeholder="2022" min="1950" max="2026" required>
            </div>
            <div class="form-group">
              <label>Пробег (км)</label>
              <input type="number" class="form-input" id="form-mileage" placeholder="45000" required>
            </div>
            <div class="form-group">
              <label>Объем двигателя (л) и тип топлива</label>
              <input type="text" class="form-input" id="form-engine" placeholder="4.4л, Бензин" required>
            </div>
            <div class="form-group">
              <label>Коробка передач и привод</label>
              <input type="text" class="form-input" id="form-tags" placeholder="автомат, полный, внедорожник" required>
            </div>
            <div class="form-group">
              <label>Цена продажи (р.)</label>
              <input type="text" class="form-input" id="form-price" placeholder="75 000 р." required>
            </div>
            <div class="form-group">
              <label>Ссылка на фото (URL-адрес)</label>
              <input type="text" class="form-input" id="form-img" placeholder="https://images.unsplash.com/photo-..." value="https://images.unsplash.com/photo-1542282088-72c9c27ed0cd?w=600">
            </div>
          </div>
          <button type="submit" class="btn-green"><i data-lucide="check" size="18"></i> Опубликовать на Poles Drive</button>
        </form>
      </div>
    </section>

    <!-- СТРАНИЦА: О НАС -->
    <section id="page-about" class="page">
      <div class="about-header">
        <h1 style="font-family:'Montserrat', sans-serif; font-weight:900; color:var(--bg-header); font-size:32px; margin-bottom:12px;">POLES DRIVE</h1>
        <p style="font-size:16px; max-width:700px; margin:0 auto; color:var(--text-gray); line-height:1.6;">Инновационный автомобильный маркетплейс №1 в Полесском регионе. Мы объединяем тысячи продавцов и покупателей, делая сделки честными, удобными и безопасными.</p>
      </div>
      <div class="about-grid">
        <div class="white-card">
          <h2 class="section-title">О нашей компании</h2>
          <p style="font-size:15px; line-height:1.7; color:#444; margin-bottom:16px;">Компания Poles Drive была основана как локальный технологичный сервис по подбору автомобилей. Сегодня мы выросли до масштабной открытой доски объявлений, где каждый житель Республики Беларусь может выгодно продать или оперативно подобрать себе проверенное авто.</p>
          <p style="font-size:15px; line-height:1.7; color:#444;">Все публикуемые объявления проходят строгую цифровую верификацию и модерацию нашими специалистами, чтобы минимизировать любые риски мошенничества.</p>
        </div>
        <div class="white-card">
          <h2 class="section-title">Контакты</h2>
          <div class="contact-item">
            <div class="contact-icon"><i data-lucide="map-pin" size="18"></i></div>
            <div><strong>Республика Беларусь</strong><br><span style="font-size:13px; color:var(--text-gray);">г. Пинск, ул. Брестская 42а</span></div>
          </div>
          <div class="contact-item">
            <div class="contact-icon"><i data-lucide="phone" size="18"></i></div>
            <div><strong>+375 (29) 444-55-66</strong><br><span style="font-size:13px; color:var(--text-gray);">Единая инфолиния (9:00 - 21:00)</span></div>
          </div>
          <div class="contact-item">
            <div class="contact-icon"><i data-lucide="mail" size="18"></i></div>
            <div><strong>info@polesdrive.by</strong><br><span style="font-size:13px; color:var(--text-gray);">По вопросам рекламы и партнерства</span></div>
          </div>
        </div>
      </div>
    </section>

    <!-- СТРАНИЦА: ПОЛИТИКА КОНФИДЕНЦИАЛЬНОСТИ -->
    <section id="page-privacy" class="page">
      <div class="white-card legal-content">
        <h1>Политика конфиденциальности</h1>
        <p><strong>Последнее обновление:</strong> 19 июня 2026 г.</p>
        <p>Мы, компания «PolesDrive» (УНП 141797643), уважаем вашу конфиденциальность и обязуемся защищать ваши персональные данные. Настоящая политика описывает, какие данные мы собираем, как мы их используем и с кем можем делиться.</p>

        <h2>1. Сбор информации</h2>
        <p>Мы собираем информацию, которую вы предоставляете нам при регистрации, размещении объявлений, оформлении покупки или связи с нашей поддержкой. Это может включать:</p>
        <ul>
          <li>Имя, контактный номер телефона, адрес электронной почты</li>
          <li>Данные об автомобилях, которые вы продаёте или ищете</li>
          <li>История просмотров и действий на сайте</li>
        </ul>

        <h2>2. Использование данных</h2>
        <p>Ваши данные используются для:</p>
        <ul>
          <li>Предоставления и улучшения наших услуг</li>
          <li>Связи с вами по вопросам сделок и поддержки</li>
          <li>Анализа и персонализации вашего опыта</li>
          <li>Соблюдения юридических обязательств</li>
        </ul>

        <h2>3. Защита данных</h2>
        <p>Мы принимаем все необходимые технические и организационные меры для защиты вашей информации от несанкционированного доступа, изменения или уничтожения. Все данные передаются по защищённым каналам.</p>

        <h2>4. Передача данных третьим лицам</h2>
        <p>Мы не продаём и не передаём ваши личные данные третьим лицам, за исключением случаев, предусмотренных законодательством Республики Беларусь, или с вашего явного согласия.</p>

        <h2>5. Ваши права</h2>
        <p>Вы имеете право доступа к своим данным, их исправления или удаления. Для этого свяжитесь с нами по адресу <a href="mailto:info@polesdrive.by" style="color:var(--bg-header);">info@polesdrive.by</a>.</p>

        <h2>6. Файлы cookie</h2>
        <p>Мы используем файлы cookie для улучшения работы сайта. Вы можете отключить их в настройках браузера, но это может повлиять на функциональность.</p>

        <p>Продолжая использовать сайт, вы соглашаетесь с условиями данной политики.</p>
      </div>
    </section>

    <!-- СТРАНИЦА: УСЛОВИЯ ИСПОЛЬЗОВАНИЯ -->
    <section id="page-terms" class="page">
      <div class="white-card legal-content">
        <h1>Условия использования</h1>
        <p><strong>Последнее обновление:</strong> 19 июня 2026 г.</p>
        <p>Добро пожаловать на сайт Poles Drive. Пожалуйста, внимательно ознакомьтесь с настоящими условиями, так как они регулируют ваше использование нашего сервиса.</p>

        <h2>1. Общие положения</h2>
        <p>Настоящие условия являются соглашением между вами и ООО «PolesDrive» (УНП 141797643) и регулируют использование сайта polesdrive.by (далее – «Сайт») и всех его услуг.</p>

        <h2>2. Регистрация и размещение объявлений</h2>
        <ul>
          <li>Вы обязаны предоставлять достоверную информацию при регистрации и размещении объявлений.</li>
          <li>За содержание объявлений и достоверность данных об автомобилях ответственность несёт исключительно продавец.</li>
          <li>Мы оставляем за собой право модерации и удаления объявлений, нарушающих наши правила.</li>
        </ul>

        <h2>3. Права и обязанности пользователей</h2>
        <ul>
          <li>Вы обязуетесь не использовать сайт для мошеннических или противоправных действий.</li>
          <li>Вы несёте ответственность за сохранность своего аккаунта и пароля.</li>
          <li>Вы имеете право размещать только те автомобили, которыми владеете или имеете право продавать.</li>
        </ul>

        <h2>4. Интеллектуальная собственность</h2>
        <p>Все материалы сайта (тексты, логотипы, дизайн) защищены авторским правом и принадлежат ООО «PolesDrive». Копирование или использование без разрешения запрещено.</p>

        <h2>5. Ответственность</h2>
        <p>Мы не являемся стороной сделки между продавцом и покупателем и не несём ответственности за качество, соответствие или юридическую чистоту автомобилей. Все риски и обязательства по сделке лежат на сторонах.</p>

        <h2>6. Заключительные положения</h2>
        <p>Мы оставляем за собой право изменять условия в любое время. Изменения вступают в силу с момента публикации на сайте. Продолжая использовать сайт, вы соглашаетесь с актуальной редакцией.</p>

        <p>По всем вопросам обращайтесь: <a href="mailto:info@polesdrive.by" style="color:var(--bg-header);">info@polesdrive.by</a>.</p>
      </div>
    </section>

  </main>

  <footer>
    <div class="container">
      <div class="footer-grid">
        <div>
          <div class="logo-container" style="margin-bottom: 12px;">
            <div class="logo-circle"><i data-lucide="car" size="15"></i></div>
            <span class="logo-text" style="font-size:16px;">POLES DRIVE</span>
          </div>
          <p style="font-size:14px; color:rgba(255,255,255,0.6); line-height:1.5;">Платформа для безопасной покупки и продажи автомобилей в Республике Беларусь.</p>
        </div>
        <div>
          <h4 class="footer-title">Пользователям</h4>
          <ul class="footer-links">
            <li><button onclick="switchPage('search', document.getElementById('link-search'))">Поиск авто</button></li>
          </ul>
        </div>
        <div>
          <h4 class="footer-title">Продавцам</h4>
          <ul class="footer-links">
            <li><button onclick="switchPage('add-ad')">Подать объявление</button></li>
          </ul>
        </div>
        <div>
          <h4 class="footer-title">Компания</h4>
          <ul class="footer-links">
            <li><button onclick="switchPage('about')">О нас</button></li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <span>© 2026 ООО «PolesDrive», УНП 141797643, Республика Беларусь, г. Пинск, ул. Брестская 42а</span>
        <div style="display:flex; gap:16px;">
          <button onclick="switchPage('privacy')" style="background:none; border:none; color:rgba(255,255,255,0.4); cursor:pointer; text-decoration:underline; font-size:12px;">Политика конфиденциальности</button>
          <button onclick="switchPage('terms')" style="background:none; border:none; color:rgba(255,255,255,0.4); cursor:pointer; text-decoration:underline; font-size:12px;">Условия использования</button>
        </div>
      </div>
    </div>
  </footer>

  <!-- Модалка для покупки -->
  <div class="modal-overlay" id="modal-buy">
    <div class="modal-card">
      <button class="modal-close" onclick="closeAllModals()"><i data-lucide="x" size="22"></i></button>
      <div id="buy-form-state">
        <h2>Оформление покупки</h2>
        <p class="modal-subtitle" id="modal-buy-car-name">Выбранный автомобиль</p>
        <div class="modal-form">
          <input type="text" placeholder="Ваше ФИО" required>
          <input type="tel" placeholder="Ваш телефон" required>
          <select>
            <option>Способ оплаты: Наличные</option>
            <option>Безналичный расчет</option>
          </select>
          <button class="btn-action-primary" style="margin-top:8px;" onclick="submitBuy()">Отправить заявку</button>
        </div>
      </div>
      <div class="success-state" id="buy-success-state">
        <div class="success-icon"><i data-lucide="check" size="32"></i></div>
        <h2>Заявка принята!</h2>
        <p class="modal-subtitle" style="margin-top:8px;">Менеджер свяжется с вами.</p>
      </div>
    </div>
  </div>

  <!-- Модалка для телефона -->
  <div class="modal-overlay" id="modal-phone">
    <div class="modal-card" style="text-align:center;">
      <button class="modal-close" onclick="closeAllModals()"><i data-lucide="x" size="22"></i></button>
      <h2>Контакт продавца</h2>
      <p class="modal-subtitle">Отдел продаж Poles Drive</p>
      <div id="phone-hidden-state">
        <button class="btn-action-primary" onclick="revealPhone()"><i data-lucide="phone" size="16" style="display:inline; margin-right:6px;"></i> Показать номер</button>
      </div>
      <div id="phone-shown-state" style="display:none;">
        <div class="phone-box">
          <div class="phone-number">+375 (29) 444-55-66</div>
          <a href="tel:+375294445566" class="btn-call"><i data-lucide="phone" size="16"></i> Позвонить</a>
        </div>
      </div>
    </div>
  </div>

  <!-- Модалка для сообщения -->
  <div class="modal-overlay" id="modal-msg">
    <div class="modal-card">
      <button class="modal-close" onclick="closeAllModals()"><i data-lucide="x" size="22"></i></button>
      <div id="msg-form-state">
        <h2>Написать владельцу</h2>
        <div class="modal-form">
          <input type="text" placeholder="Ваше имя">
          <textarea rows="4" placeholder="Здравствуйте! Заинтересовал ваш автомобиль. Актуально объявление?"></textarea>
          <button class="btn-action-primary" onclick="submitMsg()">Отправить сообщение</button>
        </div>
      </div>
      <div class="success-state" id="msg-success-state">
        <div class="success-icon"><i data-lucide="check" size="32"></i></div>
        <h2>Сообщение отправлено!</h2>
      </div>
    </div>
  </div>

  <!-- Модалка выбора всех марок -->
  <div class="modal-overlay" id="modal-brands">
    <div class="modal-card">
      <button class="modal-close" onclick="closeAllModals()"><i data-lucide="x" size="22"></i></button>
      <h2>Выберите марку</h2>
      <div class="brand-modal-grid" id="brands-list-modal">
        <!-- динамически заполняется -->
      </div>
    </div>
  </div>

  <!-- Виджет чата -->
  <div class="widget-chat" id="chatWidget">
    <button class="widget-close" onclick="document.getElementById('chatWidget').style.display='none'"><i data-lucide="x" size="16"></i></button>
    <div class="widget-header">
      <div style="width:40px; height:40px; border-radius:50%; background:var(--bg-header); color:white; display:flex; align-items:center; justify-content:center; font-weight:bold;">M</div>
      <div>
        <div class="widget-name">Консультант Марина</div>
        <div style="font-size:10px; color:#22c55e;">Онлайн</div>
      </div>
    </div>
    <div class="widget-msg">Добрый день! Подсказать что-нибудь по выбору автомобиля в РБ?</div>
    <div class="widget-input-box">
      <input type="text" placeholder="Задайте ваш вопрос">
      <button onclick="alert('Сообщение успешно отправлено!')"><i data-lucide="send" size="14" style="color:var(--bg-header)"></i></button>
    </div>
  </div>

  <script>
    lucide.createIcons();

    // --- БАЗА ДАННЫХ АВТОМОБИЛЕЙ (расширена) ---
let CARS_DATA = [
  // --- BMW ---
  {
    id: 1,
    brand: 'BMW',
    title: 'BMW X6M F96',
    year: 2021,
    price: '253 451 р.',
    tags: '2021г., автомат, полный, 4.4л.',
    images: ['https://avcdn.av.by/advertpreview/0012/1711/4706.jpg'],
    mine: false,
    mileage: '30 000 км',
    engine: '4.4л',
    transmission: 'Автомат',
    description: 'Этот автомобиль — мечта любого ценителя скорости и комфорта. Полный привод, мощный двигатель и стильный дизайн. Идеальное состояние, пробег всего 30 тыс. км. Владелец – аккуратный коллекционер. Полная сервисная история, только оригинальные запчасти. Автомобиль готов к дальним поездкам и не требует вложений.'
  },
  {
    id: 9,
    brand: 'BMW',
    title: 'BMW 320i M Sport',
    year: 2019,
    price: '89 900 р.',
    tags: '2019г., автомат, задний, 2.0л.',
    images: ['https://i.ytimg.com/vi/i9vkUKdXMDg/maxresdefault.jpg'],
    mine: false,
    mileage: '62 000 км',
    engine: '2.0л',
    transmission: 'Автомат',
    description: 'Спортивный седан с отличной управляемостью и динамикой. Полный пакет M Sport, кожаный салон, проекционный дисплей. Автомобиль в идеальном состоянии, обслуживался только у дилера. Прекрасный вариант для тех, кто ценит драйв и комфорт.'
  },
  {
    id: 10,
    brand: 'BMW',
    title: 'BMW X5 xDrive40d',
    year: 2020,
    price: '134 200 р.',
    tags: '2020г., автомат, полный, 3.0л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/2146283/e91b29f82832839742cfa63e88a0690a/1200x900'],
    mine: false,
    mileage: '48 500 км',
    engine: '3.0л',
    transmission: 'Автомат',
    description: 'Премиальный внедорожник с мощным дизельным двигателем и богатым оснащением. Адаптивная подвеска, панорамная крыша, система кругового обзора. Идеальное состояние, без ДТП. Отличный выбор для семьи и дальних путешествий.'
  },

  // --- Geely ---
  {
    id: 2,
    brand: 'Geely',
    title: 'Geely Tugella I рест.',
    year: 2022,
    price: '73 000 р.',
    tags: '2022г., автомат, передний, 2.0л.',
    images: ['https://avatars.mds.yandex.net/i?id=03df8edf2a8abf404817c0cb233abb52_l-5214808-images-thumbs&n=13'],
    mine: true,
    mileage: '45 000 км',
    engine: '2.0л',
    transmission: 'Автомат',
    description: 'Стильный кроссовер с отличным соотношением цены и качества. Полный набор опций: климат-контроль, подогрев сидений, камера заднего вида. Экономичный двигатель, расход в городе около 8 л. Отличный выбор для семьи и активного отдыха.'
  },
  {
    id: 11,
    brand: 'Geely',
    title: 'Geely Atlas 1.8T',
    year: 2021,
    price: '61 500 р.',
    tags: '2021г., автомат, передний, 1.8л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/4615031/6ac6faff1eb827b7f47a6ac54d364877/1200x900'],
    mine: false,
    mileage: '37 200 км',
    engine: '1.8л',
    transmission: 'Автомат',
    description: 'Просторный и комфортный кроссовер с турбодвигателем. Отличная шумоизоляция, мягкая подвеска, много места для пассажиров и багажа. Идеальный автомобиль для семьи и длительных поездок.'
  },
  {
    id: 12,
    brand: 'Geely',
    title: 'Geely Coolray GT',
    year: 2020,
    price: '52 300 р.',
    tags: '2020г., автомат, передний, 1.5л.',
    images: ['https://avatars.mds.yandex.net/i?id=8a39dca5651e75a9b7de221c825fff65_l-9029424-images-thumbs&n=13'],
    mine: false,
    mileage: '52 000 км',
    engine: '1.5л',
    transmission: 'Автомат',
    description: 'Компактный и маневренный городской кроссовер. Яркий дизайн, экономичный двигатель, богатое оснащение. Отличный вариант для города и парковки в условиях ограниченного пространства.'
  },

  // --- Lada ---
  {
    id: 3,
    brand: 'Lada',
    title: 'Lada Granta I рест.',
    year: 2018,
    price: '14 463 р.',
    tags: '2018г., механика, передний, 1.6л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/2155046/f3dabb12033bd3b82aef29ca19b9283b/1200x900'],
    mine: true,
    mileage: '78 500 км',
    engine: '1.6л',
    transmission: 'Механика',
    description: 'Надежный и недорогой автомобиль для повседневных поездок. В идеальном техническом состоянии, своевременное обслуживание у официального дилера. Салон чистый, без повреждений. Идеальный вариант для начинающих водителей или как второй автомобиль в семье.'
  },
  {
    id: 13,
    brand: 'Lada',
    title: 'Lada Vesta SW Cross',
    year: 2020,
    price: '24 900 р.',
    tags: '2020г., автомат, передний, 1.8л.',
    images: ['https://www.autostat.ru/application/includes/blocks/big_photo/images/cache/000/049/989/abb07017-670-0.jpg?_=1512724082'],
    mine: false,
    mileage: '41 300 км',
    engine: '1.8л',
    transmission: 'Автомат',
    description: 'Универсал повышенной проходимости с большим клиренсом и вместительным багажником. Комфортный салон, современные опции. Отличный выбор для активного отдыха и поездок за город.'
  },
  {
    id: 14,
    brand: 'Lada',
    title: 'Lada Niva Travel',
    year: 2021,
    price: '29 100 р.',
    tags: '2021г., механика, полный, 1.7л.',
    images: ['https://avatars.mds.yandex.net/i?id=2ba3261f4fa23d4ee7e8dfadd8d3118d_l-16490736-images-thumbs&n=13'], // placeholder
    mine: false,
    mileage: '22 000 км',
    engine: '1.7л',
    transmission: 'Механика',
    description: 'Легендарный внедорожник с отличной проходимостью. Новая модель Travel, улучшенный салон и шумоизоляция. Идеальный автомобиль для рыбалки, охоты и бездорожья. Надежный и неприхотливый.'
  },

  // --- Kia ---
  {
    id: 4,
    brand: 'Kia',
    title: 'Kia Rio III',
    year: 2015,
    price: '26 723 р.',
    tags: '2015г., автомат, передний, 1.6л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/2101836/7ad62d5adb26742fc4a50225835dcb4f/1200x900'],
    mine: false,
    mileage: '112 000 км',
    engine: '1.6л',
    transmission: 'Автомат',
    description: 'Популярный седан с хорошей динамикой и низким расходом топлива. Отличный выбор для города. Комплектация Comfort: кондиционер, электростеклоподъемники, подушка безопасности. Автомобиль регулярно обслуживался, все основные узлы в рабочем состоянии.'
  },
  {
    id: 15,
    brand: 'Kia',
    title: 'Kia Sportage IV',
    year: 2018,
    price: '47 800 р.',
    tags: '2018г., автомат, полный, 2.0л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/5455463/790761618a9d92c758a73b68e022da14/1200x900'], // placeholder
    mine: false,
    mileage: '63 400 км',
    engine: '2.0л',
    transmission: 'Автомат',
    description: 'Стильный кроссовер с полным приводом и богатым оснащением. Кожаный салон, подогрев всех сидений, система стабилизации. Отличное состояние, регулярное ТО. Универсальный автомобиль для города и легкого бездорожья.'
  },
  {
    id: 16,
    brand: 'Kia',
    title: 'Kia Ceed SW',
    year: 2019,
    price: '34 200 р.',
    tags: '2019г., автомат, передний, 1.6л.',
    images: ['https://a.d-cd.net/M-j5iAn9JVnnOUD4RXSr87WiKuo-1920.jpg'],
    mine: false,
    mileage: '53 000 км',
    engine: '1.6л',
    transmission: 'Автомат',
    description: 'Практичный универсал с большим багажником и современным дизайном. Экономичный двигатель, отличная управляемость. Идеальный автомобиль для семьи и путешествий.'
  },

  // --- Skoda ---
  {
    id: 5,
    brand: 'Skoda',
    title: 'Skoda Fabia 6Y',
    year: 2006,
    price: '9 229 р.',
    tags: '2006г., механика, передний, 1.2л.',
    images: ['https://avcdn.av.by/advertmedium/0002/2804/7528.jpg'],
    mine: false,
    mileage: '205 000 км',
    engine: '1.2л',
    transmission: 'Механика',
    description: 'Компактный хэтчбек, экономичный и маневренный. Прекрасно подходит для начинающих водителей и для города. Несмотря на возраст, автомобиль в хорошем рабочем состоянии, двигатель и коробка без нареканий. Отличная цена за такой надежный авто.'
  },
  {
    id: 17,
    brand: 'Skoda',
    title: 'Skoda Octavia A7',
    year: 2017,
    price: '43 600 р.',
    tags: '2017г., автомат, передний, 1.8л.',
    images: ['https://a1.drive-data.ru/An1jPNkyXrh6zYTT5dB4BLw8hQI-960.jpg'],
    mine: false,
    mileage: '89 200 км',
    engine: '1.8л',
    transmission: 'Автомат',
    description: 'Популярный лифтбек с просторным салоном и большим багажником. Отличная управляемость, надежный двигатель. Автомобиль в хорошем состоянии, регулярно обслуживался. Идеальный выбор для семьи и дальних поездок.'
  },
  {
    id: 18,
    brand: 'Skoda',
    title: 'Skoda Kodiaq 2.0 TDI',
    year: 2019,
    price: '62 300 р.',
    tags: '2019г., автомат, полный, 2.0л.',
    images: ['https://i.ytimg.com/vi/rK1OSDFsJ3I/maxresdefault.jpg'],
    mine: false,
    mileage: '46 000 км',
    engine: '2.0л',
    transmission: 'Автомат',
    description: 'Семиместный внедорожник с мощным дизелем и полным приводом. Просторный салон, множество опций. Отличное состояние, полная сервисная история. Прекрасный выбор для большой семьи и активного отдыха.'
  },

  // --- Mercedes-Benz ---
  {
    id: 6,
    brand: 'Mercedes-Benz',
    title: 'Mercedes SLR McLaren',
    year: 2004,
    price: '1 101 957 р.',
    tags: '2004г., автомат, задний, 5.4л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/4706845/27d2c0fe85cd41d7b2c4d1f58c5aa561/1200x900'],
    mine: false,
    mileage: '48 000 км',
    engine: '5.4л',
    transmission: 'Автомат',
    description: 'Легендарный спорткар с уникальным дизайном и невероятной мощностью. Эксклюзивный экземпляр, настоящая коллекционная ценность. Пробег всего 48 тыс. км, полная история обслуживания. Этот автомобиль не просто средство передвижения, а произведение инженерного искусства.'
  },
  {
    id: 19,
    brand: 'Mercedes-Benz',
    title: 'Mercedes-Benz C 300 AMG',
    year: 2018,
    price: '96 700 р.',
    tags: '2018г., автомат, задний, 2.0л.',
    images: ['https://i.ytimg.com/vi/RmYpwGDD4dk/maxresdefault.jpg'],
    mine: false,
    mileage: '57 000 км',
    engine: '2.0л',
    transmission: 'Автомат',
    description: 'Стильный седан с пакетом AMG, спортивной подвеской и мощным двигателем. Отличная динамика, комфортный салон. Автомобиль в идеальном состоянии, без ДТП. Прекрасный выбор для тех, кто ценит комфорт и стиль.'
  },
  {
    id: 20,
    brand: 'Mercedes-Benz',
    title: 'Mercedes-Benz GLE 400 d',
    year: 2020,
    price: '147 200 р.',
    tags: '2020г., автомат, полный, 3.0л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/1933512/d3cfd7026bcb84485d845e771cc187b5/584x438'],
    mine: false,
    mileage: '32 000 км',
    engine: '3.0л',
    transmission: 'Автомат',
    description: 'Роскошный внедорожник с дизельным двигателем и полным приводом. Адаптивная пневмоподвеска, кожаный салон, панорамная крыша. Идеальное состояние, минимальный пробег. Автомобиль премиум-класса для самых требовательных водителей.'
  },

  // --- Dodge ---
  {
    id: 7,
    brand: 'Dodge',
    title: 'Dodge Challenger II',
    year: 2021,
    price: '115 678 р.',
    tags: '2021г., автомат, задний, 5.7л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/2069437/6eae666711c7dd7d57e5c843bccdfcbc/1200x900'],
    mine: false,
    mileage: '25 000 км',
    engine: '5.7л',
    transmission: 'Автомат',
    description: 'Американская классика с мощным V8 и неповторимым стилем. Выделяется из толпы, привлекает внимание. Отличное состояние, как новый. Идеальный автомобиль для тех, кто ценит характер, мощь и яркий образ. Расход топлива, конечно, кусается, но эмоции того стоят!'
  },
  {
    id: 21,
    brand: 'Dodge',
    title: 'Dodge Durango RT',
    year: 2020,
    price: '103 400 р.',
    tags: '2020г., автомат, полный, 5.7л.',
    images: ['https://i.ytimg.com/vi/ICBoq0VmZ6I/maxresdefault.jpg'],
    mine: false,
    mileage: '38 000 км',
    engine: '5.7л',
    transmission: 'Автомат',
    description: 'Мощный семиместный внедорожник с V8, полным приводом и агрессивным дизайном. Просторный салон, богатое оснащение. Идеальный автомобиль для тех, кто не готов жертвовать мощностью ради практичности.'
  },
  {
    id: 22,
    brand: 'Dodge',
    title: 'Dodge Charger SRT',
    year: 2019,
    price: '98 500 р.',
    tags: '2019г., автомат, задний, 6.4л.',
    images: ['https://i.ytimg.com/vi/6iXJhhK3VaU/hqdefault.jpg'],
    mine: false,
    mileage: '29 000 км',
    engine: '6.4л',
    transmission: 'Автомат',
    description: 'Легендарный седан с атмосферным V8 мощностью 485 л.с. Спортивная подвеска, мощные тормоза, агрессивный обвес. Автомобиль в отличном состоянии, проходил только плановое ТО. Настоящий американский мускул.'
  },

  // --- Toyota ---
  {
    id: 8,
    brand: 'Toyota',
    title: 'Toyota Camry 2.5 AT',
    year: 2019,
    price: '1 490 000 ₽',
    tags: '2019г., автомат, передний, 2.5л.',
    images: ['https://images.unsplash.com/photo-1621007947382-bb3c3994e3fb?w=600', 'https://images.unsplash.com/photo-1574023240744-64c47c8c0676?w=600'],
    mine: false,
    mileage: '87 450 км',
    engine: '2.5л',
    transmission: 'Автомат',
    description: 'Надежный и престижный седан бизнес-класса. Комфортный салон, богатое оснащение, отличная управляемость. Автомобиль полностью сервисный, без ДТП. Идеальное состояние как снаружи, так и внутри. Отличная альтернатива новым авто по разумной цене.'
  },
  {
    id: 23,
    brand: 'Toyota',
    title: 'Toyota Corolla 1.6 CVT',
    year: 2020,
    price: '51 200 р.',
    tags: '2020г., вариатор, передний, 1.6л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/2163817/d4b5dfe20d9e46ae2a788093d91d989e/1200x900'],
    mine: false,
    mileage: '43 000 км',
    engine: '1.6л',
    transmission: 'Вариатор',
    description: 'Надежный и экономичный седан с отличной репутацией. Современный дизайн, комфортный салон, низкий расход топлива. Идеальный автомобиль для города и междугородних поездок. Обслуживался у официального дилера.'
  },
  {
    id: 24,
    brand: 'Toyota',
    title: 'Toyota RAV4 2.0 CVT',
    year: 2021,
    price: '82 700 р.',
    tags: '2021г., вариатор, полный, 2.0л.',
    images: ['https://avatars.mds.yandex.net/get-autoru-vos/1907806/ba3fec95e31c75f813da7b3f26b322c3/1200x900'],
    mine: false,
    mileage: '28 500 км',
    engine: '2.0л',
    transmission: 'Вариатор',
    description: 'Популярный кроссовер с полным приводом и просторным салоном. Высокий клиренс, отличная проходимость, современные системы безопасности. Автомобиль в идеальном состоянии, почти новый. Прекрасный выбор для семьи и активного отдыха.'
  }
];

    let currentImagesArray = [];
    let currentImageIndex = 0;
    let currentCarId = null;

    // --- ФУНКЦИЯ ПЕРЕКЛЮЧЕНИЯ СТРАНИЦ ---
    function switchPage(pageId, element) {
      // Скрываем все страницы
      document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
      // Показываем нужную
      const target = document.getElementById(`page-${pageId}`);
      if (target) target.classList.add('active');

      // Управление активными ссылками в навигации (только для основных)
      document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
      if (element && element.classList && element.classList.contains('nav-link')) {
        element.classList.add('active');
      } else {
        // Если переключение не через навигацию (например, футер), снимаем активные классы
        // Но оставляем активными только если страница соответствует одному из пунктов
        if (pageId === 'main') document.getElementById('link-main')?.classList.add('active');
        else if (pageId === 'search') document.getElementById('link-search')?.classList.add('active');
        else if (pageId === 'my-ads') document.getElementById('link-my-ads')?.classList.add('active');
      }
      
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // --- РЕНДЕР СЛУЧАЙНЫХ АВТО НА ГЛАВНОЙ ---
    function renderRandomMainPage() {
      const grid = document.getElementById('main-random-grid');
      grid.innerHTML = '';
      const randomized = [...CARS_DATA].sort(() => 0.5 - Math.random());
      randomized.forEach(car => {
        grid.innerHTML += `
          <div class="car-card" onclick="viewCarDetails(${car.id})">
            <div class="car-card-img"><img src="${car.images[0]}" alt=""></div>
            <div class="car-card-info">
              <div class="car-card-tags">${car.tags}</div>
              <div class="car-card-price">${car.price}</div>
              <div class="car-card-title">${car.title}</div>
            </div>
          </div>
        `;
      });
    }

    // --- ПОКАЗ ПОДРОБНОЙ ИНФОРМАЦИИ ---
    function viewCarDetails(carId) {
      const car = CARS_DATA.find(c => c.id === carId);
      if (!car) return;
      currentCarId = carId;

      document.getElementById('det-title').innerText = `${car.title}, ${car.year}`;
      document.getElementById('det-price').innerText = car.price;
      document.getElementById('det-side-price').innerText = car.price;
      document.getElementById('det-id').innerText = `ID: #4829${car.id}`;
      document.getElementById('det-spec-year').innerText = car.year;
      document.getElementById('det-spec-mileage').innerText = car.mileage;
      document.getElementById('det-spec-engine').innerText = car.engine;
      document.getElementById('det-spec-trans').innerText = car.transmission;
      document.getElementById('modal-buy-car-name').innerText = car.title;

      // Описание
      const descContainer = document.getElementById('det-description');
      descContainer.innerHTML = car.description.split('\n').map(p => `<p>${p}</p>`).join('');

      // Галерея
      currentImagesArray = car.images.length ? car.images : ['https://images.unsplash.com/photo-1542282088-72c9c27ed0cd?w=600'];
      currentImageIndex = 0;
      setupGallery();

      // Переключаем на страницу деталей и убираем активные ссылки (т.к. это не основной пункт меню)
      document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
      switchPage('detail', null);
    }

    function setupGallery() {
      document.getElementById('main-carousel-img').src = currentImagesArray[currentImageIndex];
      document.getElementById('carousel-counter-text').innerText = `${currentImageIndex + 1} / ${currentImagesArray.length}`;
      
      const thumbContainer = document.getElementById('thumb-container');
      thumbContainer.innerHTML = '';
      currentImagesArray.forEach((src, idx) => {
        thumbContainer.innerHTML += `
          <button class="thumb ${idx === currentImageIndex ? 'active' : ''}" onclick="setGalleryIndex(${idx})">
            <img src="${src}" alt="">
          </button>
        `;
      });
    }

    function setGalleryIndex(idx) {
      currentImageIndex = idx;
      setupGallery();
    }

    function changeImage(direction) {
      currentImageIndex += direction;
      if (currentImageIndex < 0) currentImageIndex = currentImagesArray.length - 1;
      if (currentImageIndex >= currentImagesArray.length) currentImageIndex = 0;
      setupGallery();
    }

    // --- РЕНДЕР ПОИСКА ПО МАРКЕ ---
    function renderSearchCars(brandFilter = 'BMW') {
      const grid = document.getElementById('search-cars-grid');
      grid.innerHTML = '';
      
      const filtered = brandFilter === 'ALL' 
        ? CARS_DATA 
        : CARS_DATA.filter(c => c.brand.toLowerCase() === brandFilter.toLowerCase());

      if (filtered.length === 0) {
        grid.innerHTML = '<div style="grid-column: 1/-1; text-align:center; padding:40px; color:#666;">Пока нет предложений для этой марки.</div>';
        return;
      }

      filtered.forEach(car => {
        grid.innerHTML += `
          <div class="car-card" onclick="viewCarDetails(${car.id})">
            <div class="car-card-img"><img src="${car.images[0]}" alt=""></div>
            <div class="car-card-info">
              <div class="car-card-tags">${car.tags}</div>
              <div class="car-card-price">${car.price}</div>
              <div class="car-card-title">${car.title}</div>
            </div>
          </div>
        `;
      });
    }

    // --- ФИЛЬТР ПО МАРКЕ (из левой колонки) ---
    function filterBrand(brand, btn) {
      document.querySelectorAll('.brand-item').forEach(b => b.classList.remove('active'));
      if (brand !== 'ALL' && btn) btn.classList.add('active');
      document.getElementById('selected-brand-title').innerText = brand === 'ALL' ? 'Все марки' : brand;
      renderSearchCars(brand);
      closeAllModals(); // закрываем модалку, если открыта
    }

    // --- ОТКРЫТИЕ МОДАЛКИ СО ВСЕМИ МАРКАМИ ---
    function openBrandModal() {
      const modal = document.getElementById('modal-brands');
      const container = document.getElementById('brands-list-modal');
      container.innerHTML = '';
      // Получаем уникальные марки
      const brands = [...new Set(CARS_DATA.map(c => c.brand))];
      brands.forEach(b => {
        const btn = document.createElement('button');
        btn.className = 'brand-modal-btn';
        btn.innerText = b;
        btn.onclick = function() {
          // Находим кнопку в левой колонке и делаем её активной, если есть
          const leftBrands = document.querySelectorAll('.brand-item');
          let leftBtn = null;
          leftBrands.forEach(el => {
            if (el.innerText.trim() === b) leftBtn = el;
          });
          // Если кнопка есть в левой колонке, активируем её, иначе снимаем все активные
          if (leftBtn) {
            filterBrand(b, leftBtn);
          } else {
            // марки нет в левой колонке - просто применяем фильтр и убираем активные
            document.querySelectorAll('.brand-item').forEach(el => el.classList.remove('active'));
            filterBrand(b, null);
          }
          closeAllModals();
        };
        container.appendChild(btn);
      });
      modal.classList.add('active');
    }

    // --- МОИ ОБЪЯВЛЕНИЯ ---
    function renderMyAds() {
      const grid = document.getElementById('my-ads-grid');
      grid.innerHTML = '';
      const myCars = CARS_DATA.filter(c => c.mine);
      
      if (myCars.length === 0) {
        grid.innerHTML = '<div style="grid-column: 1/-1; text-align:center; padding:40px; color:#666;">У вас нет опубликованных объявлений.</div>';
        return;
      }

      myCars.forEach(car => {
        grid.innerHTML += `
          <div class="car-card" onclick="viewCarDetails(${car.id})">
            <div class="car-card-img"><img src="${car.images[0]}" alt=""></div>
            <div class="car-card-info">
              <div class="car-card-tags">${car.tags}</div>
              <div class="car-card-price">${car.price}</div>
              <div class="car-card-title">${car.title}</div>
              <div style="font-size:11px; color:var(--bg-header); font-weight:700; margin-top:8px; display:flex; align-items:center; gap:4px;">
                <span style="width:6px; height:6px; background:var(--bg-main); border-radius:50%;"></span> Активно в Беларуси
              </div>
            </div>
          </div>
        `;
      });
    }

    // --- ФОРМА ПОДАЧИ ОБЪЯВЛЕНИЯ ---
    function handleFormSubmit(event) {
      event.preventDefault();
      
      const brand = document.getElementById('form-brand').value;
      const titleInput = document.getElementById('form-title').value;
      const year = document.getElementById('form-year').value;
      const mileage = document.getElementById('form-mileage').value;
      const engine = document.getElementById('form-engine').value;
      const tagsRaw = document.getElementById('form-tags').value;
      const price = document.getElementById('form-price').value;
      const img = document.getElementById('form-img').value;

      const newCar = {
        id: Date.now(),
        brand: brand,
        title: `${brand} ${titleInput}`,
        year: parseInt(year),
        price: price.includes('р.') ? price : `${price} р.`,
        tags: `${year}г., ${tagsRaw}, ${engine}, ${mileage} км.`,
        images: [img],
        mine: true,
        mileage: `${mileage} км`,
        engine: engine,
        transmission: tagsRaw.split(',')[0] || 'Не указано',
        description: 'Новое объявление от пользователя. Подробности уточняйте у продавца.'
      };

      CARS_DATA.unshift(newCar);
      alert('Объявление успешно опубликовано в Республике Беларусь!');
      event.target.reset();
      renderMyAds();
      switchPage('my-ads', document.getElementById('link-my-ads'));
    }

    // --- ЛАЙКИ ---
    let isLiked = false;
    function toggleLike() {
      isLiked = !isLiked;
      const icon = document.getElementById('heartIcon');
      if (isLiked) {
        icon.setAttribute('fill', '#ff4d6d');
        icon.setAttribute('stroke', '#ff4d6d');
      } else {
        icon.setAttribute('fill', 'none');
        icon.setAttribute('stroke', 'white');
      }
    }

    // --- МОДАЛЬНЫЕ ОКНА ---
    function openModal(type) {
      document.getElementById(`modal-${type}`).classList.add('active');
    }

    function closeAllModals() {
      document.querySelectorAll('.modal-overlay').forEach(m => m.classList.remove('active'));
      document.getElementById('buy-form-state').style.display = 'block';
      document.getElementById('buy-success-state').style.display = 'none';
      document.getElementById('msg-form-state').style.display = 'block';
      document.getElementById('msg-success-state').style.display = 'none';
      document.getElementById('phone-hidden-state').style.display = 'block';
      document.getElementById('phone-shown-state').style.display = 'none';
    }

    function revealPhone() {
      document.getElementById('phone-hidden-state').style.display = 'none';
      document.getElementById('phone-shown-state').style.display = 'block';
    }

    function submitBuy() {
      document.getElementById('buy-form-state').style.display = 'none';
      document.getElementById('buy-success-state').style.display = 'block';
      setTimeout(closeAllModals, 2000);
    }

    function submitMsg() {
      document.getElementById('msg-form-state').style.display = 'none';
      document.getElementById('msg-success-state').style.display = 'block';
      setTimeout(closeAllModals, 2000);
    }

    // --- ИНИЦИАЛИЗАЦИЯ ---
    // Заполняем левую колонку марками (все доступные)
    function initLeftBrands() {
      const container = document.getElementById('brands-list-left');
      container.innerHTML = '';
      const brands = [...new Set(CARS_DATA.map(c => c.brand))];
      brands.forEach(b => {
        const btn = document.createElement('button');
        btn.className = 'brand-item';
        btn.innerHTML = `<span class="dot"></span>${b}`;
        btn.onclick = function() {
          filterBrand(b, this);
        };
        container.appendChild(btn);
      });
      // Активируем первую марку
      const first = container.querySelector('.brand-item');
      if (first) {
        first.classList.add('active');
        renderSearchCars('BMW'); // по умолчанию BMW
      }
    }

    // Старт
    initLeftBrands();
    renderRandomMainPage();
    renderMyAds();
  </script>
</body>
</html>
