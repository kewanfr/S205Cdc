<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Cahier des charges fonctionnel - Application HACCP pour les cuisines collectives

## Entête
- Groupe de TD : 4
- Date de démarrage : 28 mai 2025 15h
- Version : 0.9.1
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

- La surveillance automatisée des paramètres critiques de sûreté alimentaire. 
  - Nous utiliserons pour cela un réseau de capteurs et des données renseignées par les utilisateurs. 
    Nous installerons dans les cuisines (frigos, chambres froides, congélateurs, etc.) des capteurs de température et d'humidité, ainsi que d'autres capteurs selon les besoins (par exemple: taux de CO2, taux de particules dans l'air).
    Ces capteurs permettront de mesurer en continu les conditions de stockage des aliments et de garantir le respect de la chaîne du froid.
    Doivent être respectées ces 4 zones de température:
    - Froid négatif : de -40 °C à 0 °C (chambres froides, congélateurs)
    - Froid positif : de 0 °C à 5 °C (chambres froides positives, frigos)
    - Zone de danger : de 5 °C à 60 °C (zone de préparation, cuisson, etc.)
    - Zone de cuisson : au-dessus de 60 °C (cuisson, maintien au chaud, etc.)

    Cela permet de superviser le fonctionnement constant des infrastructures, sans nécessiter la présence d'un humain.
    Tout écart brusque ou dépassement de seuil du HACCP déclenche aussitôt une alerte en temps réel, envoyée aux gestionnaires, avec des actions à effectuer.

- La Traçabilité des produits et la gestion de l'hygiène 
  - Chaque aliment devra être tracé, de son origine à sa consommation. À chaque changement de condition, seront notés: 
    - la date d'ouverture du produit,
    - la date de fabrication
    - la date de péremption,
    - la température à ce moment là
    - ou d'autres informations (numéro de lot, fournisseur, etc.).

  - Cela se fera par étiquettes sur les produits (QR Codes, étiquettes RFID, codes-barres) et scans via l'appareil de l'utilisateur.
    Il faut pour cela prévoir un/des appareils capables de lire ces étiquettes, et des étiqueteuses.

  - L'application permet de respecter les bonnes pratiques d'hygiène: enregistrement et suivi des tâches de nettoyage ou relevés quotidiens d'informations.

  - Ces données seront toutes enregistrées avec un historique et centralisées sur l'application.


- Nous devons implémenter une IA et des algorithmes
  - Capables d'analyser les données collectées, de détecter toute anomalie ou dérive, et de prévenir les gestionnaires en cas de non-conformité.
  - L'IA doit apprendre des tendances et des règles, et suggérer des actions préventives pour éviter les problèmes critiques.
  - L'objectif est d'anticiper les incidents avant qu'ils ne se produisent, ou de les gérer au plus tôt.
  - Elle utilise pour cela les informations saisies dans le PMS. Elle apprend constamment.


- Les chefs de cuisine ou gestionnaires pourront renseigner leur **Plan de Maîtrise Sanitaire (PMS)** et les procédures de nettoyage, ainsi que les tâches effectuées par le personnel.
  - Ce PMS sera utilisé et analysé par l'IA pour vérifier la conformité des pratiques et des procédures.
  - Il détaille les procédures de nettoyage, de désinfection, de stockage des aliments, de gestion des déchets, etc.
  - Ainsi que tous les problèmes potentiels rencontrés, les solutions apportées et les mesures de prévention mises en place.


- Alerter en temps réel, produire des rapports et fournir un tableau de bord 
  - Dès qu'un élément semble non conforme (problème de température ou humidité, nettoyage non conforme ou autre manquement), l'application envoie des alertes immédiatement.
  - Ces alertes peuvent prendre plusieurs formes: notifications mobiles, par SMS ou par e-mail.
  - De plus, un tableau de bord centralise la vue d'ensemble des systèmes et de l'hygiène des cuisines.
  - Des rapports automatisés et périodiques peuvent également être utilisés (notamment pour les autorités).
  
  - Il faut faire très attention aux faux positifs et faux négatifs, car ils peuvent entrainer des pertes de confiance dans l'application.
    On pourrait ajouter par exemple: un niveau de confiance à chaque alerte, donné par l'IA. On les analyserait ensuite et ferait apprendre à l'IA.

En résumé, l’application assure un pilotage intelligent, un contrôle et une analyse intelligente, automatisée et pratique pour les utilisateurs.
Elle vise à garantir l'application des principes de la réglementation HACCP, pour alléger la charge de travail du personnel et renforcer la conformité sanitaire.

#### 1\.1.2 Espérance de retour sur investissement

L’application présente un solide potentiel de ROI, car elle répond à un besoin largement répandu en France.

On compte environ 800 cuisines centrales en France : des établissements qui produisent des plats en grande quantité, livrés sur plusieurs sites

Mais on dénombre au total près de 90 000 restaurants collectifs (écoles, hôpitaux, EHPAD, entreprises, etc.). Ce sont toutes des cuisines collectives. C'est un terme générique désignant toute structure proposant des repas  "hors du foyer" pour une collectivité.

En France, près de *90 000 inspections sanitaires* sont effectuées chaque année dans les établissements alimentaires (pas uniquement des restaurants collectifs).

Sur les 57 500 restaurants collectifs contrôlés, on estime près de 4 600 à 6 000 fermetures par an (8% des contrôles). Ce sont donc au moins 10 000 utilisateurs potentiels, ou restaurants collectifs ayant besoin d'une solution telle que celle-ci.

##### Modèle économique

Nous prévoyons de proposer notre solution à la location. Cela permet de réduire le coût initial pour les établissements, tout en garantissant un revenu récurrent pour notre entreprise.
Nous nous occupons de la maintenance, de la mise à jour et de l'assistance technique, ce qui est un avantage pour les clients.

On peut différencier les cuisines centrales et les restaurants collectifs, selon leur taille.

\- On peut proposer pour les grandes cuisines centrales (+ de 500 repas/jour) un forfait aux alentours de 500 €/mois. Avec un coût de migration ou installation de 1 200 €   
\- Pour les cuisines moyennes (entre 100 et 300 repas/jour), l'abonnement pourrait être à 200-300€ / mois. Avec un coût de départ de 500 €.  
\- Pour les petites cuisines (50 repas/jour), l'abonnement pourrait être à 50€ / mois. Avec un coût de départ de 300 €.

Nous basons ces calculs sur le coût de nos capteurs (environ 25€ par capteur, si on sous traite la fabrication). Ainsi, l'idée est de fournir selon la taille du restaurant un certain nombre de capteurs. 

Pour une petite cuisine, 5 ou 6 capteurs devraient suffir, mais cela peut monter à 10 pour une cuisine moyenne et même 20 pour une grande cuisine centrale. Ainsi, cela fait monter le coût de fabrication d'un pack, qui inclut également plusieurs tablettes (selon la volonté de l'établissement), des répéteurs si certains capteurs sont dans des chambres froides et que les ondes ne passent pas très bien, ainsi qu'un serveur local centralisant toutes les données et enregistrant, notamment en cas de coupure avec internet.

