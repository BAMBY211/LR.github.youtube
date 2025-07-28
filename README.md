<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>BambyLove - Produits Naturels à l'Aloe Vera</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
	<link rel="stylesheet" href="style.css"> <!-- Si style.css est à côté de index.html -->
    <style>
        :root {
            --primary: #2a2a2a;
            --secondary: #d4af37;
            --light: #f8f9fa;
            --dark: #212529;
            --text: #333;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
        }
        
        /* Navigation */
        .navbar {
            background: rgba(42, 42, 42, 0.9);
            backdrop-filter: blur(10px);
            padding: 1.2rem 5%;
            position: fixed;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 30px rgba(0, 0, 0, 0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .logo {
            color: var(--secondary);
            font-size: 1.8rem;
            font-weight: 700;
            letter-spacing: 1px;
            text-decoration: none;
        }
        
        .logo span {
            color: white;
        }
        
        .nav-logo {
            height: 50px;
            width: auto;
        }
        
        .nav-links {
            display: flex;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            letter-spacing: 1px;
            position: relative;
            transition: var(--transition);
        }
        
        .nav-links a:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--secondary);
            bottom: -5px;
            left: 0;
            transition: var(--transition);
        }
        
        .nav-links a:hover:after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            height: 95vh;
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.3)), url('62.jpg') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            padding-top: 70px;
        }
        
        .hero-content {
            max-width: 800px;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            letter-spacing: 2px;
            animation: fadeIn 1.5s ease;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            animation: fadeIn 2s ease;
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: var(--dark);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            letter-spacing: 1px;
            text-decoration: none;
            transition: var(--transition);
            animation: fadeIn 2.5s ease;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(212, 175, 55, 0.3);
        }
        
        /* Products Section */
        .products-section {
            padding: 5rem 5%;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            display: inline-block;
            position: relative;
        }
        
        .section-title h2:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background: var(--secondary);
            bottom: -10px;
            left: 25%;
        }
        
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            width: 100%;
        }
        
        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: var(--transition);
            position: relative;
            width: 100%;
            margin: 0 auto;
            max-width: 450px;
        }
        
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .product-badge {
            position: absolute;
            top: 25px;
            right: 15px;
            background: var(--secondary);
            color: var(--dark);
            padding: 0.3rem 0.8rem;
            border-radius: 50px;
            font-weight: 600;
            font-size: 0.8rem;
            z-index: 1;
        }
        
        .product-img-container {
            height: 300px;
            overflow: hidden;
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .product-img {
            width: 100%;
            height: auto;
            max-height: 350px;
            object-fit: contain;
            transition: var(--transition);
        }
        
        .product-card:hover .product-img {
            transform: scale(1.1);
        }
        
        .product-info {
            padding: 1rem;
            text-align: center;
        }
        
        .product-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .product-price {
            color: var(--secondary);
            font-weight: 700;
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }
        
        .product-price-fcfa {
            color: #666;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }
        
        .product-description {
            color: #666;
            margin-bottom: 1.5rem;
            font-size: 0.9rem;
        }
        
        .product-actions {
            display: flex;
            justify-content: space-between;
        }
        
        .wishlist-btn {
            background: none;
            border: none;
            color: #ccc;
            font-size: 1.2rem;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .wishlist-btn:hover {
            color: #ff4757;
        }
        
        /* Video Section */
        .video-section {
            padding: 5rem 5%;
            background: #f5f5f5;
            text-align: center;
        }
        
        .video-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .video-container video {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        /* Footer */
        footer {
            background: var(--primary);
            color: white;
            padding: 4rem 5% 2rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
            position: relative;
            display: inline-block;
        }
        
        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 50%;
            height: 2px;
            background: var(--secondary);
            bottom: -5px;
            left: 0;
        }
        
        .footer-column p, .footer-column a {
            color: #ddd;
            margin-bottom: 0.8rem;
            display: block;
            transition: var(--transition);
            text-decoration: none;
        }
        
        .footer-column a:hover {
            color: var(--secondary);
            transform: translateX(5px);
        }
        
        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-links a {
            color: white;
            background: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }
        
        .social-links a:hover {
            background: var(--secondary);
            color: var(--dark);
            transform: translateY(-5px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Newsletter Form */
        .newsletter-form input {
            padding: 0.5rem;
            width: 100%;
            margin-bottom: 0.5rem;
            border: none;
            border-radius: 4px;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                padding: 1rem;
            }
            
            .logo-container {
                flex-direction: column;
                align-items: center;
            }
            
            .nav-links {
                margin-top: 1rem;
                gap: 1rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            .products-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Tablettes (768px et plus) */
        @media (min-width: 768px) {
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .hero h1 {
                font-size: 4rem;
            }
        }

        /* Ordinateurs (1024px et plus) */
        @media (min-width: 1024px) {
            .products-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .navbar {
                padding: 1.5rem 8%;
            }
        }

        /* Grands écrans (1200px et plus) */
        @media (min-width: 1200px) {
            .products-grid {
                grid-template-columns: repeat(4, 1fr);
            }
        }

        .payment-text {
            opacity: 0.7;
        }
        .payment-text {
            background: linear-gradient(90deg, 
                        rgba(255,255,255,0.5), 
                        rgba(255,255,255,0.8));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="logo-container">
            <a href="#" class="logo">FATOU<span>LOVE</span></a>
            <img src="66.jpg" alt="Logo BambyLove" class="nav-logo">
        </div>
        <div class="nav-links">
            <a href="LR.html">Accueil</a>
            <a href="Sert.html">Produits</a>
            <a href="Ppo.html">À propos</a>
            <a href="Ret.html">Contact</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Collection Exclusive 2025</h1>
            <p>Découvrez notre sélection de produits naturels à l'Aloe Vera, alliant bien-être et qualité exceptionnelle.</p>
            <a href="#products" class="btn">Explorer la collection</a>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products-section" id="products">
        <div class="section-title">
            <h2>Nos Produits Phares</h2>
        </div>
        <div class="products-grid">
            <!-- Produit 1 -->
            <div class="product-card">
                <div class="product-badge">Nouveau</div>
                <div class="product-img-container">
                    <img src="50.jpg" alt="Health and Beauty Gel" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Health and Beauty Gel pour Homme</h3>
                    <p class="product-price">19,90 €</p>
                    <p class="product-price-fcfa">≈ 13 035 FCFA</p>
                    <p class="product-description">Gel hydratant à base d'aloe vera pour une peau saine et rafraîchie.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 2 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="52.jpg" alt="Aloe Vera Drinking Gel" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Aloe Vera Drinking Gel</h3>
                    <p class="product-price">22,50 €</p>
                    <p class="product-price-fcfa">≈ 14 738 FCFA</p>
                    <p class="product-description">Gel à boire à l'aloe vera avec gingembre, citron et miel.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 3 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="53.jpeg" alt="Lotion et Shampoing pour Bébé" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Lotion et Shampoing pour Bébé</h3>
                    <p class="product-price">16,90 €</p>
                    <p class="product-price-fcfa">≈ 11 070 FCFA</p>
                    <p class="product-description">Produits doux sans parfum pour la peau délicate des bébés.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 4 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="67.jpg" alt="Crème correctrice" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Crème correctrice Aloe Vera</h3>
                    <p class="product-price">24,90 €</p>
                    <p class="product-price-fcfa">≈ 16 310 FCFA</p>
                    <p class="product-description">Crème réparatrice pour les imperfections cutanées.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 5 -->
            <div class="product-card">
                <div class="product-badge">Nouveauté</div>
                <div class="product-img-container">
                    <img src="60.jpg" alt="Gel Visage Possiflore bleue" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Gel Visage Possiflore</h3>
                    <p class="product-price">18,50 €</p>
                    <p class="product-price-fcfa">≈ 12 118 FCFA</p>
                    <p class="product-description">Gel rafraîchissant pour le visage à la fleur de passiflore.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 6 -->
            <div class="product-card">
                <div class="product-badge">Promo</div>
                <div class="product-img-container">
                    <img src="59.jpg" alt="Exotic Papaya" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Exotic Papaya</h3>
                    <p class="product-price"><del>25,00 €</del> 19,90 €</p>
                    <p class="product-price-fcfa"><del>≈ 16 375 FCFA</del> ≈ 13 035 FCFA</p>
                    <p class="product-description">Soin exfoliant à la papaye pour une peau lumineuse.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 7 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="54.jpg" alt="Lait nettoyant Visage" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Lait nettoyant Visage</h3>
                    <p class="product-price">15,90 €</p>
                    <p class="product-price-fcfa">≈ 10 415 FCFA</p>
                    <p class="product-description">Nettoyant doux pour le visage à l'Aloe Vera.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 8 -->
            <div class="product-card">
                <div class="product-badge">Édition limitée</div>
                <div class="product-img-container">
                    <img src="55.jpg" alt="Sérum Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Sérum Aloe Vera</h3>
                    <p class="product-price">29,90 €</p>
                    <p class="product-price-fcfa">≈ 19 585 FCFA</p>
                    <p class="product-description">Sérum intensif pour une hydratation profonde.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 9 -->
            <div class="product-card">
                <div class="product-badge">Nouveau</div>
                <div class="product-img-container">
                    <img src="76.jpg" alt="24h Moisture Face Serum" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">24h Moisture Face Serum</h3>
                    <p class="product-price">27,50 €</p>
                    <p class="product-price-fcfa">≈ 18 013 FCFA</p>
                    <p class="product-description">Sérum hydratant longue durée à l'Aloe Vera.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 10 -->
            <div class="product-card">
                <div class="product-badge">Nouveauté</div>
                <div class="product-img-container">
                    <img src="51.jpg" alt="Crème hydratante" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Crème Hydratante Aloe</h3>
                    <p class="product-price">17,90 €</p>
                    <p class="product-price-fcfa">≈ 11 725 FCFA</p>
                    <p class="product-description">Crème nourrissante à base d'aloe vera pour une peau douce.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            
            <!-- Produit 11 -->
            <div class="product-card">
                <div class="product-badge">Édition limitée</div>
                <div class="product-img-container">
                    <img src="57.jpg" alt="Kit Soin Complet" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Kit Soin Complet</h3>
                    <p class="product-price">49,90 €</p>
                    <p class="product-price-fcfa">≈ 32 685 FCFA</p>
                    <p class="product-description">Kit complet pour une routine de soin à l'Aloe Vera.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            <!-- Produit 12 -->
            <div class="product-card">
                <div class="product-badge">Nouveau</div>
                <div class="product-img-container">
                    <img src="01.jpeg" alt="Shampoing Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Shampoing Purifiant Aloe Vera</h3>
                    <p class="product-price">18,90 €</p>
                    <p class="product-price-fcfa">≈ 12 380 FCFA</p>
                    <p class="product-description">Shampoing doux à l'Aloe Vera pour cuir chevelu sain et cheveux brillants.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 13 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="05.jpeg" alt="Masque Visage Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Masque Apaisant Aloe Vera</h3>
                    <p class="product-price">21,50 €</p>
                    <p class="product-price-fcfa">≈ 14 083 FCFA</p>
                    <p class="product-description">Masque hydratant et apaisant pour peau sensible et irritée.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 14 -->
            <div class="product-card">
                <div class="product-badge">Édition limitée</div>
                <div class="product-img-container">
                    <img src="03.jpg" alt="Lotion Après-Soleil" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Lotion Après-Soleil Aloe Vera</h3>
                    <p class="product-price">23,90 €</p>
                    <p class="product-price-fcfa">≈ 15 655 FCFA</p>
                    <p class="product-description">Apaisement immédiat pour les peaux exposées au soleil.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 15 -->
            <div class="product-card">
                <div class="product-badge">Nouveauté</div>
                <div class="product-img-container">
                    <img src="04.jpg" alt="Déodorant Naturel" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Déodorant Naturel Aloe Vera</h3>
                    <p class="product-price">14,90 €</p>
                    <p class="product-price-fcfa">≈ 9 760 FCFA</p>
                    <p class="product-description">Déodorant sans aluminium à l'Aloe Vera et huile de coco.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 16 -->
            <div class="product-card">
                <div class="product-badge">Promo</div>
                <div class="product-img-container">
                    <img src="06.jpg" alt="Tonique Visage" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Tonique Raffermissant Aloe Vera</h3>
                    <p class="product-price"><del>19,90 €</del> 16,50 €</p>
                    <p class="product-price-fcfa"><del>≈ 13 035 FCFA</del> ≈ 10 808 FCFA</p>
                    <p class="product-description">Tonique purifiant pour pores resserrés et peau tonifiée.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 17 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="07.png" alt="Soin Pieds" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Crème Pieds Secs Aloe Vera</h3>
                    <p class="product-price">15,90 €</p>
                    <p class="product-price-fcfa">≈ 10 415 FCFA</p>
                    <p class="product-description">Crème réparatrice intensive pour pieds très secs.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 18 -->
            <div class="product-card">
                <div class="product-badge">Nouveau</div>
                <div class="product-img-container">
                    <img src="aloe-makeup.jpg" alt="Démaquillant" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Lait Démaquillant Aloe Vera</h3>
                    <p class="product-price">17,50 €</p>
                    <p class="product-price-fcfa">≈ 11 463 FCFA</p>
                    <p class="product-description">Démaquille en douceur tout en hydratant la peau.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 19 -->
            <div class="product-card">
                <div class="product-badge">Édition limitée</div>
                <div class="product-img-container">
                    <img src="aloe-body.jpg" alt="Lotion Corporelle" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Lotion Corporelle Aloe Vera</h3>
                    <p class="product-price">22,90 €</p>
                    <p class="product-price-fcfa">≈ 15 000 FCFA</p>
                    <p class="product-description">Hydratation intense pour le corps, absorption rapide.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 20 -->
            <div class="product-card">
                <div class="product-badge">Pack</div>
                <div class="product-img-container">
                    <img src="aloe-pack.jpg" alt="Pack Découverte" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Pack Découverte Aloe Vera</h3>
                    <p class="product-price">39,90 €</p>
                    <p class="product-price-fcfa">≈ 26 135 FCFA</p>
                    <p class="product-description">Sélection de nos meilleurs produits pour une routine complète.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
            <!-- Produit 21 -->
            <div class="product-card">
                <div class="product-badge">Nouveauté</div>
                <div class="product-img-container">
                    <img src="aloe-intimate.jpg" alt="Gel Intime Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Gel Intime Aloe Vera</h3>
                    <p class="product-price">16,90 €</p>
                    <p class="product-price-fcfa">≈ 11 070 FCFA</p>
                    <p class="product-description">Gel nettoyant doux pH neutre pour une hygiène intime respectueuse.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 22 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="aloe-toothpaste.jpg" alt="Dentifrice Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Dentifrice Blanchissant Aloe Vera</h3>
                    <p class="product-price">9,90 €</p>
                    <p class="product-price-fcfa">≈ 6 485 FCFA</p>
                    <p class="product-description">Dentifrice naturel au pouvoir blanchissant et apaisant pour les gencives.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 23 -->
            <div class="product-card">
                <div class="product-badge">Édition limitée</div>
                <div class="product-img-container">
                    <img src="aloe-massage.jpg" alt="Huile Massage Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Huile Massage Aloe Vera</h3>
                    <p class="product-price">26,50 €</p>
                    <p class="product-price-fcfa">≈ 17 358 FCFA</p>
                    <p class="product-description">Huile de massage relaxante enrichie en Aloe Vera et huiles essentielles.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 24 -->
            <div class="product-card">
                <div class="product-badge">Nouveau</div>
                <div class="product-img-container">
                    <img src="aloe-scrub.jpg" alt="Gommage Corps Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Gommage Corps Aloe Vera</h3>
                    <p class="product-price">18,90 €</p>
                    <p class="product-price-fcfa">≈ 12 380 FCFA</p>
                    <p class="product-description">Gommage exfoliant doux pour une peau lisse et radieuse.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 25 -->
            <div class="product-card">
                <div class="product-badge">Promo</div>
                <div class="product-img-container">
                    <img src="aloe-spray.jpg" alt="Spray Hydratant Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Spray Hydratant Aloe Vera</h3>
                    <p class="product-price"><del>14,90 €</del> 12,50 €</p>
                    <p class="product-price-fcfa"><del>≈ 9 760 FCFA</del> ≈ 8 188 FCFA</p>
                    <p class="product-description">Brume fraîcheur pour un coup d'éclat instantané toute la journée.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 26 -->
            <div class="product-card">
                <div class="product-badge">Best-seller</div>
                <div class="product-img-container">
                    <img src="aloe-lip.jpg" alt="Baume à Lèvres Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Baume à Lèvres Aloe Vera</h3>
                    <p class="product-price">6,90 €</p>
                    <p class="product-price-fcfa">≈ 4 520 FCFA</p>
                    <p class="product-description">Soin réparateur intensif pour lèvres gercées et sèches.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 27 -->
            <div class="product-card">
                <div class="product-badge">Nouveauté</div>
                <div class="product-img-container">
                    <img src="aloe-legs.jpg" alt="Gel Jambes Lourdes Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Gel Jambes Lourdes Aloe Vera</h3>
                    <p class="product-price">21,90 €</p>
                    <p class="product-price-fcfa">≈ 14 345 FCFA</p>
                    <p class="product-description">Sensation de fraîcheur immédiate pour jambes fatiguées.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 28 -->
            <div class="product-card">
                <div class="product-badge">Éco-responsable</div>
                <div class="product-img-container">
                    <img src="aloe-soap.jpg" alt="Savon Liquide Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Savon Liquide Aloe Vera</h3>
                    <p class="product-price">12,90 €</p>
                    <p class="product-price-fcfa">≈ 8 450 FCFA</p>
                    <p class="product-description">Nettoyant corporel doux sans savon, pH neutre.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 29 -->
            <div class="product-card">
                <div class="product-badge">Détente</div>
                <div class="product-img-container">
                    <img src="aloe-eyes.jpg" alt="Compresses Oculaires Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Compresses Oculaires Aloe Vera</h3>
                    <p class="product-price">15,50 €</p>
                    <p class="product-price-fcfa">≈ 10 153 FCFA</p>
                    <p class="product-description">Apaisement immédiat pour les yeux fatigués.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>

            <!-- Produit 30 -->
            <div class="product-card">
                <div class="product-badge">Pour Homme</div>
                <div class="product-img-container">
                    <img src="aloe-shave.jpg" alt="Stick à Raser Aloe Vera" class="product-img">
                </div>
                <div class="product-info">
                    <h3 class="product-title">Stick à Raser Aloe Vera</h3>
                    <p class="product-price">13,90 €</p>
                    <p class="product-price-fcfa">≈ 9 105 FCFA</p>
                    <p class="product-description">Prévient les irritations et les rougeons après rasage.</p>
                    <div class="product-actions">
                        <button class="wishlist-btn"><i class="far fa-heart"></i></button>
                        <a href="#" class="btn">Voir détails</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-content">
            <div class="footer-column">
                <h3>BAMBYLOVE</h3>
                <p>Nous offrons des produits naturels de haute qualité pour votre bien-être.</p>
                <div class="social-links">
                    <a href="https://facebook.com/ascesw.pasvraiment" target="_blank" title="Facebook"><i class="fab fa-facebook-f"></i></a>
                    <a href="https://www.instagram.com/bamby_diop21/"><i class="fab fa-instagram"></i></a>
                    <a href="https://www.tiktok.com/@abd221.com"><i class="fab fa-tiktok"></i></a>
                    <a href="https://wa.me/773767317" target="_blank"><i class="fab fa-whatsapp"></i></a>
                </div>
            </div>
            <div class="footer-column">
                <h3>Liens utiles</h3>
                <a href="condi.html">Conditions générales</a>
                <a href="conf.html">Politique de confidentialité</a>
            </div>
            <div class="footer-column">
                <h3>Service client</h3>
                <a href="Ret.html">Contactez-nous</a>
            </div>
            <div class="footer-column">
                <h3>Newsletter</h3>
                <p>Abonnez-vous pour recevoir nos offres exclusives.</p>
                <form class="newsletter-form">
                    <input type="email" placeholder="Votre email" required>
                    <button type="submit" class="btn">S'abonner</button>
                </form>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2024 BAMBYLOVE. Tous droits réservés.</p>
        </div>
    </footer>
    
    <script>
        // Fonction pour Wave
        function payWithWave() {
            const phone = "773767317"; // Remplacez par votre numéro Wave
            const amount = prompt("Entrez le montant (FCFA):", "5000");
            
            if (amount) {
                // Essaie d'ouvrir l'application Wave
                window.location.href = `wave://send?phone=${phone}&amount=${amount}`;
                
                // Solution de secours si le lien échoue
                setTimeout(() => {
                    alert(`Ouvrez l'application Wave et envoyez ${amount}FCFA au ${phone}\nRéférence: CMD${Date.now()}`);
                }, 500);
            }
        }

        // Fonction pour Orange Money
        function payWithOrange() {
            const amount = prompt("Entrez le montant (FCFA):", "5000");
            if (amount) {
                const codeUSSD = `*144*5*1*${amount}*12345%23`; // %23 = #
                window.location.href = `tel:${codeUSSD}`;
            }
        }
    </script>
</body>
</html>
