# awesome
Awesome CET library

## basic example

```java
private alias CubeModelArray = CubeModel[];

public aweObject CubeCollectionModel {
    props(
        double size=1feet,
        CubeModelArray cubes = CubeModelArray()
    );
}

public aweObject CubeModel {
    props(
        bool on=false,
        point origin=point()
    );
    public aweObjectDomain(
        bool on=BoolSubSet()
    );
}

public class CubeProduct extends AweProduct {
    public AweModel<CubeModel> model;
    public box localBound() {
        box b(point(), 1, 1, 1);
        b.move(this.model.origin);
        return b;
    }
    public Primitive3D medium3D() {
        Box3D b(this.localBound());
        b.setMaterial(model.on ? plainBlueMaterial3D : plainWhiteMaterial3D);
        return b;
    }
}

private aweBinder<CubeModel, CubeProduct> Cube;
public class CubeSnapper extends AweMultiProductSnapper {
    public AweObject initRoot() {
        CubeCollectionModel collection();
        bool on = false;
        for(x in 0..2) {
            for(y in 0..2) {
                for(z in 0..2) {
                    collection.cubes << Cube(origin=(x,y,z), on=on);
                    on = !on;
                }
            }
        }
        return collection;
    }
}

{
    CubeSnapper().launch();
}
```
