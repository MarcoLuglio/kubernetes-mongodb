# kubernetes-mongodb
Two MongoDB instances replicating between each other.



```mermaid
sequenceDiagram
participant MongoDBA
participant MongoDBB
MongoDBA->>John: Hello John, how are you?
loop Healthcheck
	John->>John: Fight against hypochondria
end
Note right of John: Rational thoughts <br/>prevail!
John-->>MongoDBA: Great!
John->>MongoDBB: How about you?
MongoDBB-->>John: Jolly good!
```