Nous estimons le coût de notre recherche & développement à environ **300 000 €** **sur 6 mois**  pour 4 développeurs (coût employeur de 75 000 €/an) et 1 chef de projet expérimenté + consultant métier/expert HACCP.

Pour les cuisines centrales, avec 500€\*12 mois + 1200 €, le **chiffre d'affaire serait de 7 200 €**.  
Environ 42 cuisines centrales suffiraient à couvrir le coût R&D.
Pour les cuisines moyennes, le **CA serait de 3 500 €**. Avec 86 clients, nous pouvons amortir la R&D. Il faudrait 334 petites cuisines pour cela.

##### Croissance des clients

La première année servirait de bêta : 10 grandes, 20 moyennes et 50 petites cuisines pilotes Ce qui constituerait un **CA de 187 000 €**.

La deuxième année on espère passer à 30 centrales, 200 moyennes et 100 petites. Ainsi notre CA serait de 840 k€/an. 

Si l'on inclut le coût des capteurs et matériels. Les coûts pour une petite cuisine sont de 525 € de mise en place + 96 €/an. Nous serions donc en négatif sur les petites cuisines la première année. Pour une moyenne, le coût de première année serait 875€ de coût fixe + 96€/mois = +2 029€

Le résultat la première année serait de 79 070 €, puis de 522 320 € la deuxième année. Il faudrait environ 1 an et demi pour rembourser le coût R&D.

### 1\.2 Contexte

#### 1\.2.1 Situation du projet par rapport aux autres projets de l’entreprise

Ce projet de Recherche et Développement s'inscrit dans une démarche scolaire d'innovation sur une entreprise fictive. Cette entreprise fictive a pour seul projet actuel de concevoir une application simplifiant la gestion de règles de HACCP dans des lieux de restauration, plus précisément dans des cuisines collectives.

On peut considérer ce projet comme pilote de la société fictive. L'objectif est de simuler les conditions d'une jeune entreprise innovante. Il montre la faisabilité et l'intérêt du suivi des règles HACCP de manière intelligente.
C'est donc le premier projet, et initiateur de l'entreprise fictive, qui pourrait par la suite en développer d'autres.
C'est un projet important pour cette entreprise, car il s'agira à la fois d'un essai technique des capacités technologiques de celle-ci, mais aussi d'une vitrine de son savoir faire.

#### 1\.2.2 Études déjà effectuées

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
- **Source** : <https://www.eezytrace.com>

---

**HACCP Facile**
- **Description** : Application mobile légère destinée aux petits établissements.
- **Fonctionnalités** : 
  - Checklists HACCP.
  - Saisie manuelle des températures.
  - Alertes basiques.
- **Avantages** : Simplicité, coût très abordable.
- **Limites** : Pas de capteurs, peu de fonctions avancées.
- **Source** : <https://www.haccp-facile.com>

lignes: toutes les applications
colonnes: fonctionnalités

---

#### Tableau comparatif

| Critère                  | Traqfood | Eezytrace    | HACCP Facile |
|--------------------------|----------|--------------|--------------|
| Capteurs connectés       | oui      | oui          | non          |
| Alertes automatiques     | oui      | oui          | non          |
| Historique des actions   | oui      | oui          | non          |
| Analyse prédictive / IA  | non      | non          | non          |
| Mode hors-ligne          | non      | non          | oui  partiel |
| Interface intuitive      | oui      | non          | oui          |
| Personnalisation secteur | non      | oui  partiel | non          |
| Coût                     | Moyen    | Élevé        | Faible       |

---

#### Enseignements pour notre projet (plus value du projet)

L’étude des solutions existantes met en évidence plusieurs opportunités d’amélioration :

- Intégrer une **analyse prédictive** à l’aide d’algorithmes d’IA pour prévenir les non-conformités.
- Offrir une **interface personnalisable** selon les types d’établissements (EHPAD, cantines scolaires, hôpitaux).
- Assurer un fonctionnement en **mode hors-ligne** avec synchronisation différée.
    Pour cela, il faut prévoir un serveur local qui centralise et enregistre les données, avec une synchronisation automatique dès que le réseau est de nouveau disponible.
- Maintenir une **interface simple et accessible** tout en répondant aux exigences HACCP.
- Proposer une **solution modulaire** avec des fonctionnalités avancées (analyse, rapports, alertes) en option.
- Intégrer des **capteurs robustes** adaptés aux environnements de cuisine collective (résistants à l’humidité, aux graisses, etc.).
- Permettre une **traçabilité complète** des aliments, de leur origine à leur consommation, avec des étiquettes et scans.
- Intégrer des **fonctionnalités de gestion des allergies** et des intolérances alimentaires, pour suivre les allergies des utilisateurs et générer des alertes en cas de risque d'allergie.
- Proposer une **gestion des stocks** pour suivre les produits en stock, les dates de péremption et les quantités disponibles.


Ces éléments différenciateurs permettront à notre solution de répondre de manière plus ciblée aux besoins spécifiques des cuisines collectives.

#### 1.2.3 Études menées sur des sujets voisins
#### Protection des données (RGPD)
(Règlement Général sur la Protection des Données)

- **Data Legal Drive** – Plateforme SaaS française (EQS Group) de gouvernance RGPD. Elle offre diagnostic de conformité, registres de traitement collaboratifs, gestion automatisée des demandes de droits, gestion des incidents (failles), veille juridique, et rapports centralisés  
  https://appvizer.fr  
  Plus de 20000 utilisateurs (DPO de grandes entreprises) l’utilisent  
  https://ccistore.fr  
  Tarifs :
    - TPE (≤250 personnes) : 195€/mois
    - PME (≤1000) : 375€/mois
    - ETI (≤2500) : 775€/mois (grandes entreprises sur devis)

- **Dastra** – Plateforme RGPD made in France, didactique et modulable  
  https://appvizer.fr  
  Fonctions : registre des traitements, gestion des droits (accès, rectification…), PIA, déclaration d’incidents, audits internes, plan d’action, veille RGPD.  
  Versions :
    - Starter (gratuite) : registre, planification, cartographie des données, veille, gestion documentaire
    - Pro : + AIPD, gestion des droits, incidents, audits
    - Entreprise : + gestion des risques, portail privacy, reporting personnalisés, SSO, etc.  
      https://dastra.eu  
      Tarifs : sur devis.

- **Mission RGPD** – Plateforme tout-en-un et DPO externalisé. Elle combine logiciel RGPD (audits, registres, plan d’actions, documents réglementaires) et sensibilisation (e-learning RGPD)  
  https://mission-rgpd.com  
  Plus de 1000 structures en Europe.  
  Tarifs PME (jusqu’à 50 salariés) :
    - Solo : 139€HT/mois
    - Coach : 239€HT/mois
    - Academy : 199€HT/mois
    - DPO Externe : 439€HT/mois  
      https://donnees.net

- **Witik** – Plateforme RGPD collaborative française (leur RGPD + module IA Act, Sapin II, etc.)  
  https://witik.io  
  Plan Starter (gratuit) : jusqu’à 30 traitements créés, 2 PIA, 2 audits, 10 demandes de droits/an, 10 incidents/an  
  Plan Premium (engagement 36 mois) à partir de 240€HT/mois : fonctionnalités illimitées (registres, PIA, audits, droits, incidents, etc.)  
  Version d’essai 14 jours disponible.

