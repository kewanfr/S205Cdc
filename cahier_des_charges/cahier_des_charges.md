<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Cahier des charges fonctionnel - Application HACCP pour les cuisines collectives

## Entête
- Groupe de TD : 4
- Date de démarrage : 28 mai 2025 15h
- Version : 0.3.0
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

Dans le cadre d'un projet de Recherche & Développement, l'objectif est de développer une application mobile intelligente qui facilite le respect et le suivi des règles HACCP dans les cuisines collectives.
Cette application devra intégrer une approche multifactorielle en prenant en compte les facteurs environnementaux (température des enceintes froides, humidité, etc.), opérationnels (respect des procédures de nettoyage, traçabilité des aliments, etc.) et comportementaux (formation du personnel, respect des protocoles, etc.).
Les données seront collectées à l'aide de capteurs IoT et de questionnaires intégrés à l'application, et analysées par des algorithmes prédictifs utilisant l'Intelligence Artificielle.
**L'application devra offrir aux gestionnaires de cuisine un suivi adapté grâce à une prévention personnalisée et ciblée des non-conformités, favorisant ainsi une meilleure observance des protocoles HACCP.**
Elle fournira également aux autorités sanitaires des indications pour un meilleur suivi et une meilleure évaluation des pratiques en vigueur.

#### 1.1.1 Finalités

Le projet est de concevoir une application, permettant d'assurer un suivi intelligent et en temps réel des protocoles HACCP (Hazard Analysis Critical Control Point) dans les cuisines collectives.

