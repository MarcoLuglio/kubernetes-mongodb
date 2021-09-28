# kubernetes-mongodb
Two MongoDB instances replicating between each other.

```mermaid
sequenceDiagram

%% Download mermaid diagram extension to view the sequence below.

participant Rust
participant MongoDBA
participant MongoDBB

Rust->>MongoDBA: Add record
MongoDBA->>MongoDBB: 1 Replicate
activate MongoDBB
MongoDBB-->>MongoDBA: 2 Replicated
deactivate MongoDBB
```
