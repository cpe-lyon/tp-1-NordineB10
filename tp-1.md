Bouskine Nordine 

# TP1 – Installation d’Ubuntu Server et prise en main du shell

## Exercice 2 - Prise en main de l’interpréteur de commandes 

Manuel
1.	La commande which produit le chemin complet des commandes du shell. Si elle ne peut pas reconnaitre la commande donnée.
2.	Page du mannuel : man + nom de la commande, en l’occurrence « man which »
3. La première page de la section 6 du manuel  : man 6 intro
Description : « Section 6 of the manual describes the games and funny little programs available on the system. »

Navigation dans l’arborescence
1.	cd /var/log 
2.	 cd ..
3.	 cd
4.	cd -
5.	 5.	Accès refusé : pas d'autorisations pour ce dossier.
6.	 Commande sudo non reconnue. Il faut installer le package.
7.	
```bash
cd ..
mkdir Dossier1 Dossier2
cd Dossier1
touch Fichier1
cd Dossier2
mkdir Dossier2.1
mkdir Dossier 2.2
cd Dossier2.2
touch Fichier2
touch Fichier3
```

8.	Impossible de supprimer le Fichier1 depuis le dossier personnel. Impossible supprimer le Dossier1 : la commande rm permet de supprimer des fichiers seulement.
9.	Rmdir supprime un dossier mais seulement s’il est vide.
10.	Dossier2 n’étant non vide : impossible de le supprimer.
11. rm –r Dossier2 : supprimer le dossier.

Commandes importantes
1.	 affichage de l'heure : date +%t
2.	 Fichiers commençants par un point :fichiers cachés.
3.	 Chemin pour ls : /usr/bin/ls
4.	 ll : droits de chaque utilisateur (lecture/suppression /exécution). Commande manuelle de ll : ls -alF
5.	 Contenu du dossier /bin on fait : ls /bin 
6.	 Ls .. : Dossiers et fichers précédents.
7.	 Chemin complet du dossier courant : pwd -> chemin : /home/User
8.	 La commande echo ‘bip’ > plop exécutée 2 fois : le mot bip dans le fichier plop.
9.	 La commande ajoute le bip à la fin du fichier tandis que la commande avec un seul >  écrase le fichier.
10.	 Concaténation des deux commandes. C’est pourquoi on voit s’afficher ‘toto’ et le terminal attendre 10 secondes.
11.	 Commande file : type du fichier choisie.
12.	 Cela produit une copie du fichier original et lorsqu’on modifie original, cela modifie lien_phy mais lorsqu’on le supprime, cela ne le supprime pas.
13.	 De la même manière, cela produit une copie du fichier mais cette fois-ci lorsqu’on supprime le fichier, on ne peut plus accéder au fichier.
14.	 Afficher le fichier syslog : Commande cd /var/log et cat syslog. arreter le défilement et le reprendre on fait la commande : tail -f
15.	 head -5 syslog : 5 premières lignes du fichiers et tail -15 syslog : les 15 dernières lignes. Pour les lignes 10 à 20 on utilise : cat syslog | tail –n +10 | head –n 10
16.	 dmesg | less : les logs dans un lecteur de fichier plus facile d’utilisation.
17.	 /etc/passwd : noms de tous les utilisateurs.  page de manuel du fichier : man -5 psswd
18.	  cat /etc/passwd | awk '{ print $1 }' | sort -r
19. cat /etc/passwd | wc -l
20. Man -k conversion | wc -l
21. Find / -name passwd
22. Find / -name passed 2>/dev /null > ˜/list_passwd_files.txt
23. Grep « alias ll=«  -r ˜, il se trouve dans «˜/.bashrc »
24. Impossible d’installer locate
25. Impossible d’installer locate
	
 
## Exercice 3 - Découverte de l’éditeur de texte nano 
1.	Touch log.txt : créer le fichier. cp /var/log/syslog log.txt. ouvrir le fichier : nano log.txt
2.	Remplacer le mot kernel par noyau : Ctrl \ kernel noyau A
3.  Alt + A et Ctrl + K et  Ctrl + U 	 
4.	Alt U : annuler l’action précédente

## Exercice 4 - Personnalisation du shell 

Questions 1 à 3 : tests de commandes 
4. \A[\033[01;35m] - \u@\h[\033[32m]:[\033[01;34m]\w[\033[36m]$




