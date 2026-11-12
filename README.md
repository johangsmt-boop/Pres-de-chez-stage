# Près de chez stage

Site web pour aider les étudiants à trouver un stage près de chez eux : une carte, un annuaire d'entreprises et un formulaire pour en ajouter.

Projet de BTS SIO SLAM, réalisé par Johan et Terry.

## Structure du projet

| Fichier | Rôle |
|---|---|
| `pres de ches stage.html` | Page d'accueil : carte Google Maps, tableau de l'annuaire, formulaire d'ajout d'entreprise, footer |
| `pres de chez stage.css` | Styles de la page d'accueil (grille 2 colonnes, tableau, formulaire, nav, footer, version mobile) |
| `Maps.html` | Page « Maps » : carte + tableau des entreprises |
| `Maps.css` | Styles de la page Maps (nav, iframe, tableau) |
| `login.html` | Page de connexion (username + password) |
| `login.css` | Styles de la page de connexion (fond vert, carte « glass », champs arrondis) |
| `chatbot.html` | Démo autonome d'un chatbot (HTML + CSS + JS), répond avec des mots-clés, sans IA |
| `logo.png` | Logo « Près de chez stage », utilisé dans la barre de navigation |
| `maquette.DNG` | Maquette du site |

> Les pages `annuaire.html` et `formulaire.html` sont dans le menu, mais ne font pas partie des fichiers fournis.

## Navigation

Le menu est commun à toutes les pages : Accueil, Maps, Annuaire, Formulaire, Login.

## Le chatbot

`chatbot.html` est un exemple complet : bulle en bas à droite, fenêtre de chat, réponses par mots-clés (`bonjour`, `contact`, `prix`).

Pour l'intégrer au site, deux possibilités :

1. **Copier le code** de `chatbot.html` (le `<style>`, le bloc HTML et le `<script>`) dans la page voulue.
2. **Utiliser un service** (Tidio, par exemple) : coller le script fourni avant `</body>`.

```html
<script src="//code.tidio.co/TON_CODE.js" async></script>
```

## À corriger / à faire

- **Deux versions de la page d'accueil** : `pres_de_ches_stage.html` et une « conflicted copy » créée par la synchronisation (Dropbox, OneDrive...). Elles ne diffèrent que par le script du chatbot. Garder une seule version et supprimer l'autre.
- **Scripts de chatbot à remplacer** : `TON_CODE` (Tidio) et `VOTRE_ID_CHATBOT` sont des valeurs d'exemple, le chatbot ne s'affichera pas tant qu'elles ne sont pas remplacées.
- **Texte parasite** : le mot `kiki` après `</html>` dans la copie en conflit.
- **Faute dans le nom** : `pres de ches stage.html` (« ches » au lieu de « chez »). Les liens du menu utilisent ce nom, donc il faut les modifier en même temps que le fichier. Éviter aussi les espaces dans les noms de fichiers.
- **`Maps.html`** : le `<header>` est placé en dehors du `<body>`, `lang="en"` à passer en `fr`, et le texte « This is the Maps page. » est à traduire. `Maps.css` n'a aucun style pour le footer.
- **Carte** : l'iframe est centrée sur la Tour Eiffel (exemple), à remplacer par ta zone.
- **Formulaires** : ni le formulaire d'ajout ni la connexion n'envoient rien pour l'instant (pas d'`action`, pas de backend).
- **`login.css`** : la règle `.field input:focus` est écrite deux fois, à fusionner.
- **Année du footer** : `© 2023`, à mettre à jour.

## Lancer le projet

Aucune installation : ouvrir `pres de ches stage.html` dans un navigateur. Garder tous les fichiers dans le même dossier (même `logo.png`), sinon les styles et l'image ne se chargent pas.

git clone https://github.com/TON_PSEUDO/TON_REPO.git
cd TON_REPO

git pull

git add .
git commit -m
git push

git checkout -b ajout-chatbot
git push -u origin ajout-chatbot