- **OneTrust** – Solution internationale de Privacy Management (RGPD, LGPD, CCPA, ePrivacy…) très utilisée.  
  Modules : registres, consentements, cartographie des données, audits, reporting.  
  Plusieurs éditions disponibles (gestion programme de confidentialité, privacy marketing, etc.)  
  https://appvizer.fr  
  Version de démonstration gratuite 14 jours.  
  Tarifs : sur devis.

#### Sécurité au travail

- **TEEXMA for EHS (Bassetti Group)** – Suite QHSE modulable. Modules :
    - Évaluation des risques chimiques (référentiel substances, FDS, calcul INRS CLP)
    - Document unique (DUERP, RPS)
    - Accidents du travail (déclarations AT/MP)
    - Suivi des habilitations, formations, vérifications périodiques (VPR), indicateurs QHSE  
      https://bassetti-group.com  
      Tarifs : sur devis (licences modulaires)

- **SIGMA-RH (suite SST)** – Logiciel HSE modulaire. Modules :
    - Accidents du travail / maladies professionnelles
    - DUERP et prévention
    - Cotisations AT/MP
    - Visites médicales, rappels de vaccination  
      https://sigma-rh.com  
      Automatise les déclarations réglementaires (accidents, DUERP, PAPRIPACT).  
      Tarifs : sur devis

- **Qualishare QHSE** – Plateforme française intégrée « tout-en-un » (Qualité, Sécurité, Environnement, RSE, RH).  
  Paramétrable, compatible ISO 9001, 14001, 45001.  
  Fonctionnalités : incidents, audits, CAPA, documents, tableaux de bord, etc.  
  Intégration SharePoint possible  
  https://qualishare.fr  
  Tarifs : à partir de 99€HT/mois (≤10 utilisateurs, 3Go)  
  Essai gratuit disponible.

- **SafetyCulture (iAuditor)** – Application mobile d’inspection et d’audit de sécurité.  
  Création de checklists personnalisées, contrôle qualité, prise de photos/vidéos d’incidents, actions correctives, analyses.  
  https://safetyculture.com  
  Version gratuite (≤10 utilisateurs), Premium ~24$US/mois/siège.  
  Essai gratuit 30 jours.

#### Environnement (ISO 14001, gestion des déchets)
(Organisation internationale de normalisation)
- **Nimonik** – Plateforme EHS/Q internationale.  
  Gère les obligations légales et les normes ISO (14001, 45001), audits, veille réglementaire.  
  https://nimonik.com  
  Tarifs : licence de base ~$2000/an, audits internes ~500$

- **Quentic** – Plateforme allemande EHSQ/ESG.  
  Module ISO 14001 complet : documentation, indicateurs, audits, amélioration continue.  
  https://quentic.com  
  Tarifs : sur demande.

- **Symalean – Dyo Environnement** – Plateforme française ISO 14001/50001.  
  Gère impacts environnementaux, risques, produits chimiques, déchets, incidents.  
  https://symalean.com  
  Tarifs : sur devis.

- **BlueKanGo (module déchets)** – Module HSE de gestion des déchets.  
  Traçabilité complète (bordereaux, registre, poids, transport, prestataires, traitement).  
  Intégration nomenclature INERIS + reporting.  
  https://bluekango.com  
  Tarification personnalisée (intégré à suite QHSE/RSE).

#### 1\.2.4 Suites prévues

Ce projet doit contenir plusieurs fonctionnalités essentielles telles que: 
- La collecte de données en temps réel via des capteurs IoT résistants, résilients, performants et adaptés aux environnements de cuisine collective.

- Des opérations de maintenance prédictive pour les équipements de notre application, afin d'anticiper les pannes et garantir la continuité du service.
- La traçabilité des aliments et la gestion de l'hygiène, simplifiée par des étiquettes et des scans.

- L'analyse des données collectées par l'application, avec des algorithmes d'intelligence artificielle pour prévenir les dérives et anomalies, et apprendre des tendances.
- L'envoi d'alertes en temps réel, la production de rapports et la fourniture d'un tableau de bord centralisé pour les gestionnaires et les autorités sanitaires.

- Le suivi des actes de nettoyage et des relevés quotidiens d'informations, pour garantir le respect des normes HACCP.
- La gestion de l'ouverture d'un produit, enregistrement de la date d'ouverture, de la date de péremption et des conditions de conservation (température, humidité, etc.).

- Lors de la sortie d'un produit d'une zone avec une certaine température (ex: chambre froide), l'application doit vérifier que la température est conforme aux normes HACCP, et alerter en cas de non-conformité.
    Ainsi que noter le temps de chaque étape de la préparation des aliments, pour garantir le respect des temps de cuisson et de refroidissement.
    Par exemple, ne pas rester + de 2h entre 5 °C et 60 °C / ne pas dépasser 2h entre la sortie du frigo et le passage à + de 60 °C.
- Un serveur local dans l'établissement, centralisant les données et permettant un fonctionnement en mode dégradé, sans connexion internet.

Il s'agit d'un projet ambitieux, c'est pourquoi il faut le mener en plusieurs phases.
La première est celle décrite dans ce cahier des charges, mais certaines autres fonctionnalités pourraient être envisagées dans le futur, comme :
- Une synchronisation des données entre nos serveurs et le serveur local, pour garantir la continuité du service même en cas de coupure réseau, et une synchronisation en cas de problème.
- Une interface web d'administration centralisée, permettant aux gestionnaires de visualiser et gérer les données de l'application depuis un navigateur.
- Une fonctionnalité de gestion des allergies et des intolérances alimentaires, permettant de suivre les allergies des utilisateurs et de générer des alertes en cas de risque d'allergie
(nécessite la gestion des données de santé et donc être certifié HDS).
- Une fonctionnalité de gestion des stocks, permettant de suivre les produits en stock, les dates de péremption et les quantités disponibles.

#### 1.2.5 Nature des prestations demandées

Dans le cadre de ce projet, certaines tâches seront confiées à des prestataires externes spécialisés ou à des partenaires techniques. Les prestations attendues sont les suivantes :

#### Conception et développement technique
- Développement de l’application mobile multiplateforme (Android/iOS), incluant :
    - Interfaces utilisateurs (UX/UI) conformes aux maquettes validées
    - Fonctionnalités principales : saisie du PMS, collecte de données, alertes, tableau de bord, lecture et création des étiquettes
    - Fonctionnalités complémentaires : historique, mode hors-ligne, personnalisation
- Intégration d’un système de gestion des utilisateurs et des droits d’accès
- Implémentation de mécanismes de synchronisation des données (local ↔ cloud)
- Mise en place d’un serveur local pour la centralisation des données et le fonctionnement en mode dégradé
- Développement d’algorithmes d’analyse prédictive et de détection des anomalies
- Ressources nécessaires à une évolution du produit en cas de problème avec le prestataire (documentation technique, code source, etc.)

