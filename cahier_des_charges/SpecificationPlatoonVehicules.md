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
Nous allons mettre en place une maquette fait à partir d'au moins trois robots. Le premier conducteur sera simulé par la télécommande. Ils pourront éviter les obstacles et optmiser leur vitesse et leurs déplacements.
Projet de véhicules autonomes connectés entre eux.
#### 1.1.1 Finalités
A terme nous espérons que la maquette puissent arriver au stade de modèle concret pour la mise en place dans la réalité.
#### 1.1.2 Espérance de retour sur investissement
Nous espérons que le projet apportera une meilleure image pour l'entreprise et une satifaction du client.
Nous espérons également que le projet soit rentable pour l'entreprise.
### 1.2 Contexte
Les technologies évoluent rapidement et peuvent actuellement permettre de sauver des vies. Le projet vise donc à utiliser ces technologies pour sécuriser le déplacement des véhicules.
#### 1.2.1 Situation du projet par rapport aux autres projets de l’entreprise
Le projet n'est pas prioritaire mais est phase de maquette, et une bonne partie de nos employés travaille activement sur la réalisation de cette maquette.
Ce projet est pour nous essentiel car il permettrait de révolutionner nos véhicules et de permettre une nouvelles fonctionnalités non négligeables qui augmenterait de 
manière considérable notre chiffre d'affaires et attirerait plus de clients sur notre gammes de véhicules.
Cependant, ce projet reste risqué et coûteux et reste au niveau maquette pour le moment, l'investissement mis dans ce projet est donc très raisonnables par rapport aux autres projets de l'entreprises dont
les risques et les bénéfices sont déjà bien connus.
#### 1.2.2 Études déjà effectuées
La société Scania a déjà étudiées les platoons de camion semi-autonomes : https://www.youtube.com/watch?v=n0SXO_hzYDY.
<br/>Sur le plan des études sur les voitures autonomes qui nous sont utile pour le platoon, Tesla a aussi inové et fait des recherches sur la voiture autonome : https://www.youtube.com/watch?v=1-XxCiaurms.
#### 1.2.3 Études menées sur des sujets voisins
Par exemple, des études ont été menées pour un bus autonome à la RATP : https://www.youtube.com/watch?v=Uym44SKFByE.
#### 1.2.4 Suites prévues
Nous prévoyons de créer une application de covoiturage utilisant cette technologie et également un système de demande de voiture à distance mais pour cette dernière les lois actuelles nous l'interdisent.
#### 1.2.5 Nature des prestations demandées
Réalisation d'un platoon de véhicule sécurisé.
#### 1.2.6 Parties concernées par le déroulement du projet et ses résultats (demandeurs, utilisateurs)
Les demandeurs sont les grands constructeurs automobile comme Renaud, Citroën, Peugeot, etc.
Les utilisateurs seront les familles voulant un moment convivial en voiture ou encore les conducteurs nocturnes.
#### 1.2.7 Caractère confidentiel s'il y a lieu
Secret sur les technologies utilisées.
### 1.3 Énoncé du besoin 
Suivre automatiquement des véhicules aillant également cette technologie, permettant au conducteur de se reposer ou de passer du temps avec les passagers présent à bord.
<br/>*(finalités du produit pour le futur utilisateur tel que prévu par le demandeur)*
### 1.4 Environnement du produit recherché
Le produit est destiné aux adultes de tout âges plutôt aisées.
#### 1.4.1 Listes exhaustives des éléments *(personnes, équipements, matières…)* et contraintes *(e.g. environnement)*
Contrainte environnementale (non affectation de la faune et de la flore), contrainte économique (coût de création du produit), fréquence des ondes des appareils électroniques.
#### 1.4.2 Caractéristiques pour chaque élément de l’environnement
-Les fréquences d'ondes ne doivent pas perturber les animaux ni les personnes à bord du véhicule.
<br/>-Prise en compte des usagers non liés avec le véhicule et prise en compte d'éventuels accidents.
<br/>-Reprise facile du contrôle du véhicule.
## 2. Expression fonctionnelle du besoin

