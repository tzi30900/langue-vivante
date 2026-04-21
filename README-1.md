# 🎙 Langue Vivante — Installation sur Android

Application d'apprentissage des langues par immersion conversationnelle.  
Fonctionne **hors ligne en voiture** après un premier téléchargement des scénarios en WiFi.

---

## Ce dont vous avez besoin

1. Un téléphone Android avec **Chrome**
2. Une **clé API Anthropic** (obtenez-la sur https://console.anthropic.com)
   - Coût : environ 0,01–0,05€ par conversation
   - La clé est stockée uniquement sur votre téléphone

---

## Option A — GitHub Pages (recommandé, gratuit)

### Étape 1 — Créer un compte GitHub
- Allez sur https://github.com et créez un compte gratuit

### Étape 2 — Créer un dépôt
- Cliquez sur "New repository"
- Nom : `langue-vivante` (ou ce que vous voulez)
- Cochez "Public"
- Cliquez "Create repository"

### Étape 3 — Uploader les fichiers
- Cliquez "uploading an existing file"
- Glissez les 4 fichiers : `index.html`, `manifest.json`, `sw.js`, `README.md`
- Cliquez "Commit changes"

### Étape 4 — Activer GitHub Pages
- Allez dans Settings → Pages
- Source : "Deploy from a branch" → branch "main" → dossier "/ (root)"
- Cliquez Save
- Attendez 2 minutes

### Étape 5 — Installer sur Android
- Votre URL sera : `https://VOTRE_NOM.github.io/langue-vivante/`
- Ouvrez cette URL dans **Chrome** sur votre téléphone
- Chrome affiche une bannière "Ajouter à l'écran d'accueil" — tapez dessus
- Sinon : menu ⋮ → "Ajouter à l'écran d'accueil"
- L'app s'installe comme une vraie application ✓

---

## Option B — Hébergement local sur votre réseau WiFi

Si vous avez un PC, vous pouvez héberger l'app localement :

```bash
# Python 3
cd langue-vivante-pwa
python -m http.server 8080

# Puis sur votre téléphone (même WiFi) :
# http://ADRESSE_IP_PC:8080
```

---

## Utilisation

### Première fois (WiFi requis)
1. Lancez l'app → entrez votre clé API
2. Choisissez votre langue cible et votre niveau
3. Sur l'écran des scénarios : tapez **"⬇ Tout télécharger"**
   - L'app génère et stocke les 8 scénarios sur votre téléphone
   - Comptez 2-3 minutes en tout

### En voiture (hors ligne)
- Tous les scénarios téléchargés sont disponibles
- Tapez un scénario → **"📚 Pratiquer"**
- Mode guidé avec voix : le personnage parle, vous choisissez ce que vous dites, vous vous entraînez à le prononcer
- La synthèse vocale et la reconnaissance vocale fonctionnent hors ligne sur Android

### Avec connexion (4G/WiFi)
- **"💬 Libre"** : conversation libre avec Claude qui joue le personnage
- Corrections de grammaire, vocabulaire et prononciation après chaque réplique
- **"↻"** : régénérer un scénario avec du contenu frais

---

## Les 8 scénarios inclus

| Scénario | Situations couvertes |
|----------|---------------------|
| 🗺️ Demander son chemin | Metro, rue, monument, quartier |
| 📸 Infos touristiques | Recommandations, horaires, entrées |
| 🍽️ Au restaurant | Commander, allergie, addition |
| 🛒 Au marché / magasin | Prix, tailles, couleurs, négociation |
| 🚌 Transports | Bus, métro, taxi, billet, retard |
| 🏥 Chez le médecin | Symptômes, ordonnance, urgences |
| 🏨 À l'hôtel | Check-in, réclamation, services |
| 🆘 Situation difficile | Objet perdu/volé, incompréhension |

---

## Questions fréquentes

**L'app consomme mes données mobiles en voiture ?**  
Non. En mode "Pratiquer", tout fonctionne hors ligne. Seul le mode "Conversation libre" nécessite une connexion.

**Mes données sont-elles partagées ?**  
Votre clé API est stockée uniquement sur votre téléphone (localStorage). Les conversations vont directement de votre téléphone à l'API Anthropic, sans intermédiaire.

**Comment ajouter une nouvelle langue ?**  
Allez dans ⚙ Paramètres, changez la langue. Les scénarios seront à re-télécharger pour la nouvelle langue.

**La reconnaissance vocale ne fonctionne pas ?**  
Sur Android, la reconnaissance vocale via Chrome fonctionne hors ligne (Google a les modèles en local). Si ça ne marche pas, utilisez le mode texte.

---

Bonne pratique ! 🌍
