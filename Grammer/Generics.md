## Generics
> Java Generics were introduced in JDK 5.0 with the aim of reducing bugs and adding an extra layer of abstraction over types.


ex)
```java
//array를 list로 바꾸어 주는 코드, 이 때 static 뒤의 <T>는 void를 리턴하더라도, 어느 때 더라도 필수로 들어간다.
	static <T> void fromArrayToList(T[] a) {   
	    //return Arrays.stream(a).collect(Collectors.toList());
	}
```
- Generics는 Primitive 자료형 (ex>int)에 적용이 불가능하다. 
- 왜? generics는 compile-time에서 이루어지는 것이기 때문이다. 이것은 type parameter가 삭제되고 모든 generic 타입이 Object type으로 구현된다는 것을 의미한다. 
- 그러므로 type 파라미터는 모두 Object로 변환이 가능해야 한다. Primitive type은 Object를 extend(상속)하지 않기 때문에 primitive type을 파라미터로 사용할 수 없다. 
- 하지만, Java는 primitve 형을 위해 boxed type(autoboxing, unboxing)을 제공하기 때문에 다음이 가능하다.

```java
Integer a = 17;
int b = a;
So, if we want to create a list which can hold integers, we can use the wrapper:

List<Integer> list = new ArrayList<>();
list.add(17);
int first = list.get(0);
The compiled code will be the equivalent of:

List list = new ArrayList<>();
list.add(Integer.valueOf(17));
int first = ((Integer) list.get(0)).intValue();
```

### references
- https://www.baeldung.com/java-generics
