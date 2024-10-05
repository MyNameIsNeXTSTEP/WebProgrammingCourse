Simply put the **Data structure** is the concrete form of data being composed with a specified rules.
Structure - means that it's being predefined and use in common of how the data is stored, accessed, changed, interconnected.

Common data structures:

1. **Single linked list**
    A structure where each item, starting from the first one, has sort of a pointer to the next one.
    
2. **Double linked list**
   A structure similar to a single linked list, but where each item has pointers to both sides.
   Also there can be two variations, the final one where the first item has only pointer for the next item, the last item has a poniter only to the previous items, and the circular one where the first item also has a pointer to the next item, but the last item has a forward pointer to the first item making the whole data structure circular access.
   
3. **Binary tree**
   A structure defined as a tree of nodes with two available branches to have for each node. So there's a root node, after which every child node may have 0 child nodes, or 1 node, or 2 nodes respectively.
   
4. **Indexed collections (Array)**
   A group of structures where the access to a certain data item is done by providing a special address (index) of that item in the structure.
   For example `SomeArray[1]` will return an item in a `SomeArray` array with index `1`
   
5. **Keyed collections (Map, Set, Record**)
   A group of structures where the form of stored data uses keys and values. The key is the access point to the values associated with it.
   **Map** or **Record** - is a straight structure to store data like so.
   A **Set** on the other hand - is also the same structure but with one important difference, it stores only unique values.
   
7. **Object**
   A more high-level data structure, that represents not only the data, but also some behaviour *(on a computer level also considered some datra structure)*. The object is similar to a keyed collection but with some functionality to it, like methods - functions connected to an object with specified and granted access to it's own state (internal stored data) or to given (parameters)
   
8. **Graph**
   A structure like a web of nodes where some of those are connected to others with edges.
   
9. Data-interchange format (like JSON in JavaScript)

---

For the JavaScript you can find usefull information [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)
