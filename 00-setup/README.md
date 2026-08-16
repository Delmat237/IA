# Phase 0 — Setup & Environnement

**Objectif :** avoir un environnement de travail reproductible avant de coder quoi que ce soit.

## À faire
- [x] Environnement Python — `uv` (gestion venv + dépendances via `pyproject.toml`)
- [x] Dépôt Git initialisé (local — pas encore de remote distant)
- [x] Accès GPU vérifié — **pas de GPU local** sur cette machine (`nvidia-smi` absent, `torch.cuda.is_available() == False`). Utiliser **Google Colab** ou **Kaggle Notebooks** pour l'entraînement GPU (Phases 1-3).
- [x] Jupyter installé (via `uv`) · VS Code déjà présent · Docker déjà présent

## Environnement de travail

Le projet utilise [`uv`](https://docs.astral.sh/uv/) comme gestionnaire d'environnement/dépendances (`pyproject.toml` + `.venv` à la racine, partagés par toutes les phases).

```bash
# Activer / utiliser l'environnement
uv sync                        # installe les dépendances depuis pyproject.toml
uv run jupyter notebook        # lance Jupyter
uv add <package>               # ajouter une dépendance
```

Dépendances de base installées : `jupyter`, `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `torch` (CPU-only, voir remarque GPU ci-dessus).

## GPU distant (recommandé)

Comme la machine locale n'a pas de GPU, pour les entraînements plus lourds (Phases 1-3) :
- **Google Colab** (gratuit, T4 disponible) — https://colab.research.google.com
- **Kaggle Notebooks** (gratuit, quota GPU hebdomadaire) — https://www.kaggle.com/code

## Cours recommandés
Voir [`ressources/cours/README.md`](../ressources/cours/README.md#phase-0--setup--environnement)

## Livrable
✅ [`hello_world.ipynb`](hello_world.ipynb) — notebook qui entraîne un modèle jouet (régression linéaire PyTorch) et confirme que l'environnement fonctionne. Exécuté avec succès en local sur CPU (loss converge de ~126 à ~0.25, poids appris ≈ cible).
