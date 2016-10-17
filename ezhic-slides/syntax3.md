## Named Bundles

```cpp
registry.addBundle("b1")
            .setHaven(...)
            .setValidator(...)
            .addBreaker(...)
            .addAcceptor(Logger(std::cout))
            ...

registry.setBundle("label", "b1");
Any result = registry.add("label", std::plus(), 20, 22);
```