EISE4 TP IoT - Logement éco-responsable

Description du projet
Ce projet a pour objectif de créer une application internet permettant aux utilisateurs de visualiser leur consommation (électricité, eau, etc.), de voir les économies réalisées, d'afficher l'état des capteurs, et de configurer les capteurs liés à leur logement éco-responsable.

---

Contenu du projet

Base de données : logement.sql
Ce fichier contient toutes les commandes SQL pour :
- Détruire les tables existantes.
- Créer les tables pour modéliser un logement éco-responsable.
- Ajouter des logements, des pièces, des capteurs, des types de capteurs, des mesures et des factures.





Commandes pour initialiser la base de données :
$ sqlite3 logement.db
sqlite> .read logement.sql





Fichier Python : remplissage.py
Ce fichier permet d'ajouter des mesures et des factures à la base de données logement.db.
Exécution :
$ python remplissage.py





Serveur REST : serveurREST.py

Ce fichier constitue le serveur construit avec FastAPI. Il permet :
- De consulter et d'ajouter des mesures et des factures.
- D'afficher des graphiques et des tableaux basés sur les données de la base de données.
- D'obtenir des prévisions météo via une API externe.



---

Structure du site web
Le site est contenu dans le répertoire WEBSITE et se compose des fichiers suivants :

Dossiers et fichiers :
1. CSS
   - styles.css : Contient le style du site.
2. HTML
   - index.html : Page d'accueil.
   - navbar.html : Barre de navigation incluse dans toutes les pages.
   - home.html : Page principale de gestion.
3. JS
   - Scripts JavaScript pour les interactions dynamiques.
4. Images
   - Contient les fichiers d'image utilisés dans le site.

Pages web :
1. Consommation : Affiche des graphiques de consommation (électricité, eau, déchets) selon des échelles de temps.
2. État des capteurs : Montre les informations des capteurs installés dans les pièces du logement.
3. Comparatifs économiques : Présente les économies réalisées sous forme de graphiques.
4. Configuration : Permet d'ajouter de nouveaux capteurs à la base de données.

---

Instructions d'utilisation

1. Initialisation de la base de données :
Exécutez les commandes suivantes :
$ sqlite3 logement.db
sqlite> .read logement.sql
($ python remplissage.py)



2. Navigation dans le site :
Page d'accueil (index.html) : Accédez à la page d'accueil via http://127.0.0.1:5500/WEBSITE/index.html
Pages fonctionnelles :
- Consommation : http://127.0.0.1:8000/consommation/chart
- État des capteurs : http://127.0.0.1:8000/mesures/view
- Comparatifs économiques : http://127.0.0.1:8000/economies/comparison
- Configuration : http://127.0.0.1:8000/configuration

---

Fonctionnalités du site web

1. Visualisation de la consommation :
   - Affiche des graphiques de consommation énergétique (électricité, eau, déchets) basés sur les données réelles de la base de données.
   - Possibilité de filtrer par adresse et échelle de temps (mois ou année).

2. État des capteurs :
   - Liste les capteurs installés dans chaque pièce, avec leur type, leurs valeurs mesurées et leur emplacement.

3. Comparatifs économiques :
   - Présente les économies réalisées sous forme de graphiques interactifs.
   - Les données peuvent être filtrées par adresse et période.

4. Configuration :
   - Permet d'ajouter de nouveaux capteurs, en spécifiant leur type, référence commerciale, port de communication, et la pièce associée.

---


IOANA CACAU

