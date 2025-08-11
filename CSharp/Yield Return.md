- Allows deferred, on-demand value generation.
    
- Saves memory for large collections.
    
- Logic runs only when enumerated.

```csharp
IEnumerable<int> GetEvenNumbers(int max) { for (int i=0; i<=max; i++) if (i % 2 == 0) yield return i; }
```