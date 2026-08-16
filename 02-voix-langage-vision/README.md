# Phase 2 — Spécialisation Voix, Langage & Vision (Mois 3-4)

**Objectif :** développer des briques IA adaptées à l'accessibilité (oralité, langues locales, handicap).

## Sous-dossiers
- `nlp/` — tokenization, embeddings, fine-tuning (BERT, Llama/Mistral, Hugging Face `transformers`), langues peu dotées
- `speech/` — STT (Whisper), TTS (Coqui, VITS)
- `vision/` — détection d'objets, OCR (YOLO, OpenCV, MediaPipe, Tesseract)
- `projets/` — projet étape versionné

## Cours recommandés
Voir [`ressources/cours/README.md`](../ressources/cours/README.md#phase-2--voix-langage--vision)

## Projet étape
Pipeline capable de transcrire de l'audio dans une langue/accent spécifique et de synthétiser la réponse sous forme vocale.

## Critères de réussite
- WER mesuré sur un échantillon réel
- Pipeline STT → traitement → TTS fonctionnel de bout en bout
