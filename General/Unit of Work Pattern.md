**Benefits**

- All actions in a unit are committed together or rolled back.
    
- Reduces DB calls.
    

**Example Pattern**

```csharp

`using(var context = new MyDbContext()) 
	{     // Update + save 
	   context.Customers.Update(customer);    context.SaveChanges();     // Add + save    
	   context.Orders.Add(order);    context.SaveChanges(); 
     }`