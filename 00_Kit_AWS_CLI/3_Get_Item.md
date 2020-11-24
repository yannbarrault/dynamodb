aws dynamodb get-item --table-name Music --key '{"Artist": {  "S": "Acme Band"  },  "SongTitle": { "S": "Happy Day" }}' --endpoint-url http://localhost:8000

REPONSE
========
{
    "Item": {
        "Artist": {
            "S": "Acme Band"
        },
        "SongTitle": {
            "S": "Happy Day"
        },
        "AlbumTitle": {
            "S": "Songs About Life"
        }
    }
}
