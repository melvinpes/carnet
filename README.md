# Carnet de Comptes

Une app gratuite de suivi de budget à installer sur le téléphone (Android et iPhone).
Les données restent **sur le téléphone de chaque personne** : aucun serveur, aucun compte, aucun frais.

Au premier lancement, un guide fait remplir l'essentiel étape par étape (revenus, dépenses, comptes). Chaque étape peut être passée et complétée plus tard ; le guide se relance depuis Réglages sans effacer ce qui est déjà saisi.

Trois choses dans l'app :
- **Budget** : on note ses revenus, ses dépenses obligatoires et sa vie courante prévue. L'app calcule combien on peut épargner chaque mois. Le budget se règle mois par mois : un changement s'applique à partir du mois choisi, les mois d'avant ne bougent pas. On peut aussi ajouter des dépenses ponctuelles (cadeaux, réparation…) pour un seul mois.
- **Bilan de fin de mois** : juste avant la paie, on met à jour le solde de chaque compte. L'épargne réelle = la variation du total entre deux bilans. Un bilan oublié se rattrape après coup (l'app le signale).
- **Patrimoine** : le total de tout son argent (comptes courants, livrets, placements), son évolution et le nombre de mois de dépenses couverts par l'épargne.
- **Crédits** (dans Patrimoine) : mensualités, paliers, capital restant dû et date de fin. Les mensualités s'ajoutent toutes seules au budget du bon mois, et le patrimoine net est calculé.

## Apparence

Version « Holographique » : thème sombre par défaut (clair si le téléphone est en mode clair), fond animé, carte irisée qui s'incline avec le téléphone, montants et graphiques animés. Si « Réduire les animations » est activé dans les réglages du téléphone, l'app reste immobile.

Si l'ancienne version est déjà en ligne : remplace simplement tous les fichiers du dépôt par ceux-ci. Les données de chacun sont conservées.

## Réglages utiles

- **Rappel de sauvegarde** : l'app propose une sauvegarde après chaque bilan et affiche un rappel si la dernière date de plus d'un mois.
- **Animations légères** : pour les téléphones plus anciens, coupe le flou, le fond animé et l'inclinaison de la carte.

## Mettre l'app en ligne (une seule fois, gratuit)

1. Crée un compte sur **github.com** (gratuit).
2. En haut à droite : **+** → **New repository**.
   - Nom : `carnet` (ou ce que tu veux).
   - Coche **Public**, puis **Create repository**.
3. Sur la page du dépôt, clique **uploading an existing file**.
   - Glisse **tous les fichiers de ce dossier** : index.html, manifest.webmanifest, sw.js et les 4 images .png.
   - Clique **Commit changes**.
4. Va dans **Settings** → **Pages**.
   - Dans *Branch*, choisis **main** et **/ (root)**, puis **Save**.
5. Attends 1 à 2 minutes. L'adresse de l'app s'affiche en haut de cette page.
   - Elle ressemble à `https://ton-pseudo.github.io/carnet/`.
   - C'est ce lien que tu envoies à ta famille.

## Installer l'app sur un téléphone

- **Android (Chrome)** : ouvre le lien, menu **⋮** → **Installer l'application** (ou « Ajouter à l'écran d'accueil »).
- **iPhone (Safari obligatoirement)** : ouvre le lien, bouton **Partager** → **Sur l'écran d'accueil**.

L'app a ensuite sa propre icône, s'ouvre en plein écran et fonctionne sans réseau.

## Bon à savoir

- Chacun a ses propres données : personne ne voit les comptes des autres.
- **Sauvegarde** : dans l'app, Réglages → *Exporter une sauvegarde*. Range le fichier sur Drive ou envoie-le-toi par mail. Pour récupérer tes données sur un nouveau téléphone : Réglages → *Restaurer depuis un fichier*.
- Si l'app est supprimée de l'écran d'accueil ou si les données du navigateur sont effacées, les données sont perdues. D'où l'intérêt de la sauvegarde.

## Mettre l'app à jour

1. Remplace `index.html` dans le dépôt GitHub (*Add file* → *Upload files*).
2. Dans `sw.js`, change `carnet-v1` en `carnet-v2` (puis v3, etc.).
3. Les téléphones reçoivent la nouvelle version à la prochaine ouverture avec du réseau. Les données ne sont pas touchées.

## Option : une vraie APK Android

Va sur **pwabuilder.com**, colle l'adresse de l'app, puis **Package for stores** → **Android**. Tu obtiens une APK gratuite à installer sur les téléphones Android.
