se connecter
# Se placer dans le dossier
cd ~/Desktop/info1

# Lier le projet avec le token (Remplace TON_TOKEN par le vrai)
git remote set-url origin https://TON_TOKEN@github.com/szd-szd/Info1.git

# Optionnel : Dire à Kali de retenir ce token pour ne plus le taper
git config --global credential.helper store


cloner
# 1. Ils clonent le projet (ils devront entrer LEUR token quand Git demande "Password")
git clone https://github.com/szd-szd/Info1.git
cd Info1

# 2. Pour ne pas retaper leur token à chaque fois, ils font :
git remote set-url origin https://LEUR_TOKEN_ICI@github.com/szd-szd/Info1.git



modifier 
git pull origin main
# Voir ce qui a changé
git status

# Ajouter tous les fichiers modifiés
git add .

# Enregistrer la version avec un message clair
git commit -m "Description de ce que j'ai fait"

git push origin main

Note importante : Si deux personnes modifient la même ligne du même fichier, le git push sera refusé. Il faudra faire un git pull, corriger les conflits manuellement dans le fichier, puis refaire add, commit et push.
