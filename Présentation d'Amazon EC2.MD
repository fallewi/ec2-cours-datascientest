FORMATION AWS EC2

# I - Présentation d'Amazon EC2

### 1.   Présentation :

Amazon Elastic Compute Cloud (Amazon EC2) offre une capacité de calcul évolutive dans le cloud
Amazon Web Services (AWS). Amazon EC2 permet de ne pas investir à l'avance dans du
matériel et, par conséquent, vous pouvez développer et déployer les applications plus rapidement. Vous
pouvez utiliser Amazon EC2 pour lancer autant de serveurs virtuels que nécessaire, configurer la sécurité
et les réseaux, et gérer le stockage. Amazon EC2 vous permet d'augmenter ou de diminuer l'échelle afin de
gérer les modifications en termes d'exigences ou de pics de popularité, et réduire ainsi le besoin de prévoir
le trafic.

#### 2. Fonctionnalités d'Amazon EC2

##### Amazon EC2 offre les fonctionnalités suivantes :

• Environnements de calcul virtuels, appelés instances

• Modèles préconfigurés pour vos instances, appelés Amazon Machine Images (AMI), qui combinent
les composants dont vous avez besoin pour votre serveur (système d'exploitation et logiciels
supplémentaires inclus)

• Diverses configurations de capacité d'UC de mémoire, de stockage et de mise en réseau pour vos
instances, appelées types d'instance

• Sécuriser les informations de connexion de vos instances à l'aide de paires de clés (AWS stocke la clé
publique, tandis que vous stockez la clé privée dans un endroit sécurisé)

• Volumes de stockage pour les données temporaires qui sont supprimées lorsque vous arrêtez, mettez en
veille prolongée ou résiliez votre instance, appelés volumes de stockage d'instance

• Volumes de stockage permanents pour vos données à l'aide d'Amazon Elastic Block Store (Amazon
EBS), appelés volumes Amazon EBS

• Plusieurs emplacements physiques pour vos ressources, tels que les instances et les volumes Amazon
EBS, appelés Régions et Zones de disponibilité

• Pare-feu permettant de spécifier les protocoles, ports et plages d'adresses IP source qui peuvent
atteindre vos instances à l'aide des groupes de sécurité

• Adresses IPv4 statiques pour le cloud computing dynamique, appelées adresses IP Elastic

• Métadonnées, appelées balises, que vous pouvez créer et affecter à vos ressources Amazon EC2

• Réseaux virtuels que vous pouvez créer et qui sont logiquement isolés du reste du cloud AWS, et que, le
cas échéant, vous pouvez connecter à votre propre réseau, appelés Virtual Private Clouds (VPC)
Pour plus d'informations sur les fonctions de Amazon EC2, consultez la page produit Amazon EC2.
Pour plus d'informations sur l'exécution de votre site web sur AWS, consultez Hébergement web.


Nous alternerons dans cette formation l'utilisation de la ligne de commande (Aws cli) et de la console AWS (GUI).


# II. Qu'est ce que la AWS cli et Comment l'installer  ?



L’AWS CLI facilite la création et la gestion de diverses ressources AWS. Donc, si vous êtes quelqu’un qui interagit beaucoup avec les services AWS, je suis sûr que le fait d’avoir l’interface de ligne de commande à portée de main vous facilitera la vie.

#### ***1.Qu’est-ce que l’AWS CLI ?***

***AWS CLI (Amazon Web Service Command Line Interface)*** est un outil utilitaire de ligne de commande open source pour la gestion des services Web Amazon. AWS CLI est un outil utilitaire fourni par AWS pour gérer les ressources. L’API AWS est directement accessible via l’AWS CLI. À l’aide de l’utilitaire AWS CLI, vous pouvez créer des scripts pour automatiser Amazon Web Services.

la  CLI de AWS  est un outil unifié incroyable d’AWS qui vous permet de créer et de gérer des ressources AWS à partir d’un seul endroit.

Comme son nom l’indique, vous faites tout cela à partir de la ligne de commande manuellement ou en automatisant les appels d’API via des scripts.

