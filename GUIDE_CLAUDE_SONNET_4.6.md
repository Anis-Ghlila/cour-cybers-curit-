# Guide d'utilisation de Claude Sonnet 4.6

## Comment utiliser Claude Sonnet 4.6 ?

Claude Sonnet 4.6 est un modèle d'intelligence artificielle développé par Anthropic. Voici comment l'utiliser :

### 1. Accès via l'API Anthropic

Pour utiliser Claude Sonnet 4.6 via l'API, vous devez :

#### a) Obtenir une clé API
1. Créez un compte sur https://console.anthropic.com/
2. Générez une clé API depuis votre tableau de bord
3. Conservez cette clé en sécurité (ne la partagez jamais publiquement)

#### b) Installation des bibliothèques nécessaires

**Pour Python :**
```bash
pip install anthropic
```

**Pour Node.js/TypeScript :**
```bash
npm install @anthropic-ai/sdk
```

#### c) Exemple de code Python

```python
import anthropic

client = anthropic.Anthropic(
    api_key="votre_clé_api_ici"
)

message = client.messages.create(
    model="claude-sonnet-4-6-20241205",
    max_tokens=1024,
    messages=[
        {"role": "user", "content": "Bonjour, expliquez-moi la cybersécurité"}
    ]
)

print(message.content)
```

#### d) Exemple de code JavaScript/TypeScript

```javascript
import Anthropic from '@anthropic-ai/sdk';

const client = new Anthropic({
  apiKey: 'votre_clé_api_ici',
});

const message = await client.messages.create({
  model: 'claude-sonnet-4-6-20241205',
  max_tokens: 1024,
  messages: [
    { role: 'user', content: 'Bonjour, expliquez-moi la cybersécurité' }
  ]
});

console.log(message.content);
```

### 2. Accès via Claude Code (CLI)

Si vous utilisez Claude Code, le modèle est déjà configuré. Claude Code utilise par défaut Claude Sonnet 4.5, mais vous pouvez spécifier le modèle :

```bash
# Dans votre terminal
claude --model sonnet-4.6
```

### 3. Accès via l'interface web Claude.ai

1. Visitez https://claude.ai/
2. Connectez-vous avec votre compte
3. Le modèle par défaut est automatiquement sélectionné
4. Vous pouvez utiliser Claude directement dans le navigateur

## Comment changer de modèle dans le chat ?

### Option 1 : Via l'interface web Claude.ai

1. **Accédez aux paramètres** : Cliquez sur votre profil en haut à droite
2. **Sélectionnez "Paramètres"** ou "Settings"
3. **Choisissez votre modèle** :
   - Claude Opus 4.5 (le plus puissant, pour les tâches complexes)
   - Claude Sonnet 4.6 (équilibre entre performance et rapidité)
   - Claude Haiku (le plus rapide, pour les tâches simples)

### Option 2 : Via l'API (changement de modèle)

Modifiez simplement le paramètre `model` dans votre code :

```python
# Sonnet 4.6
model="claude-sonnet-4-6-20241205"

# Opus 4.5 (plus puissant)
model="claude-opus-4-5-20251101"

# Haiku (plus rapide)
model="claude-haiku-4-0-20241022"
```

### Option 3 : Via Claude Code

Dans Claude Code, vous pouvez spécifier le modèle dans votre configuration :

**Créez ou modifiez le fichier `.claude/config.json` :**

```json
{
  "model": "sonnet-4.6",
  "temperature": 0.7,
  "max_tokens": 4096
}
```

Ou utilisez la ligne de commande :

```bash
# Utiliser Sonnet 4.6
claude --model sonnet-4.6

# Utiliser Opus 4.5
claude --model opus-4.5

# Utiliser Haiku
claude --model haiku
```

## Comparaison des modèles Claude

| Modèle | Points forts | Cas d'usage |
|--------|-------------|-------------|
| **Claude Opus 4.5** | Le plus intelligent, raisonnement complexe | Analyse approfondie, tâches complexes, programmation avancée |
| **Claude Sonnet 4.6** | Équilibre performance/vitesse | Usage quotidien, rédaction, codage, analyse générale |
| **Claude Haiku** | Très rapide, rentable | Tâches simples, réponses rapides, traitement en masse |

## Caractéristiques de Claude Sonnet 4.6

- **Fenêtre de contexte** : Jusqu'à 200K tokens (environ 150,000 mots)
- **Langues supportées** : Français, Anglais, et plusieurs autres langues
- **Capacités** :
  - Rédaction et édition de texte
  - Programmation dans de nombreux langages
  - Analyse de documents
  - Raisonnement et résolution de problèmes
  - Conversations naturelles

## Bonnes pratiques

1. **Soyez précis dans vos demandes** : Plus votre question est claire, meilleure sera la réponse
2. **Utilisez le contexte** : N'hésitez pas à fournir des informations de contexte
3. **Itérez** : Vous pouvez affiner les réponses en posant des questions de suivi
4. **Respectez les limites** : Claude ne peut pas accéder à Internet en temps réel ni exécuter du code arbitraire

## Sécurité et confidentialité

- Ne partagez jamais votre clé API publiquement
- Utilisez des variables d'environnement pour stocker vos clés :
  ```bash
  export ANTHROPIC_API_KEY="votre_clé_api"
  ```
- Les conversations via l'API ne sont pas utilisées pour entraîner les modèles
- Consultez la politique de confidentialité d'Anthropic pour plus de détails

## Ressources supplémentaires

- **Documentation officielle** : https://docs.anthropic.com/
- **Guide API** : https://docs.anthropic.com/claude/reference/
- **Communauté** : https://community.anthropic.com/
- **Support** : support@anthropic.com

## Exemples pratiques pour la cybersécurité

Étant donné que ce dépôt contient un cours de cybersécurité, voici des exemples d'utilisation de Claude Sonnet 4.6 pour l'apprentissage :

### Exemple 1 : Analyse de vulnérabilités

```python
prompt = """
Expliquez les différences entre ces trois types d'attaques :
1. Phishing
2. Ransomware
3. DDoS

Incluez des exemples concrets et des méthodes de prévention.
"""
```

### Exemple 2 : Génération de quiz

```python
prompt = """
Créez un quiz de 10 questions sur la sécurité informatique
avec des questions à choix multiples et leurs réponses.
Niveau : intermédiaire
"""
```

### Exemple 3 : Explication de concepts

```python
prompt = """
Expliquez le concept de "défense en profondeur" en cybersécurité
avec des analogies simples et des exemples pratiques.
"""
```

---

**Note** : Ce guide est à jour en mars 2026. Les fonctionnalités et les modèles d'Anthropic peuvent évoluer. Consultez toujours la documentation officielle pour les informations les plus récentes.