#### Fabrication, livraison et installation de capteurs IoT
- Conception et fourniture de capteurs IoT adaptés à l’environnement des cuisines collectives :
    - Capteurs de température, humidité, ouverture de porte ou présence
    - Boîtiers robustes, étanches, résistants aux graisses et aux basses températures

    - Autonomie minimale de 6 mois, connectivité BLE, RF 433 MHz, WiFi ou autres protocoles adaptés
        - Prévoir un remplacement facile des piles ou batteries si nécessaire, avec une seconde batterie pour les capteurs critiques
            Permettant de ne pas perdre de données durant le remplacement de la pile.
        - Prévoir un système de notification pour alerter l'utilisateur lorsque la pile est faible.
        - Prévoir des piles ou batteries également pour les capteurs branchés sur secteur, afin de garantir la continuité de l'historique 
            en cas de coupure de courant.
    - Capteurs adaptés aux conditions extrêmes (températures de -40 °C à +100 °C, humidité élevée, atmosphère chargée en graisses)
    - Il faut trouver et prévoir une solution technique pour les zones blanches (chambres froides, sous-sols, etc.) où la connectivité est limitée.
        Potentiellement des capteurs avec une connectivité RF 433 MHz (onde pouvant traverser plus facilement une couche épaisse) et/ou des répéteurs de signal pour les zones où le signal est faible.
        À développer en collaboration avec le fournisseur de capteurs.

- Personnalisation du firmware selon nos besoins :
    - Intervalle de mesure ajustable
    - Protocoles de communication compatibles avec l’application
- Livraison sur site des capteurs:
    - Préparation des capteurs (configuration, tests de connectivité)
    - Installation physique dans les zones critiques (chambres froides, zones de préparation, etc.)
    - Vérification de la connectivité et des mesures

#### Qualité, tests et validation
- Réalisation de tests unitaires et fonctionnels sur les modules applicatifs
- Tests de réception des capteurs installés
- Correction des anomalies détectées lors de la phase de recette
- Fourniture d’un protocole de tests et d’un rapport de validation

#### Conformité réglementaire et sécurité
- Mise en œuvre de mesures de sécurité conformes au RGPD :
    - Authentification sécurisée
    - Gestion des accès utilisateurs
    - Chiffrement des données sensibles
- Fourniture d’une documentation technique de conformité RGPD

#### Livraison et documentation
- Livraison d’un prototype fonctionnel de l’application mobile
- Livraison des capteurs installés et fonctionnels
- Documentation technique complète (utilisation, maintenance, RGPD)
- Accompagnement à l’installation de l’application sur terminaux mobiles

#### Options (selon budget)
- Développement d’une interface web d’administration centralisée
- Maintenance corrective sur 3 mois après livraison
- Ajout de capteurs supplémentaires ou évolutions logicielles futures

---

Toutes les prestations doivent respecter les exigences fonctionnelles définies dans le présent cahier des charges, ainsi que les contraintes techniques, environnementales et réglementaires mentionnées dans les sections précédentes.

#### 1.2.6 Parties concernées par le déroulement du projet et ses résultats (demandeurs, utilisateurs)

Diagramme RACI des parties du projet et des étapes

R: Responsible = Celui qui Réalise la tâche
A: Accountable = Décisionnaire, approuve le résultat
C: Consulted = Consulté, doit donner son avis (expert)
I: Informed = Tenu au courant de toutes les avancées

| Tâche                                              | Administration et direction | Equipe de développement | Sous traitant: capteurs, matériel et installation | Gestionnaire de cuisine | Cuisiniers |
| -------------------------------------------------- | --------------------------- | ----------------------- | ------------------------------------------------- | ----------------------- | ---------- |
| I - Conception du projet                           |                             |                         |                                                   |                         |            |
| Cahier des charges                                 | A                           | R                       |                                                   | A                       | C          |
| Besoins des utilisateurs                           | A                           | R                       |                                                   | C                       | C          |
| Conception de l'application                        | A                           | R                       |                                                   |                         |            |
| Technique et spécification des capteurs            | A                           | C                       | R                                                 | C                       |            |
| II - Développement                                 |                             |                         |                                                   |                         |            |
| Capteurs IoT et matériels                          | A                           | C                       | R                                                 | I                       | I          |
| Application mobile                                 | A                           | R                       |                                                   | I                       | I          |
| Serveurs et sauvegarde                             | A                           | R                       |                                                   |                         |            |
| III - Déploiement                                  |                             |                         |                                                   |                         |            |
| Préparation des capteurs et analyse sur le terrain | A                           | I                       | R                                                 | C                       | C          |
| Installation de l'application                      | A                           | R                       |                                                   | I                       | I          |
| Installation des capteurs                          | A                           | C                       | R                                                 | I                       | I          |
| Tests d'utilisation                                | I                           | I                       | A                                                 | C                       | R          |
| IV - Maintenance / Retour                          |                             |                         |                                                   |                         |            |
| Remplacement préventif ou curatif des capteurs     | I                           | C                       | R                                                 | A                       | I          |
| Suivi des données                                  | A                           | R                       |                                                   |                         |            |
| Mises à jour et corrections                        | A                           | R                       |                                                   | C                       | I          |



#### 1.2.7 Caractère confidentiel s'il y a lieu
Les données de ce projet peuvent être sensibles car elles incluent notamment des données précises sur l'environnement, les actions et procédures effectuées, la traçabilité des denrées et certaines informations sur le personnel.
Nous utilisons également certaines données de santé, ex: accident en contact avec la nourriture sera journalisé et noté. Nous souhaitons en inclure d'autres, comme les restrictions alimentaires.
À ce titre, nous devons pour ces données respecter l'article 4 du RGPD et être validé comme Hébergeur de Données de Santé (HDS).

En globalité, toutes les données qui incluent des données sur les utilisateurs doivent être soumises au RGPD, c'est-à-dire:
Permettre l'accès, la modification et la suppression des données de chacun. Et informer sur chaque donnée enregistrée, les raisons de cette sauvegarde, et demander le consentement de l'utilisateur.

À propos du projet en lui même, cela est un projet lourd et complexe à réaliser, il demande une lourde Recherche & Développement. Nous pensons que notre projet technique pourrait alors être sujet au dépôt d'un brevet si celui-ci est suffisamment innovant. Et d'une protection de droit d'auteur de l'application.

### 1.3 Énoncé du besoin 
*(finalités du produit pour le futur utilisateur tel que prévu par le demandeur)*

Dans les cuisines collectives, la réglementation HACCP impose des normes strictes pour garantir la sécurité alimentaire.
Le respect de ces normes est essentiel pour prévenir les risques sanitaires, il doit être systématique et rigoureux. 
Cependant, la mise en œuvre de ces normes est souvent complexe et chronophage pour le personnel.

En réponse à cela, nous proposons ce produit innovant, une application mobile dédiée à la gestion des règles HACCP dans les cuisines collectives. Accompagné d'une solution matérielle de capteurs IoT, d'écrans/tablettes et d'un serveur local, notre solution vise à simplifier et automatiser le suivi des normes HACCP.
Les capteurs IoT collecteront en temps réel les données critiques (température, humidité, etc.) et les transmettront au serveur.
Les applications permettront d'enregistrer les procédures effectuées, de suivre les tâches de nettoyage, de gérer la traçabilité des denrées alimentaires et d'analyser les données collectées.

