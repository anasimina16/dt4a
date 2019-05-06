# \#1 - L'Open Data

## Définition

### **Qu’est ce qu’une donnée ouverte / open data ?** 

C’est une donnée à laquelle tout le monde peut accéder et que tout le monde peut utiliser et partager, en respectant une licence. 

### **Et dans le domaine des transports ?**

Les transports sont un secteur où l’ouverture des données est particulièrement importante, majoritairement parce qu’elle permet la création de nouveaux services, utiles pour les usagers dans leur quotidien, mais aussi le suivi et l’optimisation des services existants.  ****

### **Quelles sont ces “données transports” ?** 

Deux grandes types de données sont en général ouverts dans le domaine des transports :

* celles concernant la **consistance** de services, à savoir : horaires, géolocalisation des points d’arrêts, fréquences, services disponibles dans chaque point d’arrêt... Ces données servent bien souvent à alimenter des services d’information voyageurs, sur smartphone, dans les gares, stations de métro, arrêts de bus… Elles peuvent être théoriques ou bien dynamiques \(et vous informer en temps réel, grâce à des dispositifs présents dans chaque véhicule du réseau de transport\). A un niveau moins pointu, mais bien souvent déjà utile, ces données peuvent aussi simplement permettre de localiser certains services \(des parkings relais par exemple\) ou encore décrire des tarifs,
* celles concernant le suivi de **l'usage** des services : ces données, générées à partir de l’utilisation des services de  chaque réseau de transports, permettent de suivre la performance de chaque réseau : régularité, ponctualité, nombre de validations, fréquentation de telle ou telle ligne, tel ou tel point d'arrêt. 

Les premières ont vocation à générer des services pour les usagers. Les secondes ont plutôt vocation à renseigner les autorités de transports et ou les exploitants, pour suivre, améliorer et rendre plus performant le service.

## Enjeux 

### **Pourquoi ouvrir une donnée ?** 

Les gouvernements, les entreprises et les individus peuvent ouvrir leurs données pour créer des avantages sociaux, économiques et environnementaux :

* aider à la prise de décisions,
* bénéficier de services utiles au quotidien : pour se déplacer, éviter le gaspillage alimentaire, connaître les services publics à proximité de son domicile,
* encourager la transparence démocratique des institutions et des élus,

### **Qui ouvre les “données transports” ?** 

En fonction des pays, des législations, des contrats, ce sont soit les autorités organisatrices ou les exploitants qui ouvrent les données de transports. C’est un sujet particulièrement important, car le data management dépend énormément de l’entité qui assure cette mission.

### **Qui va utiliser ces données transports ?** 

Des citoyens, des acheteurs, développeurs, intégrateurs, producteurs ou simplement réutilisateurs.

### **Ou trouve-t-on les données transports ouvertes ?** 

Lorsqu’une autorité organisatrice de transports ou un exploitant ouvre ses données, il les expose en général sur un portail dédié. En fonction des portails, plusieurs fonctions peuvent être mises à disposition, afin de comparer, analyser, filtrer, observer, cartographier les différentes données. Les données ouvertes peuvent alors être téléchargées directement \(plusieurs formats sont disponibles\) ou accessibles via des web-services / API, pour connecter son application directement via du code spécifique \(réservé aux développeurs\).

### **Existe-t-il différents formats de données transports ?** 

En fonction du type de données, plusieurs formats existent. Les données horaires sont majoritairement disponibles au format GTFS \(General Transit Feed Specification, format initialement développé par Google\), plus rarement au format Neptune. Mais des données sont encore disponibles aux formats CSV, XML, JSON ou parfois Excel.

### **A partir de quand considère-t-on qu’une donnée est ouverte ?** 

Pour que les données soient ouvertes, il ne doit y avoir aucune restriction quant à leur utilisation, quelle qu’elle soit. N’importe quel utilisateur devrait être libre d’utiliser, de modifier, de combiner et de partager les données, pour certaines même à des fins commerciales. Attention, dans le domaine des transports, un accent tout particulier doit être mis sur la qualité des dites données. En effet, si une donnée est ouverte, mais que sa qualité est médiocre, elle peut ensuite générer une mauvaise information et perturber l’utilisation du service par les usagers.

### **Existe-t-il différents niveaux d’ouverture ?** 

Pas directement. Il existe plutôt différents types de licences qui définissent certains critères, en fonction de l’utilisation de ladite donnée. Un processus d’ouverture des données est complexe. Il doit respecter un certain nombre d’étapes afin de permettre aux citoyens d’accéder à des données de qualité, simples à appréhender et faciles à manipuler. C’est à ces conditions que la donnée aura une valeur ajoutée pour la société.

## **Parole d’acteur**

