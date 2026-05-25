# README.md

````md
# 🤖 French AI Chatbot with Groq + OpenAI SDK

Un petit projet Python permettant de créer une IA conversationnelle française en utilisant l'API Groq avec le SDK OpenAI officiel.

---

## ✨ Fonctionnalités

- 🇫🇷 Réponses en français
- ⚡ Utilise l’API ultra rapide de Groq
- 🧠 Modèle `llama-3.3-70b-versatile`
- 💬 Chat en boucle dans le terminal
- 🔧 Simple et facile à modifier

---

## 📦 Installation

### 1️⃣ Cloner le projet

```bash
git clone https://github.com/your-username/french-ai-chatbot.git
cd french-ai-chatbot
````

### 2️⃣ Installer les dépendances

```bash
pip install openai
```

---

## 🔑 Configuration

Remplace la clé API dans le code :

```python
api_key="your_groq_api_key"
```

Tu peux obtenir une clé API ici :

👉 [https://console.groq.com/](https://console.groq.com/)

---

## 🚀 Utilisation

Lancer le script :

```bash
python main.py
```

Ensuite, écris simplement un message dans le terminal :

```bash
Awnser: Salut !
```

Exemple de réponse :

```bash
Salut 👋 Comment vas-tu ?
```

---

## 🧠 Code Source

```python
from openai import OpenAI

client = OpenAI(
    api_key="your_groq_api_key",
    base_url="https://api.groq.com/openai/v1",
)

while True:
    chat = input("Awnser: ")

    response = client.responses.create(
        model="llama-3.3-70b-versatile",
        input=[
            {
                "role": "system",
                "content": "You are a French AI..."
            },
            {
                "role": "user",
                "content": chat
            }
        ],
        max_output_tokens=80
    )

    print(response.output_text)
```

---

## 📁 Structure du projet

```bash
📦 french-ai-chatbot
 ┣ 📜 main.py
 ┣ 📜 README.md
 ┗ 📜 requirements.txt
```

---

## 🛠 Requirements.txt

```txt
openai
```

---

## ⚠️ Important

Le prompt système actuel donne beaucoup de liberté au modèle.
Fais attention si tu veux publier ce projet ou le rendre accessible au public.

---

## 💡 Idées d'amélioration

* Ajouter une mémoire de conversation
* Interface graphique avec Tkinter ou CustomTkinter
* Historique des messages
* Commandes personnalisées
* Support vocal
* Mode sombre
* Streaming des réponses

---

## 📜 Licence

Projet open-source sous licence MIT.

---

## ❤️ Crédits

* API : Groq
* SDK : OpenAI Python
* Modèle : Llama 3.3 70B Versatile

---

```
```
