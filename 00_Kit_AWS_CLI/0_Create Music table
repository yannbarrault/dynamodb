Le format de ligne de commande se compose d'un nom d'opération DynamoDB, suivi des paramètres pour cette opération. l'AWS CLI prend en charge une version raccourcie de la syntaxe pour les valeurs des paramètres, ainsi que JSON.

Par exemple, la commande suivante permet de créer une table nommée Music. La clé de partition est Artist et la clé de tri est SongTitle. (Pour une lecture plus facile, les commandes longues dans cette section sont divisées en plusieurs lignes).

aws dynamodb create-table \
    --table-name Music \
    --attribute-definitions \
        AttributeName=Artist,AttributeType=S \
        AttributeName=SongTitle,AttributeType=S \
    --key-schema AttributeName=Artist,KeyType=HASH AttributeName=SongTitle,KeyType=RANGE \
    --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1 \
    --endpoint-url http://localhost:8000

aws dynamodb describe-table --table-name Music --endpoint-url http://localhost:8000

REPONSE:
===========

{
    "TableDescription": {
        "AttributeDefinitions": [
            {
                "AttributeName": "Artist",
                "AttributeType": "S"
            },
            {
                "AttributeName": "SongTitle",
                "AttributeType": "S"
            }
        ],
        "TableName": "Music",
        "KeySchema": [
            {
                "AttributeName": "Artist",
                "KeyType": "HASH"
            },
            {
                "AttributeName": "SongTitle",
                "KeyType": "RANGE"
            }
        ],
        "TableStatus": "ACTIVE",
        "CreationDateTime": "2020-11-24T05:58:42.206000+01:00",
        "ProvisionedThroughput": {
            "LastIncreaseDateTime": "1970-01-01T01:00:00+01:00",
            "LastDecreaseDateTime": "1970-01-01T01:00:00+01:00",
            "NumberOfDecreasesToday": 0,
            "ReadCapacityUnits": 1,
            "WriteCapacityUnits": 1
        },
        "TableSizeBytes": 0,
        "ItemCount": 0,
        "TableArn": "arn:aws:dynamodb:ddblocal:000000000000:table/Music"
    }
}