***Remarque importante : Veuillez noter qu’AWS recommande d’utiliser CLI v2. Selon AWS, les nouvelles fonctionnalités ne sont pas rétroportées vers la v1, nous devons donc utiliser uniquement la v2. Par conséquent, nous nous concentrerons sur CLI v2 (dernière version majeure)***.
Conditions préalables:




#### ***2.Comment installer l’AWS CLI***

Téléchargez la dernière version du programme d’installation  de l’interface de ligne de commande à l’aide du lien ci-dessous pour votre système .

***https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html***

L’AWS CLI est disponible dans les versions 1 et 2. AWS recommande d’utiliser **AWS CLI version** 2. Si vous avez déjà la version 1, suggérez-lui de la désinstaller ou de créer un lien symbolique/alias avec un nom différent.


Pour installer l’AWS CLI sur Ubuntu, vous devez remplir les conditions suivantes :

    Compte AWS
    Serveur Machine Ubuntu
    Compte d’utilisateur privilégié Sudo

#####  Installation

Le package d’utilitaire AWS CLI est disponible dans le référentiel par défaut d’Ubuntu 20.04. Vous pouvez également utiliser Python PIP ou le programme d’installation AWS pour installer l’outil utilitaire AWS CLI.

###### 2.1 **Méthode 1 : Utilisation du script d’installation AWS**

Il s’agit de la méthode d’installation recommandée par AWS. Cette méthode fonctionne sur Ubuntu et d’autres distributions Linux telles que CentOS, Fedora, Amazon Linux 1 et Amazon Linux 2.

Pour la dernière version, téléchargez la version 64 bits à l’aide de la commande **curl** :

> sudo curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

*Remarque : Pour une version spécifique de l’AWS CLI, ajoutez un trait d’union et le numéro de version au nom de fichier*.

L’étape suivante consiste à décompresser le fichier téléchargé, qui extraira le fichier et créera un répertoire nommé 'aws'. Dans la commande unzip not present, installez décompressez le paquet ($ sudo apt install unzip).

Exécutez la commande suivante pour décompresser le fichier :

> sudo unzip awscliv2.zip

Maintenant, exécutez le programme d’installation, en utilisant:

> sudo ./aws/install

Par défaut, aws cli est installé dans **/usr/local/aws-cli** et un lien symbolique est créé dans /usr/local/bin.

Pour vérifier l’installation, tapez :

> aws --version

Sortie:

> aws-cli/2.1.33 Python/3.8.8 Linux/5.4.0-70-generic exe/x86_64.ubuntu.20 prompt/off

###### 2.2  Méthode 2 : Installation de l’AWS CLI à l’aide d’APT

L’outil utilitaire AWS CLI est disponible dans le référentiel par défaut d’Ubuntu 20.04. Pour installer l’outil à l’aide d’APT, procédez comme suit :

Mettre à jour les packages système :

Exécutez la commande suivante mettre à jour les packages système et l’index du référentiel au plus tard.

> sudo apt update

Une fois les packages système mis à jour, exécutez la commande suivante pour installer l’AWS CLI.

> sudo apt install awscli -y

Une fois l’installation terminée, exécutez la commande suivante pour vérifier.

> aws --version

Vous obtiendrez une sortie similaire à:

> aws-cli/2.5.8 Python/3.9.11 Windows/10 exe/AMD64 prompt/off



Après l’installation, vous pouvez configurer l’accès au compte AWS à l’aide de l’AWS CLI. Avant de commencer avec la configuration aws, vous devez disposer de la clé d’accès et de la clé secrète de l’utilisateur IAM fournies avec un accès approprié.

Exécutez la commande suivante pour configurer l’accès au compte aws.

> aws configure

Entrez les détails suivants en conséquence :

    AWS Access Key ID [Clé d’accès de l’utilisateur IAM]
    Clé d’accès secrète AWS [clé secrète de l’utilisateur IAM]
    Nom de région par défaut [Région Aws]
    Format de sortie par défaut [Le format JSON est correct]

Vous aurez une sortie similaire à:

