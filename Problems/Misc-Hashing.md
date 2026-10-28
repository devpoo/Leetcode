```java
class Solution {
    public int majorityElement(int[] nums) {
        HashMap<Integer, Integer> count = new HashMap<>();

        for (int n : nums) {
            count.put(n, count.getOrDefault(n, 0) + 1);
        }

        for(Map.Entry<Integer, Integer> entry : count.entrySet()) {
            if(entry.getValue() > nums.length/2) return entry.getKey();
        }

        return 1;
    }
}
```

