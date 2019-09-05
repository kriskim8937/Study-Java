## Container

- Container
    - These containers have dyanamic size
    - Collection
        - List
            - ArrayList
                - remove(obj)
            - LinkedList
        - Set
            - HashSet
                ```
                No order
                ```
            - TreeSet
                ```
                Ordered(Ascent) set
                ```
            - LinkedHashSet
        - Queue
        - stack
            ```
            Why should I use Deque over Stack?
             https://stackoverflow.com/questions/12524826/why-should-i-use-deque-over-stack

            ```
                       
    - Map
      - HashMap
          - No order
      - TreeMap
          - Map is Ordered(Ascent) by key
      - LinkedHashMap
## Hierarchy of Collections
https://en.wikiversity.org/wiki/Java_Collections_Overview

## Comparison
| Tables        | Notes           | Retrieval  |
|:-------------:|:-------------:|:-----:|
| List     | Allows you to put elements in a specific order. Each element is associated with an index. | Through iterator, or Random access by numerical index |
| Set     | 	Prohibits duplicate elements. Easy test for membership. You can't order the elements.      |   Through iterator |
| Queue | Only the "head" (next out) is available.     |   Peeking or polling, or Through iterator |
| PriorityQueue | 	High priority elements get to the head first.      |   	Peeking or polling |
| Deque | 	A "double-ended queue": insert and remove at both ends.      |    Peeking or polling, or Through iterator |
| Map | Maps keys to values      |   Lookup by key object , or Through keySet, entrySet, values "views" |