*Le __Diagramme de cas d’utilisation__, à priori chaque cas d’utilisation correspond à une fonction. Le diagramme de cas d’utilisation inclut la description détaillée de chaque cas d’utilisation (cf. cours de CO-C).*


<img src=../pictures/cas_utilisation.png alt="cas_utilisation" width="500"/>

*Chaque fonction doit être classée selon différents critères :*
- *coefficient de pondération (de 1 à 5) : selon la valeur, l’importance de la fonction*
- *critère d’appréciation : comment sera apprécié le succès de la réalisation d’une fonction (« doit rendre le résultat correct en moins de x sec. »)*
- *niveau d’un critère d’appréciation (« x de 1 à 3 sec. Acceptables »)*
- *niveau de flexibilité (« 90% dans l’intervalle, 10% à 1 sec. au delà »)*
*On peut regrouper les fonctions dans le __tableau fonctionnel__ selon ces critères puis détailler chacune des fonctions dans les sous-sections suivantes*

### 2.1 Fonctions de service et de contrainte
#### 2.1.1 Fonctions de service principales
*(qui sont la raison d’être du produit)*
<br/>-Fonction principale 1: Se suivre. (5)

-Fonction principale 2: Gérer leur vitesse. (4)

-Fonction principale 3: Gérer leur déplacement. (4)

##### 2.1.1.1 Description et détail
Fonction 1: Les robots doivent pouvoir rejoindre le convoi mais doivent aussi pouvoir le quitter.
<br/>Fonction 2: Les robots doivent communiquer les informations concernant leur vitesse.
<br/>Fonction 3: Les robots doivent contrôler leur déplacement pour rester rattacher au convoi et éviter les obstacles.

##### 2.1.1.2 Critères d’appréciation et les niveaux qui les caractérisent 
*(Niveaux dont l’obtention est imposée)*
<br/>-Fonction 1: Critère 1: Le convoi ne doit pas dépasser une certaine taille. Taille préférable: 3 véhicule  avec une marge de +/- 1.
<br/>-Fonction 2: Critère 1: Les robots doivent pouvoir échanger un grand nombre d'information. Quantité d'information: 50 Mo avec une marge de +/- 5 Mo.
<br/>Critère 2: Les informations doivent circuler rapidement. Temps d'échange: 10ms avec marge de +/- 3 ms.
<br/>-Fonction 3: Critère 1: Les robots doivent pouvoir changer de direction rapidement. Temps de réaction: 17ms avec marge de +/- 2ms.

#### 2.1.2 Fonctions de service complémentaires 
*(qui améliorent, facilitent ou complètent le service rendu)*
<br/>-Fonction complémentaire 1: Communication entre passagers (3)
<br/>-Fonction complémentaire 2: Vue du convoi (1)

##### 2.1.2.1 Description et détail
-Fonction 1: Les robots peuvent s'envoyer des messages entre eux.
<br/>-Fonction 2: Les robot peuvent voir leur place dans le convoi et une vue de haut.
##### 2.1.2.2 Critères d’appréciation et les niveaux qui les caractérisent 
*(Niveaux dont l’obtention est imposée)*
<br/>-Fonction 1: Critère 1: Ils doivent recevoir un grand nombre de caractères. Taille du message: 200 caractères avec une marge de 10 caractères.

*(Niveaux souhaités mais révisables)*
<br/>-Fonction 2: Critère 1: Les robots peuvent voir leur place dans le convoi et une vue de haut. Vue autour du véhicule 20m autour +-3m.
#### 2.1.3 Contraintes 
*(limitations à la liberté du concepteur-réalisateur)*<br/>
En termes des contraintes, nous nous limiterons à nos robots Lego pour la maquette. Le robot en tête du convoi sera contrôlé par une télécommande. <br/>
Pour les obstacles, nous nous contenterons de représenter 2 obstacles majeurs qu'on retrouve sur la route: un objet en mouvement qui passe devant le véhicule, et un nid de poule.

