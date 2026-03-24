# Aide-mémoire rapide : Claude Sonnet 4.6

## 🚀 Démarrage rapide

### Option 1 : Interface Web (Le plus simple)
1. Visitez https://claude.ai/
2. Connectez-vous
3. Commencez à discuter !

### Option 2 : API Python
```python
pip install anthropic

import anthropic
client = anthropic.Anthropic(api_key="votre_clé")
message = client.messages.create(
    model="claude-sonnet-4-6-20241205",
    max_tokens=1024,
    messages=[{"role": "user", "content": "Votre question"}]
)
print(message.content)
```

### Option 3 : Claude Code (CLI)
```bash
claude --model sonnet-4.6
```

## 🔄 Comment changer de modèle ?

| Méthode | Action |
|---------|--------|
| **Web** | Paramètres → Choisir le modèle |
| **API** | Modifier le paramètre `model` |
| **CLI** | `claude --model [opus-4.5\|sonnet-4.6\|haiku]` |

## 📊 Quel modèle choisir ?

```
┌─────────────────────────────────────────────┐
│  OPUS 4.5    → Tâches complexes            │
│  ↓ (Le plus puissant)                      │
│                                             │
│  SONNET 4.6  → Usage quotidien ⭐          │
│  ↓ (Équilibré - RECOMMANDÉ)               │
│                                             │
│  HAIKU       → Tâches simples et rapides   │
│  ↓ (Le plus rapide)                        │
└─────────────────────────────────────────────┘
```

## 💡 Modèles disponibles

| Modèle | ID API | Meilleur pour |
|--------|--------|---------------|
| **Opus 4.5** | `claude-opus-4-5-20251101` | Analyse approfondie, tâches complexes |
| **Sonnet 4.6** | `claude-sonnet-4-6-20241205` | Usage quotidien, équilibre performance/vitesse |
| **Haiku** | `claude-haiku-4-0-20241022` | Réponses rapides, tâches simples |

## 🎯 Exemples pour la cybersécurité

### Expliquer un concept
```
"Explique-moi le phishing avec des exemples concrets"
```

### Créer un quiz
```
"Crée un quiz de 10 questions sur les ransomwares"
```

### Analyser une attaque
```
"Décris les étapes d'une attaque DDoS et comment s'en protéger"
```

### Générer du code sécurisé
```
"Écris un script Python pour valider des entrées utilisateur"
```

## 🔐 Sécurité

✅ **À FAIRE**
- Utiliser des variables d'environnement pour les clés API
- Garder votre clé API confidentielle
- Lire la politique de confidentialité

❌ **À ÉVITER**
- Partager votre clé API publiquement
- Commiter des clés dans Git
- Stocker des clés en clair dans le code

## 📖 Configuration recommandée

### Variables d'environnement (Linux/Mac)
```bash
export ANTHROPIC_API_KEY="votre_clé_api_ici"
```

### Variables d'environnement (Windows PowerShell)
```powershell
$env:ANTHROPIC_API_KEY="votre_clé_api_ici"
```

### Fichier .env (pour projets)
```
ANTHROPIC_API_KEY=votre_clé_api_ici
```

## 🔗 Liens utiles

- 📚 [Guide complet](./GUIDE_CLAUDE_SONNET_4.6.md)
- 🌐 [Documentation officielle](https://docs.anthropic.com/)
- 💬 [Claude.ai](https://claude.ai/)
- 🎓 [Cours de cybersécurité](./README.md)

## ⚡ Astuces

1. **Soyez précis** : Plus votre question est claire, meilleure sera la réponse
2. **Donnez du contexte** : Expliquez ce que vous essayez d'accomplir
3. **Itérez** : Affinez les réponses avec des questions de suivi
4. **Utilisez le bon modèle** : Sonnet 4.6 pour la plupart des cas
5. **Fenêtre de contexte** : Jusqu'à 200K tokens (≈150,000 mots)

## 🎓 Pour ce cours de cybersécurité

Claude peut vous aider à :
- ✅ Comprendre des concepts complexes
- ✅ Générer des exercices pratiques
- ✅ Analyser des cas d'étude
- ✅ Écrire du code sécurisé
- ✅ Préparer des examens

---

**Conseil** : Commencez avec l'interface web sur claude.ai, c'est le plus simple !

Pour plus de détails, consultez le [GUIDE_CLAUDE_SONNET_4.6.md](./GUIDE_CLAUDE_SONNET_4.6.md)
