# TP1 — Prompt Engineering for Multi-Agent Systems

## Contexte du projet
TP universitaire sur le prompt engineering appliqué aux LLMs, réalisé avec LangChain.

## Structure du projet
- `prompt_ingeenering.ipynb` — notebook principal (tout le travail est ici)
- `pyproject.toml` — dépendances gérées avec `uv`
- `.env` — clés API (jamais committé)
- `CAPTURE/` — screenshots des résultats
- `Gemini_Generated_Image_2696ay2696ay2696.png` — image générée dans le TP

## Ce qui est déjà fait (Partie 1)
- Tokenisation avec Tiktoken (gpt-4o)
- Prompting OpenAI via ChatOpenAI (gpt-4o)
- Prompting local avec Ollama (llama3.2)
- Prompting via Groq (openai/gpt-oss-120b)
- Génération d'image texte → image
- Description d'image (image → texte)
- Analyse de sentiment orientée aspects (ABSA)

## Use Case : Sentiment Analysis (Partie 2 — en cours)
Dataset : **Financial Phrasebank** (`financial_phrasebank`, config `sentences_allagree`)
- 3 classes : `positive`, `negative`, `neutral`
- Chargement : `load_dataset("financial_phrasebank", "sentences_allagree")`
- Métrique : **micro-F1 score**
- 3 prompts à évaluer : Zero-shot, Few-shot, Chain-of-Thought (CoT)
- Évaluation sur 20 gold examples + 10 runs pour mesurer la variabilité

## Stack technique
- `langchain-openai` — ChatOpenAI (gpt-4o, gpt-4o-mini)
- `langchain-ollama` — ChatOllama (llama3.2)
- `langchain-groq` — ChatGroq
- `tiktoken` — tokenisation
- `datasets` (HuggingFace) — chargement des datasets
- `scikit-learn` — f1_score
- `uv` — gestion de l'environnement

## Règles importantes
- Ne jamais committer `.env`, `.venv`, `.claude/`
- Le fichier du prof `TP1 SMA- Prompt Engineerin For Multi Agent Systems.ipynb` reste en local uniquement (dans .gitignore)
- Ne pas ajouter de Co-Authored-By dans les commits
