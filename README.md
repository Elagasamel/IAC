# IAC
La liste d’outils ayant l’étiquette “DevOps” s’allonge de jour en jour et il est important de connaître les besoins de son équipe afin d’utiliser les bons services afin de faciliter le développement de nouvelles applications.

Cet article vous permettra de connaître les différents outils Devops par catégorie afin d’améliorer la productivité et la collaboration de vos équipes.

# SOMMAIRE

La culture Devops et ses avantages
Les différents outils utilisés en Devops
Les outils de gestion de code source
Les tests d’intégration continue / déploiement continu
Conteneurs
Cloud providers
Automatisation et gestion de configuration
Monitoring et alerting
Outils de gestion de projet
Gestion des secrets
Les outils Devops du point de vue de Padok
La culture Devops et ses avantages

DevOps est la contraction des mots “developpers” et “ops”. Il s’agit d’une culture de collaboration visant à automatiser les processus entre les équipes de développement et les services opérationnelles afin de faciliter le développement, le test et la livraison des logiciels.

Nous avons vu que traditionnellement ces équipes ont des intérêts plutôt opposés : les développeurs sont censés créer de la valeur et rendre le produit/service toujours plus innovant et les opérationnels ont pour objectif de maintenir la stabilité des infrastructures.

Les avantages de la culture Devops sont nombreux. Une collaboration Devops permet d’effectuer des mises en production plus rapidement et de meilleure qualité. L’équipe Devops livre plus souvent tout en gardant une qualité et stabilité des infrastructures. Une bonne stratégie Devops repose sur une collaboration poussée entre les ops et les développeurs, une meilleure communication et donc une meilleure performance des équipes.

Les différents outils utilisés en Devops
Les équipes de Devops utilisent quotidiennement des outils divers pour des tâches et missions variées. Nous avons préparé ici une liste (non exhaustive) de ces outils.

source-code-management-git-subversion-github-gitlab-bitbucket

Les outils de gestion de code source

La première étape d’une collaboration Devops est d’aligner les équipes de développement et les ops sur un même outil de gestion de code source. Concrètement, cela permet de connaître les différentes modifications du code et les auteurs de celles-ci. Il s’agit d’un outil de versionning : toute modification de code entraîne la création d’une nouvelle version. Historiquement, les ops n’utilisent pas ce genre d’outils car il y a peu d'automatisation, tout est manuel et il n'y a donc pas de code. Or une fois qu'il y a du code, la bonne pratique est de le partager et de le faire relire par ses pairs. C'est là que les outils de gestion de code rentrent en scène.

#### Il y a deux types de gestions de code :

Les outils comme Git et Subversion, qui servent à créer un historique de ses fichiers : à tel moment, tel changement a été fait dans tes fichier. Subversion est un outil plus ancien et moins efficace que Git.
Les outils comme Github, Gitlab et Bitbucket qui servent à partager son code, et donc l'historique qui va avec. Ils sont basés sur Git et il est possible d'avoir l'historique du code et de travailler à plusieurs dessus. Si Github a le monopole historiquement, Gitlab devient de plus en plus populaire, notamment grâce à Gitlab CI qui est efficace.

CI-CD-jenkins-gitlabci-bamboo-teamcity-concourse-circleci-travisci

Les tests d’intégration continue / déploiement continu
Les outils d’intégration continue et de déploiement continu, ou CI/CD permettent l’automatisation des tests des modifications de code source. Concrètement, les outils de CI/CD permettent la modernisation des applications en réduisant le temps nécessaire pour créer de nouvelles fonctions.

Il existe de nombreux outils de CI/CD. L’une des plateformes la plus utilisée est Jenkins, un outil open source (qui peut cependant être difficile à prendre en main).

Il existe aussi des solutions payantes comme GitlabCI (que nous utilisons chez Padok), Bamboo, TeamCity, Concourse, CircleCI ou Travis CI.

Les cloud providers, Google et AWS notamment, proposent eux aussi leur propre outil d'intégration et de déploiement continus.

containers-docker-rkt-kubernetes-mesos-docker-swarm

Conteneurs
Les conteneurs permettent d’isoler une application avec l’ensemble des éléments dont elle a besoin pour fonctionner. L’utilisation de conteneurs permet d’être le plus “iso” possible depuis le code des développeurs jusqu’à la production et de ne pas avoir de surprise au moment de la production.