Ses objectifs sont:
- La surveillance automatisée des paramètres critiques de sureté alimentaire.
	- Nous utiliserons pour cela un réseau de capteurs et de données renseignées par les utilisateurs. Notre application doit effectuer un suivi en continu des températures (chambres froides, congélateurs, plats de présentations, etc.), de l'humidité ambiante et d'autres indicateurs possibles (par exemple: taux de CO2, taux de particules dans l'air). Cela permet de superviser le respect de la **chaîne du froid** et du fonctionnement constant des infrastructures, sans nécessiter la présence d'un humain.
	Si des données venaient à changer de manière brutale, ou ne pas être conforme aux normes exigées par le HACCP, alors une alerte en temps réel est envoyée aux gestionnaires.
- La Traçabilité des produits et la gestion de l'hygiène
	- Elle permet de faciliter la traçabilité des aliments via différents fonctionnalitées (dates de péremption, suivi des lots et d'origine des produits). Cela se fera par étiquettes sur les produits (QR Codes, etiquettes RFID, codes barre) et scans via l'appareil de l'utilisateur.
	- L'application permet de respecter les bonnes pratiques d'hygiène: enregistrement et suvii des tâches de nettoyage ou relevé quotidiens d'informations.
	- Ces données seront toutes enregistrés avec un historique et centralisés sur l'application, permettant d'en effectuer des rapports aux gestionnaires ou autorités (lors d'un contrôle par exemple).
- L'analyse des données et décisions avec IA.
	- Les différentes données collectés seront analysées et utilisées par des algorithmes et des intelligences artificielles. Notre IA apprend des tendances, des règles et des valeurs critiques. Elle préviendra de dérives ou d'anomalies. 
	- Cela permet une meilleure anticipation et évite des problèmes critiques.
	- L'intelligence Artificielle établit des points forts et des points faibles, suggérant par la suite des actions préventives. L'objectif n'est pas seulement de constater les incidents, mais les empêcher avant qu'ils n'arrivent, ou les gérer au plus tot.
- Alerter en temps réel, produire des rapports et fournir un tableau de bord
	- Dès qu'un élément semble non conforme (problème de température ou humidité, nettoyage non conforme ou autre manquement), l'application envoie des alertes immédiatement.
	- Ces alertes peuvent prendre plusieurs formes: notifications mobiles, par SMS ou par e-mail. 
	- De plus, un tableau de bord centralise la vue d'ensemble des systèmes et de l'hygiène des cuisines.
	- Des rapports automatisés et périodiques peuvent également être utilisés.

Pour résumer, l'application fourni un pilotage, un contrôle et une analyse intelligente, automatisée au maximum et pratique pour les utilisateurs. 
Elle vise à garantir l'application des principes de la réglementation HACCP, pour alléger la charge de travail du personnel et renforcer la conformité sanitaire.

#### 1.1.2 Espérance de retour sur investissement


Le déploiement de cette application pourrait permettre de générer des bénéfices importants pour les utilisateurs (cantines collectives).
Les gains attendus sont:
- Gain de temps et d'efficacité
	- La gestion et le suivi des règles d'hygiène HACCP peut être long et chronophage. La gestion automatique via cette application permet d'éviter certaines taches manuelles. Par exemple, générer automatiquement des étiquettes de traçabilité et les suivre, remonter les températures et autres données en temps réel (évitant de les relever manuellement).
	- Ce temps gagné permet au personnel d'effectuer d'autres taches dans les cuisines.
- Réduire les pertes liés aux non conformités
	- Sécuriser la chaîne du froid et détecter les anomalies permet d'éviter le gaspillage de nourriture. Par exemple, si une panne est détectée sur un frigo dès le départ, on peut rapidement mettre les aliments ailleurs, la chaîne du froid n'est ainsi pas cassée.
	- On limite les pertes financières directes pour la nourriture jetée (problème de température, date de péremption, etc..).
	- Cela limite également les pertes financières liés à des problèmes plus graves. Exemple: une intoxication alimentaire, qui entrainerait des soins importants et d'indemniser la victime.
	- Une fermeture administration pour non respect des réglementations peut également être évitée.
- Faciliter le contrôle
	- L'utilisation de l'application garanti que la plupart des règles HACCP sont respectées en continue, évitant les problèmes lors d'inspections sanitaires.
	- De plus, cela permet un gain de temps car il est possible de présenter l'historique et les rapports complets effectués par l'application aux autorités, permettant de renforcer leur confiance. Il faut bien sur pour cela que l'application soit reconnue comme fiable et réputée.
 - La satisfaction des clients et une amélioration de l'image
	 - En assurant la sécurité alimentaire dans l'établissement, à travers ce système moderne, l'établissement envoie une confiance importante aux usagers. Les usagers seront mieux satisfaits des services, ce qui améliore la réputation de l'établissement.
	 - Cela a bien sur des répercussions économiques.

En conclusion,
Le retour sur investissement de ce projet est principalement une amélioration de la productivité du personnel, un renforcement du climat de confiance et une diminution des coûts liés aux risques sanitaires.

Sources: [traqfood](https://www.traqfood.com/fr/blog-methode-haccp/normes-haccp/article/les-avantages-des-solutions-digitales-haccp-en-restauration/), [formation-haccp](https://formation-haccp.info/reglementation-hygiene-alimentaire/), [traqfood](https://www.traqfood.com/fr/blog-methode-haccp/actualites-hygiene-alimentaire/article/ia-et-securite-alimentaire-comment-l-ia-transforme-la-gestion-haccp-en/)
L'IA générative à été utilisée à des fins de résumés des sources et de reformulations.
### 1.2 Contexte
#### 1.2.1 Situation du projet par rapport aux autres projets de l’entreprise

Ce projet de Recherche et Développement s'inscrit dans une démarche scolaire d'innovation sur une entreprise fictive. Cette entreprise fictive a pour seul projet actuel de concevoir une application simplifiant la gestion de règles de HACCP dans des lieux de restauration, plus précisément dans des cuisines collectives.

On peut considérer ce projet comme pilote de la société fictive. L'objectif est de simuler les conditions d'une jeune entreprise innovante. Il montre la faisabilité et l'intérêt du suivi des règles HACCP de manière intelligente. 
C'est donc le premier projet, et initiateur de l'entreprise fictive, qui pourrait par la suite en développer d'autres.
C'est un projet important pour cette entreprise, car il s'agira à la fois d'un essai technique des capacités technologiques de celle-ci, mais aussi d'une vitrine de son savoir faire.
#### 1.2.2 Études déjà effectuées

Pour la rédaction de ce cahier des charges, nous avons mené plusieurs étudies préliminaires, pour s'assurer de la pertinence et la viabilité de cette application.
Différentes analyses des textes de loi ont été effectués, en partie à l'aide de LLMs.
Une analyse détaillée de la règlementation en vigueur à propos des règlements européens (CE) n°178/2002 et n°852/2004 a été effectuée pour en extraire les exigences utiles et nécessaires à notre application.

Le règlement 178/2002, appelé plus communément *Food Law* permet de poser des principes généraux des lois sur l'alimentation. Il impose notamment la traçabilité des aliments tout au long de la chaîne. Ensuite, le règlement 852/2004 est relatif à l'hygiène des denrées alimenataires. Il rend obligatoire la mise en places de procédures basées sur le HACCP dans tous les établissements de restauration européens. Ces textes imposent notamment de surveiller tous les points critiques et de tenir des fichiers et rapports contenant tout l'historique des données et des actions effectuées.
Nous avons identifié les différents obligations pouvant être intégrées à notre produit: contrôle des températures et autre données, plan de nettoyage avec contrôle des actions, formationn 

Nous avons également consultés et analyses les règles en cuisine collectives (GBPH), qui ont notamment été présentés dans le "Paquet Hygiène", règlementation européenne de Janvier 2006.


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

Le diagramme de cas d’utilisation ci-dessous permet de visualiser les interactions entre les différents utilisateurs de l’application HACCP et les fonctionnalités proposées. Il constitue une représentation synthétique du périmètre fonctionnel de l’application, en lien direct avec les besoins exprimés dans les sections précédentes.

Ce diagramme suit la notation UML et identifie les **acteurs** principaux du système (agents de cuisine, responsables HACCP, gestionnaires d’établissement, autorités sanitaires, systèmes externes) ainsi que les **cas d’utilisation** (ou scénarios d’interaction) qui leur sont accessibles.

Les relations de **généralisation entre acteurs** sont également représentées, afin de clarifier les rôles hiérarchiques et les droits d’accès. Les flèches de généralisation indiquent qu’un acteur spécialisé hérite des fonctionnalités accessibles à un acteur plus général (ex. : un gestionnaire hérite des fonctions du responsable HACCP, qui hérite lui-même de celles de l’agent de cuisine).

Des relations de type `include` et `extend` sont aussi présentes entre certains cas d’utilisation, pour refléter des **fonctionnalités partagées** ou **optionnelles** selon le contexte.

Ce diagramme aide à :
- clarifier les frontières du système,
- structurer le développement fonctionnel,
- et faciliter la compréhension du rôle de chaque utilisateur.

Il servira de base pour la conception détaillée de l’architecture logicielle de l’application lors des phases ultérieures du projet.

<img src=img/diagramme_usecase.png>

#### 2.1.1 Fonctions de service principales 
Ce sont les fonctions qui constituent la raison d'être du produit.
##### Collecte des données
La collecte des données est une fonction centrale de l’application, visant à garantir le respect des normes HACCP à travers une surveillance continue et automatisée. Trois grandes catégories de données sont collectées à l’aide de capteurs IoT et d’interfaces numériques.

L’application collecte automatiquement les températures, l’humidité et la traçabilité via des capteurs IoT (BLE/WiFi). Les questionnaires intégrés permettent de suivre les pratiques du personnel. Toutes les données sont centralisées et analysées pour générer des alertes en temps réel.

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

**4. Transmission aux autorités sanitaires :**
- **Génération des rapports :** L’application génère automatiquement des rapports périodiques (hebdomadaires, mensuels) à partir des données collectées. Les rapports peuvent également être générés manuellement pour des périodes spécifiques ou des événements particuliers. Les rapports sont générés dans des formats standardisés (PDF, CSV) conformes aux exigences des autorités sanitaires.
- **Transmission sécurisée :** Les rapports sont chiffrés avant transmission pour garantir la confidentialité des données. Utilisation de protocoles sécurisés (HTTPS, SFTP) pour la transmission des rapports. Les autorités sanitaires sont authentifiées avant de pouvoir accéder aux rapports.
- **Traçabilité et audit :** Toutes les transmissions de rapports sont journalisées pour assurer la traçabilité. L’application envoie un accusé de réception une fois le rapport transmis avec succès. Les utilisateurs peuvent consulter l’historique des transmissions pour vérifier que les rapports ont bien été envoyés et reçus.
- **Conformité réglementaire :** La transmission des données est conforme à la RGPD. Les rapports générés respectent les normes HACCP et les exigences des autorités sanitaires.

**Méthodes de collecte :**
- Automatisée pour les capteurs environnementaux et certains capteurs opérationnels.
- Semi-automatique ou manuelle (via l’application) pour les aspects comportementaux.
- Fonctionnement possible hors-ligne avec journalisation locale, puis synchronisation serveur.

L’ensemble de ces données est centralisé, analysé en temps réel ou différé, et utilisé pour générer des alertes, des indicateurs de conformité, et des rapports exportables pour les autorités sanitaires.

Trois catégories de données sont collectées via capteurs IoT et interfaces numériques

- Données environnementales : Température (enceintes froides), humidité ambiante, conditions de ventilation (extension possible). Recueillies automatiquement via capteurs BLE/WiFi
- Données opérationnelles : Traçabilité aliments (codes-barres, RFID), détection protocoles nettoyage (capteurs présence/mouvement ou validation manuelle), informations points critiques (CCP)
- Données comportementales : Réponses questionnaires intégrés (procédures, formation), auto-évaluations, suivi sensibilisation hygiène
- Méthodes de collecte : Automatisée (capteurs), Semi-automatique/manuelle (application). Fonctionnement possible hors-ligne avec journalisation locale, puis synchronisation
- L'ensemble des données est centralisé, analysé (temps réel/différé), utilisé pour générer alertes, indicateurs conformité, rapports exportables

##### 2.1.1.2 Critères d’appréciation et les niveaux qui les caractérisent 
*(Niveaux dont l’obtention est imposée)*
- Temps de réponse : < 3 secondes pour l’affichage d’une alerte.
- Fiabilité des capteurs : précision ±0,5°C, taux de transmission >98%.
- Accessibilité : interface utilisable avec gants, multilingue.
*(Niveaux souhaités mais révisables)*

- Temps de réponse : < 3 secondes pour l'affichage d'une alerte
- Fiabilité des capteurs : précision ±0,5°C, taux de transmission >98%
- Accessibilité : interface utilisable avec gants, multilingue

#### 2.1.2 Fonctions de service complémentaires 
L’analyse comparative des solutions HACCP actuelles a permis d’identifier plusieurs fonctions de service dites complémentaires. Celles-ci ne sont pas toujours présentes, mais peuvent représenter une **valeur ajoutée stratégique** pour améliorer l’utilisabilité, l’autonomie du personnel et la personnalisation de l’application. Voici une synthèse des fonctions complémentaires observées chez trois outils majeurs du marché.

- Interface personnalisable selon le contexte (secteur, utilisateurs)
- Système de tutoriels interactifs
- Gestion complète de l'historique avec export pour audits
- Mode hors-ligne fiable
- Documentation contextuelle intégrée

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

1. Tutoriels et rappels intégrés : Accompagner utilisateurs (prise en main, bonnes pratiques). Contenu interactif/textuel, rappels sur normes HACCP, consultation libre ou notifications contextuelles. Bénéfice : Réduction erreurs humaines, auto-formation
2. Historique des alertes et actions correctives : Traçabilité complète des anomalies et mesures correctives. Journal détaillé/horodaté, archivage actions (responsable, type, délai), exportation (PDF, Excel) possible pour audits. Bénéfice : Amélioration transparence et conformité
3. Mode hors-ligne avec synchronisation différée : Garantie fonctionnement continu sans connexion. Enregistrement local des données, synchronisation automatique dès connexion, notifications échec/conflit. Bénéfice : Fiabilité accrue en environnements à faible connectivité
4. Personnalisation des indicateurs et de l’interface : Adapter l'application au contexte métier spécifique (école, EHPAD, hôpital). Choix des seuils critiques, personnalisation catégories (zones, aliments, nettoyage), affichage sur-mesure tableau de bord. Bénéfice : Pertinence accrue, meilleure appropriation
5. Documentation contextuelle : Accès immédiat aux informations réglementaires/techniques (CE 852/2004, guides HACCP). Bouton d'aide/info-bulle, liens vers réglementation, mises à jour en ligne possibles. Bénéfice : Autonomie renforcée, cohérence réglementaire facilitée

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
Le développement de l’application mobile de suivi HACCP devra strictement respecter le règlement (CE) n°852/2004 relatif à l’hygiène des denrées alimentaires, applicable à toutes les étapes de la chaîne agroalimentaire . Cela implique la mise en place de procédures fondées sur l’analyse des dangers et la maîtrise des points critiques (HACCP), la tenue de guides de bonnes pratiques d’hygiène (notamment pour les entreprises de petite taille), ainsi que la conservation réglementaire des enregistrements : un an pour les relevés des CCP tels que les températures, et trois ans pour les documents liés au nettoyage, à la traçabilité et aux audits. Par ailleurs, conformément au règlement (CE) n°178/2002, l’exploitant est responsable de la sécurité alimentaire et doit assurer une traçabilité complète “de l’amont vers l’aval”, avec réactivité en cas de retrait ou de rappel de lots. L’utilisation de codes-barres, QR Codes ou RFID sera nécessaire pour enregistrer systématiquement lors de chaque scan l’origine, le numéro de lot et la date de péremption des produits.

Sur le plan de la protection des données, l’application devra être conforme au RGPD(UE)2016/679. Les données collectées (identifiants, rôle, historiques de saisie) seront traitées uniquement dans un cadre clairement défini (suivi HACCP, audits, alertes), reposant sur les principes de licéité, transparence, limitation des finalités et minimisation . Les utilisateurs devront recevoir une information complète dès l’installation et donner leur consentement explicite. Ils auront également la possibilité d’exercer aisément leurs droits d’accès, de rectification, d’effacement, de portabilité, d’opposition et de limitation. L’architecture devra intégrer la protection dès la conception (privacy by design) avec chiffrement AES‑256 des données au repos et TLS1.2+ des échanges. La pseudonymisation, reconnue comme mesure de sécurité efficace, devra être mise en œuvre pour les exports à destination des audits . En outre, toute violation de données présentant un risque devra être notifiée à la CNIL dans un délai maximal de 72heures après constatation, avec explication des motifs en cas de retard, et documentée conformément à l’article 33 du RGPD. Enfin, l’application devra tenir à jour un registre des traitements, précisant finalités, catégories de données et mesures de sécurité, pour être prête en cas de contrôle par la CNIL.

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

> *Exemple :* Un capteur BLE placé dans une chambre froide envoie une température de 7,2°C. L'application la reçoit, compare au seuil critique (4°C), et déclenche une alerte immédiate.

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
- Le capteur BLE de la chambre froide relève une température de 6,8°C à 6h30.
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
- **Temps de réponse** : < 3 secondes pour l’affichage d’une alerte (testé sur 10 scénarios).
- **Fiabilité** : Précision des capteurs ±0,5°C, taux de transmission >98% (tests de validation sur 1 semaine).
- **Accessibilité** : Interface utilisable avec gants, multilingue (tests utilisateurs en conditions réelles).
#### 3.1.3 Part du prix attribué à chaque fonction
- **Collecte des données** : 30% du budget (capteurs, intégration IoT, stockage sécurisé).
- **Tableau de bord** : 20% du budget (UX/UI, développement front-end, personnalisation).
- **Alertes et notifications** : 10% du budget (système d’alerte, notifications mobiles/SMS).
- **Synchronisation/hors-ligne** : 15% du budget (gestion des données locales, synchronisation serveur).
- **Conformité RGPD** : 10% du budget (anonymisation, gestion des droits, logs).
- **Documentation et tutoriels** : 5% du budget (contenus, intégration).
- **Maintenance/évolutivité** : 10% du budget (support, mises à jour).

#### 3.1.4 Jalons associés
| Fonction                | Jalon (date/étape)           | Modalité de contrôle           |
|-------------------------|------------------------------|-------------------------------|
| Collecte des données    | Prototype capteurs (Semaine 3) | Test de collecte automatisée   |
| Tableau de bord         | Maquette validée (Semaine 5)   | Test utilisateur               |
| Alertes                 | Système opérationnel (Semaine 6) | Simulation d’anomalie         |
| Synchronisation         | Démo hors-ligne (Semaine 7)     | Test de coupure réseau         |
| RGPD                    | Audit conformité (Semaine 8)    | Vérification documentation     |

### 3.2 *Pour chaque fonction : fonction 2*

#### 3.2.1 Solution proposée

Le tableau de bord est l’interface centrale de l’application. Il doit permettre aux gestionnaires et aux agents de cuisine de **visualiser rapidement l’état global de conformité HACCP**, de **réagir efficacement en cas de non-conformité**, et de **gérer les actions à entreprendre**.

L’UX/UI proposée s’appuie sur les principes de **clarté, synthèse, hiérarchisation visuelle** et **accessibilité rapide à l’information critique**.

##### Structure du tableau de bord

- **Affichage principal** sous forme de **vignettes** ou **cartes thématiques**, représentant les grandes familles de données :
  - Températures des enceintes froides
  - Procédures de nettoyage
  - Traçabilité des aliments
  - Historique des alertes
  - Niveau de conformité global

- **Système de couleurs type "feux tricolores"** pour chaque vignette :
  - Conforme (vert)
  - A surveiller / en attente (jaune)
  - Non conforme (rouge)

- **Accès rapide** à chaque section via un **menu horizontal ou une barre latérale** :
  - Tableau synthétique
  - Données détaillées
  - Historique
  - Export / rapport

- **Indicateurs clés** visibles en un coup d’œil :
  - % de conformité général
  - Nombre d’anomalies actives
  - Alertes non résolues
  - Dernière synchronisation
  - Profil de risque actuel

- **Notifications visuelles et sonores** en cas de changement d’état (ex : dépassement de seuil).

##### Personnalisation

- Choix de l’affichage par **établissement, zone, période, utilisateur**.
- Possibilité de filtrer et trier les indicateurs.
- Mise à jour automatique des données affichées à chaque synchronisation.

##### UX mobile

- Affichage **responsive** (smartphone/tablette).
- **Navigation simplifiée** : interaction à une main, boutons larges, interface tactile optimisée.
- **Mode hors-ligne** : accès au dernier état synchronisé avec message "données en attente de mise à jour".

---

#### 3.2.2 Niveau atteint

- **Temps de chargement** : < 3 secondes sur la majorité des terminaux Android/iOS.
- **Taux de satisfaction** visé sur la navigation UX : ≥ 90% (évaluation via questionnaire utilisateur intégré).
- **Mises à jour** en temps réel ou différé selon la connectivité.

---

#### 3.2.3 Coût estimé

- Estimation : **20 % du budget total**.
- Inclus : conception UX, développement front-end, animations, personnalisation, documentation intégrée.

---

Le tableau de bord représente la **porte d’entrée principale** vers la donnée critique. Il doit être **lisible, modulaire et réactif**, conçu pour des utilisateurs en environnement contraint, avec une **expérience fluide**, même sous stress ou contrainte de temps.
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
### Solutions envisagées mais non retenues

Dans le cadre de l’étude de faisabilité, plusieurs options technologiques et fonctionnelles ont été envisagées mais finalement écartées pour la version initiale du projet. Voici les principales solutions non retenues et les raisons de leur exclusion :

#### 1. Capteurs longue portée LoRaWAN

- **Description** : Utilisation de capteurs IoT communiquant via le protocole LoRaWAN pour couvrir de très grandes surfaces ou des sites multi-bâtiments.
- **Raison du rejet** : Coût d’infrastructure élevé (passerelles LoRa, abonnements réseau), complexité de déploiement et de maintenance, surdimensionné pour la majorité des cuisines collectives ciblées. BLE/WiFi jugés suffisants pour la portée requise.

#### 2. Stockage cloud externe (type AWS, Azure)

- **Description** : Hébergement des données critiques sur des plateformes cloud publiques.
- **Raison du rejet** : Risques accrus en matière de confidentialité et de conformité RGPD, coûts récurrents d’abonnement, dépendance à la connectivité Internet. Préférence pour un stockage local sécurisé avec synchronisation sur serveur interne ou hébergement souverain.

#### 3. Interface web complète (application desktop)

- **Description** : Développement d’une interface web accessible depuis un navigateur pour la gestion et la consultation des données.
- **Raison du rejet** : Complexité de développement supplémentaire, risques de divergence UX/UI avec la version mobile, nécessité de sécuriser l’accès distant. L’application mobile couvre déjà les besoins principaux sur le terrain.

#### 4. Reconnaissance vocale pour la saisie des données

- **Description** : Intégration d’un module de saisie vocale pour faciliter l’enregistrement des tâches ou des alertes.
- **Raison du rejet** : Fiabilité insuffisante en environnement bruyant (cuisine), complexité technique, coût de développement et d’intégration élevé pour un gain limité.

#### 5. Intégration de la blockchain pour la traçabilité

- **Description** : Utilisation d’une blockchain privée pour garantir l’immutabilité des historiques de traçabilité.
- **Raison du rejet** : Surcoût important, complexité technique, absence de besoin réglementaire à ce stade, et impact limité sur la valeur ajoutée pour les utilisateurs finaux.

#### 6. Application multiplateforme (Windows, Linux, Mac)

- **Description** : Développement d’une version desktop native pour tous les systèmes d’exploitation.
- **Raison du rejet** : Ressources de développement non justifiées par rapport à la cible principale (utilisation mobile/tablette en cuisine), coûts de maintenance accrus.

---

**Conclusion** :  
Ces solutions pourront être réévaluées lors de futures évolutions du projet, en fonction des retours utilisateurs, de l’évolution des besoins ou de l’extension à de nouveaux marchés. Pour la version initiale, le choix s’est porté sur des technologies éprouvées, simples à déployer et à maintenir, tout en garantissant la sécurité et la conformité réglementaire.
#### 3.x.3 Mesures prises pour respecter les contraintes et leurs conséquences économiques
### Mesures prises pour respecter les contraintes et leurs conséquences économiques

#### Conformité RGPD

- **Consentement explicite** : Mise en place d’un écran d’information et de consentement à la première utilisation, gestion des droits d’accès, possibilité de retrait du consentement.
- **Minimisation des données** : Collecte uniquement des données strictement nécessaires au suivi HACCP.
- **Droits utilisateurs** : Fonctionnalités pour accéder, rectifier, supprimer ou exporter ses données personnelles.
- **Registre des traitements** : Documentation interne des traitements, finalités, catégories de données et mesures de sécurité.
- **Pseudonymisation/anonymisation** : Export des données pour audits sans informations identifiantes.

*Conséquence :* Développement de modules spécifiques, temps de conception juridique, coût de validation légale, maintenance accrue pour suivre l’évolution de la réglementation.

#### Sécurité

- **Chiffrement** : Données stockées localement et transmises via des protocoles sécurisés (AES-256, TLS 1.2+).
- **Authentification forte** : Gestion des accès par profils, mots de passe robustes, éventuellement double authentification.
- **Journalisation** : Traçabilité des accès et modifications, logs consultables en cas d’incident.
- **Mises à jour de sécurité** : Politique de patching régulier de l’application et des serveurs.

*Conséquence :* Surcoût lié à l’intégration de bibliothèques de sécurité, tests de pénétration, audits réguliers, gestion des incidents.

#### Robustesse

- **Redondance des capteurs** : Installation de capteurs critiques en double dans les zones sensibles.
- **Stockage local résilient** : Buffer sécurisé pour fonctionnement hors-ligne, synchronisation automatique dès retour réseau.
- **Gestion des erreurs** : Notifications en cas de panne, modes dégradés pour garantir la continuité de service.
- **Tests intensifs** : Scénarios de coupure réseau, saturation mémoire, crash applicatif.

*Conséquence :* Investissement matériel plus élevé (capteurs redondants), développement de mécanismes de reprise, coût de tests et validation.

#### Impact économique et complexité

- **Coût initial augmenté** : Développement de fonctionnalités avancées, achat de matériel sécurisé, validation RGPD.
- **Maintenance renforcée** : Suivi des évolutions réglementaires, mises à jour de sécurité, support utilisateur.
- **Complexité technique** : Architecture logicielle modulaire, gestion des synchronisations, gestion fine des droits et des logs.

En résumé, pour garantir la conformité RGPD, la sécurité et la robustesse impliquent un investissement initial et une complexité technique accrus, mais c’est indispensable pour la viabilité, la confiance des utilisateurs et la conformité réglementaire du produit.

#### 3.x.4 Outils d’installation, de maintenance … à prévoir
#### 3.x.5 Décomposition en modules, sous-ensembles

L’application sera composée de plusieurs modules fonctionnels, organisés de manière modulaire afin de faciliter le développement, l’entretien et l’évolution de la solution. Parmi eux, le **module tableau de bord** est un point central de l’expérience utilisateur.

#### Liste des modules fonctionnels principaux

- **Module Capteurs** : collecte des données environnementales (température, humidité, etc.).
- **Module Traçabilité** : suivi des produits via RFID, codes-barres.
- **Module Nettoyage** : validation et contrôle des procédures d’hygiène.
- **Module Questionnaires** : recueil des données comportementales.
- **Module Alertes** : détection, gestion et suivi des non-conformités.
- **Module Synchronisation** : gestion du mode hors-ligne et des connexions serveur.
- **Module RGPD** : conformité réglementaire, anonymisation, gestion des accès.
- **Module Tableau de bord** : **interface centrale de visualisation et de pilotage**.

---

#### Module "Tableau de bord" – Proposition UX

Ce module est conçu comme le **centre de contrôle visuel** de l'application. Il offre à l’utilisateur une vision synthétique, claire et immédiate de la situation HACCP de la cuisine.

##### Objectifs UX/UI :

- Permettre une **lecture rapide** de l’état global de conformité.
- Offrir des **indicateurs visuels clairs** (codes couleur, pictogrammes).
- Faciliter l’accès aux données détaillées sans surcharge cognitive.
- Fonctionner **efficacement en mobilité**, avec un design adapté aux environnements contraints (gants, bruit, stress, humidité).

##### Composants UX clés :

- **Cartes thématiques (widgets)** avec couleur de statut : conforme (vert), à surveiller (jaune), non conforme (rouge).
- **Graphiques simples et dynamiques** : courbes de température, taux de conformité sur 7 jours, nombre d’alertes par zone.
- **Filtres rapides** : par date, zone, type de donnée, niveau de risque.
- **Affichage hiérarchisé** : données critiques en haut, informations secondaires repliées.
- **Bouton "Exporter le rapport"** visible et rapide d’accès.
- **Notifications contextuelles** intégrées dans l’interface.

##### UX mobile :

- Design **responsive**, testée sur écrans ≥ 5 pouces.
- Utilisation possible à **une main** avec gestuelle simple.
- Mode hors-ligne avec données conservées localement + alerte de synchronisation.

---

#### Résumé UX du module

| Critère                   | Spécification UX attendue                    |
| ------------------------- | -------------------------------------------- |
| Temps d’accès aux données | < 3 secondes                                 |
| Taux de clarté perçue     | ≥ 90 % (test utilisateur)                    |
| Navigation mobile         | Optimisée pour écran tactile + gants         |
| Visibilité des alertes    | Immédiate (signal visuel/sonore)             |
| Accessibilité             | Texte lisible, contraste élevé, pictogrammes |

---

Le module "tableau de bord" est au cœur de la **stratégie UX de l’application**. Il doit garantir à l’utilisateur une **expérience fluide, rassurante et efficace**, même en situation de stress ou de surcharge opérationnelle.
#### 3.x.7 Perspectives d’évolution technologique
## 4 Prévisions de fiabilité – Gestions des risques
### 4.1 Risques à la réalisation
*__Profils de risques__ pour chaque fonction de service*
<img src=img/profil_de_risque.png>
### 4.2 Prévision des défaillances
*Table de défaillance pour chaque fonction de service avec un paragraphe commentant chaque défaillance et/ou chaque cause/effet/détection d’importance notable*
| Fonction du produit              | Mode de défaillance                   | Effet de la défaillance                              | Causes possibles de la défaillance                   | Détection | Occurrence | Gravité | Criticité (D×O×G) |
|----------------------------------|---------------------------------------|------------------------------------------------------|------------------------------------------------------|------------|-------------|----------|--------------------|
| Capteur IoT       | Capteur inactif                       | Non-détection d’un dépassement de seuil critique     | Batterie vide, signal coupé, défaut matériel         | 6          | 5           | 9        | 270                |
| Capteur de présence nettoyage    | Pas de détection durant le créneau    | Tâche non réalisée mais non signalée                 | Mauvais positionnement, zone non couverte            | 1          | 3           | 8        | 24                |
| Synchronisation mobile-serveur   | Données non transmises ou corrompues  | Perte de traçabilité, non-conformité réglementaire   | Perte de réseau, plantage de l’app mobile            | 8          | 4           | 10        | 320                |
| Stockage local des données       | Saturation mémoire, perte hors ligne  | Données perdues avant synchronisation                | Manque de contrôle espace, bug système               | 8          | 3           | 10       | 240                 |
| Application mobile               | Crash ou freeze                       | Blocage temporaire de la collecte                    | Erreur de code, surcharge mémoire, conflits système  | 3          | 3           | 8        | 72                 |
| Saisie questionnaire personnel   | Réponses incomplètes ou erronées      | Mauvais suivi comportemental                         | Oubli, inattention, interface mal conçue             | 3          | 7           | 4        | 84                |
| Scan RFID / QR code              | Produit non reconnu ou mal scanné     | Rupture de la traçabilité d’un lot alimentaire       | Étiquette abîmée, éclairage insuffisant              | 3          | 6           | 7        | 126                |
| Capteur IoT               | Données incohérentes                  | Sous-estimation du risque microbien                  | Capteur mal calibré, condensation                    | 6          | 6           | 9        | 324                 |


### 4.3 Gestion des défaillances

*La __Matrice de criticité__*
<img src=img/matrice_de_criticité.png>

### Capteur inactif (Gravité : Catastrophique, Probabilité : rare)

**Empêcher :**  
Déployer des capteurs redondants dans les zones critiques (ex. : chambres froides), avec un plan de vérification hebdomadaire (test de signal, batterie). Installer des capteurs validés IP65 avec autonomie longue durée et indicateur d'état.

**Alerter :**  
Configurer une alerte automatique dès qu’un capteur n’émet plus de données pendant une durée donnée (ex. 30 minutes). Surveiller les écarts de transmission via un watchdog intégré à l’application.

**Réagir :**  
Envoyer immédiatement une notification au responsable HACCP. Activer un mode manuel de saisie temporaire. Remplacer le capteur dès que possible et historiser l’incident dans le tableau de bord.

---

### Capteur de présence non déclenché (Gravité : Critique, Probabilité : Rare)

**Empêcher :**  
Optimiser l’emplacement des capteurs avec un guide d’installation (zone de détection, hauteur, orientation). Prévoir une validation manuelle complémentaire à chaque tâche planifiée (ex. : bouton “nettoyage effectué”).

**Alerter :**  
Générer une alerte si aucune activité n’est détectée pendant une plage horaire où une action est prévue (nettoyage, désinfection). Journaliser l’absence de détection.

**Réagir :**  
Envoyer une notification au responsable avec la possibilité de valider manuellement l’action. Documenter l'écart de conformité. Planifier une intervention de vérification capteur si récurrence.

---

### Données non transmises ou corrompues (Gravité : Catastrophique, Probabilité : Rare)

**Empêcher :**  
Prévoir une architecture de stockage local robuste avec buffer sécurisé et file d’attente résiliente. Tester les scénarios de déconnexion pour valider la reprise.

**Alerter :**  
Afficher un indicateur d’état de synchronisation dans l’application. Déclencher une alerte si une donnée n’a pas été synchronisée après un délai maximum (ex. 2h).

**Réagir :**  
En cas de perte réseau, activer un mode hors-ligne prolongé. Lors du retour de connexion, déclencher la synchronisation automatique. En cas d’échec persistant, activer un export manuel local chiffré.

---

### Saturation mémoire, perte hors ligne  (Gravité : Catastrophique, Probabilité : Rare)

**Empêcher :**  
Mettre en place une vérification régulière de l’espace disponible sur l’appareil (monitoring de capacité mémoire). Définir une politique de nettoyage automatique des anciennes données ou des logs non critiques. Compresser les données localement pour limiter l’occupation.

**Alerter :**  
Générer une alerte dès que le seuil d’alerte de capacité (ex. 80 %) est atteint. Afficher une notification dans l’interface de l’application signalant le risque de saturation imminente.

**Réagir :**  
Passer temporairement en mode dégradé en bloquant les nouvelles saisies non urgentes. Autoriser un export manuel des données sur support externe (clé USB, WiFi local). Une fois l’espace libéré ou la synchronisation rétablie, restaurer les fonctions bloquées et historiser l’incident.




## 5 Annexe
*Le planning ne fait pas partie de la norme car sa décomposition n’importe pas au client à cette phase du projet. Il n’est alors intéressé que par les jalons qui ponctuent la réalisation des différentes fonctionnalités.
Nous placerons donc le __diagrammes de Gantt__ ici.*

Le diagramme de Gantt ci-dessous présente le **planning prévisionnel du développement de l’application mobile HACCP**, en lien avec les objectifs du projet définis dans ce cahier des charges.

Chaque tâche est représentée sous forme de barre horizontale, positionnée selon sa date de début et sa durée estimée. Cette visualisation permet de :

- Suivre la **séquence logique des étapes** du projet,
- Identifier les **phases critiques** et les chevauchements,
- Anticiper les **ressources nécessaires** à chaque moment.

Le planning est structuré autour de **dix grandes étapes**, depuis l’analyse des exigences jusqu’à la livraison finale du prototype fonctionnel. Il inclut notamment :
- La définition des besoins,
- La conception UX/UI,
- Le développement modulaire (capteurs, alertes, tableau de bord, mode hors-ligne),
- La mise en conformité RGPD,
- Les phases de tests et d’ajustements,
- La livraison du prototype.

Certaines tâches sont parallélisables, tandis que d’autres suivent des **dépendances logiques** (par exemple, les tests ne peuvent être effectués qu’après le développement des modules).

Ce diagramme constitue un outil essentiel pour le **pilotage du projet**, en assurant une vision globale de son avancement, et en facilitant la coordination entre les membres de l’équipe.

<img src=img/diagramme_gantt.png>



#### Répartition du travail

### Alex
| Tâche                                   | Section             | Durée estimée |
|-----------------------------------------|---------------------|---------------|
| Etude des applications existantes       | 1.2.3 / 1.2.5 (LLM) | 30min         |
| Synthèse comparative outils HACCP       | 1.2.3 / 2.1.2 (LLM) | 1h            |
| Rédaction de l'environnement du produit | 1.4.1 / 1.4.2 (LLM) | 1h            |
| Rédaction fonctions complémentaires     | 2.1.2.1             | 1h30          |
| Diagramme de cas d'utilisation          | 2.1                 | 2h            |
| Proposition de l'UX du tableau de bord  | 3.2 / 3.3.5         | 1h            |            
| Diagramme de Gantt                      | 5 Annexe            | 1h30          |


