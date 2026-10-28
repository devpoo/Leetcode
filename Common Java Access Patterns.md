### Arrays (`int[]`)

| Operation     | Syntax                              | Notes                               |
| ------------- | ----------------------------------- | ----------------------------------- |
| Length        | `arr.length`                        | Property, no parentheses            |
| Sort          | `Arrays.sort(arr)`                  | O(n log n)                          |
| Sort range    | `Arrays.sort(arr, from, to)`        | `to` is exclusive                   |
| Fill          | `Arrays.fill(arr, val)`             | Useful for DP init                  |
| Copy          | `Arrays.copyOf(arr, newLen)`        |                                     |
| Copy range    | `Arrays.copyOfRange(arr, from, to)` | `to` is exclusive                   |
| Print         | `Arrays.toString(arr)`              | 1D arrays                           |
| Equals        | `Arrays.equals(a, b)`               |                                     |
| Binary search | `Arrays.binarySearch(arr, key)`     | Array must be sorted                |
| To list       | `Arrays.asList(1, 2, 3)`            | Works with `Integer[]`, not `int[]` |
| Stream sum    | `Arrays.stream(arr).sum()`          | Also `.max()`, `.min()`             |

### List / ArrayList

| Operation       | Syntax                                        | Notes                                  |
| --------------- | --------------------------------------------- | -------------------------------------- |
| Size            | `list.size()`                                 |                                        |
| Get             | `list.get(i)`                                 |                                        |
| Set             | `list.set(i, val)`                            | Replaces the element at index i        |
| Add             | `list.add(val)`                               | Appends to the end                     |
| Add at index    | `list.add(i, val)`                            | Shifts the rest, O(n)                  |
| Remove by index | `list.remove(i)`                              | `int` argument means index             |
| Remove by value | `list.remove(Integer.valueOf(x))`             | Must box, or it is treated as an index |
| Contains        | `list.contains(x)`                            | O(n)                                   |
| Index of        | `list.indexOf(x)`                             | Returns -1 if not found                |
| Is empty        | `list.isEmpty()`                              |                                        |
| Clear           | `list.clear()`                                |                                        |
| Sublist         | `list.subList(from, to)`                      | View, `to` is exclusive                |
| Sort            | `list.sort(null)` or `Collections.sort(list)` |                                        |
| Copy            | `new ArrayList<>(list)`                       |                                        |

### String

|Operation|Syntax|Notes|
|---|---|---|
|Length|`s.length()`|With parentheses|
|Char at|`s.charAt(i)`||
|Substring|`s.substring(from)` / `s.substring(from, to)`|`to` is exclusive|
|To char array|`s.toCharArray()`|Sort the chars for anagram checks|
|Char array to String|`new String(chars)` or `String.valueOf(chars)`||
|Equals|`s.equals(t)`|Never use `==`|
|Compare|`s.compareTo(t)`|Lexicographic|
|Index of|`s.indexOf(ch)` / `s.indexOf(str)`|Returns -1 if not found|
|Last index of|`s.lastIndexOf(ch)`||
|Contains|`s.contains("ab")`||
|Starts / ends with|`s.startsWith(p)` / `s.endsWith(p)`||
|Split|`s.split(" ")`|Takes a regex|
|Trim|`s.trim()`||
|Case|`s.toLowerCase()` / `s.toUpperCase()`||
|Replace|`s.replace("a", "b")`||
|Is empty|`s.isEmpty()`||
|Join|`String.join(",", list)`||
|Int to String|`String.valueOf(n)` or `Integer.toString(n)`||
|String to int|`Integer.parseInt(s)`||