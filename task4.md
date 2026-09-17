# 1.

The design pattern is Composite because we are building a tree structure with the objects: Product is the composite node and DVD and Book are the leafs. This lets clients treat individual objects and compositions of objects uniformly through the same interface.

# 2.

```
@Override
public int price(){
    int total = 0;
    for (Product p : products) {
        total += p.price();
    }
    return total;

}
```

This gets the total price of the shelf and we are allowed to use an enhanced for loop and polymorphically convert the products due to the Composite design pattern.
