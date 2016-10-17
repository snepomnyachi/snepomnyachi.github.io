## Configuration

```cpp
string label = "plus";

registry.setValidator(label, NonNegative<int>());
registry.setHaven    (label, FixedHaven<int>(42));
registry.addBreaker  (label, ManyExceptions(3,5,true)); 

Any result = registry.add(label, std::plus(), 20, 22);
ASSERT(result->get<int>() == 42);
```
