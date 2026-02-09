# Nova Life Moscou RP - API Backend

Backend API pour le site Nova Life Moscou RP hébergé sur Firebase.

## 🚀 Fonctionnalités

- **Statut Serveur** : Monitoring en temps réel du serveur Nova Life
- **Intégration Discord** : Nombre de membres et informations serveur
- **Gestion Équipe** : Liste et détails des membres de l'équipe
- **Actualités** : Système de publication d'actualités

## 🛠️ Endpoints API

### `/api/server.php` - Statut Serveur
```json
{
  "status": "online",
  "players": 25,
  "max_players": 100,
  "ip": "83.150.217.127",
  "port": 7021
}
```

### `/api/discord.php` - Informations Discord
```json
{
  "members": 1250,
  "online": 45,
  "guild_id": "1458581949043183638"
}
```

### `/api/team.php` - Équipe
```json
[
  {
    "name": "John Doe",
    "role": "Administrateur",
    "avatar": "avatar.jpg"
  }
]
```

### `/api/news.php` - Actualités
```json
[
  {
    "id": "123",
    "title": "Nouvelle mise à jour",
    "content": "Description de l'actualité",
    "author": "Admin",
    "date": "2024-01-15T10:30:00Z"
  }
]
```

## 🚀 Déploiement sur Render.com

1. Créez un compte sur [Render.com](https://render.com)
2. Créez un nouveau **Web Service**
3. Connectez ce dépôt GitHub
4. Configuration :
   - **Build Command** : `npm install`
   - **Start Command** : `npm start`
   - **Environment Variables** :
     - `NODE_VERSION=18.17.0`

## 📁 Structure du Projet

```
nova-life-api/
├── server.js          # Serveur Express principal
├── package.json       # Dépendances Node.js
├── api/              # Endpoints API
│   ├── server.php    # Statut serveur
│   ├── discord.php   # Intégration Discord
│   ├── team.php      # Gestion équipe
│   └── news.php      # Actualités
├── data/             # Données JSON
│   ├── team.json     # Liste équipe
│   └── news.json     # Actualités
└── README.md         # Documentation
```

## 🔧 Variables d'Environnement

```bash
# Optionnel - Discord Bot (si utilisé)
DISCORD_BOT_TOKEN=votre_token_bot
DISCORD_GUILD_ID=id_serveur_discord
```

## 🎯 URLs après déploiement

- **API Endpoint** : `https://[service-name].onrender.com`
- **Site Frontend** : `https://moscou-rp-d38cd.web.app`

## 📞 Support

Contactez l'équipe Nova Life Moscou RP pour toute question.