> AWS Access Key ID [****************GAPB]:
> AWS Secret Access Key [****************TMmi]:
> Default region name [eu-west-1]:
> Default output format [None]:


**Désinstallation de l’AWS CLI à partir d’ubuntu**

Pour désinstaller l’AWS CLI d’ubuntu, vous devez vérifier le chemin d’installation de l’AWS CLI. Exécutez la commande suivante pour vérifier le répertoire d’installation de l’AWS CLI.

> which aws

Vous obtiendrez la sortie comme suit: 

> /usr/local/bin/aws

Utilisez la commande suivante pour vérifier le lien symbolique et le chemin d’installation.

> ls -l /usr/local/bin/aws

Vous obtiendrez une sortie en tant que:

> lrwxrwxrwx 1 root root 37 Mar 31 04:01 /usr/local/bin/aws -> /usr/local/aws-cli/v2/current/bin/aws

Supprimez d’abord les deux liens symboliques, tapez :

> sudo rm /usr/local/bin/aws sudo rm /usr/local/bin/aws_completer

Supprimez maintenant le répertoire d’installation à l’aide de la commande suivante.

> sudo rm -rf /usr/local/aws-cli

Vous avez réussi à supprimer l’AWS CLI du système Ubuntu.

###### 2.3 **Méthode 3 : Installation de l’AWS CLI à l’aide de Python PIP**

Vous pouvez utiliser Python PIP pour installer l’AWS CLI sur votre serveur Ubuntu. Python 2.x n’est pas pris en charge sur Ubuntu 20.04, vous devez donc installer Python 3.x.

Tout d’abord, installez python-pip sur votre système. Exécutez la commande suivante pour installer le package 
**python-pip**.

> sudo apt-get install python3-pip

Une fois l’installation terminée, vous devez mettre à niveau PIP vers la dernière version.

> sudo pip3 install --upgrade pip

Maintenant, exécutez la commande suivante pour installer l’AWS CLI à l’aide de PIP.

> sudo pip3 install awscli

Pour vérifier l’installation, exécutez la commande suivante.

> python3 -m awscli --version

Sortie:

> aws-cli/1.18.69 Python/3.8.5 Linux/5.8.0-45-generic botocore/1.16.19

***La sortie indique que la version de l’AWS CLI installée est 1.18 ***


# III. Création d'une instance avec la ligne de commande

**Avant que vous ne lanciez un environnement de production, vous devez répondre aux questions suivantes.**

***.Quel type d'instance répond le mieux à mes besoins ?.***

Amazon EC2 fournit différents types d'instance pour vous permettre de choisir les capacités d'UC, de
mémoire, de stockage et de mise en réseau dont vous avez besoin pour exécuter vos applications.

***.Quelle option d'achat répond le mieux à mes besoins ?.***
Amazon EC2 prend en charge les instances à la demande (instances par défaut), les instances Spot et
les instances réservées.

***.Quel type de volume racine répond à mes besoins ?.***

Chaque instance est basée sur Amazon EBS ou sur le stockage d'instances. Sélectionnez une AMI en
fonction du type de volume racine dont vous avez besoin.


#### 1.**instances et AMI**
Une ***Amazon Machine Image (AMI)*** est un modèle qui contient une configuration logicielle (par exemple,
un système d'exploitation, un serveur d'applications et des applications). À partir d'une AMI, vous lancez
une instance qui est une copie de l'AMI s'exécutant en tant que serveur virtuel dans le cloud. Vous pouvez
lancer plusieurs instances d'une AMI en configurant simplement le nombre d'instance au lancement.


Amazon Web Services (AWS) publie de nombreuses Amazon Machine Images (AMI) contenant des
configurations logicielles courantes pour un usage public. En outre, des membres de la communauté de
développeurs AWS ont publié leurs propres AMI personnalisées. Vous pouvez également créer votre ou
vos propres AMI personnalisées. Cela vous permet de démarrer rapidement et facilement de nouvelles
instances disposant de tout ce dont vous avez besoin. Par exemple, si votre application est un site web
ou un service web, votre AMI peut inclure un serveur web, le contenu statique associé et le code pour
les pages dynamiques. Ainsi, quand vous lancez une instance à partir de cette AMI, votre serveur web
démarre et votre application est prête à accepter des demandes.