_Tristram Gräbener est  développeur pour le Gouvernement français, au sein des équipes de beta.gouv. ****Docteur en informatique, Tristram s’est spécialisé dans les questions de calculs d’itinéraires. Un savoir faire qu’il a ensuite rendu opérationnel durant plusieurs années chez Canal TP \(devenu Kisio Digital\) puis Captain Train \(devenu Trainline\)._ 

> **Comment définirais tu l'open data ?**
>
> L’open data, c’est la mise à disposition des __données, lisibles par une machine, sans contraintes ni préjugés concernant l’utilisation de ces dernières. Il ne faut pas avoir peur de dire “ouvrons à tout va !”. 
>
> **Pourquoi le domaine des transports est il particulièrement concerné ?**

> Les transports sont \(en Europe en tous cas\) financés par des budgets publics, et destinés au public. Il est donc normal, logique, que les données qu’ils génèrent soient aussi rendues publiques. Le mouvement d’Open Data actuel rattrape en quelque sorte une aberration. Par ailleurs, ces données sont peu sensibles, il est donc plus facile de les ouvrir. 
>
> **Que permet l'open data dans ce domaine ?**

> L’ouverture permet de croiser ces données avec d’autres domaines, ou encore de pouvoir analyser finement le domaine des transports. Durant ma thèse à Toulouse par exemple, j’ai été obligé d’utiliser les données de Rennes et Los Angeles car celles de Toulouse n’étaient pas ouvertes à l’époque. Cela illustre parfaitement mon propos. L’ouverture permet aussi très clairement à des tiers de développer des services utiles pour la population. Un exemple que j’aime citer est celui de TransportR au Brésil... Les autres gains sont connus, mais il est bon de les rappeler : cela permet de rendre les offres de transports plus visibles ; cela donne la possibilité à “la communauté” de faire remonter des erreurs et de les corriger. Les bénéfices pour le public sont vraiment très nombreux. 
>
> **Quels conseils pourrais tu donner à une entité qui souhaite se lancer ?**
>
> Franchir les étapes une par une, et ne pas hésiter à commencer par des choses très basiques, à savoir ouvrir l’existant, avant d’entamer un travail d’amélioration continue. Un des __éléments essentiel est aussi d’itérer avec la communauté. Enfin, et c’est un élément compliqué à faire comprendre et à expliquer : il faut dégager un temps dédié pour l’animation autour de l’open data, c’est primordial.

## Cas d'usage

### **Londres \(UK\) : l’open data créatrice d’innovation et de valeur économique**

