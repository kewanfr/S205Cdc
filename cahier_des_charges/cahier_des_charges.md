<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Cahier des charges fonctionnel - Application HACCP pour les cuisines collectives

## Entête
- Groupe de TD : 4
- Date de démarrage : 28 mai 2025 15h
- Version : 0.1.0  *Il s'agit d'un numéro de version logique en visant d'arriver à la version 1.0 le jour du rendu (git gère une autre numérotation pour le versionnage*) 
- Destinataire : EL MAMOUNI Saïd


| Nom               | Prénom  | Mail                                        |
| ----------------- | ------- | ------------------------------------------- |
| BERNIER           | Kéwan   | kewan.bernier@etu.univ-nantes.fr            |
| BLANCHET          | Alex    | alex.blanchet@etu.univ-nantes.fr            |
| MORICEAU--MOINARD | Pacôme  | pacome.moriceau--moinard@etu.univ-nantes.fr |
| RAYNARD           | Livio   | livio.raynard@etu.univ-nantes.fr            |
| GALLY             | Chianti | chianti.gally@etu.univ-nantes.fr            |



## 1. Présentation générale du problème
### 1.1 Projet
#### 1.1.1 Finalités
#### 1.1.2 Espérance de retour sur investissement
### 1.2 Contexte
#### 1.2.1 Situation du projet par rapport aux autres projets de l’entreprise
#### 1.2.2 Études déjà effectuées
#### 1.2.3 Études menées sur des sujets voisins
#### 1.2.4 Suites prévues
#### 1.2.5 Nature des prestations demandées
#### 1.2.6 Parties concernées par le déroulement du projet et ses résultats (demandeurs, utilisateurs)
#### 1.2.7 Caractère confidentiel s'il y a lieu
### 1.3 Énoncé du besoin 
*(finalités du produit pour le futur utilisateur tel que prévu par le demandeur)*
### 1.4 Environnement du produit recherché
#### 1.4.1 Listes exhaustives des éléments *(personnes, équipements, matières…)* et contraintes *(e.g. environnement)*
##### Capteurs connectés (IoT)

L’application repose sur un réseau de capteurs connectés (IoT) permettant la collecte automatisée des données critiques en lien avec les exigences HACCP. Ces capteurs doivent être sélectionnés en fonction des contraintes spécifiques des cuisines collectives, à savoir : humidité, température extrême, graisses, nettoyages fréquents, connexions instables.

**Types de capteurs envisagés** :

- **Capteurs de température** : placés dans les réfrigérateurs, congélateurs ou chambres froides pour vérifier le respect de la chaîne du froid.
- **Capteurs d’humidité** : mesurent l’hygrométrie ambiante pour éviter les zones favorables au développement microbien.
- **Capteurs de présence / mouvement** : détectent les interventions de nettoyage ou les ouvertures de portes.
- **Lecteurs RFID / codes-barres** : assurent la traçabilité des denrées alimentaires.



#### 1.4.2 Caractéristiques pour chaque élément de l’environnement
##### Capteurs connectés (IoT)
**Contraintes fonctionnelles et techniques** :

- **Connectivité** : Bluetooth Low Energy (BLE) pour compatibilité mobile, WiFi si disponible ; possibilité d’extension à LoRa dans des environnements plus vastes.
- **Autonomie** : minimum 6 mois avec batterie intégrée, fréquence d’envoi ajustable selon le niveau de criticité des données.
- **Robustesse** : matériel certifié IP65 ou plus (résistance à l’eau, à la vapeur, aux projections de graisse).
- **Fiabilité** : précision attendue de ±0,5 °C pour les capteurs de température, fiabilité de transmission supérieure à 98 %.
- **Sécurité** : chiffrement des données (AES-256), appairage sécurisé, identification unique des capteurs.

**Fonctionnement hors-ligne** : les capteurs doivent pouvoir continuer à stocker ou transmettre leurs données à l’application même en cas de perte de réseau, avec synchronisation dès rétablissement de la connexion.

Ces capteurs forment la base technique de la surveillance HACCP automatisée. Leur sélection devra répondre aux exigences de fiabilité, d’autonomie et de sécurité tout en respectant les contraintes d’environnement des cuisines collectives.

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
##### 2.1.1.1 Description et détail

##### 2.1.1.2 Critères d’appréciation et les niveaux qui les caractérisent 
*(Niveaux dont l’obtention est imposée)*

*(Niveaux souhaités mais révisables)*
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