## 3. Cadre de réponse
*__Diagramme de classes métiers__ : à base de classes métiers (des concepts indépendants de la programmation, avec des attributs mais sans méthodes, ainsi que des relations entre les concepts sur les agissements des classes métiers les unes sur les autres)*

<img src=../pictures/DDC.png alt="Diagramme de classe" width="1000"/>

*Synthèse des jalons : __tables synthétiques des jalons__ du projet.*

| Jalon 1 | Jalon 2 | Jalon 3
| ------ | ------ | ------ |
| Fin Analyse | Fin Développement | Fin Construction |


### 3.1 *Pour chaque fonction : fonction 1 (Se suivre)*
#### 3.1.1 Solution proposée
*Tâches à réaliser pour la solution -> __WBS__*

<img src=../pictures/WBS_F1.png alt="WBS Fonction 1" width="1000"/>

*Description de __scénarios__ (potentiellement avec un Diagramme de séquence)*

<img src=../pictures/DiagrammeDeSequenceF1.png alt="Diagramme de séquence" width="1000"/>

*__Jalon__ : Doit être livrée le 19/07 maximum (fin du codage)*

#### 3.1.2 Niveau atteint pour chaque critère d’appréciation de cette fonction et modalités de contrôle
Critère 1 : Le système fonctionne parfaitement jusqu'à 7 véhicules et commence a avoir des ralentissements, notre objectif de 2 à 4 véhicules est donc valide. <br/>
Il faut contrôler le prix des équipements utilisés, le temps d'installation de la fonction et le fait qu'elle fonctionne sans risque pour les usagers.
#### 3.1.3 Part du prix attribué à la première fonction
5/10 du budget
### 3.2 *Pour chaque fonction : fonction 2 (Gérer leur vitesse)*
#### 3.2.1 Solution proposée
*Tâches à réaliser pour la solution -> __WBS__*

<img src=../pictures/WBS_F2.png alt="WBS fonction 2" width="1000"/>

*Description de __scénarios__ (potentiellement avec un Diagramme de séquence)*

<img src=../pictures/DiagrammeDeSequenceF2.png alt="Diagramme de séquence fonction 2" width="1000"/>

*__Jalon__ : Doit être livrée le 9/07 maximum.*

#### 3.2.2 Niveau atteint pour chaque critère d’appréciation de cette fonction et modalités de contrôle
Critère 1 : La quantité d'information envoyé est de 53Mo/s.<br/>
Critère 2 : Le temps de latence est de 12ms.<br/>
Il faut contrôler le prix des équipements utilisés, le temps d'installation de la fonction et le fait qu'elle envoie assez d'informations aux autres véhicules pour qu'ils puissent réagit de la meilleur manière possible.
#### 3.2.3 Part du prix attribué à la fonction 2
2/10 du budget
### 3.3 *Pour chaque fonction : fonction 3 (Gérer leur déplacement)*
#### 3.3.1 Solution proposée
*Tâches à réaliser pour la solution -> __WBS__*

<img src=../pictures/WBS_F3.png alt="WBS fonction 3" width="1000"/>

*Description de __scénarios__ (potentiellement avec un Diagramme de séquence)*

<img src=../pictures/DiagrammeDeSequenceF3.png alt="Diagramme de séquence fonction 3" width="1000"/>

*__Jalon__ : Doit être livrée le 11/07 maximum.*

#### 3.3.2 Niveau atteint pour chaque critère d’appréciation de cette fonction et modalités de contrôle
Critère 1 : Les informations partagés dans le groupent mettent 16ms à atteindre tout les véhicules, c'est donc un succès.<br/>
Il faut contrôler le prix des équipements utilisés, le temps d'installation et le fait qu'elle envoie assez d'informations aux autres véhicules pour qu'ils puissent réagit de la meilleur manière possible.
#### 3.3.3 Part du prix attribué à la fonction 3
3/10 du budget

