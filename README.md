# NDARA, site vitrine

Page unique, cinematique, pilotee par le defilement. HTML, CSS et JavaScript
simples. Aucun cadre logiciel, aucune etape de construction, aucun paquet a
installer : le dossier se sert tel quel.

## Ce que contient le dossier

```
index.html              la page entiere, styles et scripts compris
assets/hero-scrub.mp4   le plan de 2,6 s, une image cle toutes les 8 images
assets/hero-poster.jpg  la premiere image, affichee avant que la video arrive
assets/hero-ending.jpg  la derniere image, heros fixe du telephone et fond de fin
```

## Voir la page

Un double-clic sur `index.html` montre le heros fixe : les navigateurs
bloquent la lecture de fichiers locaux par le script, donc le repli s'affiche,
et c'est voulu. Pour voir le defilement qui pilote la video, il faut servir le
dossier :

```
python -m http.server 5190
```

puis ouvrir `http://localhost:5190/`.

## Ce qui a ete mesure

| Epreuve | Resultat |
|---|---|
| Erreurs dans la console | aucune, de 375 px a 1440 px |
| Contraste, pire pixel sous chaque texte | de 5,37 a 7,18 pour 1 |
| Rythme des bandes, test de la chiquenaude | 5 a 6 coups de molette par bande |
| Telephone | heros fixe compose, la video n'est jamais telechargee |
| Mouvement reduit | bascule dans les deux sens, en cours de session |
| Video absente | la page reste complete |
| Poids | 230 Ko sans la video, 1,4 Mo avec |

## Deux choses a remplacer avant la mise en ligne

Cherchez `DEPLOY STEP` dans `index.html` :

1. `og:url` et `og:image` attendent l'adresse absolue du site.
2. `DEMO_URL` attend l'adresse de la demonstration en direct.
