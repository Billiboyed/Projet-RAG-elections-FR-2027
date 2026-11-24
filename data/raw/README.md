# Données brutes (`data/raw`)

Programmes et déclarations de patrimoine des principaux candidats à l'élection
présidentielle française de 2022. Ces PDF sont **statiques et versionnés** :
ils constituent le jeu de données figé de référence du projet RAG.

## Convention de nommage

`<Prenom>-<Nom>-<Type>.pdf` avec `<Type>` valant `Programme` ou `Declaration`.
Le nom du candidat est en ASCII (sans accents), les espaces remplacées par des
 tirets. Exemple : `Anne-Hidalgo-Programme.pdf`.

## Inventaire

| Fichier | Candidat | Type | Source | Date de collecte |
|---|---|---|---|---|
| `Anne-Hidalgo-Programme.pdf` | Anne Hidalgo | Programme | Site officiel du candidat | 2026-11-20 |
| `Anne-Hidalgo-Declaration.pdf` | Anne Hidalgo | Déclaration de patrimoine | Site officiel du candidat | 2026-11-20 |
| `Emmanuel-Macron-Programme.pdf` | Emmanuel Macron | Programme | Site officiel du candidat | 2026-11-19 |
| `Eric-Zemmour-Programme.pdf` | Éric Zemmour | Programme | Site officiel du candidat | 2026-11-20 |
| `Eric-Zemmour-Declaration.pdf` | Éric Zemmour | Déclaration de patrimoine | Site officiel du candidat | 2026-11-20 |
| `Jean-Luc-Melenchon-Programme.pdf` | Jean-Luc Mélenchon | Programme | Site officiel du candidat | 2026-11-22 |
| `Marine-Le-Pen-Programme.pdf` | Marine Le Pen | Programme | Site officiel du candidat | 2026-11-19 |
| `Nathalie-Arthaud-Programme.pdf` | Nathalie Arthaud | Programme | Site officiel du candidat | 2026-11-20 |
| `Nathalie-Arthaud-Declaration.pdf` | Nathalie Arthaud | Déclaration de patrimoine | Site officiel du candidat | 2026-11-20 |
| `Nicolas-Dupont-Aignan-Programme.pdf` | Nicolas Dupont-Aignan | Programme | Site officiel du candidat | 2026-11-20 |
| `Philippe-Poutou-Programme.pdf` | Philippe Poutou | Programme | Site officiel du candidat | 2026-11-20 |
| `Philippe-Poutou-Declaration.pdf` | Philippe Poutou | Déclaration de patrimoine | Site officiel du candidat | 2026-11-20 |
| `Yannick-Jadot-Programme.pdf` | Yannick Jadot | Programme | Site officiel du candidat | 2026-11-20 |
| `Yannick-Jadot-Declaration.pdf` | Yannick Jadot | Déclaration de patrimoine | Site officiel du candidat | 2026-11-20 |

## Notes

- **Provenance** : documents publics, téléchargés manuellement depuis les sites
  officiels des candidats (ou leur équivalent archivé) en vue d'un usage de
  recherche / démonstration.
- **Intégrité** : en cas de mise à jour d'un fichier, conserver l'ancien
  historique via git et renseigner la nouvelle date de collecte dans ce README.
- **Périmètre** : programmes 2022 de 8 candidats majeurs (+ déclarations de
  patrimoine pour 5 d'entre eux). Les données `data/processed` (résultats de
  parsing, chunks, embeddings) sont ignorées par git.