Vos instances continuent de s'exécuter jusqu'à ce que vous les arrêtiez, les mettiez en veille prolongée ou
les résiliiez, ou jusqu'à ce qu'elles connaissent une défaillance. En cas de défaillance d'une instance, vous
pouvez en lancer une nouvelle à partir de l'AMI.

### 2.**instances**

Une **instance** est un serveur virtuel dans le cloud . Sa configuration au moment du lancement est une copie
de l'AMI que vous avez spécifiée quand vous avez lancé l'instance.

Vous pouvez lancer différents types d'instance à partir d'une seule AMI. Un type d'instance détermine
essentiellement les capacités matérielles de l'ordinateur hôte utilisé pour votre instance. Chaque type
d'instance offre des capacités de calcul et de mémoire différentes. 

Sélectionnez un **type d'instance** en fonction de la quantité de mémoire et de la puissance de calcul dont vous avez besoin pour l'application ou le logiciel que vous prévoyez d'exécuter sur l'instance. 


Une fois une instance lancée, celle-ci ressemble à un hôte classique et vous pouvez interagir avec elle
comme avec n'importe quel ordinateur. Vous exercez un contrôle total sur vos instances. Vous pouvez
utiliser sudo pour exécuter des commandes nécessitant des privilèges racine (root).


### 3.**Stockage pour votre instance**

Le périphérique racine pour votre instance contient l'image utilisée pour démarrer l'instance. L'appareil
racine est un volume **Amazon Elastic Block Store (Amazon EBS)** ou un volume de stockage d'instances.

Votre instance peut inclure des volumes de stockage local, appelés volumes de stockage d'instances,
que vous pouvez configurer au moment du lancement avec la fonctionnalité de mappage de périphérique
de stockage en mode bloc.

Une fois que ces volumes ont été ajoutés et mappés à votre instance, ils sont
à votre disposition pour être montés et utilisés. Si votre instance est défaillante, ou si elle est arrêtée ou
terminée, les données sur ces volumes sont perdues. Ces volumes sont donc mieux adaptés aux données
temporaires. 


#### 4.**Lancement d’une instance EC2 à l’aide de l’AWS CLI**


Commençons donc par l’AWS CLI en lançant une instance EC2 à l’aide de celle-ci. La création d’une instance avec l’AWS CLI est identique au lancement d’une instance avec la console AWS. Ouvrez votre invite de commande en tant qu’administrateur en cliquant dessus avec le bouton droit de la souris.

***4.1 Création d’un VPC***

La première chose à faire est de créer un VPC (virtual private cloud) sous lequel une instance EC2 sera lancée. Pour créer un VPC dans l’interface de ligne de commande, tapez la commande donnée sur le cmd.

> aws ec2 create-vpc --cidr-block 10.0.0.0/16

Ici, le bloc CIDR que j’ai pris est 10.0.0.0/16, vous pouvez le modifier selon vos besoins. Après avoir exécuté cette commande, la sortie suivante sera donnée au format JSON. Notez le vpcId . 

![creatingvpc](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\creatingvpc.png)



***4.2 Création de sous-réseaux***

Ensuite, créez deux sous-réseaux et rendez-en un public pour le rendre accessible à partir d’Internet. Pour ce faire, utilisez la commande ci-dessous :

> aws ec2 create-subnet --vpc-id <vpcId> --cidr-block 10.0.1.0/24

Notez le SubnetId généré ici, afin que ce sous-réseau puisse être rendu public ultérieurement. Le bloc CIDR que nous avons utilisé ici est 10.0.1.0/24.

Créez maintenant un deuxième sous-réseau avec le bloc CIDR 10.0.0.0/24. (Les valeurs des blocs CIDR peuvent être modifiées selon les besoins de l’utilisateur) :

> aws ec2 create-subnet --vpc-id <vpcId> --cidr-block 10.0.0.0/24

![describertbsubnet](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\describertbsubnet.png)



***4.3 Création d’une passerelle Internet***

