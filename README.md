# Formation DynamoDB

## Installing, updating, and uninstalling the AWS CLI
L'AWS CLI est disponible à l'adresse  [http://aws.amazon.com/cli](https://aws.amazon.com/cli). Elle s'exécute sous Windows, macOS ou Linux. Après avoir téléchargé l'AWS CLI, procédez comme suit pour l'installer et la configurer :

1.  Accédez au  [AWS Command Line Interface Guide de l'utilisateur](https://docs.aws.amazon.com/cli/latest/userguide/).
    
2.  Suivez les instructions d'[Installation de l'interface de ligne de commande AWS](https://docs.aws.amazon.com/cli/latest/userguide/installing.html)  et de  [Configuration de l'interface de ligne de commande AWS](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).

### Docker
[https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-docker.html](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-docker.html)

### Linux
[https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html)

### MacOS
[https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-mac.html](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-mac.html)

### Windows
[https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-windows.html](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-windows.html)

## Configuring the AWS CLI

### AWS Configure 

    $ aws configure
    AWS Access Key ID [None]: AKIAIOSFODNN7EXAMPLE
    AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
    Default region name [None]: us-west-2
    Default output format [None]: json

### Access key ID and secret access key

https://console.aws.amazon.com/iam/


## DynamoDB Local

### Utilisation de l'AWS CLI avec DynamoDB téléchargeable
L'AWS CLI peut également interagir avec DynamoDB (version téléchargeable) qui s'exécute sur votre ordinateur. Pour ce faire, ajoutez le paramètre suivant pour chaque commande :

--endpoint-url http://localhost:8000

L’exemple suivant utilise l'AWS CLI pour répertorier les tables dans une base de données locale.

aws dynamodb list-tables --endpoint-url http://localhost:8000
Si DynamoDB utilise un numéro de port autre que la valeur par défaut (8000), modifiez la valeur --endpoint-url en conséquence.

### Installation de DynamoDB Local
Amazon fournit une image Docker de DynamoDB Local: https://hub.docker.com/r/amazon/dynamodb-local/
Ainsi, vous pouvez instancier une base de données DynamoDB sur votre poste de travail.

"DynamoDB local is a downloadable version of DynamoDB that enables developers to develop and test applications using a version of DynamoDB running in your own development environment."

La commande à executer pour démarrer le conteneur est la suivante:

```
docker run -p 8000:8000 amazon/dynamodb-local
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg0NjEzMTA0MV19
-->