La solution permet également d'être alerté en temps réel en cas de non-conformité, de générer des rapports et de fournir un tableau de bord centralisé pour les gestionnaires et les autorités sanitaires.


Le client attend une solution complète, robuste et intuitive, qui lui permettra de garantir la conformité aux normes HACCP tout en allégeant la charge de travail du personnel.
Il doit aussi pouvoir réduire considérablement les risques sanitaires et alimentaires.

### 1.4 Environnement du produit recherché

#### 1.4.1 Liste exhaustive des éléments *(personnes, équipements, matières…)* et contraintes *(environnement, matériel, usage)*

L’application repose sur un réseau de capteurs connectés (IoT) permettant la collecte automatisée des données critiques en lien avec les exigences HACCP. Ces capteurs doivent être sélectionnés en fonction des contraintes spécifiques des cuisines collectives, à savoir : humidité, température extrême, graisses, nettoyages fréquents, connexions instables.


L’application repose sur un réseau de capteurs connectés (IoT) pour la collecte automatisée des données critiques HACCP. Elle devra fonctionner dans un environnement professionnel contraignant, avec des utilisateurs variés et une infrastructure réseau parfois instable.

##### Types de capteurs envisagés

- **Capteurs de température** : réfrigérateurs, congélateurs, fours, chambres froides.
- **Capteurs d’humidité** : contrôle de l’hygrométrie ambiante.
- **Capteurs de présence / ouverture** : détection de nettoyage, cycles HACCP.
- **Lecteurs RFID / codes-barres** : traçabilité des denrées alimentaires.

##### Conditions physiques d’utilisation

- **Températures extrêmes** : de –40°C (chambre froide) à **+100°C** (zone cuisson, plonge).
- **Humidité élevée, vapeur, graisses** : zones lavables, atmosphère chargée.
- **Surfaces glissantes / manipulabilité réduite** : nécessite interface robuste.
- **Utilisation avec gants / mains mouillées** : ergonomie renforcée.

##### Appareils utilisés

- **Smartphones / tablettes durcies** Android/iOS, souvent en usage intensif.
- Écrans de taille variable : besoin d’interface **responsive** et minimaliste.
- Application utilisée dans un environnement **bruyant et sous pression**.

##### Contraintes réseau et connectivité

- **Zones blanches fréquentes** (chambres froides, sous-sols).
- Besoin impératif d’un **mode hors-ligne stable**, avec **synchronisation automatique** dès retour réseau.
- Choix de capteurs adaptés selon la zone :
  - BLE (zones ouvertes, courte portée),
  - RF433 (zones isolées ou métalliques).

##### Contraintes d’usage et utilisateurs

- Profils variés : agents de cuisine, responsables HACCP, inspecteurs.
- **Compétences numériques hétérogènes** : interface simple et guidée.
- Application utilisée dans un **cadre normé** (audits, contrôles).
- Multilingue, avec **contraste fort et pictogrammes clairs**.

##### Sécurité des données – cadre réglementaire

- Données sensibles : identifiants personnels, historique d’interventions.
- Conformité **RGPD** :
  - consentement utilisateur obligatoire,
  - anonymisation partielle,
  - chiffrement local.

---

#### 1.4.2 Caractéristiques techniques attendues des éléments matériels

Les capteurs IoT, terminaux et modules doivent répondre à un ensemble de spécifications techniques garantissant leur bon fonctionnement dans les environnements visés.

##### Spécifications minimales pour les capteurs IoT

| Critère                     | Exigence minimale attendue                                 |
|-----------------------------|-------------------------------------------------------------|
| Température supportée       | De –40°C à **+100°C** selon zone                         |
| Étanchéité                  | **IP65 minimum**, IP68 recommandé                          |
| Précision capteurs          | ±0,5°C (température), ±5 % HR (humidité)                 |
| Autonomie                   | ≥ 6 mois (objectif 2 à 5 ans sur pile) avec batterie de rechange et câble                 |
| Stockage local              | ≥ 7 jours en cas de perte de liaison (jusqu’à 125 jours)  |
| Connectivité radio          | BLE / RF 433 MHz selon cas                 |
| Fixation                    | Aimant, collier ou support sans perçage                   |
| Matériaux                   | Inertes, étanches, certifiés usage alimentaire             |
| Compatibilité mobile        | Android 9+ / iOS 13+ / BLE 4.2+                            |
| Appairage / installation    | QR code, ID unique, reconnexion automatique               |

##### Technologies de transmission recommandées

| Technologie | Usage recommandé | Portée / Fiabilité | Autonomie | Débit |
|-------------|------------------|---------------------|----------|--------|
| BLE         | Zones proches, compatibilité mobile | 10–50m (obstacles sensibles) | Très bonne | Moyenne |
| RF 433 MHz  | Chambres froides / métalliques | 50–100m (très bonne traversée) | Bonne | Faible |

##### Sécurité, conformité et intégration

- Chiffrement des données : **AES-128 / AES-256** selon modules.
- Journalisation horodatée obligatoire pour audit HACCP.
- API REST ou MQTT pour intégration avec serveurs cloud / locaux.
- Conformité aux directives CE 852/2004, CE 178/2002, RGPD.

####  Interfaces utilisateurs

Les interfaces devront être pensées pour une **utilisation rapide et intuitive** dans des environnements de travail où les utilisateurs sont soumis à des contraintes physiques et temporelles.

- **Ergonomie tactile renforcée** : grands boutons, navigation simplifiée, menus déroulants adaptés à une manipulation avec gants ou mains mouillées.
- **Affichage adaptatif (responsive)** : l’application s’ajuste automatiquement à la taille et à l’orientation des écrans de smartphones ou tablettes.
- **Mode sombre / contraste élevé** : visibilité optimale dans des environnements à éclairage variable.
- **Multilingue** : au minimum français et anglais, avec possibilité d’extensions selon les utilisateurs.
- **Accessibilité** : prise en charge des bonnes pratiques d’accessibilité numérique (polices lisibles, navigation au doigt, alternatives textuelles aux icônes).

####  Architecture logicielle adaptée

L’application devra fonctionner dans des contextes **avec ou sans connexion Internet stable**. L’architecture doit donc permettre un **mode dégradé temporaire** sans perte de données.

- **Stockage local sécurisé** : les données doivent être enregistrées temporairement en local avec un serveur exterieur en cas de déconnexion, avec chiffrement (ex : AES-256).
- **Synchronisation différée** : automatique dès détection d’une connexion, avec gestion des conflits si plusieurs utilisateurs modifient les données.
- **Modularité** : architecture capable de désactiver certaines fonctionnalités non critiques si l’environnement réseau ou matériel l’exige.

####  Sécurité et conformité

- **Conformité RGPD** : gestion des droits utilisateurs, traçabilité des actions, consentement explicite à la première utilisation.
- **Chiffrement des échanges et stockage** : HTTPS pour la transmission, chiffrement local pour les données sensibles.
- **Journalisation** : tous les accès sensibles et modifications critiques doivent être tracés et consultables.

####  Profil utilisateur hétérogène