### 3.x Pour l’ensemble du produit
#### 3.x.1 Prix de la réalisation de la version de base
*Ici, il faut imaginer en faisant une petite étude de marchée (cf des sites marchands spécialisés)* <br/>
Salariés : 200 000€ (50 salariés x 2 mois de travail à 2000€) <br/>
Matériels : 500 000€ <br/>
Autre frais (électricité, loyer ..) : 1 000 000€ <br/>
Total : 1 700 000€

#### 3.x.2 Options et variantes proposées non retenues au cahier des charges
Pouvoir partager et recevoir les itinéraires des véhicules du platoon. <br>
Pouvoir communiquer par un tchat textuel local aux autres véchiules.

#### 3.x.3 Mesures prises pour respecter les contraintes et leurs conséquences économiques
Pour rester dans notre budget, lors des tests, nous nous assurerons que nos robots ne se cassent pas, pour ainsi éviter d'en refaire.<br/>
Lors des tests pour simuler un fossé ou un nid de poule, nous utiliserons les rebords d'une table. Pour éviter que le robot ne se casse s'il y a une chute, nous installerons des matelas pour amortir sa chute. Les objets en mouvement sur la route seront simuler par une balle passant devant le convoi, cela nous évitera de devoir construire un autre robot.
Nous nous assurerons aussi d'utiliser au maximum nos pièces de construction. Pour être dans les temps, nos test seront coder en parallèle du code principale.

#### 3.x.4 Outils d’installation, de maintenance … à prévoir
Pour l'installation et la maintenance, il faut prévoir une maquette de route avec des obtacles, des voitures LEGO, un ordinateur qui sert de télécommande.
#### 3.x.5 Décomposition en modules, sous-ensembles
<img src=../pictures/WBS_Projet.png alt="Diagramme de Gantt" width="10000"/>

#### 3.x.7 Perspectives d’évolution technologique
Pouvoir permettre au platoon d'accepter d'autres véhicules que les voitures (ex: Moto, camping-car).

## 4 Prévisions de fiabilité – Gestions des risques
### 4.1 Risques à la réalisation
*__Profils de risques__ pour chaque fonction de service*


Degré du risque de la fonction principale 1
|Nature du Risque| 0 | 1 | 2 | 3 | 4 | 5 
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| Taille de la fonction | 0 | 0 | 0 | 0 | 0 | 1 |
| Difficulté technique | 0 | 0 | 0 | 0 | 1 | 0 |
| Degré d’intégration | 0 | 0 | 0 | 0 | 1 | 0 |
| Configuration organisationnelle | 0 | 0 | 1 | 0 | 0 | 0 |
| Changement | 0 | 1 | 0 | 0 | 0 | 0 |
| Instabilité de l’équipe de projet | 0 | 0 | 1 | 0 | 0 | 0 |


Degré du risque de la fonction principale 2
|Nature du Risque| 0 | 1 | 2 | 3 | 4 | 5 
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| Taille de la fonction | 0 | 0 | 0 | 0 | 1 | 0 |
| Difficulté technique | 0 | 0 | 0 | 0 | 1 | 0 |
| Degré d’intégration | 0 | 0 | 0 | 1 | 0 | 0 |
| Configuration organisationnelle | 0 | 0 | 1 | 0 | 0 | 0 |
| Changement | 0 | 1 | 0 | 0 | 0 | 0 |
| Instabilité de l’équipe de projet | 0 | 1 | 0 | 0 | 0 | 0 |


Degré du risque de la fonction principale 3
|Nature du Risque| 0 | 1 | 2 | 3 | 4 | 5 
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| Taille de la fonction | 0 | 0 | 0 | 0 | 1 | 0 |
| Difficulté technique | 0 | 0 | 0 | 0 | 1 | 0 |
| Degré d’intégration | 0 | 0 | 0 | 1 | 0 | 0 |
| Configuration organisationnelle | 0 | 0 | 1 | 0 | 0 | 0 |
| Changement | 0 | 1 | 0 | 0 | 0 | 0 |
| Instabilité de l’équipe de projet | 0 | 0 | 1 | 0 | 0 | 0 |

