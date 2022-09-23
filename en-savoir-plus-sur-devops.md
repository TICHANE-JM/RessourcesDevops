# Culture et pratiques DevOps

DevOps, terme que l'on entend de plus en plus dans les entreprises avec des expressions
telles que *nous faisons DevOps ou nous utilisons des outils DevOps* , est la contraction des
mots Development et Operations.

DevOps est une culture différente des cultures d'entreprise traditionnelles et nécessite un
changement de mentalité, de processus et d'outils. Elle est souvent associée aux pratiques
d'**intégration continue (CI)** et de **livraison continue (CD)** qui sont des pratiques de génie
logiciel, mais aussi à l' **Infrastructure as Code (IaC)**, qui consiste à codifier la structure et la
configuration de l'infrastructure.

Ici, je vais essayer de vous montrer ce qu'est la culture DevOps, quels sont les principes DevOps et les avantages qu'elel apporte à une entreprise. Ensuite, j'expliquerai les pratiques de CI/CD et, enfin je détaillerai IaC avec ses patrons et ses pratiques.

Voici les sujets qui vont être abordés ici :
* Premiers pas avec DevOps
* Implémentation CI/CD et déploiement continu
* Comprendre IaC

## Premiers pas avec DevOps

Le terme DevOps a été introduit en 2007-2009 par Patrick Debois, Gene Kim et John Willis, et il
représente la combinaison de **Développement (Dev)** et **Operations (Ops)**. Elle a donné naissance à
un mouvement qui prône le rapprochement entre développeurs et opérations au sein d'équipes. Il
s'agit de pouvoir fournir plus rapidement une valeur commerciale ajoutée aux utilisateurs et donc
d'être plus compétitifs sur le marché.

**La culture DevOps** est un ensemble de pratiques qui réduisent les barrières entre les
développeurs, qui veulent innover et livrer plus vite, d'un côté et, de l'autre, les opérations, qui
veulent garantir la stabilité des systèmes de production et la qualité du système changements qu'ils
font.

La culture DevOps, c'est aussi le prolongement des processus agiles (scrum, XP, etc.), qui
permettent de réduire les délais de livraison et impliquent déjà les développeurs et les équipes
métiers, mais sont souvent freinés du fait de la non-inclusion des Ops dans le même équipes.

La communication et ce lien entre Dev et Ops permet donc un meilleur suivi des déploiements de
production de bout en bout et des déploiements plus fréquents de meilleure qualité, économisant
de l'argent pour l'entreprise.

Pour faciliter cette collaboration et améliorer la communication entre Dev et Ops, il y a plusieurs éléments clés dans les processus à mettre en place, comme dans les exemples suivants :
* Des déploiements d'applications plus fréquents avec intégration et livraison continue (appelés CI/CD)
* La mise en place et l'automatisation de tests unitaires et d'intégration, avec un processus axé sur le **Behavior-Driven Design (BDD)** ou **Test-Driven Design (TDD)**
* La mise en place d'un moyen de recueillir les retours des utilisateurs
* Surveillance des applications et de l'infrastructure
      
