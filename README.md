<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="موقع لبيع وشراء العقارات في منطقتك. استكشف العقارات المتاحة، وابحث عن منزلك المثالي اليوم!">
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
    <title>7ASIR</title>
</head>
<body>
    <header>
        <nav>
            <div class="logo">شركة العقارات</div>
            <ul class="nav-links">
                <li><a href="#home" class="lang" data-en="Home" data-fr="Accueil">الرئيسية</a></li>
                <li><a href="#properties" class="lang" data-en="Properties" data-fr="Propriétés">العقارات</a></li>
                <li><a href="#about" class="lang" data-en="About Us" data-fr="À Propos">عن الشركة</a></li>
                <li><a href="#contact" class="lang" data-en="Contact Us" data-fr="Contactez-Nous">اتصل بنا</a></li>
            </ul>
            <input type="text" id="search-bar" placeholder="ابحث عن عقارك..." />
            <div>
                <button id="lang-ar" onclick="changeLanguage('ar')">عربي</button>
                <button id="lang-en" onclick="changeLanguage('en')">English</button>
                <button id="lang-fr" onclick="changeLanguage('fr')">Français</button>
            </div>
        </nav>
    </header>

    <main>
        <section id="hero">
            <h1 class="lang" data-en="Discover Your Perfect Home" data-fr="Découvrez Votre Maison Parfaite">اكتشف منزلك المثالي</h1>
            <p class="lang" data-en="Explore a wide range of available properties for sale or rent." data-fr="Explorez une large gamme de propriétés disponibles à la vente ou à la location.">استعرض مجموعة واسعة من العقارات المتاحة للشراء أو الإيجار.</p>
        </section>

        <section id="properties">
            <h2 class="lang" data-en="Available Properties" data-fr="Propriétés Disponibles">العقارات المتاحة</h2>
            <div id="filters">
                <label for="min-price" class="lang" data-en="Min Price:" data-fr="Prix Min:">السعر الأدنى:</label>
                <input type="number" id="min-price" placeholder="0">
                
                <label for="max-price" class="lang" data-en="Max Price:" data-fr="Prix Max:">السعر الأقصى:</label>
                <input type="number" id="max-price" placeholder="500000">
                
                <label for="bedrooms" class="lang" data-en="Bedrooms:" data-fr="Chambres:">عدد الغرف:</label>
                <select id="bedrooms">
                    <option value="">-- اختر عدد الغرف --</option>
                    <option value="1">1</option>
                    <option value="2">2</option>
                    <option value="3">3</option>
                    <option value="4">4</option>
                    <option value="5">5+</option>
                </select>

                <button id="filter-button" class="lang" data-en="Filter" data-fr="Filtrer">تصفية</button>
            </div>
            <div class="property-list" id="property-list">
                <!-- قائمة العقارات ستُضاف هنا بواسطة JavaScript -->
            </div>
        </section>

        <section id="map">
            <h2 class="lang" data-en="Explore the Area" data-fr="Explorer la Zone">استكشاف المنطقة</h2>
            <div id="mapid"></div>
        </section>

        <section id="about">
            <h2 class="lang" data-en="About Us" data-fr="À Propos de Nous">عن الشركة</h2>
            <p class="lang" data-en="We are a leading real estate company, providing high-quality services to help you find your perfect home." data-fr="Nous sommes une entreprise immobilière leader, offrant des services de haute qualité pour vous aider à trouver votre maison idéale.">نحن شركة رائدة في مجال العقارات، نقدم خدمات عالية الجودة للمساعدة في العثور على المنزل المثالي لك.</p>
        </section>

        <section id="contact">
            <h2 class="lang" data-en="Contact Us" data-fr="Contactez-Nous">اتصل بنا</h2>
            <form id="contact-form">
                <label for="name" class="lang" data-en="Name:" data-fr="Nom:">الاسم:</label>
                <input type="text" id="name" required>
                <label for="email" class="lang" data-en="Email:" data-fr="Email:">البريد الإلكتروني:</label>
                <input type="email" id="email" required>
                <label for="message" class="lang" data-en="Message:" data-fr="Message:">الرسالة:</label>
                <textarea id="message" required></textarea>
                <button type="submit" class="lang" data-en="Send" data-fr="Envoyer">إرسال</button>
            </form>
        </section>
    </main>

    <footer>
        <p class="lang" data-en="&copy; 2024 Real Estate Company. All rights reserved." data-fr="&copy; 2024 Société Immobilière. Tous droits réservés.">&copy; 2024 شركة العقارات. جميع الحقوق محفوظة.</p>
    </footer>

    <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
    <script src="script.js"></script>
</body>
</html>
