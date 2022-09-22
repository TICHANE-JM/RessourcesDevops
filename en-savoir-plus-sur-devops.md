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

Pour faciliter cette collaboration et améliorer la communication entre Dev et Ops, il y a plusieurs
éléments clés dans les processus à mettre en place, comme dans les exemples suivants :
      * Des déploiements d'applications plus fréquents avec intégration et livraison continue (appelés CI/CD)
      * La mise en place et l'automatisation de tests unitaires et d'intégration, avec un processus axé sur le **Behavior-Driven Design (BDD)** ou **Test-Driven Design (TDD)**
      * La mise en place d'un moyen de recueillir les retours des utilisateurs
      * Surveillance des applications et de l'infrastructure
      
Le mouvement DevOps repose sur trois axes :  

      * **La culture de collaboration:** C'est l'essence même du DevOps, le fait que les équipes ne
sont plus séparées par des spécialisations en silos (une équipe de développeurs, une
équipe d'Ops, une équipe de testeurs, etc.), mais au contraire, ces personnes sont amenées
ensemble en constituant des équipes pluridisciplinaires ayant le même objectif : apporter
au plus vite une valeur ajoutée au produit.