L’application sera utilisée par :
- Des **agents de cuisine**/ **chef de cuisine**, avec peu de temps disponible et parfois peu formés au numérique.
- Des **responsable HACCP**, plus à l’aise avec les outils, mais exigeant des données synthétiques claires.
- Éventuellement des **inspecteurs ou autorités sanitaires**, avec besoin d’accès ponctuel, sécurisé et en lecture seule.

La conception devra donc proposer :
- Des **profils utilisateurs distincts** (droits, vues, actions autorisées).
- Une **interface épurée**, focalisée sur les actions prioritaires selon le profil connecté.

---

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
- **Conformité réglementaire :** Les rapports générés respectent les normes HACCP et les exigences des autorités sanitaires.

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

Ces fonctions complémentaires ne sont pas accessoires (qui améliorent, facilitent ou complètent le service rendu) : elles participent à la **pérennité**, la **conformité** et la **bonne adoption** de la solution sur le terrain.

##### 2.1.2.1 Description et détail

Outre les fonctions principales indispensables au respect des règles HACCP, l’application devra proposer plusieurs **fonctions de service complémentaires**. Ces fonctionnalités, bien que non essentielles au strict fonctionnement du système, apporteront une **valeur ajoutée significative** en termes d’utilisabilité, d’autonomie, de conformité et d’adoption par les utilisateurs.

1. Tutoriels et rappels intégrés : Accompagner utilisateurs (prise en main, bonnes pratiques). Contenu interactif/textuel, rappels sur normes HACCP, consultation libre ou notifications contextuelles. Bénéfice : Réduction erreurs humaines, auto-formation
2. Historique des alertes et actions correctives : Traçabilité complète des anomalies et mesures correctives. Journal détaillé/horodaté, archivage actions (responsable, type, délai), exportation (PDF, Excel) possible pour audits. Bénéfice : Amélioration transparence et conformité
Selon le PMS, l'IA donne les actions correctives
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
#### 3.1.1 Fonction : Collecte automatique de données environnementales

##### Objectif

Assurer la **collecte automatisée, sécurisée et traçable** des données environnementales, opérationnelles et comportementales liées à la conformité HACCP. Cette collecte doit rester fonctionnelle même en conditions extrêmes (chaleur, froid, humidité) ou sans réseau, et déclencher des alertes en cas de non-conformité.

---

##### Architecture fonctionnelle de la collecte

1. **Capteurs → Application mobile**  
   - Capteurs connectés via BLE ou RF 433 MHz (selon zones).  
   - Données stockées localement sur l’application (cryptées).  
   - Synchronisation différée automatique vers le serveur HACCP.

2. **Systèmes de traçabilité**  
   - Lecture RFID ou codes-barres.  
   - Enregistrement des mouvements produits/lots.  
   - Journalisation des opérations.

3. **Interface utilisateur**  
   - Questionnaires hygiène / formation / validation manuelle.  
   - Données saisies → stockage local → analyse → transmission serveur.

---

##### Sécurité & confidentialité

- **Chiffrement AES-256** des données transmises et stockées localement.
- **Appairage sécurisé** des capteurs par QR code ou ID unique.
- **Consentement utilisateur** requis à l’activation.
- **Traçabilité complète** : tous les accès et modifications sont loggés (journalisation activée).

---

##### Points forts de la solution proposée

- Collecte **multi-source** : capteurs environnementaux, saisie manuelle, RFID.
- Fonctionnement **hors-ligne garanti**, avec **synchronisation automatique**.
- Système **modulaire**, compatible multi-sites (scolaire, hospitalier, EHPAD).
- Déclenchement **immédiat d’alertes** en cas de non-conformité.

---

##### Scénarios d’usage

**Scénario 1 – Alerte de dépassement de température (capteur IoT)**  
- 6h30 : le capteur BLE de la chambre froide enregistre 6,8 °C.  
- Le seuil critique étant 4°C, l’application déclenche une **alerte immédiate**.  
- Le chef cuisine est notifié, accède à l’historique, confirme une action corrective.

**Scénario 2 – Validation automatique du nettoyage**  
- Un capteur de présence est fixé dans la zone de plonge.  
- À 15h30, un nettoyage est prévu. À 15h45, aucune détection.  
- L’application **détecte une tâche non effectuée** → alerte.  
- Si une présence est détectée ensuite (15h30–16h), la tâche est **validée automatiquement**.

**Scénario 3 – Questionnaire d’hygiène saisi par un agent**  
- L’agent ouvre l’application sur tablette durcie.  
- Il complète un **formulaire de 5 questions** (hygiène poste froid).  
- Les réponses sont stockées localement puis transmises.  
- Un **score est généré** et accessible au responsable HACCP.

---

##### WBS associé à la collecte HACCP

La collecte automatique s’appuie sur les 7 sous-fonctions suivantes :

1. **Intégration des capteurs IoT**  
   - 1.1 Sélection (température, humidité, présence)  
   - 1.2 Compatibilité radio (BLE / RF433)  
   - 1.3 Appairage sécurisé  
   - 1.4 Test IP65/IP68, autonomie, précision

2. **Lecture automatisée des données**  
   - 2.1 Configuration des intervalles (ex : toutes les 10 min)  
   - 2.2 Stockage local chiffré  
   - 2.3 Déclenchement d’alertes

3. **Synchronisation des données**  
   - 3.1 Mécanisme de synchro différée  
   - 3.2 Transmission HTTPS/MQTT  
   - 3.3 File d’attente et gestion des conflits

4. **Traçabilité alimentaire**  
   - 4.1 Scan RFID / codes-barres  
   - 4.2 Association lots-produits  
   - 4.3 Journalisation des stocks

5. **Données comportementales**  
   - 5.1 Questionnaires hygiène / formation  
   - 5.2 Stockage et scoring automatisé  
   - 5.3 Suivi nominatif ou anonyme

6. **Système d’alertes et journalisation**  
   - 6.1 Relevés capteurs  
   - 6.2 Historique actions correctives  
   - 6.3 Suivi des validations manuelles

7. **Sécurité et conformité RGPD**  
   - 7.1 Chiffrement AES-256  
   - 7.2 Gestion des droits (profils utilisateurs)  
   - 7.3 Consentement utilisateur

---

**WBS – Collecte des données HACCP**
<img src=img/export.png>

Cette architecture permet un contrôle rigoureux, automatisé et intelligent du respect des normes HACCP, tout en restant simple à déployer et à maintenir.
*__Jalon__ : date à laquelle la fonction doit être livrée.*

#### 3\.1.2 Niveau atteint pour chaque critère d’appréciation de cette fonction et modalités de contrôle

- **Temps de réponse** : < 3 secondes pour l’affichage d’une alerte (testé sur 10 scénarios).
- **Fiabilité** : Précision des capteurs ±0,5°C, taux de transmission >98% (tests de validation sur 1 semaine).
- **Accessibilité** : Interface utilisable avec gants, multilingue (tests utilisateurs en conditions réelles).

#### 3\.1.3 Part du prix attribué à chaque fonction