![](https://lh3.googleusercontent.com/S76TH1kFlS-uyM8SS2-VUXa0ymL0lfQdcoPeL9GRwIDrIk7jhiN7cri8Ma85dd9Z8HOBswvghu8u98WH5N94fUUBnhL1wvWd-mMjA6WQERwhkAAs1c_6XBvpWtbLHahmOfbC3chJ)

Transport For London \(TfL\) est l’autorité de transports qui assure la gestion au quotidien de quelques 9200 bus, 900 trains, 650 km de voies ferrées, 580 km d’autoroutes, ou encore 6300 feux tricolores de la capitale britannique… Sans parler de l’ensemble des autres modes de transports. Des données, l’autorité de transports en génère et en récupère chaque jour. Lorsqu’elle a débuté son processus d’Open Data il y a plus de 10 ans, elle avait quatre objectifs : “permettre la transparence, répondre à la cible, créer des produits de niche et produire un avantage économique”. ****En 2018, l’autorité de transports fêtait les 10 ans de son programme d’ouverture, l’occasion de faire un bilan positif de l’expérience : "la publication de données ouvertes par TfL génère des bénéfices et des économies pouvant atteindre 130 millions de livres par an". Comment en est-on arrivé là ? selon les chefs de projet, ce niveau d’impact a été atteint davantage par un changement de culture que par la technologie elle-même. Pour y arriver, il a fallu assurer un portage au niveau conseil d’administration, insister sur l’importance du service pour le client \(plutôt qu’un projet technologique\) et engager TfL dans cette direction avec les équipes les plus compétentes et séduites par le projet. Voilà comment TfL a ouvert, via une API, plus de 200 jeux de données dont les horaires de bus, de métro, la disponibilité des vélos en libre service, les horaires des bateaux, des différents trains, l’accessibilité. L’autorité de transports a également mis à disposition un calcul d’itinéraires via son API. Surtout, TfL a travaillé avec un large éventail de développeurs professionnels et amateurs, allant des start-ups aux innovateurs mondiaux \(Twitter, Amazon, Apple et Google\), pour livrer de nouveaux produits adaptés à la demande des clients. Résultat : plus de 700 applications \(utilisées par 42% des Londoniens\) sont alimentées en utilisant spécifiquement les flux de données ouverts de TfL, 14 000 développeurs les utilisent désormais.

### **Rennes \(FR\), les transports à l’origine d’un projet Open Data métropolitain**

![](.gitbook/assets/geovelo-velib-velgo-1-1.jpg)

A Rennes, le mouvement Open Data a débuté en 2010, avec la mise en place d'un libre accès aux fichiers issus du réseau de transports \(Keolis Rennes\) et de la vie associative. A l’époque, un concours baptisé "Rennes Métropole en accès libre" récompensait les meilleures innovations, de quoi encourager les développeurs à se triturer les méninges pour inventer des applications véritablement innovantes. Rennes était à l’époque la première collectivité en France à ouvrir ses données transports. En 2012, elle ouvrait des jeux de données de transport en temps réel.

Depuis, la métropole a vu se créer de nombreuses applications utilisant ses données transports, et ce notamment grâce à un démarche \(inédite en France\) de labellisation des applications issues du travail de la communauté de développeurs Open Data autour de la donnée transport des réseaux STAR et LE vélo STAR de Rennes Métropole. Cette démarche de création d’un label a été  motivée par plusieurs enjeux :

* garantir à l'utilisateur final la qualité, l'exactitude et l’homogénéité de l'information diffusée par différents canaux ;
* promouvoir les applications, les faire connaître auprès du grand public ;
* proposer aux développeurs de bénéficier d'un cadre de travail privilégié avec l’opérateur de transport Keolis Rennes et de promouvoir ses travaux auprès des utilisateurs des services du réseau STAR.

Cette année, lauréate du Programme d’investissements d’avenir lancé par l’État français, la métropole bretonne a créé un “service public de la donnée” et se donne deux ans pour valoriser ses données, notamment de transports. Elle s’est également engagé dans un programme d'accompagnement à l'open data pour les collectivités de plus de 3500 habitants qui ont, depuis la loi " Pour une République numérique", l'obligation légale de publier leurs données publiques. Pour conduire ce programme, l'Etat soutient financièrement l'association Open Data France qui oeuvre avec 9 territoires pilotes, répartis sur toute la France, pour mutualiser les "bonnes pratiques" destinées à faciliter l'open data. Rennes est ainsi associée à la Région Bretagne, le département des Côtes d'Armor, Saint-Malo Agglomération, le syndicat Morbihan Energie et Megalis Bretagne.

## **DigitalTransport4Africa**

**Dans le cadre du projet Digital Transport For Africa, un des objectifs est de recenser et de mettre à disposition tous les jeux de données créés dans le cadre de projets de transports en Afrique. Pourquoi ?**

* Insuffler l’ouverture dès à présent permet de mieux construire les jeux de données. Cela pousse à respecter un certain nombre de normes et/ou de standards et à mettre à jour ses données,
* parce que d’autres projets pourront s’inspirer des données déjà ouvertes, voire même les utiliser,
* aussi car demain, lorsque des modes lourds seront déployés, cela permettra de créer des dispositifs d’information multimodaux,
* une telle démarche permet également d'assurer les conditions de l’indépendance de la donnée \(pas de dispositif propriétaire\),
* c’est donc un gain pour le collectif, à l’échelle de l’Afrique toute entière, et pourquoi pas demain d’autres continents.

Dans le cadre de Digital Transport For Africa, [plusieurs jeux de données](https://git.digitaltransport4africa.org/explore/groups) ont déjà été ouverts sur le Gitlab de la communauté, à savoir : Nairobi, Accra, Le Caire.  

  
![](https://lh5.googleusercontent.com/DQrxrimL2u8Zk_DHCHyFVm6b4vdk8EBDgjDMhcAEBMPqwUrVIy3OeWSqIlSqP5bwT1NoY9n-xZwPDJeHDvt4ynJRP8sDsaO_ANBroW4a9e_pynXQZuBfWhtF6xGvRKvpH8VnNmDG)![](https://lh4.googleusercontent.com/HTnuBo1TnaG_3D6uKa19c2gj-n2kpM7_srCy20lERES_dK0r82jPZYoxnkiRDwI2ynu48CGfo4fSdKO8cuj5Gce2WR53g0k-3mKpXZLlNN6S5TwvZ4k5JtkUiQrsk67ElM0Q0PJJ)![](https://lh4.googleusercontent.com/HTnuBo1TnaG_3D6uKa19c2gj-n2kpM7_srCy20lERES_dK0r82jPZYoxnkiRDwI2ynu48CGfo4fSdKO8cuj5Gce2WR53g0k-3mKpXZLlNN6S5TwvZ4k5JtkUiQrsk67ElM0Q0PJJ)  
  
  


