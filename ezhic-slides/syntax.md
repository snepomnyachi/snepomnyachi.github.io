## Usage (sync. variant)

####Functor version  
```cpp
Any result = registry.schedule("label", std::plus(), 20, 22);
ASSERT(result->isEmpty() || result->get<int>() == 42);
```

####Block scope version
```cpp
E_START("label") //will create a scope anyway 
{
    int result = 20+22;
    ASSERT(result == 42);
}
E_END

```
