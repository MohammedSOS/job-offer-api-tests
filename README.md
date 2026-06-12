Parfait ! Voici le guide complet pour automatiser ta collection avec Newman.
Étape 1 — Installer Node.js et Newman
Vérifie d'abord si Node.js est installé :
bashnode -v
npm -v
Si pas installé, télécharge Node.js sur nodejs.org (version LTS), puis :
bashnpm install -g newman
Vérifie l'installation :
bashnewman --version

Étape 2 — Lancer la collection avec Newman
bash# Assure-toi d'être dans ~/Documents/postman
cd ~/Documents/postman

newman run job-offer-collection_Export.json \
  --environment "Job Offer Mock Env.postman_environment.json"

Étape 3 — Rapport HTML (optionnel mais utile)
Installe le reporter HTML :
bashnpm install -g newman-reporter-htmlextra
Lance avec rapport :
bashnewman run job-offer-collection_Export.json \
  --environment "Job Offer Mock Env.postman_environment.json" \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export rapport-tests.html
