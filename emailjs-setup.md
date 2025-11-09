# Configuration EmailJS pour Akoa Digital

## 📧 Service d'envoi d'emails automatique

### Problème résolu :
- ❌ **Formspree** : URL invalide (`xpwnqkqr` n'existe pas)
- ✅ **EmailJS** : Service fiable et gratuit

### Configuration EmailJS (GRATUIT) :

#### 1. Créer un compte EmailJS :
1. Allez sur : https://www.emailjs.com/
2. Cliquez sur "Sign Up" (gratuit)
3. Créez votre compte

#### 2. Configurer le service email :
1. Dans le dashboard, allez dans "Email Services"
2. Cliquez "Add New Service"
3. Choisissez votre fournisseur email :
   - **Gmail** (recommandé pour `akoa211d@gmail.com`)
   - **Outlook** 
   - **Yahoo**
4. Suivez les instructions de connexion
5. **Copiez le SERVICE_ID** (ex: `service_abc123`)

#### 3. Créer un template d'email :
1. Allez dans "Email Templates"
2. Cliquez "Create New Template"
3. Utilisez ce template :

```
Sujet : Nouveau message de contact - Akoa Digital

Bonjour,

Vous avez reçu un nouveau message de contact depuis votre site web :

Nom : {{name}}
Email : {{email}}
Téléphone : {{phone}}
Entreprise : {{company}}
Service : {{service}}
Budget : {{budget}}

Message :
{{message}}

---
Message envoyé depuis akooa.netlify.app
```

4. **Copiez le TEMPLATE_ID** (ex: `template_xyz789`)

#### 4. Obtenir la clé publique :
1. Allez dans "Account" → "General"
2. **Copiez la PUBLIC_KEY** (ex: `user_abc123def456`)

#### 5. Mettre à jour le code :
Dans `contact.html`, remplacez :
- `YOUR_PUBLIC_KEY` par votre clé publique
- `YOUR_SERVICE_ID` par votre service ID
- `YOUR_TEMPLATE_ID` par votre template ID

### Exemple de configuration finale :
```javascript
emailjs.init("user_abc123def456");
emailjs.send('service_abc123', 'template_xyz789', formData)
```

### Avantages EmailJS :
- ✅ **100% gratuit** (200 emails/mois)
- ✅ **Fonctionne avec tous les hébergeurs**
- ✅ **Pas de serveur backend nécessaire**
- ✅ **Sécurisé** (clés API)
- ✅ **Templates personnalisables**
- ✅ **Support Gmail, Outlook, Yahoo**

### Test du formulaire :
1. Configurez EmailJS avec vos clés
2. Remplissez le formulaire de contact
3. Cliquez sur "Envoyer le Message"
4. Vérifiez que l'email arrive dans `akoa211d@gmail.com`

### Alternative rapide (sans configuration) :
Si vous voulez tester immédiatement, vous pouvez utiliser :
- **Netlify Forms** (si hébergé sur Netlify)
- **Getform** (alternative à Formspree)
- **Formspree** avec une nouvelle URL valide

### Support :
- Documentation EmailJS : https://www.emailjs.com/docs/
- Support gratuit : support@emailjs.com



