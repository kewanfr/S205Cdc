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

Ce projet de Recherche et Développement s'inscrit dans une démarche scolaire d'innovation sur une entreprise fictive. Cette entreprise fictive a pour seul projet actuel de concevoir une application simplifiant la gestion de règles de HACCP dans des lieux de restauration, plus précisément dans des cuisines collectives.
C'est donc le premier projet, et initiateur de l'entreprise fictive, qui pourrait par la suite en développer d'autres.
#### 1.2.2 Études déjà effectuées
Nous avons effectués des recherches préliminaires pour identifier les différentes exigences HACCP dans les règlements CE 178/2002 et CE 852/2004, ainsi que les pratiques courantes dans la restauration collective.
#### 1.2.3 Études menées sur des sujets voisins
Afin d’enrichir la conception de l’application mobile HACCP, une étude comparative de plusieurs solutions existantes sur le marché a été menée. Cette analyse a permis d’identifier les fonctionnalités courantes, les manques fréquents, ainsi que les opportunités d’innovation.

#### Applications étudiées

---

**Traqfood**
- **Description** : Solution HACCP utilisée dans les cuisines professionnelles.
- **Fonctionnalités** :
    - Relevés de température via capteurs Bluetooth.
    - Fiches d’hygiène et de traçabilité numériques.
    - Génération d’alertes en temps réel.
