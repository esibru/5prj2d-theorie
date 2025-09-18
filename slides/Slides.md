---
title       : Gestion de projet II
author      : Jonathan Lechien
description : Supports de l'unité 5PRJ2D.
keywords    : Marp, Slides, Informatique, Projet, Java.
marp        : true
paginate    : true
theme       : godel
mermaid     : true
footer      : "JLC - 5PRJ2D"

--- 

<!-- _class: titlepage -->

# 5PRJ2D - Théorie
## Gestion de projet II
### Jonathan Lechien - JLC
#### Bruxelles, septembre 2025
##### Haute École Bruxelles-Brabant : Département des Sciences Informatiques 
##### Basé sur un cours de Frédéric Pluquet
---        
     
# Objectifs pédagogiques

**Planifier** le développement d'un projet en **équipe**.

**Concevoir**, **développer** et **tester** une application complète en **équipe**.

**Utiliser** un logiciel de gestion de version en **équipe**.

**Évaluer** la qualité d’un code.


> Une équipe est composée d’environ 10 personnes.

---        
     
# Matières

<div class="columns">
<div>
      
<!-- _class: cool-list -->

### Théorie

1. *Méthodologies de projet*
1. *XP : l'eXtrême Programming*
1. *Scrum*
   
</div>  
<div>    

### Laboratoires

1. *Worflow git*
1. *Pratique de XP* 
1. *Projet en équipe* 
 
</div>    
</div> 

---

# Organisation de l'unité

<div class="columns">
<div>
      
<!-- _class: cool-list -->

### BIM1

- 2H par semaine de théorie
- 2H par semaine de laboratoires
   
</div>  
<div>    

### BIM2

- pas de cours théorique
- 6H par semaine de laboratoires
 
</div>    
</div> 

---

# Évaluation

<div class="columns">
<div>
      
<!-- _class: cool-list -->

### Théorie

- 20% de la note de l'unité

- QCM durant le Sprint 1 **en laboratoire**

- Exemples de questions durant les séances
   
</div>  
<div>    

### Laboratoires

- 80% de la note de l'unité

- **Présence obligatoire**

- Note pondérée par le taux de présence

- **Défense** de projet en fin de semestre

- **Pas de projet en seconde session** 

</div>    
</div> 

---  
<!-- _class: transition2 -->  
Partie 1 : Les méthodologies de projet

--- 

# Les grandes étapes d’un projet
<!-- _class: cool-list -->
1. *Appréhender le problème*
1. *Analyser le problème*
1. *Réaliser la solution*
1. *Tester*
1. *Déployer (mise en production)*
1. *Maintenir le logiciel dans le temps*

<!-- notes
Tout projet logiciel, qu’il soit mené en cascade ou en agile, suit globalement les mêmes grandes étapes. On commence par comprendre et analyser le problème, ensuite on conçoit une solution, on la réalise, on la teste, puis on la met en production. Enfin, un logiciel doit toujours être maintenu dans le temps, car les besoins évoluent, les bugs apparaissent, les technologies changent. La différence entre méthodologies, ce n’est pas vraiment quelles étapes on suit, mais plutôt comment on les organise, à quel moment on prend les décisions, et à quel rythme on livre de la valeur.
-->

--- 
# Clarifier les attentes : la collecte des besoins

Comprendre **ce que l’utilisateur attend** du système

Types de besoins/requirements :
  - Fonctionnels : **ce que le logiciel doit faire**
  - Non-fonctionnels : **performance, sécurité, ergonomie...**
  - Métier/domaine : **contraintes propres au contexte**

Rédaction du **Software Requirements Document** (SRD)

<!-- notes

La collecte des besoins, c’est une étape clé. Il s’agit de bien comprendre ce que l’utilisateur attend réellement du système. On distingue trois types de besoins : les besoins fonctionnels, qui décrivent ce que le logiciel doit faire concrètement ; les besoins non-fonctionnels, qui concernent la performance, la sécurité, l’ergonomie ; et enfin les besoins métier, qui traduisent les contraintes spécifiques au domaine. Dans une approche classique, on consigne tout cela dans un gros document, le Software Requirements Document. En agile, l’approche est plus légère et évolutive : on parle de user stories qui capturent l’essentiel des besoins tout en restant flexibles.

-->

---

# Qualité logicielle : une histoire de point de vue

La qualité n’a pas la même signification pour :

