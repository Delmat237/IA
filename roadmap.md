# Roadmap — IA à impact sociétal (Accessibilité, Voix, Edge AI)

Feuille de route progressive en **5 phases** , pensée pour aller de la théorie jusqu'au déploiement d'applications IA à fort impact sociétal (accessibilité, langues peu dotées, usage hors-ligne).

> Structure de dossiers correspondante créée dans ce répertoire — voir section [Arborescence du projet](#arborescence-du-projet) en fin de document.

---

### **Phase 0 : Setup & Environnement (Semaine 0)**

*Objectif : Avoir un environnement de travail reproductible avant de coder quoi que ce soit.*

* **Environnement Python :** `pyenv`/`conda`, environnements virtuels, gestion de dépendances (`uv` ou `poetry`).
* **Contrôle de version :** Git + dépôt distant (GitHub/GitLab), convention de commits.
* **Calcul :** accès GPU (Google Colab / Kaggle Notebooks gratuits, ou local si dispo), vérification CUDA/PyTorch.
* **Outils :** Jupyter/VS Code, Docker (pour reproductibilité future en Phase 3-4).
* **Livrable :** dépôt initialisé, environnement `01-fondations` fonctionnel, un notebook "hello world" qui entraîne un modèle jouet sur GPU.

---

### **Phase 1 : Fondations Data & Deep Learning (Mois 1 - 2)**

*Objectif : Maîtriser le pipeline complet de machine learning et deep learning en Python.*

* **Mathématiques appliquées :** Vectorisation, calcul matriciel, métriques de performance (F1-score, WER pour l'audio, BLEU pour le texte).
* **Machine Learning classique :** Manipulation de données (`pandas`, `numpy`) et modèles de base (`scikit-learn`).
* **Deep Learning avec PyTorch :**
  * Réseaux de neurones denses (MLP).
  * Réseaux convolutionnels (CNN) pour la vision.
  * Réseaux séquentiels et introduction aux **Transformers**.
* **Bonnes pratiques dès le départ :** versionnage des expériences (`MLflow` ou simple CSV de suivi), séparation train/val/test rigoureuse, seed fixe pour la reproductibilité.
* **Projet étape :** Construire un classifieur de données tabulaires ou d'images simple et évaluer ses biais sur différents sous-groupes de données.
* **Critères de réussite :** modèle qui bat une baseline naïve, matrice de confusion analysée par sous-groupe, code versionné et documenté.

---

### **Phase 2 : Spécialisation Voix, Langage & Vision (Mois 3 - 4)**

*Objectif : Développer des briques IA adaptées à l'accessibilité (oralité, langues locales, handicap).*

* **Traitement du Langage Naturel (NLP) :**
  * Tokenization, embeddings vectoriels, *Fine-Tuning* de modèles de langue (BERT, Llama/Mistral) avec la bibliothèque `transformers` de Hugging Face.
  * Gestion de jeux de données pour les **langues peu dotées** (*low-resource languages*) — ex. Common Voice pour langues africaines/locales.
* **Traitement de l'Audio & Speech :**
  * Reconnaissance automatique de la parole (STT) avec des architectures comme **Whisper**.
  * Synthèse vocale (TTS) pour restituer du texte sous forme orale (Coqui TTS, VITS).
* **Computer Vision & Accessibilité :**
  * Détection d'objets et OCR pour la description de scènes ou de documents aux malvoyants (YOLO, OpenCV, MediaPipe, Tesseract).
* **Projet étape :** Créer un pipeline capable de transcrire de l'audio dans une langue/accent spécifique et de synthétiser la réponse sous forme vocale.
* **Critères de réussite :** WER mesuré sur un échantillon réel, pipeline STT→traitement→TTS fonctionnel de bout en bout.

---

### **Phase 3 : IA Frugale & Embarquée / Edge AI (Mois 5 - 6)**

*Objectif : Rendre les modèles exécutables hors-ligne ou sur des appareils mobiles bas de gamme.*

* **Techniques de Compression de Modèles :**
  * **Quantification** (passer de FLOAT32 à INT8/INT4).
  * Distillation de connaissances (entraîner un petit modèle « élève » à partir d'un grand modèle « maître »).
  * Pruning (élagage de poids) comme technique complémentaire.
* **Frameworks d'Exécution sur Appareil (On-Device) :**
  * Prise en main de **LiteRT** (TensorFlow Lite), **ONNX Runtime** et `llama.cpp`.
  * Conversion et optimisation de modèles pour mobile et web.
* **Architecture Système & APIs :**
  * Conception d'APIs REST/gRPC légères (FastAPI, Node.js, Spring Boot) gérant les requêtes asynchrones en cas de réseau instable.
  * Stratégies de synchronisation offline-first (queue locale, retry).
* **Projet étape :** Embarquer un modèle de STT/TTS quantifié dans une application locale sans connexion Internet.
* **Critères de réussite :** taille du modèle réduite mesurée (avant/après), latence d'inférence acceptable sur matériel bas de gamme, fonctionne 100% hors-ligne.

---

### **Phase 4 : UX Inclusif, Multimodalité & Déploiement (Mois 7+)**

*Objectif : Transformer vos modèles en un produit utilisable par n'importe quel public.*

* **Design Inclusif & Accessibilité (UX/UI) :**
  * Respect des normes **WCAG** (contrastes, lecteurs d'écran).
  * Conception d'interfaces vocales et visuelles (pictogrammes, guidage audio) adaptées aux personnes non alphabétisées.
  * Développement cross-platform (ex: Flutter, Next.js / PWA).
* **Éthique & Audit de Biais :**
  * Évaluation de la robustesse des modèles face à la diversité des utilisateurs (accents régionaux, dialectes, éclairage pour la vision).
  * Documentation type "model card" pour transparence.
* **Déploiement & Suivi :**
  * CI/CD basique, monitoring d'usage, boucle de feedback utilisateurs terrain.
* **Projet Final :** Concevoir de bout en bout une application complète (ex: assistant vocal hors-ligne pour la santé, l'agriculture ou les services publics).
* **Critères de réussite :** test utilisateur réel avec le public cible, audit WCAG passé, model card publiée.

---

### **Synthèse de la Progression**

| Phase | Focus Principal | Outils Phares | Livrable Clé |
| --- | --- | --- | --- |
| **0. Setup** | Environnement, reproductibilité | Git, Conda/uv, Colab, Docker | Dépôt + env fonctionnels |
| **1. Fondations** | Python, Math, Deep Learning | PyTorch, Scikit-Learn | Classifieur robuste |
| **2. Spécialisation** | NLP, Speech, Vision | Hugging Face, Whisper, OpenCV | Pipeline Speech-to-Text / TTS |
| **3. IA Frugale** | Quantification, Edge AI | LiteRT, ONNX, llama.cpp | Modèle embarqué hors-ligne |
| **4. Produit Inclusif** | UX Multimodale, Web/Mobile | Flutter, Next.js, WCAG | Application complète accessible |

---

### **Arborescence du projet**

```
IA/
├── roadmap.md
├── 00-setup/
├── 01-fondations-data-deep-learning/
│   ├── notebooks/
│   ├── projets/
│   └── ressources/
├── 02-voix-langage-vision/
│   ├── nlp/
│   ├── speech/
│   ├── vision/
│   └── projets/
├── 03-ia-frugale-edge/
│   ├── quantification/
│   ├── on-device/
│   └── projets/
├── 04-ux-inclusif-deploiement/
│   ├── ux-ui/
│   ├── ethique-audit/
│   └── projet-final/
└── ressources/
    ├── datasets/
    ├── papers/
    └── cours/
```

Chaque dossier de phase contient un `README.md` rappelant l'objectif, les livrables et les critères de réussite de la phase.