La passerelle Internet est utilisée par le sous-réseau privé pour accéder à Internet pour ses mises à jour et autres installations de packages. Créez une passerelle Internet à l’aide de la commande suivante :

> aws ec2 create-internet-gateway

Une fois la passerelle Internet créée, notez InternetGatewayId et attachez cette passerelle Internet au VPC déjà créé. Pour ce faire, utilisez la commande ci-dessous :

> aws ec2 attach-internet-gateway --vpc-id <vpcId> --internet-gateway-id <InternetGatewayId>

Tapez ici le vpcId noté (à la place de <vpcId>) et InternetGatewayId (à la place de <InternetGatewayId>)

***4.4 Création d’une table de routage***

L’étape suivante consiste à créer une table de routage et à l’affecter au VPC déjà créé. Après avoir créé la table de routage, affectez l’itinéraire à cette table de routage. Les commandes pour la même chose sont celles données.

> aws ec2 create-route-table --vpc-id <vpcId>

Maintenant, utilisez le RouteTableId et utilisez-le à l’étape suivante:

>aws ec2 create-route --route-table-id <RouteTableId> 
>              --destination-cidr-block 0.0.0.0/0 --gateway-id <nternetGatewayI>

Ici, nous avons utilisé le 0.0.0.0/0 comme bloc CIDR de destination.

![igwrtb](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\igwrtb.png)

***Affichage de la table de routage et des sous-réseaux***

Pour vérifier si la table de routage et les sous-réseaux sont créés et affectés avec succès, utilisez les commandes ci-dessous :

> aws ec2 describe-route-tables --route-table-id <RouteTableId>

> aws ec2 describe-subnets --filters "Name=vpc-id,Values=<vpcId>"
>                         --query "Subnets[*].{ID:SubnetId,CIDR:CidrBlock}"

Ici, remplacez votre vpcId par <vpcId>.

![describertbsubnet](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\describertbsubnet.png)



  ***4.5 Association de la table de routage et modification du sous-réseau ***

L’étape suivante consiste à associer la table de routage au sous-réseau et à créer le même sous-réseau que public en y mappant l’adresse IP publique. Entrez le SubnetId et le RouteTableId que vous avez notés précédemment. Pour associer le type de table de routage...

Tapez:

> aws ec2 associate-route-table --subnet-id <SubnetId> --route-table-id <RouteTableId>


Pour mapper l’adresse IP publique au sous-réseau, utilisez la commande ci-dessous :

> aws ec2 modify-subnet-attribute --subnet-id <SubnetId> --map-public-ip-on-launch


***4.6 Création d’une paire de clés et d’un groupe de sécurité***

L’étape la plus importante consiste à créer une paire de clés. Cette paire de clés doit être conservée en toute sécurité avec l’utilisateur afin que la personne puisse accéder à l’instance EC2 créée à l’aide de cette paire de clés.

Maintenant, créez la paire de clés à l’aide de la commande ci-dessous:

> aws ec2 create-key-pair --key-name AWS-Keypair --query "KeyMaterial" 
>                        --output text > "$(pwd)/AWS_Keypair.pem"

Ici, nous avons nommé le fichier de paire de clés (fichier .pem) comme AWS-Keypair et le chemin d’accès où notre fichier sera téléchargé est **AWS_Keypair.pem**. Ces deux choses peuvent être modifiées par l’utilisateur.

Pour le groupe de sécurité, utilisez les commandes ci-dessous :

> aws ec2 create-security-group --group-name <security-group-name> --description "<description>"
>                              --vpc-id <vpcId>



Ici, fournissez le nom et la description du groupe de sécurité et ajoutez-le à la place de <security-group-name> et <description> respectivement. Notez le GroupId et utilisez-le à l’étape suivante.

> aws ec2 authorize-security-group-ingress --group-id <GroupId> 
>                                         --protocol tcp --port 22 --cidr 0.0.0.0/0

*Le protocole/port que nous utilisons ici est TCP/22.*

***4.7 Exécution de l’instance EC2***

