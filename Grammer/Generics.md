## Generics
> Java Generics were introduced in JDK 5.0 with the aim of reducing bugs and adding an extra layer of abstraction over types.


ex)
```
//array를 list로 바꾸어 주는 코드, 이 때 static 뒤의 <T>는 void를 리턴하더라도, 어느 때 더라도 필수로 들어간다.
	static <T> void fromArrayToList(T[] a) {   
	    //return Arrays.stream(a).collect(Collectors.toList());
	}
```

