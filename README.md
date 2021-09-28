# kubernetes-mongodb
Two MongoDB instances replicating between each other.

```mermaid
sequenceDiagram

%% Download mermaid diagram extension to view the sequence below.
%% Try it on https://mermaid-js.github.io/mermaid-live-editor/edit

participant Rust
participant MongoDB A
participant MongoDB B

Rust->>MongoDB A: 1 Upsert record
activate MongoDB A
MongoDB A-->>Rust: 2 Acknowledge upsertion
MongoDB A->>MongoDB B: 3 Replicate
activate MongoDB B
MongoDB B-->>MongoDB A: 4 Acknowledge replication
deactivate MongoDB B
deactivate MongoDB A
```
