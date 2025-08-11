**Garbage Collection (GC)**

- Automatic managed memory cleanup.
    
- Cannot handle unmanaged resources (file handles, sockets, native memory).
    
- Uses object generations for efficiency.
    

**IDisposable**

- Allows deterministic cleanup of unmanaged resources.
    
- `using` statement ensures prompt disposal.