- le **Client** : respect du budget et des délais
- l'**Utilisateur** : facilité d’usage, fiabilité
- le **Développeur** : code maintenable, tests, performance
- le **Manager** : alignement avec les objectifs stratégiques

<!-- notes

La notion de qualité n’est pas la même pour tout le monde. Pour le client, c’est surtout de livrer dans les temps et sans exploser le budget. Pour l’utilisateur, c’est que le logiciel soit simple, fiable et agréable. Pour le développeur, la qualité se mesure dans un code maintenable, testé et performant. Enfin, pour le manager, c’est que le logiciel soit aligné avec la stratégie de l’entreprise. Comprendre ces différents points de vue est essentiel, car un projet échoue souvent non pas faute de compétences techniques, mais parce qu’on n’a pas bien aligné les attentes autour de ce mot : qualité.

-->

--- 
 
# Qualité logicielle

**Norme ISO 9000:2005** : Ensemble des caractéristiques d’une entité qui lui confèrent l’aptitude à satisfaire des besoins exprimés ou implicites.
   
Exemples de critères de qualité :

- Pertinence : le logiciel répond-il aux objectifs visés ?
- Apport de bénéfices : génère-t-il de la valeur pour l’utilisateur ?
- Fonctionnement correct : respecte-t-il les spécifications ?
- Performance : rapidité, consommation de ressources, fiabilité
- Facilité d’apprentissage : ergonomie et intuitivité
- Évolutivité : possibilité d’ajouter de nouvelles fonctionnalités
- Réutilisabilité : modularité et capacité à être utilisé dans d’autres contextes
- Portabilité : capacité à fonctionner sur différentes plateformes

<!-- notes

Si on regarde une définition plus “officielle”, la norme ISO nous dit que la qualité logicielle, c’est la capacité d’un logiciel à satisfaire des besoins exprimés ou implicites. Cela recouvre des critères très variés : la pertinence, les bénéfices concrets, le bon fonctionnement, les performances ; mais aussi des aspects plus humains comme la facilité d’apprentissage, la réutilisabilité, l’évolutivité ou la portabilité. Cette vision nous rappelle que la qualité ne se réduit pas à l’absence de bug : elle englobe tout ce qui rend un logiciel utile et durable dans son contexte.

-->

--- 

# Tour d’horizon des méthodologies

**Méthodologie : Procédé qui a pour objectif de permettre de formaliser les étapes préliminaires du développement d'un système afin de rendre ce développement plus fidèle aux besoins du client.**

<div class="columns">
<div>

RACINES
SCRUM
XP
Merise
3AR
MMTS
MASE
CISAD
MKSH

</div>  
<div>    
 
SART
MACAO
FAST
Unified Process
OOD
EVO
RAD
DSDM
Kanban

</div>    
</div> 

<!-- notes

Pour mettre en œuvre ces étapes et assurer la qualité, il existe de nombreuses méthodologies. Certaines sont orientées analyse, comme Merise ; d’autres mettent l’accent sur la rapidité, comme RAD ; d’autres encore sur la discipline, comme le Unified Process. Du côté agile, on trouve Scrum, Kanban, XP. Chaque méthode propose un cadre de travail différent, mais toutes visent le même objectif : mieux organiser la collaboration et transformer des besoins en un logiciel qui fonctionne.

RACINES : Méthode d’analyse et de conception basée sur les besoins fondamentaux du système.

SCRUM : Méthodologie agile centrée sur des itérations courtes et des équipes auto-organisées.

XP (eXtreme Programming) : Approche agile poussant les bonnes pratiques de développement à l’extrême pour la qualité du code.

Merise : Méthode structurée française pour l’analyse, la conception et la modélisation des systèmes d’information.

3AR : Méthode d’ingénierie des systèmes orientée architecture, analyse et rationalisation des besoins.

MMTS : Méthode de modélisation des systèmes techniques et logiciels pour la planification du développement.

MASE : Méthode d’analyse et de structuration des exigences pour les systèmes industriels et logiciels.

CISAD : Approche de conception des systèmes d’information centrée sur les besoins de l’utilisateur.

MKSH : Méthode de conception logicielle basée sur les modèles, pour gérer la complexité.

SART : Méthode structurée pour l’analyse et la résolution des tâches dans les projets logiciels.

MACAO : Méthode d’analyse et de conception orientée objets pour les systèmes d’information.

FAST : Développement rapide d’applications (Rapid Application Development), centrée sur prototypage et itérations.

