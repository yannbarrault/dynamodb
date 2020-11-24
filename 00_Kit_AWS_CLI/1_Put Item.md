aws dynamodb put-item --table-name Music  \
    --item  '{"Artist": {"S": "No One You Know"}, "SongTitle": {"S": "Call Me Today"}, "AlbumTitle": {"S": "Somewhat Famous"}}' \
    --return-consumed-capacity TOTAL \
    --endpoint-url http://localhost:8000 

aws dynamodb put-item \
    --table-name Music \
    --item '{ \
        "Artist": {"S": "Acme Band"}, \
        "SongTitle": {"S": "Happy Day"}, \
        "AlbumTitle": {"S": "Songs About Life"} }' \
    --return-consumed-capacity TOTAL \
    --endpoint-url http://localhost:8000 

REPONSE
============

{
    "ConsumedCapacity": {
        "TableName": "Music",
        "CapacityUnits": 1.0
    }
}
