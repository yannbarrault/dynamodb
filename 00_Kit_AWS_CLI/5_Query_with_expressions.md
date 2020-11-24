aws dynamodb query --table-name Music     --key-condition-expression "Artist = :v1 AND SongTitle = :v2"     --expression-attribute-values file://expression-attributes.json --endpoint-url http://localhost:8000

REPONSE
========
{
    "Items": [
        {
            "Artist": {
                "S": "No One You Know"
            },
            "SongTitle": {
                "S": "Call Me Today"
            },
            "AlbumTitle": {
                "S": "Somewhat Famous"
            }
        }
    ],
    "Count": 1,
    "ScannedCount": 1,
    "ConsumedCapacity": null
}