Le mouvement DevOps repose sur trois axes :  

 * **La culture de collaboration:** C'est l'essence même du DevOps, le fait que les équipes ne sont plus séparées par des spécialisations en silos (une équipe de développeurs, une équipe d'Ops, une équipe de testeurs, etc.), mais au contraire, ces personnes sont amenées ensemble en constituant des équipes pluridisciplinaires ayant le même objectif : apporter au plus vite une valeur ajoutée au produit.
 * **Processus:** Pour espérer un déploiement rapide, ces équipes doivent suivre des processus de développement issus de méthodologies agiles avec des phases itératives qui permettent une meilleure qualité des fonctionnalités et un retour rapide. Ces processus doivent non seulement être intégrés dans le workflow de développement avec intégration continue, mais également dans le workflow de déploiement avec livraison et déploiement continus. Le processus DevOps est divisé en plusieurs phases :
       - La planification et la priorisation des fonctionnalités
       - Développement
       - Intégration et livraison continues
       - Déploiement continu
       - Contrôle monitoring continu
Ces phases sont réalisées de manière cyclique et itérative tout au long de la vie du projet.
* **Outils:** Le choix des outils et des produits utilisés par les équipes est très important en DevOps. En effet, lorsque les équipes étaient séparées en Dev et Ops, chaque équipe utilisait leurs outils spécifiques (outils de déploiement pour les développeurs et outils d'infrastructure pour les opérations), ce qui a encore creusé les écarts de communication.

Avec des équipes qui rassemblent le développement et les opérations, et avec cette culture d'unité, les outils utilisés doivent être utilisables et exploitables par tous les membres.

Les développeurs doivent s'intégrer aux outils de surveillance utilisés par les équipes Ops pour détecter les problèmes de performances le plus tôt possible et aux outils de sécurité fournis par Ops pour protéger l'accès aux diverses ressources.

Les Ops, quant à eux, doivent automatiser la création et la mise à jour de l'infrastructure et intégrer le code dans un gestionnaire de code ; c'est ce qu'on appelle l'infrastructure en tant que code, mais cela ne peut se faire qu'en collaboration avec des développeurs qui connaissent l'infrastructure nécessaire aux applications. Les opérations doivent également être intégrées dans les processus et les outils de publication des applications.

Le schéma suivant illustre les trois axes de la culture DevOps : la collaboration entre Dev et Ops, les processus et l'utilisation des outils :

![image](https://user-images.githubusercontent.com/107214400/191802064-92ee3b35-4907-4040-ae05-b2448e286de1.png)

Donc, on peut revenir à la culture DevOps avec la définition de Donovan Brown (http://donovanbrown.com/post/what-is-devops):
*"DevOps est l'union de personnes, de processus et de produits pour permettre une livraison continue de valeur à nos utilisateurs finaux."*

Les avantages d'établir une culture DevOps au sein d'une entreprise sont les suivants :
* Une meilleure collaboration et communication dans les équipes, ce qui a un impact humain et social au sein de l'entreprise.
* Des délais de production plus courts, ce qui se traduit par de meilleures performances et la satisfaction de l'utilisateur final.
* Réduction des coûts d'infrastructure avec IaC.
* Un gain de temps considérable avec des cycles itératifs qui réduisent les erreurs d'application et des outils d'automatisation qui réduisent les tâches manuelles, afin que les équipes se concentrent davantage sur le développement de nouvelles fonctionnalités à valeur commerciale ajoutée.

>  Pour plus d'informations sur la culture DevOps et son impact sur la transformation des entreprises, lisez le livre de Gene Kim et Kevin Behr,*Le projet Phoenix : un roman sur l'informatique, DevOps et aider votre entreprise à gagner, et le manuel DevOps : comment créer une agilité, une fiabilité et une sécurité de classe mondiale dans les organisations technologiques* par Gene Kim, Jez Humble, Patrick Debois et John Willis.

## Mise en oeuvre CI/CD et déploiement continue

Nous avons vu précédemment que l'une des pratiques clés de DevOps est le processus d'intégration et de livraison continue, également appelé CI/CD. En fait, derrière les acronymes de CI/CD, il y a trois pratiques :
* **Intégration continue (CI)**
* **Livraison continue (CD)**
* **Déploiement continu**

A quoi correspond chacune de ces pratiques ? Quels sont leurs prérequis et bonnes pratiques ? Sont-ils applicables à tous ?
Détaillons chacune de ces pratiques, en commençant par l'intégration continue.

### Intégration continue (CI)

Dans la définition suivante donnée par Martin Fowler, il y a trois éléments clés mentionnés, les membres d'une équipe, s'intègrent et le plus rapidement possible :

> *"L'intégration continue est une pratique de développement logiciel où les membres d'une équipe intègrent fréquemment leur travail... Chaque intégration est vérifiée par un build automatisé (test compris) pour détecter les erreurs d'intégration le plus rapidement possible."*

C'est-à-dire que CI (Intégration Continue) est un processus automatique qui vous permet de vérifier l'intégralité du code d'une application à chaque fois qu'un membre de l'équipe effectue une modification. Cette vérification doit être faite le plus rapidement possible.

Nous voyons très clairement la culture DevOps dans CI (intégration continue), avec l'esprit de collaboration et de communication, car l'exécution de CI (Intégration continue) impacte tous les membres en termes de méthodologie de travail et donc de collaboration ; de plus, CI (Intégration continue) nécessite la mise en place de processus (branch, commit, pull request, code review, etc.) avec une automatisation qui se fait avec des outils adaptés à toute l'équipe (Git, Jenkins, Azure DevOps, etc.). Et enfin, CI (intégration continue) doit fonctionner rapidement pour recueillir le plus rapidement possible des retours sur l'intégration du code et ainsi être en mesure de fournir plus rapidement de nouvelles fonctionnalités aux utilisateurs.

#### Mise en oeuvre de CI (Intégration continue)

Pour mettre en place CI (Intégration continue), il est donc nécessaire de disposer d'un **Source Code Manager (SCM)** qui permettra la centralisation du code de tous les membres. Ce gestionnaire de code peut être de n'importe quel type : Git, SVN, ou **Team Foundation Source Control (TFVC)**. Il est également important d'avoir un gestionnaire de build automatique (serveur CI (Intégration continue)) qui prend en charge l'intégration continue comme Jenkins, GitLab CI, TeamCity, Azure Pipelines, GitHub Actions, Travis CI, Circle CI, etc.

> En ce qui me concerne j'utilise Git comme un SCM (Source Code Manager).

Chaque membre de l'équipe travaillera quotidiennement sur le code de l'application, de manière itérative et incrémentielle (comme dans les méthodes agiles et scrum). Chaque tâche ou fonctionnalité doit être partitionnée des autres développements à l'aide de branches.

Régulièrement, voire plusieurs fois par jour, les membres archivent ou commitent leur code et de préférence avec de petits commits (trunks) qui peuvent facilement être corrigés en cas d'erreur. Celui-ci sera donc intégré dans le reste du code de l'application avec tous les autres commits des autres membres.

Cette intégration de tous les commits est le point de départ du processus CI (Intégration continue).

Ce processus, exécuté par le serveur CI (Intégration continue), doit être automatisé et déclenché à chaque commit. Le serveur récupérera le code et procédera comme suit :
* Créez le package d'application (compilation, transformation de fichier, etc.).
* Effectuer des tests unitaires (avec couverture de code).

> Il est également possible d'enrichir le processus avec du code statique et une analyse de vulnérabilité avec SonarQube qui est dédié aux tests.

Ce processus CI (Intégration continue) doit être optimisé dès que possible afin qu'il puisse s'exécuter rapidement et que les développeurs puissent avoir un retour rapide sur l'intégration de leur code. Par exemple, un code archivé et qui ne se compile pas ou dont l'exécution des tests échoue peut impacter et bloquer toute l'équipe.

Parfois, de mauvaises pratiques peuvent se traduire par l'échec des tests dans le CI (Intégration continue), la désactivation de l'exécution des tests, en prenant comme arguments : *ce n'est pas grave, il faut livrer rapidement, ou le code qui le compile est indispensable.*

Au contraire, cette pratique peut avoir de lourdes conséquences lorsque les erreurs détectées par les tests se révèlent en production. Le temps gagné pendant le CI (Intégration continue) sera perdu à corriger les erreurs avec des correctifs et à les redéployer rapidement avec le stress. C'est le contraire de la culture DevOps avec une mauvaise qualité d'application pour les utilisateurs finaux et pas de réel retour d'expérience, et, au lieu de développer de nouvelles fonctionnalités, nous passons du temps à corriger les erreurs.

Avec un processus CI (Intégration continue) optimisé et complet, le développeur peut rapidement résoudre son problème et améliorer son code ou en discuter avec le reste de l'équipe et valider son code pour une nouvelle intégration :

![image](https://user-images.githubusercontent.com/107214400/191963561-93d01285-e2fd-4e34-acdc-ad56a25338da.png)

Ce diagramme montre les étapes cycliques de l'intégration continue qui incluent le code poussé dans le SCM par les membres de l'équipe et l'exécution de la construction et du test par le serveur CI (Intégration Continue). Et le but de ce processus rapide est de fournir une rétroaction rapide aux membres.
