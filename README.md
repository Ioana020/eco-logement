EISE4 TP IoT - Logement éco-responsable

Description du projet
Ce projet a pour objectif de créer une application internet permettant aux utilisateurs de visualiser leur consommation (électricité, eau, etc.), de voir les économies réalisées, d'afficher l'état des capteurs, et de configurer les capteurs liés à leur logement éco-responsable.

---

#Contenu du projet


Base de données : logement.sql
Ce fichier contient toutes les commandes SQL pour :
- Détruire les tables existantes.
- Créer les tables pour modéliser un logement éco-responsable.
- Ajouter des logements, des pièces, des capteurs, des types de capteurs, des mesures et des factures.


Fichier Python : remplissage.py
Ce fichier permet d'ajouter des mesures et des factures à la base de données logement.db.


Serveur REST : serveurREST.py



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




--------

Instructions d'utilisation



## Dépendances utilisées dans le projet:

- FastAPI : Utilisée pour créer et gérer l’API du projet.
- HTMLResponse : permet de retourner des pages HTML en réponse aux requêtes.
- Pydantic : Utilisée pour valider les données des requêtes entrantes.
- sqlite3 : Permet de gérer la base de données SQLite pour stocker les données du projet.
- typing : Utilisée pour définir les types de données, comme les listes dans les réponses.
- os : Permet de vérifier ou gérer des fichiers dans le système.
- httpx : Utilisée pour effectuer des requêtes HTTP vers des API externes.
- StaticFiles : Permet de servir des fichiers statiques, comme le CSS et le JavaScript.




## 1ERE ETAPE: INITIALISATION DE LA BASE DE DONNEES:


- Télécharger SQLite : https://www.sqlite.org/download.html

- Une fois SQLite installé, ouvrez un terminal et initialisez la base de données en utilisant la commande :

				sqlite3 logement.db


- Dans le même terminal, charger les tables depuis le fichier logement.sql :
				
				.read logement.sql



## 2EME ETAPE : LANCER LE SERVEUR

1. Python 3.8 doit être installé pour faire fonctionner le serveur. 
2. Créer un environnement virtuel (tutoriel : https://fastapi.tiangolo.com/tutorial/#run-the-code)
		
3. Une fois l’environnement virtuel activé, installez les bibliothèques nécessaires :
				bash: 
				pip install fastapi uvicorn httpx

4. Lancer le serveur: 
				bash: 
				fastapi dev serveurREST.py




----

# Navigation dans le site :

Une fois le serveur lancé, nous pouvons naviguer facilement sur le site web créé. 


Page d'accueil (index.html) : Accédez à la page d'accueil via http://127.0.0.1:8000/
Pages fonctionnelles :
- Consommation : http://127.0.0.1:8000/consommation/chart
- État des capteurs : http://127.0.0.1:8000/mesures/view
- Comparatifs économiques : http://127.0.0.1:8000/economies/comparison
- Configuration : http://127.0.0.1:8000/configuration

---

# Fonctionnalités du site web

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

