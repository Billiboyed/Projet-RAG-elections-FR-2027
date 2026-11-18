# Projet RAG - Élections FR 2027

Assistant de synthèse des programmes électoraux français : pose une question sur une thématique (pouvoir d'achat, énergie, sécurité, immigration, retraites...), obtiens une synthèse comparative par candidat, avec citations vers les passages sources des programmes.

## Objectif

Démontrer une architecture RAG complète et production-like :

- **Ingestion** : parsing des PDF de programmes, chunking par section thématique, métadonnées (candidat, date, version, source)
- **Indexation** : embeddings via API Mistral AI, stockage PostgreSQL + pgvector
- **Retrieval** : hybride (dense + BM25), filtrable par candidat et thématique
- **Génération** : synthèse avec citations obligatoires vers les passages sources
- **Updates automatisées** : scraping planifié, détection de changement, re-indexation incrémentale
- **Évaluation** : jeu de questions-réponses de référence, métrique de fidélité (groundedness), garde-fous hors-périmètre

## Stack

| Brique | Choix | Justification |
|---|---|---|
| Langage | Python | Écosystème IA, rapidité d'itération |
| Orchestration RAG | LlamaIndex / LangChain | Code visible et versionnable, migration facile |
| LLM + embeddings | API Mistral AI | Coût quasi nul à cette volumétrie, acteur français cohérent avec le sujet |
| Base vectorielle | PostgreSQL + pgvector | Une seule brique d'infra, migration triviale vers Qdrant si besoin |
| Front | Streamlit | Minimum syndical pour la démo |
| Run | Docker Compose, GitHub Actions | Reproductible, CI pour tests et évaluation |

## Structure du projet

```
data/raw        Programmes PDF sources (versionnés statiquement)
data/processed Chunks et métadonnées générés
src/ingestion   Parsing, chunking, embeddings, stockage
src/retrieval   Recherche hybride, filtres
src/rag         Chaîne de génération, prompts, citations
src/evaluation  Jeu de QA de référence, métriques, garde-fous
src/scraping    Scraper planifié, détection de changement
frontend        Application Streamlit
infra           Docker Compose, configuration
docs            Architecture, décisions, résultats d'évaluation
```

## Statut

 :construction: Projet en cours. MVP en 12-14 semaines, démarré en novembre 2026.

- Corpus initial : programmes des présidentielles 2022 (les programmes 2027 n'existent pas encore au démarrage)
- 5-6 candidats majeurs, 4-5 thématiques clés

Le README sera enrichi au fil de l'avancement : architecture détaillée, résultats d'évaluation, démo.
