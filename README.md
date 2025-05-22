# 🚂 n8n Self-Hosting with Railway

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/new/template?template=https://github.com/Orlando17/n8n_Hosting)

One-click deploy the powerful n8n automation platform to Railway. Get your own n8n instance running in minutes!

## ✨ What is n8n?

n8n is a free, open-source workflow automation tool that lets you connect different services and automate tasks without coding. Think Zapier, but self-hosted and more powerful!

## 🚀 Quick Deploy to Railway

1. **Click the "Deploy on Railway" button above**
2. **Connect your GitHub account**
3. **Set your environment variables** (see below)
4. **Deploy and enjoy!**

Your n8n instance will be live at `https://your-app-name.up.railway.app`

## 🔧 Required Environment Variables

Set these in your Railway dashboard under **Variables**:

### Basic Setup
```bash
N8N_HOST=0.0.0.0
N8N_PORT=8080
N8N_PROTOCOL=https
N8N_BASIC_AUTH_ACTIVE=true
N8N_BASIC_AUTH_USER=admin
N8N_BASIC_AUTH_PASSWORD=your-secure-password-here
```

### Webhook Configuration
```bash
WEBHOOK_URL=https://your-app-name.up.railway.app/
```

### Database (Recommended for Production)
```bash
# Add a PostgreSQL database in Railway, then use:
DB_TYPE=postgresdb
DB_POSTGRESDB_HOST=${{Railway.PGHOST}}
DB_POSTGRESDB_PORT=${{Railway.PGPORT}}
DB_POSTGRESDB_DATABASE=${{Railway.PGDATABASE}}
DB_POSTGRESDB_USER=${{Railway.PGUSER}}
DB_POSTGRESDB_PASSWORD=${{Railway.PGPASSWORD}}
```

### Optional Settings
```bash
# Timezone
GENERIC_TIMEZONE=America/New_York

# Encryption key for credentials (generate a 32-character key)
N8N_ENCRYPTION_KEY=your-32-character-encryption-key

# Disable user management in production
N8N_USER_MANAGEMENT_DISABLED=true
```

## 📋 Manual Deployment Steps

If you prefer to deploy manually:

1. **Fork this repository**
2. **Go to [Railway.app](https://railway.app)**
3. **Click "Deploy from GitHub repo"**
4. **Select your forked repository**
5. **Set the environment variables above**
6. **Deploy!**

## 🔒 Security Notes

- Always change the default password (`N8N_BASIC_AUTH_PASSWORD`)
- Use a strong, unique encryption key
- Consider adding a PostgreSQL database for production use
- Enable HTTPS (automatically handled by Railway)

## 📖 What's Included

- **Dockerfile**: Optimized for Railway deployment
- **railway.json**: Railway-specific configuration
- **Health checks**: Ensures your n8n stays running
- **Security**: Basic auth enabled by default

## 🛠️ Customization

You can customize your n8n deployment by:

1. **Modifying environment variables** in Railway dashboard
2. **Adding custom nodes** by extending the Dockerfile
3. **Setting up custom domains** in Railway settings
4. **Configuring webhooks** for external integrations

## 📚 Learn More

- [n8n Documentation](https://docs.n8n.io/)
- [Railway Documentation](https://docs.railway.app/)
- [n8n Community](https://community.n8n.io/)

## 🤝 Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**Happy Automating!** 🎉

Need help? Check out the [n8n community forum](https://community.n8n.io/) or [Railway's help center](https://help.railway.app/).
