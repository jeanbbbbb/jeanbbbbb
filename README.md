- 👋 Hi, I’m @jeanbbbbb
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
jeanbbbbb/jeanbbbbb is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Compte à rebours du Nouvel An</title>
    <!-- Intégration de la feuille de style -->
    <style>body {
        margin: 0;
        padding: 0;
        font-family: 'Arial', sans-serif;
        background: linear-gradient(135deg, #1f1c2c, #928dab);
        color: #fff;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh; /* Permet au contenu de s'étendre au-delà de 100vh */
        overflow-y: auto; /* Active le défilement vertical si nécessaire */
     } 
     /* Conteneur principal */
     .container {
        max-width: 700px;
        padding: 20px;
        background: rgba(0, 0, 0, 0.5);
        border-radius: 15px;
     }
     /* Style du titre */
     h1 {
        font-size: 2em;
        margin-bottom: 20px;
     }
     /* Style du compte à rebours */
     p {
        font-size: 1.5em;
     }
     /* Style du message final */
     #finalMessage h2 {
        color: #ff9a9e;
        font-size: 2.5em;
        margin-bottom: 20px;
     }
     #finalMessage p {
        font-size: 1.2em;
        margin-top: 10px;
        line-height: 1.8;
     }
     /* Style pour les sous-titres du message */
     #finalMessage h3 {
        color: #ff9a9e;
        margin-top: 20px;
        font-size: 1.8em;
     }</style>
</head>
<body>
    <!-- Conteneur principal -->
    <div class="container">
        <!-- Titre -->
        <h1>Compte à rebours pour Ma Femme !</h1>
        <!-- Zone pour le compte à rebours -->
        <p id="countdown">Chargement du compte à rebours...</p>
        <!-- Zone pour le message final -->
        <div id="finalMessage" class="hidden"></div>
    </div>
    <script>// Sélection des éléments HTML
        const countdownElement = document.getElementById("countdown");
        const finalMessage = document.getElementById("finalMessage");
        
        // Définir la date cible : 1er janvier 2025 à 00:00:00
        const targetDate = new Date("2025-01-01T00:00:00").getTime();
        
        // Mettre à jour le compte à rebours toutes les secondes
        const interval = setInterval(() => {
            const now = new Date().getTime(); // Heure actuelle
            const difference = targetDate - now; // Temps restant
        
            // Si le compte à rebours est terminé
            if (difference <= 0) {
                clearInterval(interval);
        
                // Masquer le compte à rebours et afficher le message final
                countdownElement.style.display = "none";
                finalMessage.innerHTML = `
                    <h2>Bonne année 2025, mon amour Fayiza ❤️</h2>
                    <p>
                        "Le 1er décembre 2024, notre histoire a commencé, et depuis ce jour, ma vie a pris une tournure magique. Aujourd’hui, alors que 2025 commence, je ressens le besoin de te parler avec mon cœur, comme jamais auparavant."
                    </p>
                    <p>
                        Mon amour,  
                        Quand je pense à toi, je vois une lumière douce et rassurante, celle qui illumine mes journées, même les plus sombres. En seulement quelques semaines, tu as réussi à me montrer à quel point l’amour peut être puissant, sincère et transformateur. Être avec toi, c’est redécouvrir la beauté des petites choses : un sourire, une parole, un regard échangé même à distance.
                    </p>
                    <p>
                        En cette nuit de Nouvel An, alors que tout le monde célèbre l’avenir, moi, je veux célébrer <strong>nous</strong>. Car 2024 m’a offert le plus beau cadeau qu’on puisse recevoir : <em>toi</em>.
                    </p>
                    <h3>2025 : une promesse d’amour</h3>
                    <p>
                        Cette nouvelle année, je veux qu’elle soit à ton image : douce, lumineuse, pleine de rêves et de bonheur. Je promets d’être là, à chaque étape, pour te soutenir, pour te rassurer, pour t’aimer dans les bons comme les mauvais moments.
                    </p>
                    <h3>Un avenir avec toi</h3>
                    <p>
                        Fayiza, quand je regarde devant moi, je te vois. Toi, et tout ce que nous pourrions construire ensemble. Des souvenirs précieux, des projets fous, et surtout une histoire écrite à deux. Je ne veux rien de plus que t’aimer, te rendre heureuse, et être celui sur qui tu peux toujours compter.
                    </p>
                    <h3>Merci d’être toi</h3>
                    <p>
                        Merci pour ta patience, pour ta douceur, pour ta confiance. Merci de me montrer qu’aimer est une force, et non une faiblesse. Merci d’être toi, tout simplement, avec tes qualités qui me font fondre et tes petits défauts que j’adore aussi.
                    </p>
                    <p>
                        Fayiza, je t’aime. Je t’aime plus que les mots ne peuvent le dire. Et en 2025, je t’aimerai encore plus. Ensemble, faisons de cette année la plus belle de toutes.
                    </p>
                    <h2>Bonne année, mon cœur. ❤️</h2>
                    <p>
                        Merci d’être entrée dans ma vie. Tu es mon trésor, mon étoile, mon tout.  
                        Avec tout mon amour,  
                        <strong>Herman</strong>
                    </p>
                `;
                finalMessage.classList.add("show");
                return;
            }
        
            // Calcul des jours, heures, minutes et secondes restants
            const days = Math.floor(difference / (1000 * 60 * 60 * 24));
            const hours = Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((difference % (1000 * 60)) / 1000);
        
            // Afficher le compte à rebours formaté
            countdownElement.textContent = `${days} jours, ${hours} heures, ${minutes} minutes et ${seconds} secondes`;
        }, 1000);
        </script> 
</body>
</html>
