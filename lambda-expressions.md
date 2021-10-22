# Lambda Expression

### 模板： `(元素1, 元素2) -> 元素1底下某个小数据a - 元素2底下某个小数据a;`

**意思是：**`元素1`和`元素2`是我们要进行排序的数据，排序的顺序是根据`元素底下某个小数据a`来决定的，按照`元素底下某个小数据a`把元素按照**从小到大顺序升序排列**ascending order。

简便记忆：前面的减去后面的就是**升序**，后面的减前面的就是降序。



例如：

●`int[][] intervals;`\
&#x20;  `Arrays.sort(intervals, (int[] a, int[] b) -> a[0] - b[0]);`\
意思是：根据intervals这个二维数组里面小数组的第一个元素，把小数组从小到大排列。



●`Node node;`\
&#x20; `PriorityQueue<Node> pq = new PriorityQueue<>((node1, node2) -> node1.val - node2.val);`\
意思是：根据ListNode的val值，构建min Heap，它的Heap堆顶会存放val值最小的node。



●`String[] words;`\
&#x20; `Arrays.sort(words, (a,b) -> a.length()-b.length());` // Sort the words based on their lengths\
意思是：根据words数组里每个单词的长度，把单词从小到大排序。