Unified Process : Méthode itérative et incrémentale basée sur les cas d’utilisation et les meilleures pratiques.

OOD (Object-Oriented Design) : Conception orientée objet pour modéliser et développer des systèmes logiciels.

EVO (Evolutionary Project Management) : Gestion de projet itérative basée sur livraisons progressives et ajustements continus.

RAD (Rapid Application Development) : Développement rapide centré sur prototypage et retour utilisateur rapide.

DSDM (Dynamic Systems Development Method) : Méthode agile centrée sur le développement rapide et itératif avec gestion des priorités.

Kanban : Méthode visuelle de gestion de flux de travail pour améliorer l’efficacité et limiter le travail en cours.

-->

--- 

# Waterfall : comment tout est séquencé

![](./img/Modèle_en_cascade_générique_avec_livrables.png)

<!-- notes

Le modèle en cascade, ou Waterfall, est l’approche historique. Ici, les étapes sont bien ordonnées et séquentielles : on commence par tout définir, puis on conçoit, ensuite seulement on code, on teste et on livre. L’image de la cascade illustre bien cette logique descendante, où l’on ne revient pas en arrière. Cette méthode est très structurée, elle a l’avantage de donner une grande visibilité et un plan clair, mais elle suppose que l’on connaisse très précisément les besoins dès le départ… ce qui n’est pas toujours réaliste.

-->

--- 

# Waterfall : quand la définition bloque le projet

<!-- _class: cool-list -->

1. *Définition du cahier des charges*
1. *puis, document de spécifications*
1. *puis, document de conception générale*
1. *puis, document de conception détaillée*
1. *puis, plans de tests*
1. *et finalement... on code l’application !*

<!-- notes

Les limites de la cascade viennent du fait qu’on doit tout définir à l’avance. On commence par un cahier des charges très complet, suivi de spécifications, de conceptions générales et détaillées, puis des plans de test. Ce n’est qu’une fois tout cela terminé qu’on commence à coder. Le problème, c’est que dans le monde réel, les besoins changent, les utilisateurs découvrent ce qu’ils veulent en cours de route. Et plus on est loin dans le projet, plus il est coûteux de revenir en arrière. C’est ce qui a motivé la recherche de méthodes plus souples.

-->

--- 

# Succès et échecs de projets selon le Chaos Report

<center>

![](./img/agile-vs.-waterfall-success-rate.png)

<figcaption align="center">
<b>Figure</b>: Source: Ambysoft, 2013 IT Project Success Rates Survey Results, 2013.
</figcaption>
</center>

<!-- notes

Le Chaos Report, une étude bien connue, a montré que les projets menés en cascade réussissaient beaucoup moins souvent que ceux menés en agile. Dans certains chiffres, moins de 15 % des projets en cascade aboutissaient sans problème, alors qu’en agile on atteignait plus de 40 %. Ce n’est pas que l’agile soit une recette miracle, mais simplement que cette approche gère mieux l’incertitude et l’évolution des besoins. Ce constat a poussé de nombreuses entreprises à revoir leur manière de gérer les projets informatiques.

-->

--- 

# Waterfall : dans quels cas ça marche ?

**Attention** la méthode en cascade possède ses avantages : 

- Découpe en phases permettant une parallélisation
- Utile si besoin de tout spécifier avant de construire
- Par exemple: si la construction est onéreuse, si la qualité de chaque étape doit être évaluée finement, …

<!-- notes

Attention toutefois : la méthode en cascade a encore ses avantages. Elle est utile lorsqu’on doit absolument tout spécifier avant de construire, par exemple dans des projets industriels lourds, dans l’aéronautique, dans les infrastructures. La découpe en phases permet aussi une bonne répartition des responsabilités et un suivi rigoureux. En clair, la cascade n’est pas “mauvaise” : elle est adaptée à des contextes où les besoins sont stables et où le coût d’un changement est prohibitif.

-->

--- 

# Une première évolution : le cycle en V

<center>

![](./img/Cycle_de_developpement_en_v.svg)

</center>

<!-- notes

Après avoir vu le modèle Waterfall, qui est linéaire et séquentiel, le cycle en V est apparu comme une évolution naturelle pour mieux gérer la qualité.

Le cycle en V reprend les mêmes phases que Waterfall – analyse, conception, développement, tests – mais met l’accent sur la correspondance entre chaque étape de conception et une étape de test.