- **Avantages** : Interface intuitive, automatisation poussée.
- **Limites** : Peu de personnalisation, dépendance au réseau.
- **Source** : [https://www.traqfood.com/fr](https://www.traqfood.com/fr)

---

**Eezytrace**
- **Description** : Plateforme complète pour la gestion HACCP dans les établissements collectifs.
- **Fonctionnalités** :
    - Suivi de température, nettoyage, traçabilité.
    - Historique d’actions et rapports d’audit.
- **Avantages** : Solution robuste et conforme aux normes.
- **Limites** : Interface complexe, coût élevé.
- **Source** : [https://www.eezytrace.com](https://www.eezytrace.com)

---

**HACCP Facile**
- **Description** : Application mobile légère destinée aux petits établissements.
- **Fonctionnalités** :
    - Checklists HACCP.
    - Saisie manuelle des températures.
    - Alertes basiques.
- **Avantages** : Simplicité, coût très abordable.
- **Limites** : Pas de capteurs, peu de fonctions avancées.
- **Source** : [https://www.haccp-facile.com](https://www.haccp-facile.com)

---

#### Tableau comparatif

| Critère                              | Traqfood | Eezytrace | HACCP Facile |
|--------------------------------------|---|-----|----------|
| Capteurs connectés                  | oui | oui | non      |
| Alertes automatiques                 | oui | oui  | non         |
| Historique des actions               | oui | oui  | non         |
| Analyse prédictive / IA              | non  | non    | non         |
| Mode hors-ligne                      | non  | non    | oui  partiel |
| Interface intuitive                  | oui | non    | oui      |
| Personnalisation secteur             | non  | oui  partiel | non         |
| Coût                                 | Moyen | Élevé | Faible   |

---

#### Enseignements pour notre projet

L’étude des solutions existantes met en évidence plusieurs opportunités d’amélioration :

- Intégrer une **analyse prédictive** à l’aide d’algorithmes d’IA pour prévenir les non-conformités.
- Offrir une **interface personnalisable** selon les types d’établissements (EHPAD, cantines scolaires, hôpitaux).
- Assurer un fonctionnement en **mode hors-ligne** avec synchronisation différée.
- Maintenir une **interface simple et accessible** tout en répondant aux exigences HACCP.

Ces éléments différenciateurs permettront à notre solution de répondre de manière plus ciblée aux besoins spécifiques des cuisines collectives.

#### 1.2.4 Suites prévues
#### 1.2.5 Nature des prestations demandées
dans le cadre de cette phase de cadrage du projet, la principale prestation attendue est **l’étude approfondie des applications existantes dédiées à la gestion HACCP**. Cette étude vise à analyser les solutions actuellement disponibles sur le marché afin d’identifier les meilleures pratiques, les fonctionnalités clés, les manques à combler, et les opportunités d’innovation pour le futur développement de l’application.

Cette prestation comprend les actions suivantes :

####  Recensement et sélection d’applications pertinentes

- Identifier les principales solutions logicielles utilisées dans la restauration collective ou commerciale pour le suivi HACCP.
- Sélectionner des applications représentatives selon différents critères : niveau d’automatisation, secteur cible, accessibilité, modèle économique.

#### Analyse fonctionnelle des applications

Pour chaque application étudiée (ex. : Traqfood, Eezytrace, HACCP Facile) :
- Décrire les fonctionnalités disponibles : relevés automatiques, traçabilité, alertes, rapports, tutoriels, etc.
- Évaluer l’ergonomie et la simplicité d’utilisation.
- Repérer les éléments techniques (présence de capteurs, fonctionnement hors-ligne, interfaces, export de données).
- Apprécier le respect des normes (HACCP, RGPD).

####  Comparaison des forces et faiblesses

- Dresser un tableau comparatif des solutions analysées.
- Identifier les avantages compétitifs de chaque application.
- Mettre en lumière les limites récurrentes : absence d’IA, manque de personnalisation, complexité d’usage, non prise en charge du mode hors-ligne, etc.

#### Recommandations pour le futur prototype

- Dégager des axes d’amélioration ou d’innovation à partir de l’étude de l’existant.
- Proposer des fonctionnalités différenciantes pour la future application, notamment :
    - Intégration d’une **analyse prédictive basée sur l’IA**.
    - Personnalisation selon le type d’établissement (école, EHPAD, hôpital).
    - **Robustesse en environnement contraint** (mode hors-ligne, interface simplifiée).
    - Conformité stricte aux **exigences HACCP et RGPD**.

Cette prestation analytique constitue une base stratégique pour le futur développement logiciel. Elle permettra à l’équipe de développement SAE5/SAE6 d’éviter les erreurs de conception courantes et de se positionner dès le départ avec une solution pertinente, innovante et adaptée au terrain.

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

L’environnement dans lequel sera utilisée l’application mobile impose un ensemble de contraintes spécifiques, liées aux conditions physiques, au contexte professionnel, et à l’usage sur le terrain. Le produit devra être conçu pour être **robuste, accessible et fiable** dans un cadre de travail contraint, typique des cuisines collectives.

####  Conditions physiques d’utilisation

- **Milieu humide et chaud/froid** : l’application sera utilisée dans des environnements comportant de la vapeur, de l’humidité, voire du froid extrême (chambres froides).
- **Surfaces glissantes ou grasses** : manipulations parfois difficiles, nécessité d’une interface résistante aux fausses manipulations.
- **Utilisation avec des gants ou des mains mouillées** : exige une interface à boutons larges et des zones de clic étendues.

####  Appareils utilisés

- **Smartphones et tablettes professionnels** : matériel Android ou iOS, souvent en coque durcie.
- Résolution d’écran variable, parfois réduite : l’interface doit être **responsive** et adaptée à différents formats.
- Risque de chute ou d’usage intensif : application conçue pour un usage rapide, avec **accès direct aux fonctions critiques**.

####  Contexte de connectivité

- **Réseau instable ou absent** dans certaines zones (cuisines en sous-sol, murs épais, zones rurales).
- L’application devra être utilisable **en mode hors-ligne**, avec une **synchronisation automatique des données** dès retour de la connexion.

####  Sécurité des données

- Présence de **données sensibles** (identité de l’utilisateur, données de formation, informations sanitaires).
- Application soumise au **RGPD**, avec :
    - chiffrement local des données (ex : AES-256),
    - anonymisation partielle des profils,
    - consentement utilisateur obligatoire à la première utilisation.

####  Contexte d’usage

- Utilisateurs à profils variés : agents de cuisine, gestionnaires, inspecteurs – tous avec des niveaux de compétence numérique hétérogènes.
- Application utilisée dans un cadre **professionnel normé** (HACCP), parfois sous contrôle d’audits ou d’autorités sanitaires.
- Nécessité d’une **prise en main rapide**, avec interface simplifiée, **multilingue** et **accessibilité renforcée**.

---

**Conclusion** :  
Le produit devra être adapté à un **environnement opérationnel contraint**, tant sur le plan physique que numérique. L’interface et l’architecture logicielle devront être pensées pour garantir **fiabilité, simplicité et sécurité** dans ces conditions spécifiques.


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

L’application mobile HACCP sera utilisée dans des environnements professionnels exigeants tels que les cuisines collectives. Les caractéristiques des éléments constitutifs de la solution doivent permettre un usage **fluide, sécurisé et fiable**, malgré les contraintes physiques, techniques et humaines du terrain.

####  Interfaces utilisateurs

Les interfaces devront être pensées pour une **utilisation rapide et intuitive** dans des environnements de travail où les utilisateurs sont soumis à des contraintes physiques et temporelles.

- **Ergonomie tactile renforcée** : grands boutons, navigation simplifiée, menus déroulants adaptés à une manipulation avec gants ou mains mouillées.
- **Affichage adaptatif (responsive)** : l’application s’ajuste automatiquement à la taille et à l’orientation des écrans de smartphones ou tablettes.
- **Mode sombre / contraste élevé** : visibilité optimale dans des environnements à éclairage variable.
- **Multilingue** : au minimum français et anglais, avec possibilité d’extensions selon les utilisateurs.
- **Accessibilité** : prise en charge des bonnes pratiques d’accessibilité numérique (polices lisibles, navigation au doigt, alternatives textuelles aux icônes).

####  Architecture logicielle adaptée

L’application devra fonctionner dans des contextes **avec ou sans connexion Internet stable**. L’architecture doit donc permettre un **mode dégradé temporaire** sans perte de données.

- **Stockage local sécurisé** : les données doivent être enregistrées temporairement en local en cas de déconnexion, avec chiffrement (ex : AES-256).
- **Synchronisation différée** : automatique dès détection d’une connexion, avec gestion des conflits si plusieurs utilisateurs modifient les données.
- **Modularité** : architecture capable de désactiver certaines fonctionnalités non critiques si l’environnement réseau ou matériel l’exige.

####  Sécurité et conformité

- **Conformité RGPD** : gestion des droits utilisateurs, traçabilité des actions, consentement explicite à la première utilisation.
- **Chiffrement des échanges et stockage** : HTTPS pour la transmission, chiffrement local pour les données sensibles.
- **Journalisation** : tous les accès sensibles et modifications critiques doivent être tracés et consultables.

####  Profil utilisateur hétérogène

L’application sera utilisée par :
- Des **agents de cuisine**, avec peu de temps disponible et parfois peu formés au numérique.
- Des **gestionnaires HACCP**, plus à l’aise avec les outils, mais exigeant des données synthétiques claires.
- Éventuellement des **inspecteurs ou autorités sanitaires**, avec besoin d’accès ponctuel, sécurisé et en lecture seule.

La conception devra donc proposer :
- Des **profils utilisateurs distincts** (droits, vues, actions autorisées).
- Une **interface épurée**, focalisée sur les actions prioritaires selon le profil connecté.

---

**Conclusion** :  
Les caractéristiques logicielles et ergonomiques de l’application doivent tenir compte de la réalité du terrain : contraintes physiques, instabilité réseau, hétérogénéité des utilisateurs. La robustesse de l’expérience utilisateur est un enjeu central de la réussite du projet.


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
L’analyse comparative des solutions HACCP actuelles a permis d’identifier plusieurs fonctions de service dites complémentaires. Celles-ci ne sont pas toujours présentes, mais peuvent représenter une **valeur ajoutée stratégique** pour améliorer l’utilisabilité, l’autonomie du personnel et la personnalisation de l’application. Voici une synthèse des fonctions complémentaires observées chez trois outils majeurs du marché.

#### Tableau comparatif des fonctions complémentaires

| Fonction complémentaire                   | Traqfood | Eezytrace | HACCP Facile | État dans notre projet |
|-------------------------------------------|-----|--------|----------|-------------------------|
| Tutoriels intégrés (formation, rappels)   | non | oui partiel | non      | oui (interactifs et contextualisés) |
| Historique des alertes/actions            | oui    | oui      | non      | oui (consultable + exportable)   |
| Mode hors-ligne                           | non    | non    | oui partiel | oui (avec synchronisation automatique) |
| Personnalisation selon le type de cuisine | non    | oui partiel | non      | oui (profils : scolaire, EHPAD, hôpital) |
| Documentation intégrée                    | non    | oui       | non      | oui (règlementation HACCP intégrée) |

---

#### Enseignements et positionnement de notre application

Aucune des applications étudiées ne propose **l’ensemble de ces fonctions complémentaires** de manière intégrée, intuitive et modulaire. Notre projet vise donc à se différencier en :

- Proposant une **interface personnalisable** selon le contexte d’utilisation (secteur, utilisateurs).
- Intégrant un **système de tutoriels interactifs** pour accompagner le personnel dans l’adoption des bonnes pratiques HACCP.
- Offrant une **gestion complète de l’historique** avec possibilité d’export pour audits internes ou externes.
- Garantissant un **mode hors-ligne fiable**, indispensable en environnement à connectivité limitée.
- Centralisant une **documentation contextuelle** directement accessible dans l’application.

Ces fonctions complémentaires ne sont pas acc*(qui améliorent, facilitent ou complètent le service rendu)*essoires : elles participent à la **pérennité**, la **conformité** et la **bonne adoption** de la solution sur le terrain.

##### 2.1.2.1 Description et détail

Outre les fonctions principales indispensables au respect des règles HACCP, l’application devra proposer plusieurs **fonctions de service complémentaires**. Ces fonctionnalités, bien que non essentielles au strict fonctionnement du système, apporteront une **valeur ajoutée significative** en termes d’utilisabilité, d’autonomie, de conformité et d’adoption par les utilisateurs.

---

**1. Tutoriels et rappels intégrés**

- **Objectif** : Accompagner les utilisateurs dans la prise en main de l’application et le respect des bonnes pratiques d’hygiène.
- **Contenu** :
    - Modules interactifs ou textes illustrés.
    - Rappels sur les normes HACCP (nettoyage, températures, stockage…).
    - Possibilité de consultation libre ou notifications contextuelles.
- **Bénéfice** : Réduction des erreurs humaines, auto-formation continue du personnel.

---

**2. Historique des alertes et actions correctives**

- **Objectif** : Permettre la **traçabilité complète** des anomalies détectées et des mesures prises pour les corriger.
- **Fonctionnement** :
    - Journal détaillé et horodaté de toutes les alertes.
    - Archivage des actions entreprises (responsable, type d’action, délai de réaction).
    - Exportation possible pour les audits (PDF, Excel).
- **Bénéfice** : Amélioration de la transparence et de la conformité réglementaire.

---

**3. Mode hors-ligne avec synchronisation différée**

- **Objectif** : Garantir le fonctionnement continu de l’application même en l’absence de connexion Internet.
- **Fonctionnement** :
    - Enregistrement local des données sur le terminal.
    - Synchronisation automatique dès que la connexion est rétablie.
    - Notifications d’échec de synchronisation ou de conflit.
- **Bénéfice** : Fiabilité accrue dans des environnements à faible connectivité (sous-sols, zones rurales…).

---

**4. Personnalisation des indicateurs et de l’interface**

- **Objectif** : Adapter l’application au **contexte métier** spécifique de chaque établissement (école, EHPAD, hôpital…).
- **Fonctionnement** :
    - Choix de seuils critiques selon les normes en vigueur dans l’établissement.
    - Personnalisation des catégories (zones, types d’aliments, plans de nettoyage).
    - Affichage sur-mesure dans le tableau de bord.
- **Bénéfice** : Pertinence accrue des informations affichées, meilleure appropriation par les utilisateurs.

---

**5. Documentation contextuelle**

- **Objectif** : Fournir un accès immédiat à des informations réglementaires ou techniques selon l’écran affiché.
- **Fonctionnement** :
    - Bouton d’aide ou info-bulle sur chaque écran.
    - Liens vers extraits de réglementation (CE 852/2004, guides HACCP).
    - Mises à jour possibles en ligne.
- **Bénéfice** : Autonomie renforcée des utilisateurs, cohérence réglementaire facilitée.

---

Ces fonctions complémentaires contribueront à faire de l’application un **véritable assistant numérique** pour les cuisines collectives, en améliorant à la fois **l’usage quotidien**, **la conformité réglementaire** et **l’expérience utilisateur**.


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
##### Collecte des données et capteurs IoT
La collecte des données critiques liées à la sécurité alimentaire repose sur un système hybride combinant capteurs connectés (IoT), modules de traçabilité, et interfaces utilisateurs. Cette solution garantit une surveillance continue, une traçabilité fiable et une remontée d’information conforme aux exigences HACCP.

---

**1. Collecte des données environnementales :**
- Déploiement de capteurs IoT connectés (BLE ou WiFi) dans les enceintes froides et zones de stockage.
- Paramètres mesurés : **température**, **humidité**, parfois **vibrations** (ex. panne de machine).
- Lecture automatisée toutes les 10 à 15 minutes.
- Données stockées localement en cas de coupure réseau, puis synchronisées avec le serveur.

> *Exemple :* Un capteur BLE placé dans une chambre froide envoie une température de 7,2 °C. L'application la reçoit, compare au seuil critique (4 °C), et déclenche une alerte immédiate.

---

**2. Collecte des données opérationnelles :**
- **Traçabilité alimentaire** assurée par lecture de codes-barres ou étiquettes RFID (lot, origine, DLC).
- **Détection des procédures de nettoyage** via capteurs de présence ou validation manuelle sur l’application.
- Enregistrement automatique ou semi-automatique des événements critiques (nettoyage, réception marchandise).

---

**3. Collecte des données comportementales :**
- Intégration de **questionnaires numériques** dans l’application.
- Suivi des **pratiques du personnel** : respect des protocoles, formations suivies.
- Saisie manuelle, avec enregistrement horodaté, signature numérique et anonymisation RGPD si nécessaire.

---

**Architecture fonctionnelle de la collecte :**

1. **Capteurs → application mobile** :
   - Lecture via BLE/WiFi → stockage local → synchronisation serveur.
2. **Systèmes de traçabilité** :
   - Scan RFID ou code-barres → enregistrement événement produit.
3. **Interface utilisateur** :
   - Questionnaire ou validation manuelle → stockage → analyse locale → envoi serveur.

---

**Sécurité & confidentialité :**
- Chiffrement AES-256 des données transmises et stockées.
- Appairage sécurisé des capteurs.
- Consentement utilisateur requis pour toute donnée personnelle.
- Journalisation et logs d’accès activés.

---

**Points forts de la solution proposée :**
- Collecte multi-source : environnementale, opérationnelle, comportementale.
- Fonctionnement **hors-ligne assuré** avec reprise automatique.
- Intégration **modulaire**, adaptable à différents établissements (EHPAD, scolaire, hospitalier).
- Système d’alertes immédiates en cas de non-conformité détectée.

**Scénarios d’usage**

**Scénario 1 – Alerte de dépassement de température (capteur IoT)**
- Le capteur BLE de la chambre froide relève une température de 6,8 °C à 6h30.
- L’application détecte que le seuil critique de 4 °C est dépassé.
- Une **alerte immédiate** est affichée sur l’écran du responsable cuisine.
- L’utilisateur accède à l’historique, déclenche une vérification et enregistre une action corrective dans l’application.

**Scénario 2 – Validation automatique du nettoyage**
- Un capteur de présence est installé dans la zone plonge.
- Le planning prévoit un nettoyage à 15h30.
- À 15h45, aucune détection n’a eu lieu : l’application déclenche une **alerte de tâche non effectuée**.
- Si présence détectée entre 15h30 et 16h, la tâche est automatiquement validée dans le tableau de bord.

**Scénario 3 – Saisie d’un questionnaire personnel**
- Un employé ouvre l’application sur tablette.
- Il complète un **questionnaire de 5 questions** sur les règles d’hygiène en poste froid.
- Les réponses sont enregistrées localement puis transmises au serveur.
- Un score est généré, consultable par le responsable HACCP.

---

**WBS – Collecte des données HACCP**
<img src=img/export.png>

Cette architecture permet un contrôle rigoureux, automatisé et intelligent du respect des normes HACCP, tout en restant simple à déployer et à maintenir.
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


