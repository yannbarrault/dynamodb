## Visualiseur de données

A l'aide du [tutorial AWS](https://docs.aws.amazon.com/fr_fr/amazondynamodb/latest/developerguide/workbench.Visualizer.AddData.html), chargez [ce modèle de données](https://github.com/aws-samples/nosql-workbench-for-amazon-dynamodb-new-model) et répondez aux questions suivantes

Quel est le nom de la table ?
Quelle est la clé de partition ?
Y-a-t-il une clé de tri ? Si oui laquelle ?
Y-a-t-il des indexes GSI/LSI ?

### Opérations

Chargez l'exemple concernant les remontées mécaniques (code/Ski Resort Data Model.json) et répondez aux questions suivantes:

En utilisant une facet du modèle, répondez à la question suivante: quel(s) est(sont) les remontées mécaniques dont la durée de remontée est la plus longue ?
    PK: Lift = Lift 3
    SK: Metadata = Static Data
    Attribute = LiftTime
    Value: 7:30

Trouvez le nombre total de passagers uniques qui ont empruntés l'une des remontées le 03/01/20
    Operation Builder
    Operation: SCAN
    Metadata: 03/01/20
    Projection attributes: TotalUniqueLiftRiders  & Lift
    RUN
    Sort on 'TotalUniqueLiftRiders'
    Answer: Lift 3 had 5500 riders on 03/01/20

### Resources

https://docs.aws.amazon.com/fr_fr/amazondynamodb/latest/developerguide/workbench.html