Bonjour,

Après une enquête approfondie, nous avons pu récolter un maximum d’informations sur l’individu ayant infiltré vos systèmes. Voici un résumé des étapes menées pour identifier le suspect et retracer son activité.
# TP Yboost OSINT

* Pour cette première mission, j’ai utilisé l’outil Sherlock afin de rechercher les comptes associés à un pseudonyme. L’analyse m’a permis de retrouver plusieurs comptes sur différentes plateformes, dont un GitHub qui a retenu notre attention.
* Nous avons analysé la photo de profil GitHub du suspect. Les métadonnées contenaient des coordonnées GPS qui pointaient vers un commerce au Bouscat.
* En consultant les avis Google du commerce, nous avons trouvé une photo contenant un QR code. Ce code renvoyait vers une page contenant un message encodé en plusieurs couches.
* Après avoir décodé le texte, nous avons obtenu un lien menant vers le site de son employeur. Le site semblait douteux, nous avons donc poursuivi l’investigation.
* Nous avons utilisé l’outil Nikto pour analyser le site et détecter des failles connues. Cela nous a permis de trouver un fichier contenant des mots de passe administrateurs.
* Grâce à ces identifiants, nous avons accédé à la section admin du site. Là, nous avons récupéré le nom et prénom d’un étudiant suspect.
* Nous avons trouvé le CV du suspect, qui mentionnait un numéro de téléphone et un profil LinkedIn. En ajoutant ce numéro sur WhatsApp, son profil renvoyait vers un GitHub contenant un projet en cours.
* Dans le projet GitHub, une variable JavaScript contenait une chaîne encodée. En la décodant, nous avons obtenu un lien MEGA pointant vers un fichier binaire.
* À l’aide de l’outil strings, nous avons extrait des chaînes du fichier binaire. Une d’elles était un lien d’invitation vers un serveur Discord.
* Sur le serveur, nous avons intercepté un message mentionnant une faille dans les chemins d’accès du site :

"Faut absolument qu'on fix la SQLi sur /Sup3r_S3cre3t_f0ld3rz/"

* Nous avons tenté une injection SQL sur cette route. Cela nous a permis d’accéder à une URL .onion pointant vers un Darknet marketplace.
* Sur ce marché, un vendeur actif utilisait un pseudo particulier. En le recherchant avec des outils de type Namechk, nous avons retrouvé un profil Instagram.
* Sur ce profil Instagram, on pouvait lire la citation suivante :

"Je ne pirate pas, j'explore les limites des systèmes."

Cela confirmait son état d’esprit.
* Le compte Instagram @phantom_0xsec comportait une photo de son espace de travail. Un post-it visible révélait un début d’adresse MAC.

À l’aide de la base wigle.net, nous avons pu relier cette adresse MAC à une localisation physique :
283 Rue Pasteur, Bordeaux, Nouvelle-Aquitaine, FR, 33200



