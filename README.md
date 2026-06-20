# 🎻 Violon à l'oreille

Petite application web pour entraîner son oreille au violon : une note (ou un
intervalle) est jouée, et tu dois la reconnaître.

## Lancer

Aucune installation, aucune dépendance. Ouvre simplement le fichier dans un
navigateur :

```bash
xdg-open index.html      # ou double-clic sur index.html
```

Tout est dans un seul fichier `index.html` et fonctionne **hors-ligne**.
🎧 Un casque est recommandé pour bien juger les hauteurs.

## Modes

- **Nommer la note** — une note est jouée, tu cliques son nom (Do, Ré, Mi…).
  Entraîne l'oreille absolue / le repérage sur le manche.
- **Reconnaître l'intervalle** — une note de référence puis une cible sont
  jouées, tu identifies l'intervalle (3ce Maj, 5te juste…).

## Étendue des notes

- **Cordes à vide** — Sol3, Ré4, La4, Mi5
- **1re position** — Sol3 → Si5
- **Complète** — toute la tessiture du violon (Sol3 → La7)

## Comment ça marche

Le son est **synthétisé** en direct avec la Web Audio API (oscillateurs
sawtooth désaccordés + filtre passe-bas + formant + vibrato + enveloppe
d'archet) — pas de fichiers audio à télécharger.
