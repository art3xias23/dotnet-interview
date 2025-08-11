**Singleton**

- Single instance for app lifetime.
    
- Use cases: config objects, logging, DB pools, caching.
    

**Scoped**

- Instance per request.
    
- Use cases: EF DbContext, session tracking.
    

**Transient**

- Created each time requested.
    
- Use cases: mappers, validators.