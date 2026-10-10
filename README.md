# Suites & Défis

Entraînement aux suites logiques pour enfants (timer, sons, badges, progression).

## Structure du dépôt

```
index.html            ← l'application
semaines/
  2026-10-12.json     ← un fichier par semaine, nommé avec la date du LUNDI
  2026-10-19.json
```

## Mise en ligne (une seule fois)

1. Crée un dépôt **public** sur GitHub, ajoute `index.html` et le dossier `semaines/`.
2. Settings → Pages → Source : *Deploy from a branch* → branche `main`, dossier `/ (root)`.
3. L'app est disponible sur `https://<ton-compte>.github.io/<nom-du-dépôt>/`.

## Chaque semaine

1. Ouvre l'onglet **Préparer la semaine**, colle le texte du chatbot (plusieurs sessions), choisis le lundi, télécharge le fichier.
2. Upload-le dans `semaines/` sur GitHub (Add file → Upload files → Commit).
3. Compte 1 à 2 minutes, puis rafraîchis la page de l'app.

## Format d'un fichier de semaine

```json
{
  "semaine": "2026-10-12",
  "sessions": [
    {
      "titre": "Session 1 — Débutant",
      "jour": "2026-10-12",
      "temps": 30,
      "suites": [
        { "suite": "2 – 4 – 6 – 8 – ?", "reponse": "10", "regle": "+2" }
      ]
    }
  ]
}
```

- `jour` : date de la session (les jours à venir sont verrouillés). Optionnel.
- `temps` : secondes par question. Optionnel (30 par défaut).
- `regle` : optionnelle, affichée à l'enfant seulement s'il se trompe.
- `reponse` et `regle` peuvent être encodées avec le préfixe `b64:` (option du convertisseur).
