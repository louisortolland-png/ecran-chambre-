# Écran chambre

Un écran d'infos pour une vieille tablette Samsung posée en paysage :
heure, météo à Thônes, to-do, échéances d'études, Bitcoin et compte à rebours Thaïlande.

**Adresse du site : https://louisortolland-png.github.io/ecran-chambre-/**

Tout est dans un seul fichier : `index.html`.

---

## 1. Mettre le site en ligne (une seule fois)

1. Sur GitHub, ouvre le dépôt `ecran-chambre-`.
2. Clique sur **Settings** (en haut), puis **Pages** (menu de gauche).
3. Dans **Build and deployment** → **Source**, choisis **Deploy from a branch**.
4. Dans **Branch**, choisis **main** et **/ (root)**, puis **Save**.
5. Attends 1 à 2 minutes : l'adresse ci-dessus fonctionne.

À chaque modification de `index.html` sur la branche `main`, le site se met à jour tout seul
(la tablette récupère la nouvelle version pendant la nuit, vers 3 h 30).

## 2. Installer sur la tablette

1. Ouvre **Chrome** sur la tablette (mets-le à jour depuis le Play Store si possible).
2. Va à l'adresse : `https://louisortolland-png.github.io/ecran-chambre-/`
3. Appuie sur le menu **⋮** (en haut à droite) → **Ajouter à l'écran d'accueil** → **Ajouter**.
4. Lance l'écran depuis la nouvelle icône : il s'ouvre en plein écran, sans barre d'adresse.
5. Pose la tablette en **paysage**.

> Si la météo ou le Bitcoin restent vides alors qu'internet marche, c'est souvent que le
> navigateur est trop ancien pour les certificats de sécurité actuels. Installe alors
> **Firefox** depuis le Play Store et fais la même manip (menu → **Installer** ou
> **Ajouter à l'écran d'accueil**).

## 3. Empêcher l'écran de se mettre en veille

Laisse la tablette **branchée sur son chargeur**, puis :

1. **Activer le mode développeur** : *Paramètres* → *À propos de l'appareil*
   (ou *À propos de la tablette* → *Infos logiciel*) → touche **7 fois** sur **Numéro de version**.
   Un message dit « Le mode développeur a été activé ».
2. Reviens dans *Paramètres* → **Options de développement**.
3. Active **Rester activé** (« L'écran ne se met jamais en veille pendant le chargement »).

En plus (conseillé) : *Paramètres* → *Affichage* → **Mise en veille de l'écran** → durée maximale.

Astuce : baisse la luminosité au minimum le soir, et utilise le **mode nuit** (voir plus bas).

## 4. Utilisation

| Carte | Ce qu'on peut faire |
|---|---|
| Heure | Bouton **lune** en haut à droite : mode nuit (seulement l'heure, en gris foncé). Touche l'écran n'importe où pour en sortir. |
| Météo | Mise à jour toutes les 15 min. |
| À faire | **+** pour ajouter, touche le rond pour cocher (la tâche se barre), **×** pour supprimer. |
| Études | **+** pour ajouter une échéance (nom + date). Affiche « J-12 », en orange à moins de 7 jours, en rouge à moins de 2 jours. **×** pour supprimer. |
| Bitcoin | Prix en euros, variation 24 h, courbe sur 7 jours. Mise à jour toutes les 2 min. |
| Thaïlande | Jours restants avant le départ. Roue dentée pour changer la date. |

- Les tâches, échéances et la date du voyage sont gardées **dans la tablette** (elles ne
  disparaissent pas si on éteint).
- Si internet coupe, l'écran garde les dernières valeurs et affiche « Mis à jour à HH:MM · hors ligne ».
- La page se recharge toute seule chaque nuit vers 3 h 30 (seulement si internet marche).