### 4.2 Prévision des défaillances
*Table de défaillance pour chaque fonction de service avec un paragraphe commentant chaque défaillance et/ou chaque cause/effet/détection d’importance notable*
Table de de défaillance de la fonction principale 1
| Défaillance Possible | Causes Potentielles | Effets Potentiels de la défaillance | Comment détecter?
| ------ | ------ | ------ | ------ |
| Ne suivent pas le premier robot | Problème de capteur | Danger matériel et humain | Vérification Technique Régulière |
| Ne quitte jamais le convoi | Programme défaillant | Contraint à suivre le premier véhicule | Tester Régulièrement la Fonctionnalité |


----------------------------------------
Table de de défaillance de la fonction principale 2
| Défaillance Possible | Causes Potentielles | Effets Potentiels de la défaillance | Comment détecter?
| ------ | ------ | ------ | ------ |
| Accélère trop/pas assez | Bug dans le programme/Valeurs de vitesse incorrectes | Collision entre les véhicules | Tester le calibrage |


----------------------------------------
Table de de défaillance de la fonction principale 3
| Défaillance Possible | Causes Potentielles | Effets Potentiels de la défaillance | Comment détecter?
| ------ | ------ | ------ | ------ |
| Crémaillère de direction endommagée | Problème mécanique | Dangers pour la sécurité du véhicule et de ses occupants | Contrôle technique régulier de l'appareil |
| Trajectoire mal calculée | Bug dans le programme/Tests insuffisants | Dangers pour la sécurité du véhicule et de ses occupants | Test du programme régulier |




### 4.3 Gestion des défaillances

*La __Matrice de criticité__*16:02 27/05/2022
*Pour chaque défaillance critique (en zone noire ou proche), un paragraphe expliquant comment
- L’empêcher
- Alerter que elle est en voie de se produire
- Réagir quand elle s’est produite*


<img src=../pictures/matriceCritP1.png alt="Matrice de Criticité fonction Principale 1" width="500"/>

----------------------------------------
<img src=../pictures/matriceCritP2.png alt="Matrice de Criticité fonction Principale 2" width="500"/>

Défaillance critique (fonction Principale 2, défaillance 1) : Accélère trop/pas assez

Pour empêcher cette défaillance critique d'avoir lieu, on peut mettre en place un système de calcul de distance avec le véhicule de devant pour empêcher les collisions et corriger la vitesse.<br/>
Pour alerter sur cette défaillance critique, on peut mettre en place une alerte sonore et visuelle quand la distance entre le véhicule de devant ou le véhicule de derrière est trop petite.<br/>
Pour réagir à cette défaillance critique on peut redonner immédiatement le contrôle au conducteur.

----------------------------------------
<img src=../pictures/matriceCritP3.png alt="Matrice de Criticité fonction Principale 3" width="500"/>

Défaillance critique (fonction Principale 3, défaillance 2) : Trajectoire mal calculée

Pour empêcher cette défaillance critique d'avoir lieu, on peut mettre en place un système d'auto-correction de la trajectoire.<br/>
Pour alerter sur cette défaillance critique, on peut mettre en place une alerte sonore et visuelle quand la trajectoire actuelle du véhicule ne correspond pas à la trajectoire de la route.<br/>
Pour réagir à cette défaillance critique on peut redonner immédiatement le contrôle au conducteur.


## 5 Annexe
Le planning ne fait pas partie de la norme car sa décomposition n’importe pas au client à cette phase du projet. Il n’est alors intéressé que par les jalons qui ponctuent la réalisation des différentes fonctionnalités.
Nous placerons donc le diagrammes de Gantt ici.

<img src=../pictures/Gantt.png alt="Diagramme de Gantt" width="10000"/>


