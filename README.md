# Holodeck
Machines Virtuelles Web pour les Ingénieurs de Starfleet
Prêt pour le Retour des Vacances.

Introduction du sujet

À bord de l'USS Enterprise-D, la Fédération des Planètes Unies souhaite
équiper ses ingénieurs du Holodeck de machines virtuelles pour faciliter le
développement de leurs sites web stellaires.

La problématique

Il va falloir créer 2 VM Debian, une qui va servir de Serveur Web, PHP, SQL
et une VM cliente pour tester la partie Web.

Pour la VM Serveur : Debian de base sans interface Graphique – 2 Go RAM –
2vpcu – Disque 32 Go. Avec 2 cartes réseaux (une WAN et une LAN).

Pour la VM Cliente : une Debian avec GUI – 2 Go RAM – 2vcpu – Disque 16 Go
et connecté sur le «LAN» de la VM serveur et un navigateur web.
La VM serveur va servir de Serveur DHCP / DNS (sur la carte «LAN») de serveur



FTP, serveur Web, serveur de base de données SQL et serveur LDAP.

Les contraintes :
- Pas de compte sudo, conformément aux directives de Starfleet.
- Mise en place d'un pare-feu pour autoriser uniquement les ports requis.
- Le serveur Web doit être Nginx et en HTTPS.
- PHP , MariaDB , et Nginx doivent être la dernière version (pas celle des
dépôts Debian).

Pour PHP, la version 7.x et 8.x doivent cohabiter

Mise en place du serveur DHCP/DNS, domaine : starfleet.lan
au Niveau Web :
www8.starfleet.lan ⇒ site web en php8
www7.starfleet.lan ⇒ site web en php7
php.starfleet.lan ⇒ phpMyAdmin
admin.starfleet.lan ⇒ administration de la VM

Un serveur FTP (en SSL/TLS) pour copier les fichiers du serveur Web (chrooté
sur le dossier web).

Création d’un certificat SSL qui serviras pour le serveur Web et le Serveur FTP.

Pour authentifier les Utilisateurs, le serveur Web utilisateur un annuaire LDAP.

Documentation

Faire une procédure pour l’export des VM.
Écrire la notice d’installation et d’utilisation pour l’utilisateur final. (installation
des outils VMWare, Installation des VM... )



Pour aller plus loin

Sur le serveur Web , installez « Visual Studio Code Server » qui devra répondre
sur vscore.starfleet.lan

Développer un script automatisé capable de sauvegarder la configuration
complète de la machine serveur, incluant les paramètres réseau, les services
installés et les configurations spécifiques.

Rendu

Le projet est à rendre sur : https://github.com/prenom-nom/holodeck,
pensez à mettre votre repository en public .

L’évaluation se fera sous forme de présentation avec support à l’équipe
pédagogique.

Base de connaissances

Webmin
Cockpit
Ldap
Php
DNS
FTP
Nginx Proxy



Compétences visées

Virtualisation
Réseau
Système
Sécurité
