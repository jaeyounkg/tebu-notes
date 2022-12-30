-   ジェネリック・インターフェースを実装するクラスがジェネリック・クラスである必要はない
-   ラムダ式
	-   ThreeIntsToInt f = (int n, int m, int p) -> { return n + m + p; }
	-   型推論が行われる

```java
public interface Comparable<T> {  
    int compareTo(T o);  
}  
public interface BinarySearchTree<Elm extends Comparable<Elm>> {  
    ...  
}  
public class Leaf<Elm extends Comparable<Elm>> implements BinarySearchTree<Elm> {  
    ...  
}  
public class Branch<Elm extends Comparable<Elm>> implements BinarySearchTree<Elm> {  
    ...  
}
```