<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Cahier des charges fonctionnel - Application HACCP pour les cuisines collectives

## Entête
- Groupe de TD : 4
- Date de démarrage : 28 mai 2025 15h
- Version : 0.1.1
*Il s'agit d'un numéro de version logique en visant d'arriver à la version 1.0 le jour du rendu (git gère une autre numérotation pour le versionnage*) 
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

*A Remplir*

#### 1.1.1 Finalités
Ce projet a pour objectif de développer une application mobile intelligente, destinée aux cuisines collectives afin de faciliter le respect des règles HACCP (Hazard Analysis Critical Control Point). Elle permettra de surveiller de manière en partie automatisée, et en temps réel les pratiques d'hygiène et de sécurité alimentaire à travers:
- Une collecte de données (environnementales, opérationnelles et comportementales)
  C'est à dire le suivi des températures et de l'humidité, la gestion des dates de peremtion, assurer la traçabilité des produits alimentaires, et la gestion des interventions de nettoyage.
- Le traitement de toutes les données à l'aide d'algorithmes et d'Intelligence Artificielle
- La génération d'alertes et de rapports à destination des gestionnaires et autorités compétentes.

#### 1.1.2 Espérance de retour sur investissement

Cette application vise à réduire les risques de non-conformité à l'HACCP. L'objectif est donc la sureté alimentaire pour les clients des cuisines collectives.
En s'assurant de la conformité à l'HACCP, on limite les pertes alimentaires dues à des incidents (rupture de la chaine du froid, erreurs de traçabilité), améliore la productivité du personnel par l'automatisation de certaines tâches de contrôle, et renforce la sécurité sanitaire. Ces améliorations permettront à terme une réduction des coûts, moins d'efforts pour une mise en conformité avec la loi (et donc éviter des audits non réussis), ainsi qu'une meilleure réputation pour les établissements utilisateurs.

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
##### Collecte des données
La collecte des données est une fonction centrale de l’application, visant à garantir le respect des normes HACCP à travers une surveillance continue et automatisée. Trois grandes catégories de données sont collectées à l’aide de capteurs IoT et d’interfaces numériques.

**1. Données environnementales :**
- Température des enceintes froides (réfrigérateurs, congélateurs).
- Humidité ambiante dans les cuisines et zones de stockage.
- Conditions de ventilation ou d’atmosphère si nécessaire (extension possible).
- Données recueillies automatiquement via des capteurs BLE/WiFi, installés sur site.

**2. Données opérationnelles :**
- Traçabilité des aliments à l’aide de codes-barres ou étiquettes RFID (lot, date, origine, DLC).
- Détection de l’exécution des protocoles de nettoyage via capteurs de présence/mouvement ou validation manuelle sur tablette.
- Informations associées à des points critiques (CCP) de la méthode HACCP.

**3. Données comportementales :**
- Réponses à des questionnaires intégrés (respect des procédures, formation du personnel).
- Auto-évaluations des responsables HACCP.
- Suivi de la sensibilisation à l’hygiène (score individuel ou équipe).

**Méthodes de collecte :**
- Automatisée pour les capteurs environnementaux et certains capteurs opérationnels.
- Semi-automatique ou manuelle (via l’application) pour les aspects comportementaux.
- Fonctionnement possible hors-ligne avec journalisation locale, puis synchronisation serveur.

L’ensemble de ces données est centralisé, analysé en temps réel ou différé, et utilisé pour générer des alertes, des indicateurs de conformité, et des rapports exportables pour les autorités sanitaires.
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
*Fonctionnement prévu :*

- Les capteurs mesurent les données toutes les 10 à 15 minutes (fréquence configurable).
- L’application mobile interroge les capteurs à intervalles réguliers via BLE.
- Les données sont stockées localement sur l’appareil mobile si la connexion internet est absente, puis synchronisées automatiquement avec le serveur dès rétablissement de la connexion.
- En cas de dépassement des seuils critiques (ex. : température > 4 °C), une alerte immédiate est générée dans l’application.

*Tâches à réaliser pour la solution -> __WBS__*
1. Sélection de capteurs compatibles BLE/WiFi (normes IP65+, précision > 98 %).
2. Développement du module d’appairage sécurisé avec l’application.
3. Intégration du module de lecture périodique (avec journalisation locale).
4. Déclenchement d’alertes conditionnelles sur seuils dépassés.
5. Implémentation de la synchronisation des relevés vers le serveur cloud/local.

*Description de __scénarios__ (potentiellement avec un Diagramme de séquence)*
- Un capteur BLE placé dans une chambre froide envoie automatiquement les données toutes les 10 minutes. À 6h30, la température mesurée est de 7,2 °C. L’application reçoit la valeur, la compare au seuil critique (4 °C) et génère une notification d’alerte. Cette donnée est stockée localement et synchronisée avec le tableau de bord central dès que le réseau est disponible.
*__Jalon__ : date à laquelle la fonction doit être livrée.*
#### 3.1.2 Niveau atteint pour chaque critère d’appréciation de cette fonction et modalités de contrôle
#### 3.1.3 Part du prix attribué à chaque fonction
### 3.2 *Pour chaque fonction : fonction 2*
#### Etc.
### 3.x Pour l’ensemble du produit
#### 3.x.1 Prix de la réalisation de la version de base
##### Capteurs connectés (IoT)
Le coût lié aux capteurs IoT représente une part significative du budget initial de l’application. Ce budget couvre l’acquisition de capteurs de température, d’humidité et de présence, nécessaires à la surveillance automatisée des paramètres HACCP en cuisine collective.

**Estimation des coûts (à l’unité) :**

| Type de capteur                   | Prix unitaire estimé | Quantité prévue | Sous-total |
|----------------------------------|----------------------|------------------|------------|
| Capteur de température BLE (IP65) | ~25 €                | 5                | 125 €      |
| Capteur d’humidité / présence     | ~30 €                | 3                | 90 €       |
| Lecteur RFID mobile (optionnel)   | ~40 €                | 1                | 40 €       |
| **Total capteurs IoT**           |                      |                  | **255 €**  |

**Références tarifaires** :
- Capteurs consultés sur les catalogues fournisseurs (ex. : Distrelec, Seeed Studio, Yoctopuce).
- Prix basés sur des modèles avec connectivité BLE, étanchéité IP65 minimum et compatibilité mobile.

**Part du budget global estimé :** environ **30 % du coût total** de la solution de base (application + capteurs + hébergement serveur).

Cette estimation pourra évoluer selon les sites pilotes (surface, nombre de chambres froides, besoins en redondance) et les choix de fournisseurs lors du prototypage.
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


