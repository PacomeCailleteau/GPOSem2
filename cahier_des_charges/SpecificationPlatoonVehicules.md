*Ce document est une structure de base, classique pour rédiger un cahier des charges. Elle est un peu différente de celle vue en TD. Elle n’est pas tout à fait standard non plus en couvrant davantage d’éléments qu’un cahier des charges normal (en particulier le Gantt est fait plus tard normalement, à part ses jalons)
Tout ce qui est en italique doit être remplacé. Chaque section doit contenir au moins un paragraphe. Certaines choses sont à imaginer, en se documentant un minimum pour être réaliste.*

<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Cahier des charges fonctionnel - Platoon de véhicules

## Entête
- Groupe de TD : Groupe 4
- Date de démarrage : 28/04/2022
- Version : *Il s'agit d'un numéro de version logique en visant d'arriver à la version 1.0 le jour du rendu (git gère une autre numérotation pour le versionnage*
- Destinataire : Florent CORDEAU

|Nom | Prénom | mail
| ------ | ------ | ------ |
| PAYET | Lucas | lucas.payet@etu.univ-nantes.fr |
| DELHOMMEAU | Lilian | lilian.delhommeau@etu.univ-nantes.fr |
| CAILLETEAU | Pacôme | pacome.cailleteau@etu.univ-nantes.fr |
| LEBOEUF | Arnaud | arnaud.leboeuf@etu.univ-nantes.fr |


## 1. Présentation générale du problème
Nous souhaitons développer un modèle de voitures autonomes capable de se suivre et de communiquer entre elles.
Pour ce faire, nous commençons par développer une maquette des prototypes.
### 1.1 Projet
Nous allons mettre en place une maquette fait à partir d'au moins trois robots. Le premier conducteur sera simuler par la télécommande. Il pourront éviter les obstacles et optmiser leur vitesses et déplacements.
Projet de véhicules autonomes connectés entre eux

#### 1.1.1 Finalités
A terme nous espérons que la maquette puissent arriver au stade de modèle concret pour la mise en place dans la réalité.
(bon)
#### 1.1.2 Espérance de retour sur investissement
Nous espérons que le projet apportera une meilleure image pour l'entreprise et une satifaction du client.
Nous espérons également que le projet soit rentable pour l'entreprise.
(bon)
### 1.2 Contexte
Les technologies évoluent rapidement et peuvent actuellement permettre de sauver des vies. Le projet vise donc à utiliser ces technologies pour sécuriser le déplacement des véhicules.
#### 1.2.1 Situation du projet par rapport aux autres projets de l’entreprise

Le projet n'est pas prioritaire mais est phase de maquette, et une bonne partie de nos employés travaille activement sur la réalisation de cette maquette.
Ce projet est pour nous essentiel car il permettrait de révolutionner nos véhicules et de permettre une nouvelles fonctionnalités non négligeables qui augmenterait de 
manière considérable notre chiffre d'affaires et attirerait plus de clients sur notre gammes de véhicules.
Cependant, ce projet reste risqué et coûteux et reste au niveau maquette pour le moment, l'investissement mis dans ce projet est donc très raisonnables par rapport aux autres projets de l'entreprises dont
les risques et les bénéfices sont déjà bien connus.
(bon)
#### 1.2.2 Études déjà effectuées
La société Scania a déjà étudiées les platoons de camion semi-autonomes : https://www.youtube.com/watch?v=n0SXO_hzYDY
Sur le plan des études sur les voitures autonomes qui nous sont utile pour le platoon, Tesla a aussi inové et fait des recherches sur la voiture autonome : https://www.youtube.com/watch?v=1-XxCiaurms
(bon)
#### 1.2.3 Études menées sur des sujets voisins
Par exemple, des études ont été menées pour un bus autonome à la RATP : https://www.youtube.com/watch?v=Uym44SKFByE
(bon)
#### 1.2.4 Suites prévues
Nous prévoyons de créer une application de covoiturage utilisant cette technologie et également un système de demande de voiture à distance mais pour cette dernière les lois actuelles nous l'interdisent.
(bon)
#### 1.2.5 Nature des prestations demandées
Réalisation d'un platoon de véhicule sécurisé.
#### 1.2.6 Parties concernées par le déroulement du projet et ses résultats (demandeurs, utilisateurs)
Les demandeurs sont les grands constructeurs automobile comme Renaud, Citroën, Peugeot, ...
Les utilisateurs seront les familles voulant d'un moment convivial en voiture ou encore les conducteurs nocturnes.
#### 1.2.7 Caractère confidentiel s'il y a lieu
Secret sur les technologies utilisées.
(bon)
### 1.3 Énoncé du besoin 
Suivre automatiquement des véhicules aillant également cette technologie permettant au conducteur de se reposer ou de passer du temps avec les passagers présent à bord.
*(finalités du produit pour le futur utilisateur tel que prévu par le demandeur)*
(bon)
### 1.4 Environnement du produit recherché
Le produit est destiné aux adultes de tout âges plutôt aisées.
(bon)
#### 1.4.1 Listes exhaustives des éléments *(personnes, équipements, matières…)* et contraintes *(e.g. environnement)*
Contrainte environnementale (non affectation de la faune et de la flore), contrainte économique (coût de création du produit), fréquence des ondes des appareils électroniques.
(bon)
#### 1.4.2 Caractéristiques pour chaque élément de l’environnement
-Fréquences d'ondes qui ne doivent pas perturber les animaux ni les personnes à bord de la voiture.
-Prise en compte des usagers non liés avec la voiture et d'éventuels accidents.
-Reprise facile du contrôle du véhicule.
(bon)
## 2. Expression fonctionnelle du besoin

