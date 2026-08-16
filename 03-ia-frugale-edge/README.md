# Phase 3 — IA Frugale & Embarquée / Edge AI (Mois 5-6)

**Objectif :** rendre les modèles exécutables hors-ligne ou sur des appareils mobiles bas de gamme.

## Sous-dossiers
- `quantification/` — quantification (FLOAT32 → INT8/INT4), distillation, pruning
- `on-device/` — LiteRT (TF Lite), ONNX Runtime, `llama.cpp`, conversion mobile/web
- `projets/` — projet étape versionné (inclut architecture API légère : FastAPI/Node.js/Spring Boot, offline-first)

## Cours recommandés
Voir [`ressources/cours/README.md`](../ressources/cours/README.md#phase-3--ia-frugale--edge-ai)

## Projet étape
Embarquer un modèle de STT/TTS quantifié dans une application locale sans connexion Internet.

## Critères de réussite
- Taille du modèle réduite mesurée (avant/après)
- Latence d'inférence acceptable sur matériel bas de gamme
- Fonctionne 100% hors-ligne