Docker automatise et standardise le déploiement d’application dans ces conteneurs virtuels et s’impose comme le leader de ce segment d’outils. L’alternative à Docker est RKT, qui est le standard poussé par la fondation CoreOS.

Lorsque l’on utilise des conteneurs, le besoin d’un orchestrateur se fait très rapidement sentir.

L’orchestration de conteneurs permet de simplifier leur déploiement et leur gestion. L’orchestrateur le plus utilisé sur le marché est Kubernetes, mais il en existe d’autres comme MesOs et Docker-Swarm.

cloud-providers-google-aws-azure-haproxy-

Cloud providers
Les Cloud providers proposent aux entreprises et particuliers des solutions de stockage distant. Aujourd’hui, trois importants players se partagent le marché du service cloud : Google Cloud Platform, Azure et AWS. En proposant le plus large éventail de services, AWS est sans conteste le leader mondial de ce marché.

Quand on parle de Cloud providers, on pense aux services de load balancing. Les services de load balancing ont pour mission de répartir les charges sur différents appareils, permettant une amélioration du temps de réponse. HAproxy est la référence en load balancing.

automation-terraform-ansible-puppet-salt

Automatisation et gestion de configuration
L’automatisation permet d’éliminer les tâches répétitives des équipes Devops.

Plusieurs types d’automatisation en Devops existent :

Mettre en place des configurations automatiques sur les serveurs
Automatiser les actions des serveurs
Plusieurs outils existent en fonction de l’infrastructure existante et des besoins de l’entreprise :

Terraform : provisioning d’infrastructure ;
Ansible : gestion de la configuration des serveurs esclaves ;
Puppet : gestion de la configuration des serveurs esclaves ;
Salt : gestion de la configuration des serveurs esclaves.
Monitoring-prometheus-grafana-ELK

Monitoring et alerting
Les outils de monitoring et alerting permettent d’avoir une vue d’ensemble sur son infrastructure, de résoudre les problèmes qui surviennent et d’améliorer les performances.

L’application open source Prometheus et le service Grafana permettent de monitorer les clusters Kubernetes. En couplant trois outils, ELK (Elasticsearch, Logstash et Kibana) est une solution d’analyse de logs performante. On peut jouer sur les performances de chaque outil individuellement et les adapter à ses besoins : Logstash pour la normalisation/envoi des logs, Elasticsearch pour le stockage et Kibana pour la visualisation. ELK permet de faire de l'analyse de logs (forensics) et de l'agrégation (dashboard).

Project-management-jira-trello

Outils de gestion de projet
Pour mener à bien le développement d’un logiciel, miser sur un outil de management de projet commun dans l’équipe Devops paraît indispensable.

Jira est un outil de gestion de projet Agile qui permet de planifier, suivre et gérer les projets de développement logiciel. Avec Jira, chaque membre de l’équipe de développement peut suivre l’avancée des projets et définir les priorités du sprint.

D’un autre côté, Trello se démarque par son intuitivité et sa simplicité pour gérer les différentes tâches du projet.

secrets-vault-secrets

## Gestion des secrets
Avec le besoin d’avoir une sécurisation toujours plus performante, de nouveaux outils de gestion des secrets apparaissent comme Vault. Vault permet uneorganisationdes secrets statique et dynamique.

Secrets, le service de gestion des secrets de Kubernetes est une alternative à Vault.

Les outils Devops du point de vue de Padok
Il n’existe pas de stack parfaite en Devops. Il est surtout question de connaître les outils adaptés à vos besoins, ce qui nécessite du temps et de nombreux tests. Nous vous recommandons de faire des tests d’outils grâce aux essais gratuits proposés par la plupart des services. Cela vous permet d’évaluer cet outil sans allouer de ressources financières.

Petit rappel : le déploiement de ces divers outils ne sert à rien s’ils ne sont pas accompagnés d’une réelle envie de coopération entre les équipes de développement et les ops. Chez Padok, notre stack techno est la suivante :

Conteneurisation : Docker, Kubernetes
Hébergement : AWS, GCP
Monitoring : Grafana, Prometheus
CI : GitlabCI.
