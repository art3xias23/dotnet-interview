When big data is shared across several nodes (servers with one or more databases),  
an update to one database may take time to reach the other replicas.  
Therefore, a choice must be made regarding **which consistency model to use**.  
This will affect **consistency**, **availability**, and **latency**.

##  Considerations

- **Consistency**
    
    - Strong consistency → All reads return the most recent write.
        
    - Eventual consistency → Temporary discrepancies are allowed between replicas.
        
- **Availability**
    
    - Strong consistency → Lower availability (must wait for sync)
        
    - Eventual consistency → Higher availability (writes can finish without waiting for replicas)
        
- **Latency**
    
    - Strong consistency → Higher latency (coordination among nodes needed)
        
    - Eventual consistency → Lower latency for writes (no need to wait for agreement)
        

##  Comparison Table

| Consistency Model | Availability | Latency |
| ----------------- | ------------ | ------- |
| **Strong**        | Low          | High    |
| **Eventual**      | High         | Low     |
##  Examples

- **Strong Consistency** → Stock Market data, where the latest data is critical.
    
- **Eventual Consistency** → YouTube view counts, where a slight delay is acceptable.