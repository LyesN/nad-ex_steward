# Plan de visibilité – Dictée Dubois

> Suivi des actions proposées par NAD‑ex Steward (SOUL.md).  
> Cochez les cases au fur et à mesure de l’avancement.  
> Revue suggérée : chaque vendredi (15 min) → mettre à jour ce fichier.

---

## 🔎 SEO
- [ ] Identifier les 10 requêtes longues traîne (Search Console / Ubersuggest)  
- [ ] Créer 2 pages « guide pratique » ciblant ces requêtes  
- [ ] Ajouter maillage interne CTA depuis les articles de blog les plus lus  
- [ ] Implémenter bloc FAQ avec schéma.org sur la page d’accueil  
- [ ] Valider le rich snippet via l’outil de test des données structurées  

## 📣 Marketing de contenu
- [ ] Réaliser la première vidéo « Astuces dictée » (60 s)  
- [ ] Publier la vidéo sur YouTube Shorts + TikTok  
- [ ] Créer le guide téléchargeable « Plan de progression dictée (4 semaines) »  
- [ ] Mettre en ligne la landing page (formulaire prénom/email, RGPD)  
- [ ] Rédiger et envoyer les propositions d’article invité à 3 blogs éducatifs  
- [ ] Préparer le webinaire avec orthophoniste (date, inscription, replay)  

## 🤝 Partenariats & communautés
- [ ] Rédiger le formulaire de candidature « Écoles pilotes »  
- [ ] Contacter les inspecteurs académiques pour lancer le appel  
- [ ] Rejoindre 2‑3 groupes Facebook/Discord de parents, préparer réponses type  
- [ ] Planifier le premier post de participation utile (non promotionnel)  

## 📧 Email marketing & nurturing
- [ ] Configurer la séquence d’onboarding (3 emails) dans l’outil d’email  
- [ ] Rédiger le contenu des 3 emails (bienvenue, astuce, parrainage doux)  
- [ ] Créer le modèle de newsletter mensuelle « Le coin de l’orthographe »  
- [ ] Programmer l’envoi du premier numéro (premier jeudi du mois prochain)  

## 🎁 Programme de parrainage éthique
- [ ] Implémenter le code de parrainage unique dans le profil utilisateur  
- [ ] Définir la règle : 1 mois premium après 5 dictées du filleul  
- [ ] Tester le flux complet (parrain → filleul → récompense)  
- [ ] Communiquer le programme via l’email d’onboarding et la newsletter  

## 📰 Relations presse & médias
- [ ] Rédiger le communiqué de lancement de la nouvelle fonctionnalité (suivi des progrès)  
- [ ] Identifier 5 journalistes spécialisés (éducation, tech‑éducative, santé scolaire)  
- [ ] Envoyer le communiqué + offre d’interview exclusive  
- [ ] Identifier 2 podcasts éducatifs pertinents, préparer les points clés  
- [ ] Proposer une intervention de 10‑15 min  

## ⚡ Optimisation UX (levier indirect de visibilité)
- [ ] Exécuter un audit Lighthouse sur la page d’accueil (performance < 2 s)  
- [ ] Corriger les points critiques (images, JS bloquant)  
- [ ] Réaliser un audit d’accessibilité axe DevTools (contraste, navigation clavier, ARIA)  
- [ ] Corriger les écarts prioritaires (score > 80 %)  

## 📊 Suivi & indicateurs
- [ ] Définir les métriques de succès dans le tableau de bord (voir propositions SOUL)  
- [ ] Mettre en place un suivi mensuel simple (Google Sheet ou fichier CSV)  
- [ ] Planifier une revue de chiffres chaque premier lundi du mois  

---
*Ce fichier est destiné à être versionné (git) afin de garder un historique des décisions et des avancées.*  
## 🕷️ Cartographie de l'écosystème web et surveillance agentic

En tant que startup AI-native, nous devons déployer des agents pour surveiller en permanence les espaces web où notre public cible pourrait s'exprimer sur la dictée, l'orthographe et les outils éducatifs.

### 📋 Tâches à réaliser

- [ ] **Identifier les sources pertinentes** :
  - Groupes Facebook publics (ex. : « Parents d'élèves CP/CE1 », « Enseignants du primaire »)
  - Communautés Reddit (ex. : r/france, r/education, r/Apprentissage)
  - Forums éducatifs (ex. : Les-Cahiers-educatifs.fr, Forum des profs)
  - Chaînes YouTube éducatives francophones (ex. : « La classe de Mallory », « Maxetom »)
  - Blogs de professeurs et de parents (via recherche Google et flux RSS)
  - Comptes Twitter/X éducatifs (@EducationFrance, @eduscol, etc.)

- [ ] **Mettre en place un agent de scan quotidien** :
  - Utiliser des outils comme `curl`, `grep` ou des scripts Python pour analyser les nouvelles publications
  - Cibler les mots-clés : « dictée gratuite », « exercices orthographe CE1 », « application orthographe enfant », « problème d’orthographe »
  - Scanner les flux RSS des blogs identifiés
  - Surveiller les nouveaux posts dans les groupes Facebook/Reddit via leurs APIs publiques (si disponibles) ou via scraping léger (respectueux des CGU)

- [ ] **Définir des critères de priorisation** :
  - **Récence** : publications des dernières 24h (score élevé)
  - **Importance de la communauté** : nombre de membres/abonnés, taux d’engagement
  - **Visibilité de la publication** : nombre de vues, likes, commentaires, partages
  - **Pertinence sémantique** : présence de mots-clés liés à la dictée/orthographe et à un besoin non satisfait
  - **Score final** = pondération des critères ci-dessus (à affiner)

- [ ] **Mettre en place un système d’alerte en temps réel** :
  - Lorsqu’une publication dépasse un seuil de priorité (ex. : score > 8/10),
  - Déclencher une alerte via Telegram bot vers un canal dédié
  - Le message d’alerte doit inclure :
    * Lien direct vers la publication
    * Résumé en une phrase du besoin exprimé
    * Proposition de réponse type (ex. : « Bonjour, connaissez-vous NAD-ex ? C’est une app gratuite pour s’entraîner en dictée avec suivi de progression… »)
    * Bouton d’action pour répondre directement (si possible via API)

- [ ] **Intégrer avec les outils existants** :
  - Lier ce système au projet GitHub `nad-ex_steward` pour suivre les tâches
  - Créer des issues automatiquement pour les alertes à haute priorité
  - Utiliser les agents de développement (Claude Code, Codex) pour implémenter les scripts

### 📅 Fréquence et maintenance

- **Scan quotidien** : exécuter chaque matin à 8h00 (heure de Paris)
- **Revue hebdomadaire** : chaque lundi, ajuster les mots-clés et les sources
- **Rapport mensuel** : analyser les tendances et les opportunités manquées

### 🛠️ Outils suggérés (à valider avec l’équipe)

- Pour le scraping léger : `requests` + `BeautifulSoup` (Python) ou `curl` + `grep`
- Pour les APIs officielles : Facebook Graph API (limité), Reddit API, YouTube Data API
- Pour l’alerte Telegram : créer un bot via @BotFather et utiliser l’API Telegram
- Pour le suivi : utiliser le projet GitHub `nad-ex_steward` avec des colonnes « À surveiller », « Alerte envoyée », « Réponse donnée »

> ⚠️ Respecter toujours les CGU des plateformes et privilégier les APIs officielles lorsqu’elles existent. Éviter le scraping agressif.
