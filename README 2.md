# Écran chambre

Un écran d'infos pour une vieille tablette Samsung posée en paysage :
heure, météo à Thônes, to-do, actualités, PEA et compte à rebours Thaïlande.

**Adresse du site : https://louisortolland-png.github.io/ecran-chambre-/**

Le site, c'est le fichier `index.html`. À côté, `manifest.json` et les icônes `icon-192.png`
et `icon-512.png` permettent de l'ouvrir en plein écran, sans barre de navigateur.

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
   Si une barre reste visible en haut, supprime l'icône, recharge la page dans Chrome et
   refais l'ajout. En secours, toucher l'écran une fois le passe en plein écran.
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
| Actualités | Les derniers titres de franceinfo, du plus récent au plus ancien. Mise à jour toutes les 15 min. On peut faire défiler la liste du doigt. |
| PEA | Valeur totale, variation du jour, plus-value, courbe sur 1 mois et détail par ligne. Cours mis à jour toutes les 2 min quand la Bourse est ouverte (30 min sinon), avec quelques minutes de retard. |
| Thaïlande | Jours restants avant le départ. Roue dentée pour changer la date. |

- Les tâches et la date du voyage sont gardées **dans la tablette** (elles ne
  disparaissent pas si on éteint).
- Si internet coupe, l'écran garde les dernières valeurs et affiche « Mis à jour à HH:MM · hors ligne ».
- La page se recharge toute seule chaque nuit vers 3 h 30 (seulement si internet marche).

## 5. Mettre à jour le PEA

Les lignes du PEA sont écrites dans `index.html`, dans le bloc `var PEA = { ... }`
(cherche « MON PEA »). Pour chaque ligne : le nombre de parts (`quantite`) et le prix de
revient (`prixMoyen`), comme affichés dans l'appli Boursorama. `especes` = l'argent non investi.

Après un achat ou une vente : modifie ces chiffres (ou demande à Claude), puis renvoie
`index.html` sur GitHub. La tablette se met à jour dans la nuit, ou tout de suite si tu
recharges la page.

Attention : le dépôt est public, donc ces chiffres sont visibles par quelqu'un qui irait voir le code.
