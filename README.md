# 🧠 Générateur de Proposition Commerciale avec N8N et Google Gemini

Ce projet N8N vous permet de **générer automatiquement une proposition commerciale personnalisée** à partir d’un formulaire ou d’une ligne Google Sheet. Il s’appuie sur **Google Gemini (PaLM 2 ou Gemini 1.5)** pour produire des textes marketing adaptés au client, puis remplit dynamiquement un Google Doc avec les informations générées.

---

## 📸 Aperçu visuel

Voici une capture du workflow :

![Aperçu du workflow](workflow-apercu.png)
 

---

## 🧩 Fonctionnement

1. **Déclenchement manuel** (`Execute Workflow`)
2. **Lecture d'une ligne dans Google Sheets** contenant les données du client
3. **Envoi d'une requête structurée au modèle Google Gemini**, en lui fournissant le nom du client, son secteur, ses objectifs, etc.
4. **Analyse et parsing** de la réponse en JSON (sections : introduction, services, etc.)
5. **Découpage et concaténation des services** pour une meilleure lisibilité
6. **Duplication d’un template Google Docs** avec un nom personnalisé
7. **Remplacement des champs dans le document** par le contenu généré (intro, services, budget, etc.)

---

## 📂 Fichiers contenus dans ce dépôt

- `Agent_IA_avec_N8N.json` : Fichier JSON contenant le **workflow complet exporté** depuis N8N. Vous pouvez l’importer directement.
- `image.png` : Capture d’écran du workflow (vous pouvez la remplacer par une image personnalisée)
- `README.md` : Ce fichier d'explication
- `Capture d’écran.png` : Une autre vue du flux (optionnelle)

---

## 🛠️ Technologies utilisées

- [N8N](https://n8n.io/) (open source automation)
- [Google Sheets](https://www.google.com/sheets/)
- [Google Docs](https://docs.google.com/)
- [Google Gemini API](https://deepmind.google/technologies/gemini/)
- LangChain (via les nœuds N8N)

---

## 📥 Importer le workflow

1. Aller dans votre instance N8N
2. Cliquer sur `Import` > `Import from file`
3. Sélectionner le fichier `Agent_IA_avec_N8N.json`
4. Configurer vos identifiants Google Drive, Sheets et API Gemini
5. Lancer le workflow avec un exemple dans la Google Sheet

---

## 💡 Exemple d’usage

Dans votre Google Sheet, ajoutez une ligne comme :

| nom du client | Entreprise           | Secteur              | Budget | Delai(jours) | Objectifs Principaux                              | Points Spécifiques                                |
|---------------|----------------------|----------------------|--------|--------------|---------------------------------------------------|--------------------------------------------------|
| Sophie Martin | Ecovert Solutions    | Développement durable | 15000  | 60           | Refonte complète de l’identité visuelle           | Design épuré, UX fluide pour contenu technique   |

---

## 📄 Résultat

Un Google Doc comme celui-ci sera généré automatiquement :

👉 [Exemple de document](https://docs.google.com/document/d/1W0n4KNhGkoON-DiH3jMdTvsQ10fDMYVYHAtousQzpRY/edit)

---

## 👤 Auteur

Développé par [@Falleiz](https://github.com/Falleiz) dans le cadre de projets d’automatisation de la génération de contenu.

