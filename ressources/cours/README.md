# Cours en ligne recommandés — par phase

Sélection de cours/tutoriels vérifiés (août 2026), classés par phase de la [roadmap](../../roadmap.md). 🆓 = gratuit, 💶 = payant (souvent avec audit gratuit sur Coursera).

---

## Phase 0 — Setup & Environnement

- 🆓 [uv — documentation officielle](https://docs.astral.sh/uv/) — l'outil déjà utilisé dans ce projet
- 🆓 [Learn Git Branching](https://learngitbranching.js.org/) — apprendre Git de façon interactive et visuelle
- 🆓 [Google Colab](https://colab.research.google.com/) — pour l'accès GPU gratuit (pas de GPU local sur cette machine, voir `00-setup/README.md`)

---

## Phase 1 — Fondations Data & Deep Learning

**Mathématiques appliquées**
- 💶 [Mathematics for Machine Learning (Coursera, Imperial College London)](https://www.coursera.org/specializations/mathematics-machine-learning) — algèbre linéaire, calcul multivarié, PCA
- 🆓 [3Blue1Brown — Essence of Linear Algebra](https://www.3blue1brown.com/topics/linear-algebra) — intuition visuelle, excellent complément

**Python / ML classique**
- 🆓 [Kaggle Learn](https://www.kaggle.com/learn) — micro-cours gratuits : Python, Pandas, Intro/Intermediate Machine Learning, Feature Engineering (1-7h chacun, dans le navigateur)

**Deep Learning / PyTorch**
- 🆓 [fast.ai — Practical Deep Learning for Coders](https://course.fast.ai/) — approche pratique "code first", par Jeremy Howard (ex-Kaggle)
- 🆓 [PyTorch — Tutoriels officiels](https://docs.pytorch.org/tutorials/index.html) — MLP, CNN, bases des Transformers
- 💶 [Deep Learning Specialization (Coursera, Andrew Ng / DeepLearning.AI)](https://www.coursera.org/specializations/deep-learning) — référence académique classique

---

## Phase 2 — Voix, Langage & Vision

**NLP / LLM**
- 🆓 [Hugging Face — LLM/NLP Course](https://huggingface.co/learn/llm-course/en/chapter1/1) — tokenization, embeddings, fine-tuning (BERT, Llama/Mistral) avec `transformers`

**Audio / Speech (STT, TTS)**
- 🆓 [Hugging Face — Audio Course](https://huggingface.co/learn/audio-course) — Whisper (STT), synthèse vocale (TTS), assistant vocal de bout en bout
- 🆓 [Mozilla Common Voice](https://commonvoice.mozilla.org/) — dataset audio ouvert, utile pour les **langues peu dotées**

**Computer Vision & OCR**
- 🆓 [OpenCV University — Free Course](https://opencv.org/university/free-opencv-course/) — cours officiel OpenCV (manipulation image/vidéo, détection)
- 🆓 [Stanford CS231n](http://cs231n.stanford.edu/) — cours de référence en vision par ordinateur (notes + vidéos publiques)

---

## Phase 3 — IA Frugale & Edge AI

- 🆓 [HarvardX — Fundamentals of TinyML (edX)](https://www.edx.org/learn/machine-learning/harvard-university-fundamentals-of-tinyml) — bases ML embarqué, quantification, déploiement sur microcontrôleurs (gratuit en mode audit)
- 🆓 [ONNX Runtime — Getting Started](https://onnxruntime.ai/getting-started) — conversion et inférence optimisée cross-framework
- 🆓 [Google AI Edge / LiteRT — Documentation](https://ai.google.dev/edge/litert) — ex-TensorFlow Lite, déploiement mobile/on-device
- 🆓 [llama.cpp (dépôt officiel)](https://github.com/ggml-org/llama.cpp) — inférence LLM quantifiée en local, `llama-server` compatible API OpenAI
- 🆓 [FastAPI — Tutoriel officiel](https://fastapi.tiangolo.com/tutorial/) — pour l'API légère servant les modèles embarqués

---

## Phase 4 — UX Inclusif, Multimodalité & Déploiement

- 🆓 [web.dev — Learn Accessibility](https://web.dev/learn/accessibility) — cours de référence sur les normes WCAG
- 🆓 [Flutter — Parcours d'apprentissage officiel](https://docs.flutter.dev/get-started/codelab) — pour le développement cross-platform
- 🆓 [Next.js — Learn](https://nextjs.org/learn) — cours officiel Vercel pour construire une PWA/app full-stack
- 🆓/💶 [Google Cloud — Responsible AI for Developers: Fairness & Bias (Coursera)](https://www.coursera.org/learn/responsible-ai-for-developers-fairness--bias) — audit de biais, équité des modèles
- 🆓 [Kaggle Learn — Intro to AI Ethics](https://www.kaggle.com/learn) — micro-cours court sur l'éthique de l'IA

---

## Conseil d'usage

Pas besoin de tout suivre en intégral : utiliser ces cours comme référence à consulter au fil des projets étape de chaque phase (voir critères de réussite dans les `README.md` de chaque dossier), plutôt que de les suivre linéairement de bout en bout avant de coder.
