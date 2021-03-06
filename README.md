# oBlog POO

Actuellement, oBlog affiche des données écrites « en dur » dans le code HTML. On souhaite rendre tout ça dynamique, c'est-à-dire que les articles ne devraient pas être écrits directement dans index.html, mais plutôt venir d'une source d'information séparée. Du code PHP s'occuperait d'injecter les derniers articles en date dans un template HTML :ok_hand:

Du coup… on va un peu structurer les données coté article, pour préparer le terrain :tada:

> Dans cet exercice, on abandonne temporairement l'idée d'une belle intégration HTML/CSS, pour se concentrer sur la programmation orientée-objet en PHP => on va travailler en noir & blanc, puis on reviendra plus tard dans oBlog !

## Une classe pour les articles

Le code du fichier index.php fourni dans ce repo permet de tester le bon fonctionnement d'une classe `Article`, qu'il va falloir écrire :thinking:

### Étapes d'implémentation

- Comme indiqué en commentaire dans index.php, définir une classe `Article` (dans index.php, ou dans un fichier dédié à inclure dans index.php, au choix).
- Définir les propriétés de cette classe (indice : lire & analyser le code de `index.php` en entier, ça peut vous aider à déterminer quelles propriétés sont requises).
- À plusieurs endroits dans index.php, il manque du code pour utiliser la classe `Article`. Compléter les blancs et tester que tout fonctionne comme prévu !

### Bonus

Créer une _méthode_ `getDateFr()` (rappel : méthode == propriété-fonction définie dans une classe) qui retourne la date au format `dd/mm/yyyy` (soit pour le 13 juillet 2017 => `"13/07/2017"`).

On partira du principe que la date fournie dans un objet `Article` est toujours au format `yyyy-mm-dd`, comme c'est le cas dans index.php.

### Super-bonus

Ajouter une méthode `getDate($lang)` réalisant le même travail que `getDateFr`, mais pour plusieurs formats d'affichage (par exemple, anglais et français, avec anglais par défaut). Modifier `getDateFr` pour qu'elle délègue son travail à `getDate`.
