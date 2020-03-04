
### WSL
pour accéder à vos fichiers WSL depuis windows ( Si votre windows est à jour)
https://www.omgubuntu.co.uk/2019/02/access-linux-files-from-windows-explorer-wsl

### Comment le web fonctionne :
https://www.freecodecamp.org/news/how-the-web-works-a-primer-for-newcomers-to-web-development-or-anyone-really-b4584e63585c/


### Internet History :
https://www.computerhistory.org/internethistory/1960s/

### NETCAT
Quelques exemples d'utilisation de NETCAT, pour mieux comprendre tcp/ip, les différents protocoles, la ligne de commande unix.. :
https://www.thegeekstuff.com/2012/04/nc-command-examples/
https://doc.fedora-fr.org/wiki/Netcat,_connexion_client/serveur_en_bash


Pour ceux qui veulent aller encore plus loin en compréhension du réseau avec NMAP :
https://www.varonis.com/blog/nmap-commands/

### Linux Terminal Basics

Afficher le dossier courant:
`pwd`
= Print Working Directory

Aller dans un dossier "enfant" du répértoire courant :
`cd NomDuDossier`

Aller dans n'importe quel dossier du système de fichiers (en commençant par /)  :
`cd /CheminCompletVersLeDossier`

Aller dans le dossier parent:
`cd ..`

Lancer une commande en root (adminsitrateur):
`sudo commande`

Devenir root :
`su`

Si mon invite de commande finit par un $ , je ne suis pas root.
Si mon invite de commande finit par un # , je suis root.

Crééer un script python, bash, php, perl



### Un mini serveur web avec python3

Ce serveur vous permet d'accéder à vos fichiers. 
A lancer depuis le répértoire que vous vous voulez mettre à disposition.

python3 -m http.server 8000

https://docs.python.org/3/library/http.server.html

### TUTO HTML & CSS
https://www.w3schools.com/html/html_intro.asp

https://internetingishard.com/html-and-css/



https://www.w3schools.com/css/css_intro.asp

https://www.w3schools.com/css/css_selectors.asp


Pour debugger CSS quand vous ne comprenez pas pourquoi votre style n'est pas pris en compte:
https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Cascade_and_inheritance


Comprendre Block, Inline, Float:
https://openweb.eu.org/articles/initiation_flux/

https://openweb.eu.org/articles/initiation_float

Unites css, taille de police, em:
https://www.w3.org/Style/Examples/007/units.fr.html

Bien utiliser les outils developpeurs chrome:
https://developers.google.com/web/tools/chrome-devtools

https://developers.google.com/web/tools/chrome-devtools/css


### Responsive web design
https://www.w3schools.com/html/html_responsive.asp

Pour aller plus loin:
https://www.w3schools.com/css/css_rwd_intro.asp

### NGINX

Trouver le fichier de conf : nginx -t

Linux:
lancer nginx
`service nginx status`

Arreter nginx
`service nginx status`

Mac (brew):
lancer nginx
`brew services start nginx`
ou
`sudo nginx`

Arreter nginx
`brew services stop nginx`
ou
`sudo nginx -s stop`



nginx sur mac :
https://medium.com/@ThomasTan/installing-nginx-in-mac-os-x-maverick-with-homebrew-d8867b7e8a5a

nginx linux tres complet (= windows WSL):
https://www.digitalocean.com/community/tutorials/comment-installer-nginx-sur-ubuntu-18-04-fr



### JavaScript HTML DOM

Le DOM est une arborescence d'objets javascript correpondant à la page affichée dans le navigateur.

Coder coté Navigateur web en Javascript se résume en général à manipuler les objets du dom, et à réagir à leur évènements.

https://www.w3schools.com/js/js_htmldom.asp


### Bottle
http://bottlepy.org/docs/dev/


### Introduction to Node.js

https://itnext.io/introduction-to-node-js-a-beginners-guide-to-node-js-and-npm-eca9c408f9fe



### Node + Express

https://developer.mozilla.org/fr/docs/Learn/Server-side/Express_Nodejs/Introduction

https://flaviocopes.com/express/


### REACT

https://dev.to/aspittel/a-complete-beginners-guide-to-react-2cl6

https://morioh.com/p/b856ead14ab7

https://fr.reactjs.org/tutorial/tutorial.html

https://www.w3schools.com/REACT/default.asp

https://www.youtube.com/watch?v=DLX62G4lc44


### WEB DEVELOPPER ROADMAP

Attention, ceci n'est que l'avis d'un developpeur. Il existe d'autres listes de ce genre. Celle ci est assez exhaustive. L'auteur propose 3 chemins : Frontend - Backend - Devops.


Il précise que l'usage basique du terminal est requis pour les 3 chemins : 
"Basic Terminal Usage - The Bash Command Line, SSH, and other skills
This could be the terminal on a Mac, a Windows DOS prompt, or Bash/ZSH. Note that regardless of which operating system you use, you should probably learn Linux. Even if you're not using it for your laptop/desktop environment, you'll almost certainly use it for servers."

2019 :
https://github.com/kamranahmedse/developer-roadmap


2020:
https://www.freecodecamp.org/news/2019-web-developer-roadmap/

Je ne trouve pas Node.js dans la roadmap 2020, j'ai essayé de comprendre pourquoi il l'avait retiré mais je n'ai rien trouvé..