Enfin, une fois toute l’installation terminée avec succès, le moment est venu d’exécuter l’instance. Pour exécuter l’instance EC2, utilisez la commande comme indiqué ci-dessous.

> aws ec2 run-instances --image-id <ami-id> --count 1 --instance-type t2.micro 
>                     --key-name <Keypair-name> --security-group-ids <SecurityGroupId> 
>                     --subnet-id <SubnetId>

À cette étape, vous aurez besoin d’un ID d’image AMI (Amazon Machine Image). Pour cela, connectez-vous à votre console AWS et choisissez n’importe quelle AMI de votre type. Copiez l’ID de l’image et remplacez-le ici à la place de <ami-id>. Utilisez également le nom de votre paire de clés, l’ID du groupe de sécurité et l’ID du sous-réseau au bon endroit dans la commande ci-dessus. Notez également l’InstanceId.

![runinstance](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\runinstance.png)



![runinstance2](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\runinstance2.png)



***4.8 Affichage de l’instance***

Maintenant que l’état de l’instance est « en cours d’exécution », tapez la commande pour afficher les détails complets de l’instance EC2 que vous venez de créer :

> aws ec2 describe-instances --instance-id <InstanceId>

Entrez l’InstanceId que vous avez noté à l’étape ci-dessus.

![describeinstance](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\describeinstance.png)

***4.9 Vérification de l’instance EC2***

Pour vérifier si l’instance EC2 créée à l’aide de l’AWS CLI est créée selon les besoins, connectez-vous à votre console AWS, ouvrez le service EC2 et recherchez l’instance.



![awsec2instancelaunchedusingcli](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\awsec2instancelaunchedusingcli.png)



***4.10 Se connecter à l'instance en ssh grâce à Mobaxterm***

On peut déja vérifier que le port 22 qui est le port ssh qui nous servira pour la connexion est bien ouvert dans les règles d'entrée de notre sécurity group

![allow-22-port-in-aws-security-group](https://www.devopshint.com/wp-content/uploads/2020/08/allow-22-port-in-aws-security-group-1024x292.png)

###### Étape #1: Télécharger MobaXTerm

Téléchargez et installez MobaXTerm à partir du [site officiel de MobaXTerm](https://mobaxterm.mobatek.net/download-home-edition.html) pour Windows 10.

###### Étape #2 : Comment se connecter à une instance AWS EC2 à l’aide de MobaXTerm

Une fois installé, ouvrez le mobaxterm, allez dans le menu **Sessions**, cliquez sur **Nouvelle session** comme indiqué ci-dessous.

![choosessh](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\choosessh.png)

Entrez votre adresse IP d’instance AWS EC2, username dans **le champ Remote Host** et **Specify UserName**.

Ici, je me connecte à  Instance Ubuntu, Si vous connectez AWS EC2, tapez user **ec2-user** dans le champ **Spécifier le nom d’utilisateur**

Cliquez sur **l’onglet Paramètres SSH avancés** et donnez le chemin de votre fichier .pem d’instance dans le champ **utiliser la clé privée** comme indiqué ci-dessous

Cliquez sur **le bouton OK** pour connecter une instance AWS EC2 à l’aide de mobaxterm

![moba](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\moba.png)

Une fois connecté, vous verrez comme ci-dessous le terminal AWS Instance SSH

![logged-in-to-aws-ec2-instance](C:\Users\fallewi\Documents\aws-ec2-course\labs\assets\images\logged-in-to-aws-ec2-instance.png)

Maintenant que nous avons pu nous connecter à notre instance , nous pouvons la supprimer afin de libérer des ressources

***4.11 Mettre fin à l' instance Amazon EC2***

si nous voulons terminer l'instance (résilier) , nous devons taper la Commande:

```
aws ec2 terminate-instances --instance-ids <id-instance>
```

Sortie:

```
{
    "TerminatingInstances": [
        {
            "InstanceId": "i-1234567890abcdef0",
            "CurrentState": {
                "Code": 32,
                "Name": "shutting-down"
            },
            "PreviousState": {
                "Code": 16,
                "Name": "running"
            }
        }
    ]
}
```

# 

