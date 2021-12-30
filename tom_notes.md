# NoSQL

    Name typically explained as "Not Only SQL" or "Non-relational"

## Relational Databases:
- Great with data consistency
- Hard to scale
- Resource intensive

Basically, at some point it won't be able to handle the load, can scale vertically but not horizontally.

## NoSQL Databases
- Can scale vertically and horizontally.
    - Vertically would be like adding space by adding stories to an existing building.
    - Horizontally can be thought of as building new buildings.
- Do away with relationships
- **Key/Value** stores, basically. Every item stands on it's own.
- **Partitions** are different servers (*horizontal*).
- Primary Key is converted to *Hash* value within the *keyspace*.
    - **Keyspace** ->  
        - Each partition (server) is assigned a range within the keyspace range 
        - How it knows where to store the data, and where to find the data.
- Can only be retrieved by the primary key.
- Schema-less
- Partitions are mirrored to other servers to prevent loss from hardware failure
    - May cause data to not be immediately returned.
    - *Eventually consistent*, it will be returned after milliseconds.

## Who's using them?

- Cloud providers
    - For scalability
    - DynamoDB, BigTable, CosmosDB
        - ***Prime Day 2019*** -> Amazon's NoSQL database peaked at 45 million requests per second.
        - ***Apple*** -> 75,000+ servers (largest known) NoSQL database.
- Self-hosted
    - Cassandra, Scylla, CouchDB, MongoDB

