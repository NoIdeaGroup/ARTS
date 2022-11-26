## Algorithm
![算法](../../images/temp/sisyphus-2022-12-03-lc.png)
```java
class Solution {
    public List<Integer> findDisappearedNumbers(int[] nums) {

        ArrayList<Integer> ret = new ArrayList<>();
        int len = nums.length;

        for (int num : nums) {
            num = (num - 1) % len;
            nums[num] += len;
        }

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] <= len) {
                ret.add(i+1);
            }
        }
        return ret;
    }
}
```
> 利用下标
> * 当前数范围1~n, 所有出现过的数+len，遍历第二次如果数小于等于len，则该数未出现
> * 计算下标需要(n-1) % len
## Review


## Tip

### 甘特图
甘特图（Gantt Chart）是条状图的一种流行类型，**显示项目、进度**以及其他与时间相关的系统进展的内在关系随着时间进展的情况，
是由亨利·甘特 (Henry Laurence Gantt) 于1910年开发出。在项目管理中，甘特图显示项目的终端元素的开始和结束，概要元素或终端元素的依赖关系，
管理者可透过甘特图，监控项目当前各任务的进度。若想要同时显示多个不同的项目开始与结束的时间，就可以利用甘特图呈现，_监控项目当前各任务的进度_。

### shell for循环curl
需求，需要恢复数据，但是接口只支持输入单个id，将id通过awk分割后，通过脚本批量处理300个id。
```shell
cat ids.txt | while read line
do
  echo "$line"
  curl "http://your url?product-id=$line"
done
```

## Share