Si vous regardez le schéma, vous voyez que les phases descendent d’un côté, puis remontent en forme de V. Chaque phase de spécification a sa phase de test correspondante :

Les spécifications fonctionnelles sont vérifiées par des tests d’acceptation.

La conception détaillée est vérifiée par des tests unitaires.

La conception générale est vérifiée par des tests d’intégration.

L’intérêt principal est donc de relier directement chaque étape à son contrôle de qualité, ce qui réduit les erreurs qui passent entre les mailles et rend le processus plus sûr, surtout pour des projets critiques.

Cependant, le cycle en V reste assez rigide, comme Waterfall : il faut bien définir les besoins avant de commencer, et il n’est pas très flexible face aux changements en cours de projet.

-->

--- 

# Nouvelle évolution : le cycle en spirale

<center>

![](./img/Spirale_(Boehm,_1988).svg)

</center>

<!-- notes

Le cycle en spirale, proposé par Barry Boehm en 1988, est une réponse aux limites des approches linéaires et rigides comme Waterfall et le cycle en V.

Au lieu de suivre un chemin strictement descendant, la spirale combine itérations et analyse des risques. Chaque tour de spirale correspond à une phase complète du projet, incluant :

L’analyse des objectifs et des alternatives,

L’évaluation des risques,

Le développement et les tests,

La planification du prochain cycle.

L’avantage est que l’on commence rapidement avec un prototype, puis on répète les étapes en affinant le produit et en réduisant les risques à chaque itération. Cela permet de s’adapter aux changements, d’intégrer le feedback des utilisateurs, et de mieux maîtriser les incertitudes.

En résumé, si Waterfall est linéaire et le cycle en V met l’accent sur les tests, la spirale introduit l’itération, l’évaluation des risques et la flexibilité, des idées qui préfigurent ce que l’on retrouve aujourd’hui dans les méthodes agiles.

-->

--- 

# Agile : une alternative au Waterfall

**Les individus et leurs interactions** plus que les processus et les outils.

**Un logiciel qui fonctionne** plus qu’une documentation exhaustive.

**La collaboration avec les clients** plus que la négociation contractuelle.

**L’adaptation au changement** plus que le suivi d’un plan.