*Le __Diagramme de cas d’utilisation__, à priori chaque cas d’utilisation correspond à une fonction. Le diagramme de cas d’utilisation inclut la description détaillée de chaque cas d’utilisation (cf. cours de CO-C).*

*Chaque fonction doit être classée selon différents critères :*
- *coefficient de pondération (de 1 à 5) : selon la valeur, l’importance de la fonction*
- *critère d’appréciation : comment sera apprécié le succès de la réalisation d’une fonction (« doit rendre le résultat correct en moins de x sec. »)*
- *niveau d’un critère d’appréciation (« x de 1 à 3 sec. Acceptables »)*
- *niveau de flexibilité (« 90% dans l’intervalle, 10% à 1 sec. au delà »)*
*On peut regrouper les fonctions dans le __tableau fonctionnel__ selon ces critères puis détailler chacune des fonctions dans les sous-sections suivantes*

### 2.1 Fonctions de service et de contrainte
#### 2.1.1 Fonctions de service principales 
*(qui sont la raison d’être du produit)*
-Fonction principale 1: Se suivre. (5)
-Fonction principale 2: Gérer leur vitesse. (4)
-Fonction principale 3: Gérer leur déplacement. (4)
##### 2.1.1.1 Description et détail
-Fonction 1: Les robots doivent pouvoir rejoindre le convoi mais doivent aussi pouvoir le quitter.
-Fonction 2: Les robots doivent communiquer les informations concernant leur vitesse.
-Fonction 3: Les robots doivent contrôler leur déplacement pour rester rattacher au convoi.

##### 2.1.1.2 Critères d’appréciation et les niveaux qui les caractérisent 
*(Niveaux dont l’obtention est imposée)*
-Fonction 1: Critère 1: Le convoi doit pouvoir atteindre une grande taille.
-Fonction 2: Critère 1: Les robots doivent pouvoir échanger un grand nombre d'information; Critère 2: Les informations doivent circuler rapidement.
-Fonction 3: Critère 1: Les robots doivent pouvoir changer de direction et/ou de vitesse rapidement.



#### 2.1.2 Fonctions de service complémentaires 

*(qui améliorent, facilitent ou complètent le service rendu)*
##### 2.1.2.1 Description et détail
##### 2.1.2.2 Critères d’appréciation et les niveaux qui les caractérisent 
*(Niveaux dont l’obtention est imposée)*

*(Niveaux souhaités mais révisables)*
#### 2.1.3 Contraintes 
*(limitations à la liberté du concepteur-réalisateur)*

## 3. Cadre de réponse
*__Diagramme de classes métiers__ : à base de classes métiers (des concepts indépendants de la programmation, avec des attributs mais sans méthodes, ainsi que des relations entre les concepts sur les agissements des classes métiers les unes sur les autres)*

*Synthèse des jalons : __tables synthétiques des jalons__ du projet.*
### 3.1 *Pour chaque fonction : fonction 1*
#### 3.1.1 Solution proposée
*Tâches à réaliser pour la solution -> __WBS__*

*Description de __scénarios__ (potentiellement avec un Diagramme de séquence)*

*__Jalon__ : date à laquelle la fonction doit être livrée.*
#### 3.1.2 Niveau atteint pour chaque critère d’appréciation de cette fonction et modalités de contrôle
#### 3.1.3 Part du prix attribué à chaque fonction
### 3.2 *Pour chaque fonction : fonction 2*
#### Etc.
### 3.x Pour l’ensemble du produit
#### 3.x.1 Prix de la réalisation de la version de base
*Ici, il faut imaginer en faisant une petite étude de marchée (cf des sites marchands spécialisés)*
#### 3.x.2 Options et variantes proposées non retenues au cahier des charges
#### 3.x.3 Mesures prises pour respecter les contraintes et leurs conséquences économiques
#### 3.x.4 Outils d’installation, de maintenance … à prévoir
#### 3.x.5 Décomposition en modules, sous-ensembles
#### 3.x.7 Perspectives d’évolution technologique
## 4 Prévisions de fiabilité – Gestions des risques
### 4.1 Risques à la réalisation
*__Profils de risques__ pour chaque fonction de service*


#| 0 | Degré du risque pour la fonction |

|Nature du Risque| 0 | 1 | 2 | 3 | 4 | 5 |
| ------ | ------ | ------ | ------ | ------ | ------ |
| Taille de la fonction | 0 | 0 | 0 | 0 | 0 |
| Taille de la fonction | 0 | 0 | 0 | 0 | 0 |
| Taille de la fonction | 0 | 0 | 0 | 0 | 0 |
| Taille de la fonction | 0 | 0 | 0 | 0 | 0 |
| Taille de la fonction | 0 | 0 | 0 | 0 | 0 |

### 4.2 Prévision des défaillances
*Table de défaillance pour chaque fonction de service avec un paragraphe commentant chaque défaillance et/ou chaque cause/effet/détection d’importance notable*
### 4.3 Gestion des défaillances

*La __Matrice de criticité__*
*Pour chaque défaillance critique (en zone noire ou proche), un paragraphe expliquant comment
- L’empêcher
- Alerter que elle est en voie de se produire
- Réagir quand elle s’est produite*


## 5 Annexe
*Le planning ne fait pas partie de la norme car sa décomposition n’importe pas au client à cette phase du projet. Il n’est alors intéressé que par les jalons qui ponctuent la réalisation des différentes fonctionnalités.
Nous placerons donc le __diagrammes de Gantt__ ici.*


