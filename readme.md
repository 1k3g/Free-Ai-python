# 🤖 Groq Chatbot CLI

Un chatbot en ligne de commande utilisant l'API **Groq** via le client OpenAI, propulsé par le modèle **LLaMA 3.3 70B**.

## 📋 Prérequis

- Python 3.8+
- Une clé API [Groq](https://console.groq.com/)

## 📦 Installation

```bash
pip install openai
```

## ⚙️ Configuration

Remplace `"grok key"` dans le code par ta clé API Groq :

```python
api_key="TA_CLE_API_GROQ"
```

> ⚠️ Ne partage jamais ta clé API publiquement. Utilise de préférence une variable d'environnement :
> ```python
> import os
> api_key=os.getenv("GROQ_API_KEY")
> ```

## 🚀 Utilisation

```bash
python chatbot.py
```

Le bot démarre une boucle interactive. Tape ton message et appuie sur Entrée pour obtenir une réponse.

```
Awnser: Bonjour, comment tu vas ?
> Ça va, merci de demander. Et toi ?
Awnser: _
```

Pour quitter, utilise `Ctrl+C`.

## 🧠 Modèle utilisé

| Paramètre        | Valeur                    |
|------------------|---------------------------|
| Modèle           | `llama-3.3-70b-versatile` |
| Max tokens       | 80                        |
| Fournisseur      | Groq                      |

## 📁 Structure

```
.
└── chatbot.py   # Script principal
```