# enum

```
public enum EnumTest {
    MON, TUE, WED, THU, FRI, SAT, SUN;
}
```

这段代码实际上调用了7次 Enum\(String name, int ordinal\)：

```java
new Enum<EnumTest>("MON",0);
new Enum<EnumTest>("TUE",1);
new Enum<EnumTest>("WED",2);
....
```



