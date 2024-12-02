<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sami Design - Designer Web</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            color: #333;
            overflow-x: hidden;
            background: linear-gradient(to bottom, #ffffff, #f0f0f0);
        }

        header {
            background: linear-gradient(90deg, #0052cc, #ff5f5f, #ffffff);
            color: white;
            padding: 1.5rem 2rem;
            text-align: center;
            animation: fadeInDown 2s;
        }

        nav {
            display: flex;
            justify-content: center;
            background: linear-gradient(90deg, #0052cc, #ffffff, #ff5f5f);
            animation: slideInLeft 1.5s;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
        }

        nav a {
            color: rgb(0, 0, 0);
            text-decoration: none;
            padding: 1rem 1.5rem;
            font-weight: bold;
            transition: background-color 0.3s, color 0.3s;
        }

        nav a:hover {
            background-color: #ff5f5f;
            color: white;
            border-radius: 5px;
        }

        .hero {
            text-align: center;
            padding: 4rem 1rem;
            background: linear-gradient(90deg, #0052cc, #ff5f5f, #ffffff); 
                        url('hero-image.jpg') no-repeat center center/cover;
            color: white;
            animation: zoomIn 2s;
            border-bottom: 8px solid #0052cc;
        }

        .hero h1 {
            font-size: 4rem;
            margin: 0;
        }

        .hero p {
            font-size: 1.5rem;
            margin-top: 1.5rem;
            opacity: 0.9;
        }

        .tabs {
            display: flex;
            justify-content: center;
            margin: 3rem 0;
            animation: fadeIn 2s;
        }

        .tabs button {
            padding: 1rem 1.5rem;
            border: none;
            background: linear-gradient(90deg, #0052cc, #ff5f5f);
            color: white;
            margin: 0 0.5rem;
            cursor: pointer;
            border-radius: 8px;
            font-weight: bold;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .tabs button:hover {
            transform: scale(1.1);
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.3);
        }

        .tabs button.active {
            background: linear-gradient(90deg, #ffffff, #0052cc);
            color: white;
        }

        .tab-content {
            display: none;
            padding: 3rem;
            margin: 0 auto;
            max-width: 80%;
            background: rgb(255, 255, 255);
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
            border-radius: 12px;
            animation: fadeInUp 1.5s;
        }

        .tab-content.active {
            display: block;
        }

        footer {
            background: linear-gradient(90deg, #0052cc, #ff5f5f, #ffffff);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
            animation: fadeIn 2s;
            box-shadow: linear-gradient(90deg, #0052cc, #ff5f5f, #ffffff);
        }

        footer a {
            color: #ff5f5f;
            text-decoration: none;
            font-weight: bold;
        }

        footer a:hover {
            text-decoration: underline;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @keyframes slideInLeft {
            from { transform: translateX(-100%); }
            to { transform: translateX(0); }
        }

        @keyframes zoomIn {
            from { transform: scale(0.8); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const tabs = document.querySelectorAll('.tabs button');
            const contents = document.querySelectorAll('.tab-content');

            tabs.forEach((tab, index) => {
                tab.addEventListener('click', () => {
                    tabs.forEach(t => t.classList.remove('active'));
                    contents.forEach(c => c.classList.remove('active'));

                    tab.classList.add('active');
                    contents[index].classList.add('active');
                });
            });
        });
    </script>
</head>
<body>
    <header>
        <h1>Sami Design</h1>
        <p>Designer Web : Sites Internet, Affiches, Montages et Gestion de Pages</p>
    </header>

    <nav>
        <a href="#portfolio">Portfolio</a>
        <a href="#contact">Contact</a>
    </nav>

    <section class="hero">
        <h1>Créez votre univers numérique unique</h1>
        <p>Avec Sami Design, donnez vie à vos idées grâce à des créations web et graphiques sur mesure.</p>
    </section>

    <div class="tabs">
        <button class="active">Sites Internet</button>
        <button>Affiches</button>
        <button>Montages</button>
        <button>Gestion de Pages</button>
    </div>

    <div class="tab-content active">
        <h2>Création de Sites Internet</h2>
        <p>Des sites modernes, responsives et adaptés à vos besoins.</p>
        <img src="web-design.jpg" alt="Web Design" style="width:100%; border-radius: 12px;">
    </div>

    <div class="tab-content">
        <h2>Design d'Affiches</h2>
        <p>Des affiches uniques pour vos événements et campagnes.</p>
        <img src="poster-design.jpg" alt="Affiches" style="width:100%; border-radius: 12px;">
    </div>

    <div class="tab-content">
        <h2>Montages Graphiques</h2>
        <p>Des montages créatifs pour donner vie à vos projets.</p>
        <img src="montage.jpg" alt="Montage" style="width:100%; border-radius: 12px;">
    </div>

    <div class="tab-content">
        <h2>Gestion de Pages Web</h2>
        <p>Optimisez et animez vos pages avec une expertise dédiée.</p>
        <img src="social-media.jpg" alt="Gestion de Pages" style="width:100%; border-radius: 12px;">
    </div>

    <footer>
        <p>&copy; 2024 Sami Design. Tous droits réservés. | <a href="#">Mentions Légales</a></p>
    </footer>
</body>
</html>