> [Manifeste agile](https://manifesteagile.fr/)

<!-- notes

L’agile, c’est un changement de philosophie. Le manifeste agile de 2001 met en avant quatre valeurs : les individus et leurs interactions plutôt que les processus, un logiciel qui fonctionne plutôt que la documentation, la collaboration avec le client plutôt que la négociation, et l’adaptation au changement plutôt que le suivi rigide d’un plan. Ce n’est pas une recette unique, mais un ensemble de principes pour travailler de manière plus souple, plus réactive et plus centrée sur l’utilisateur.

-->

--- 

# Comment l’agile a évolué

**EVO** (Evolutionary Project Management) (1976)

**RAD** (Développement rapide d'applications) (1991)

**DSDM** (Dynamic System Development Method, la version anglaise du RAD) (1994)

**Kanban** (issue de la méthode industrielle Lean, Toyota)

**XP** (par Kent Beck) (1999)

**Scrum** (par Ken Schwaber et Jeff Sutherland) (2001)

<!-- notes

L’agilité n’est pas née d’un coup. Dès les années 70, des approches comme EVO cherchaient déjà à rendre les projets plus évolutifs. Les années 90 ont vu apparaître RAD, DSDM, puis Kanban dans l’industrie. À la fin des années 90, Kent Beck a popularisé XP, et en 2001 Scrum a été formalisé par Schwaber et Sutherland. On voit donc une maturation progressive, qui a culminé avec le manifeste agile. Aujourd’hui, ces méthodes sont devenues des standards dans le développement logiciel.

-->

--- 

# Agile : changer de perspective

<center>

![](./img/boats-agile-vs-waterfall.png)

</center>

<!-- notes

Passer de la cascade à l’agile, c’est changer de manière de voir le projet. Dans la cascade, on est dans une logique linéaire, planifiée, où l’on avance étape par étape comme un grand navire qui suit sa route. En agile, on est plus proche d’un voilier : on garde un cap, mais on ajuste en permanence la voile selon le vent et les conditions. Ce changement de référentiel, c’est accepter que l’incertitude fait partie du projet, et que l’adaptation est une force plutôt qu’un défaut.

-->

--- 

# Une méthode agile : eXtreme Programming (XP)

XP favorise l’agilité à plusieurs niveaux :
- **Code** : qualité, tests automatisés, refactoring
- **Équipe** : collaboration, communication, pair programming
- **Gestion de projet** : itérations courtes, livraisons fréquentes, adaptation au changement
- **Valeurs** : approche humaine, confiance, simplicité et vision positive du développement

<!-- notes

Parmi les méthodes agiles, XP est l’une des plus connues pour sa focalisation sur le code. XP cherche l’agilité à trois niveaux : le code lui-même, avec des pratiques comme le refactoring et les tests automatisés ; l’équipe de développement, avec du pair programming ou un rythme de travail durable ; et la gestion de projet, avec des itérations courtes et un dialogue permanent avec le client. XP a aussi une dimension humaniste : valoriser la communication, la confiance et le respect entre développeurs.

-->

---

# Rôles, pratiques, artifacts et valeurs

**Rôles** : Client, Testeur, Développeurs, Coach

**Artifact** : Logiciel, Histoires, Scénarios de tests

**Pratiques** : Livraisons fréquentes, Planification itérative, Client sur site,Rythme durable, Pair Programming, Responsabilité collective du code

**Valeurs** : Communication, Simplicité, Feedback, Courage

<!-- notes

Dans XP, on définit plusieurs rôles : le client, qui exprime les besoins ; les développeurs ; les testeurs ; et un coach qui aide l’équipe à rester fidèle aux principes. Les artefacts sont les logiciels livrés régulièrement, les histoires utilisateurs, et les scénarios de tests. Les pratiques incluent la livraison fréquente, la planification itérative, la présence du client sur site, le pair programming, la responsabilité collective du code. Et tout cela repose sur des valeurs : communication, simplicité, feedback, courage.

-->

--- 
 
<!-- _class: cite -->        

**XP pousse à l’extrême certaines bonnes pratiques** pour maximiser la qualité et l’adaptabilité : tests automatisés, refactoring fréquent, collaboration constante avec le client, livraisons rapides.

<!-- notes


-->

--- 

# Les limites de l’agilité

**Dérives commerciales** : certaines entreprises exploitent l’agile comme un argument marketing plutôt qu’une véritable pratique

**Imposition aux équipes** : appliquer l’agile sans appropriation par les développeurs peut créer des frustrations

**Faux-agile** : suivre les rituels sans respecter les principes fondamentaux (rituels vides, “cargo-cult agile”)

<!-- notes

Enfin, il ne faut pas croire que l’agile est parfait. Comme toute approche, il a ses limites. Certaines entreprises détournent l’agile pour en faire un produit commercial, sans respecter l’esprit. Parfois, on impose l’agile aux équipes sans leur donner le temps de s’approprier les pratiques. On parle alors de “faux-agile” ou “cargo-cult agile”, où l’on suit des rituels sans en comprendre le sens. La clé, c’est de garder un regard critique et de s’assurer que l’agile reste au service du projet et de l’équipe, et non l’inverse.

-->

---

# Mise en situation 💬
 
Un membre de l'équipe annonce qu'il a commencé une tâche il y a deux jours  
mais qu'elle n'est toujours pas terminée. Il ajoute qu'il **devrait la finir demain**, mais ne s'engage pas fermement.

**Que feriez-vous dans cette situation ?**  

- A. Attendre que la tâche soit finie sans intervenir  
- B. Relancer le membre de l'équipe pour comprendre le problème  
- C. Proposer de l'aider ou de réévaluer la charge de travail  
- D. Escalader directement au manager  

<!-- notes


-->

---
<!-- _class: transition2 -->  

Partie 2 : Gestion de projet XP

--- 
  
<center>

![](./img/work-in-progress.jpeg)

</center>

---
<!-- _class: transition2 -->  

Partie 3 : Gestion d'équipe XP

--- 
 
<center>

![](./img/work-in-progress.jpeg)

</center>


---
<!-- _class: transition2 -->  

Partie 4: Gestion de la qualité XP

--- 
 
<center>

![](./img/work-in-progress.jpeg)

</center>

---
<!-- _class: transition2 -->  

Partie 5 : SCRUM

--- 
 
<center>

![](./img/work-in-progress.jpeg)

</center>

---
<!-- _class: transition2 -->  

Partie 6 : Grande structure, nouvelle méthode : Safe, ITIL

--- 
 
<center>

![](./img/work-in-progress.jpeg)

</center>