- **Collecte des données** : 30% du budget (capteurs, intégration IoT, stockage sécurisé).
- **Tableau de bord** : 20% du budget (UX/UI, développement front-end, personnalisation).
- **Alertes et notifications** : 10% du budget (système d’alerte, notifications mobiles/SMS).
- **Synchronisation/hors-ligne** : 15% du budget (gestion des données locales, synchronisation serveur).
- **Conformité RGPD** : 10% du budget (anonymisation, gestion des droits, logs).
- **Documentation et tutoriels** : 5% du budget (contenus, intégration).
- **Maintenance/évolutivité** : 10% du budget (support, mises à jour).

#### 3\.1.4 Jalons associés

| Fonction             | Jalon (date/étape)               | Modalité de contrôle         |
|----------------------|----------------------------------|------------------------------|
| Collecte des données | Prototype capteurs (Semaine 3)   | Test de collecte automatisée |
| Tableau de bord      | Maquette validée (Semaine 5)     | Test utilisateur             |
| Alertes              | Système opérationnel (Semaine 6) | Simulation d’anomalie        |
| Synchronisation      | Démo hors-ligne (Semaine 7)      | Test de coupure réseau       |
| RGPD                 | Audit conformité (Semaine 8)     | Vérification documentation   |

### 3\.2 *Pour chaque fonction : fonction 2*

#### 3\.2.1 Solution proposée

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
### 3.3 Pour l’ensemble du produit
#### 3.3.1 Prix de la réalisation de la version de base
##### Capteurs connectés (IoT)
la version de base de l’application HACCP repose sur un déploiement fonctionnel dans une cuisine collective de taille moyenne (type EHPAD, lycée, cuisine centrale). Elle inclut les capteurs environnementaux, les équipements mobiles, la connectivité, ainsi que l’infrastructure serveur et la maintenance initiale.

---

#####  Estimation des coûts – Matériel et services (HT)

