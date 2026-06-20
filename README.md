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

- **Sur le manche** *(par défaut)* — une note est jouée, tu cliques sa position
  sur le manche du violon (corde à vide ou position de doigt). Une même note
  peut se jouer à plusieurs endroits (ex. *La* = corde La à vide **ou** position
  haute sur la corde Ré) : toutes les positions correctes sont acceptées.
  Case **« Afficher les noms »** pour s'aider au début.
- **Nommer** — une note est jouée, tu cliques son nom (Do, Ré, Mi…).
- **Intervalle** — une note de référence puis une cible sont jouées, tu
  identifies l'intervalle (3ce Maj, 5te juste…).
- **Gammes** *(écoute, pas un jeu)* — choisis une tonique (Do, Ré… Sol) et
  majeur/mineur : les notes de la gamme s'affichent sur le manche (tonique
  cerclée de blanc) et se jouent une à une (montante puis descendante) avec
  ▶, chaque note s'animant au passage.

## Étendue des notes

- **Cordes à vide** — Sol3, Ré4, La4, Mi5
- **1re position** — Sol3 → Si5
- **Complète** — toute la tessiture du violon (Sol3 → La7)

## Comment ça marche

Le son est **synthétisé** en direct avec la Web Audio API (oscillateurs
sawtooth désaccordés + filtre passe-bas + formant + vibrato + enveloppe
d'archet) — pas de fichiers audio à télécharger.
