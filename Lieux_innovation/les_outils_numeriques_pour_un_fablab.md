# OUTILS NUMÉRIQUES POUNE FABLAB

Contenus adaptés en cours de formalisation en format patterns.


## MATÉRIEL INFORMATIQUE

Pour la gestion des matériels informatiques, GLPI + FusionInventory remplissent leur office(*)

## WIKI

Nous avions un dokuwiki (un peu cassé dernièrement) pour permettre aux membres de documenter leurs réalisations sous licence CC-by-SA ;  nous nous orientons plutôt vers [wikifab](http://wikifab.org/w/index.php/Wikifab:Developers) basé sur mediawiki et [assez joli](http://wikifab.org/wiki/Accueil) :

- il simplifie l'interface pour les membres (pas de connaissance spécifique de mediawiki et guide pour remplir une page de documentation de son projet, taggué selon les technologies et rattaché à un groupe
- capacité à l'instancier sur notre serveur, ce qui évite de transmettre l'intégralité de notre base d'adhérents à un service centralisé
- il conserve les avantages de mediawiki et il y a des outils de migration de dokuwiki vers mediawiki
- il n'y a pas de forum communautaire mais notre contact avec les développeurs à la _Maker Faire_ de la Villette en Juin 2017 nous a encouragé à travailler avec eux

## SITE WEB

Le site web principal a été migré sur le nouveau serveur, en conservant wordpress :

- l'agenda par défaut  est peu pratique pour les événements récurrents chaque semaine (il faut créer tous les événements plutôt que donner une période et un jour)
- l'utilisation d'une carte openstreetmap reste à mettre en place (le greffon googlemaps a été utilisé par défaut o_O)
- des greffons telegram ou plutôt mastodonte seraient nécessaires
- les greffons facebook et twitter ne demandent qu'à être remplacés
- un greffon meetup pourrait être utile (et une autre plateforme plus pratique)

## CLOUD

Notre migration de owncloud vers nextcloud a fonctionné :

- tous les documents sont disponibles et la synchro est opérationnelle
- nous regardons l'ajout de l'agenda au besoin, plutôt que dans wordpress
- le greffon pour les photos nous évitera de remettre en place un piwigo (nous souhaitons à l'IT diminuer le nombre de logiciels utilisés si un existant fait le taf')

(*) pour GLPI, ce sont de l'ordre de 60 portables / PC fixes sur 2 sites qui sont actuellement gérés :

- déjà un recensement de l'existant, affecté à des groupes : ateliers, utilisation au FabLab, spécifique matériel (découpe laser, CNC, graveuse laser, ateliers scratch ou arduino) mais cela fonctionne pour les matériels complets ayant démarré et installés, moins bien pour le matos qui a des glitchs (manque disque dur, écran défaillant, mémoire défaillante) et qui devrait être rentré manuellement + mettre une action pour améliorer la situation
- les fonctions de réservation de matériel pourraient être intéressantes :
  - recenser les matériels pouvant être réservés, déléguer la gestion des réservations (à tester), gérer les matériels non informatique pouvant être prêtés
  - inventaire manuel à tester
  - reste à tester l'interface avec de vrais utilisateurs (GLPI étant par nature très orienté IT...), surtout pour l'aspect réservation et complétude de ce qui est disponible par atelier (groupe ?)
- nous souhaitons éviter FabManager côté IT : 
  - intéressant fonctionnellement (réservation de ressource, gestion des membres, contacts entre membres), 
  - mais c'est un docker (difficulté de mise à jour) et c'est la foire aux logiciels à gérer (aussi complexe qu'un mailman 3 que nous avons déjà)
- GLPI à rendre plus joli : la migration en 9.2 va rénover le 0.84 de debian jessie déployé actuellement et utilisé uniquement par 2 personnes... 
- si vous avez un retour d'expérience ou des exemples utilisables par le commun des mortels, je suis preneur :D Sur stretch idéalement.

## LOGICIELS

Pour la gestion des membres :

- grisbi côté comptabilité
- fusiondirectory pour la gestion de l'authentification et des droits utilisateur
- mailing-lists via mailman 3 (améliorable, pour traduction en français, gestion des spams, conso mémoire on a passé la VM à 4 Go de RAM pour s'éviter l'OOMK :D).


## Source

Adapté à partir de:

URL:     https://linuxfr.org/users/baud/journaux/les-outils-de-l-it-pour-un-fablab

Title:   Les outils de l'IT pour un FabLab
Authors: BAud
Date:    2017-11-02T19:15:43+01:00
License: CC by-sa