| Équipement / service                         | Qté | Prix unitaire (€ HT) | Coût total (€ HT) | Références / Remarques |
|---------------------------------------------|-----|----------------------|--------------------|-------------------------|
| **Capteurs (T°, H°, présence)**             | 7   | 25                   | 175€              | Estimation basée sur capteurs BLE / RF 433 sur [AliExpress](https://fr.aliexpress.com/item/1005004905171281.html) |
| **Lecteur RFID / code-barres**              | 1   | 90                   | 90€               | Lecteur fixe ou mobile standard |
| **Passerelles RF433**                       | 2   | 19                   | 38€               | Sonoff RF Bridge R2 : [Domotique-store.fr](https://www.domotique-store.fr/domotique/types-d-objets/objets-connectes/gateways-passerelles/6598-sonoff-rf-bridge-r2-passerelle-433mhz-wifi.html) |
| **Batteries rechargeables**                 | 7   | 5                    | 35€               | Batterie Li-ion / CR2032 rechargeables |
| **Chargeurs (USB)**                         | 2   | 15                   | 30€               | Chargeurs doubles ou stations |
| **Tablettes / smartphones durcis**          | 2   | 249,90               | 499,80€           | Crosscall Core-M5 : [crosscall.com](https://www.crosscall.com/fr/produit/core-m5/) |
| **Serveur local / mini-PC (type Raspberry)**| 1   | 200                  | 200€              | Serveur local, stockage sécurisé |
| **Installation initiale**                   | 1   | 300                  | 300€              | Pose capteurs, appairage, test |
| **Maintenance annuelle (estimée)**          | 1   | 200                  | 200€              | Contrôle, support, remplacement |

| **TOTAL ESTIMÉ HT**                         |     |                      | **1567,80€**     | Sans coûts de développement logiciel |

---

##### Hypothèses

- Capteurs BLE ou RF433 avec stockage local + synchronisation.
- 2 tablettes durcies pour alternance ou multi-utilisateurs.
- Passerelles RF433 pour zones métalliques.
- Le serveur local assure la synchronisation des données chiffrées.

**Part du budget global estimé :** environ **30 % du coût total** de la solution de base (application + capteurs + hébergement serveur).

Cette estimation pourra évoluer selon les sites pilotes (surface, nombre de chambres froides, besoins en redondance) et les choix de fournisseurs lors du prototypage.


#### 3.3.2 Options et variantes proposées non retenues au cahier des charges
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
#### 3.3.3 Mesures prises pour respecter les contraintes et leurs conséquences économiques
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

#### 3.3.4 Outils d’installation, de maintenance … à prévoir

**1. Maintenance logicielle**

- **Mises à jour de l’application mobile** :
  - Fréquence : mensuelle (corrections de bugs, améliorations UX, sécurité).
  - Canal : via les stores (Google Play, App Store) ou MDM interne pour appareils pro.
  - Rétrocompatibilité assurée avec les capteurs existants et données stockées.

- **Suivi de la synchronisation et des performances** :
  - Journalisation des erreurs (logs techniques).
  - Système d’alerte automatique en cas d’échec ou lenteur de synchronisation.
  - Correctifs déployés en mise à jour prioritaire en cas de dysfonctionnement critique.

- **Maintenance des modules IA (si activés ultérieurement)** :
  - Recalibrage ou entraînement périodique des modèles.
  - Vérification des seuils d’alerte (non-conformité prédite, profil de risque évolutif).

---

**2. Maintenance matérielle – Capteurs IoT**

- **Vérification périodique du bon fonctionnement** :
  - Contrôle hebdomadaire automatisé des transmissions (signal, batterie, valeurs).
  - Détection des capteurs inactifs (inactivité > 30 min) → alerte au gestionnaire.

- **Remplacement des capteurs** :
  - Capteurs à batterie longue durée (≥ 6 mois).
  - Remplaçables sans reconfiguration (ID unique, auto-reconnaissance via l’application).
  - Procédure standardisée d’installation disponible dans l’app (guide ou tutoriel).

- **Calibration** :
  - Température / humidité recalibrées tous les 6 à 12 mois selon environnement.
  - Enregistrement des interventions de maintenance dans le journal système.

---

**3. Maintenance des données**

- **Archivage automatique** :
  - Les données HACCP (relevés, alertes, questionnaires) sont archivées localement puis exportées vers le serveur sécurisé (fréquence configurable, ex. 7 jours).
  - Conformité RGPD assurée : durée de conservation limitée, droit à l’effacement, anonymisation possible.

- **Sauvegarde** :
  - Backup automatique des bases locales (app mobile) en cas de plantage ou désinstallation.
  - Export manuel possible sur demande (clé USB, PDF, fichier chiffré).

---

**4. Support technique**

- Interface dédiée pour les administrateurs (facultative) permettant :
  - Suivi en temps réel de l’état des capteurs
  - Consultation de l’historique des erreurs et interventions
  - Déclenchement manuel d’une synchronisation ou d’une vérification système

#### 3.3.5 Décomposition en modules, sous-ensembles

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
#### 3.3.7 Perspectives d’évolution technologique
## 4 Prévisions de fiabilité – Gestions des risques
### 4.1 Risques à la réalisation
*__Profils de risques__ pour chaque fonction de service*
<img src=img/profil_de_risque.png>
### 4.2 Prévision des défaillances
*Table de défaillance pour chaque fonction de service avec un paragraphe commentant chaque défaillance et/ou chaque cause/effet/détection d’importance notable*
| Fonction du produit              | Mode de défaillance                   | Effet de la défaillance                              | Causes possibles de la défaillance                   | Détection | Occurrence | Gravité | Criticité (D×O×G) |
|----------------------------------|---------------------------------------|------------------------------------------------------|------------------------------------------------------|------------|-------------|----------|--------------------|
| 1-Capteur IoT       | Capteur inactif                       | Non-détection d’un dépassement de seuil critique     | Batterie vide, signal coupé, défaut matériel         | 6          | 5           | 9        | 270                |
| 1-Capteur de présence nettoyage    | Pas de détection durant le créneau    | Tâche non réalisée mais non signalée                 | Mauvais positionnement, zone non couverte            | 1          | 3           | 8        | 24                |
| 3-Synchronisation mobile-serveur   | Données non transmises ou corrompues  | Perte de traçabilité, non-conformité réglementaire   | Perte de réseau, plantage de l’app mobile            | 8          | 4           | 10        | 320                |
| 2-Stockage local des données       | Saturation mémoire, perte hors ligne  | Données perdues avant synchronisation                | Manque de contrôle espace, bug système               | 8          | 3           | 10       | 240                 |
| 6-Application mobile               | Crash ou freeze                       | Blocage temporaire de la collecte                    | Erreur de code, surcharge mémoire, conflits système  | 3          | 3           | 8        | 72                 |
| 5-Saisie questionnaire personnel   | Réponses incomplètes ou erronées      | Mauvais suivi comportemental                         | Oubli, inattention, interface mal conçue             | 3          | 7           | 4        | 84                |
| 4-Scan RFID / QR code              | Produit non reconnu ou mal scanné     | Rupture de la traçabilité d’un lot alimentaire       | Étiquette abîmée, éclairage insuffisant              | 3          | 6           | 7        | 126                |
| 1-Capteur IoT               | Données incohérentes                  | Sous-estimation du risque microbien                  | Capteur mal calibré, condensation                    | 6          | 6           | 9        | 324                 |


### 4.3 Gestion des défaillances

*La __Matrice de criticité__*
<img src=img/matrice_de_criticité.png>

### 1-Capteur inactif (Gravité : Catastrophique, Probabilité : rare)

**Empêcher :**  
Déployer des capteurs redondants dans les zones critiques (ex. : chambres froides), avec un plan de vérification hebdomadaire (test de signal, batterie). Installer des capteurs validés IP65 avec autonomie longue durée et indicateur d'état.

**Alerter :**  
Configurer une alerte automatique dès qu’un capteur n’émet plus de données pendant une durée donnée (ex. 30 minutes). Surveiller les écarts de transmission via un watchdog intégré à l’application.

**Réagir :**  
Envoyer immédiatement une notification au responsable HACCP. Activer un mode manuel de saisie temporaire. Remplacer le capteur dès que possible et historiser l’incident dans le tableau de bord.

---

### 1-Capteur de présence non déclenché (Gravité : Critique, Probabilité : Rare)

**Empêcher :**  
Optimiser l’emplacement des capteurs avec un guide d’installation (zone de détection, hauteur, orientation). Prévoir une validation manuelle complémentaire à chaque tâche planifiée (ex. : bouton “nettoyage effectué”).

**Alerter :**  
Générer une alerte si aucune activité n’est détectée pendant une plage horaire où une action est prévue (nettoyage, désinfection). Journaliser l’absence de détection.

**Réagir :**  
Envoyer une notification au responsable avec la possibilité de valider manuellement l’action. Documenter l'écart de conformité. Planifier une intervention de vérification capteur si récurrence.

---

### 3-Données non transmises ou corrompues (Gravité : Catastrophique, Probabilité : Rare)

**Empêcher :**  
Prévoir une architecture de stockage local robuste avec buffer sécurisé et file d’attente résiliente. Tester les scénarios de déconnexion pour valider la reprise.

**Alerter :**  
Afficher un indicateur d’état de synchronisation dans l’application. Déclencher une alerte si une donnée n’a pas été synchronisée après un délai maximum (ex. 2h).

**Réagir :**  
En cas de perte réseau, activer un mode hors-ligne prolongé. Lors du retour de connexion, déclencher la synchronisation automatique. En cas d’échec persistant, activer un export manuel local chiffré.

---

### 2-Saturation mémoire, perte hors ligne  (Gravité : Catastrophique, Probabilité : Rare)

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

Certaines tâches sont parallélisables, tandis que d’autres suivent des **dépendances logiques** (par exemple: les tests ne peuvent être effectués qu’après le développement des modules).

Ce diagramme constitue un outil essentiel pour le **pilotage du projet**, en assurant une vision globale de son avancement, et en facilitant la coordination entre les membres de l’équipe.

<img src=img/diagramme_gantt.png>



#### Répartition du travail

### Alex
| Tâche                                  | Section             | Durée estimée |     |
| -------------------------------------- | ------------------- | ------------- | --- |
| Etude des applications existantes      | 1.2.3 / 1.2.5 (LLM) | 2h            |     |
| Synthèse comparative outils HACCP      | 1.2.3 / 2.1.2 (LLM) | 1h            |     |
| Rédaction fonctions complémentaires    | 2.1.2.1             | 1h30          |     |
| Diagramme de cas d'utilisation         | 2.1                 | 2h            |     |
| Proposition de l'UX du tableau de bord | 3.2 / 3.3.5         | 1h            |     |
| Diagramme de Gantt                     | 5 Annexe            | 1h30          |     |


### Kéwan

| Tâche                                                                                       | Section        | Durée estimée |     |
| ------------------------------------------------------------------------------------------- | -------------- | ------------- | --- |
| Rédaction des finalités                                                                     | 1.1.1          | 1h            |     |
| "espérance de retour sur investissement" (ROI) et modèle économique                         | 1.1.2          | 1h            |     |
| Situation du projet par rapport aux autres projets de l’entreprise                          | 1.2.1          | 15min         |     |
| Suites prévues                                                                              | 1.2.4          | 2h            |     |
| Analyse des autres applications (même sujet et sujets voisins) avec LLMs                    | 1.2.2 et 1.2.3 | 30min         |     |
| Parties concernées par le déroulement du projet et ses résultats (demandeurs, utilisateurs) | 1.2.6          | 1h            |     |
| Caractère confidentiel s'il y a lieu                                                        | 1.2.7          | 30min         |     |
| Énoncé du besoin                                                                            | 1.3            | 30min         |     |



### Pacôme

| Tâche                                            | Section                   | Durée estimée |
| ------------------------------------------------ | ------------------------- | ------------- |
| Etude des capteurs possibles                     | 1.4 / 3.1.1 / 3.3.1 (LLM) | 1h30          |
| Rédaction collecte des données environnementales | 2.1.1.1 / 3.1.1 (LLM)     | 1h50          |
| Rédaction scénarios de fonctionnement(WBS)       | 3.1.1                     | 1h            |
| Analyse des risques techniques                   | 4.1 / 4.2                 | 1h            |
| Table de défaillance (technique)                 | 4.2                       | 1h            |
| Matrice de criticité (technique)                 | 4.3                       | 50min         |
| Solutions techniques (maintenance,modules) (LLM) | 3.3.4 / 3.3.5             | 1h            |