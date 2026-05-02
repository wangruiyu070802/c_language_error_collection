# 🎉C语言错题集——TylerRay📋📈

>个人整理的 C 语言常见错误题目，用于快速复习


## 分类索引

### 指针

1.字符移位加密（字符串处理）

![题目预览](assets/string/字符移位加密（字符串处理）-001.png)

[查看答案](assets/string/answer-001.png)

## 排序算法

| 算法 | 文件 | 描述 |
|------|------|------|
| 鸡尾酒排序 (Cocktail Sort) | [cocktail_sort.c](algorithms/sorting/cocktail_sort.c) | 双向冒泡排序，每轮遍历从两端同时进行

```c
void cocktailSort(int arr[], int n) {
    int swapped = 1;
    int start = 0;
    int end = n - 1;

    while (swapped) {
        swapped = 0;
        for (int i = start; i < end; ++i) {
            if (arr[i] > arr[i + 1]) {
                int temp = arr[i];
                arr[i] = arr[i + 1];
                arr[i + 1] = temp;
                swapped = 1;
            }
        }
        if (!swapped) break;
        end--;

        swapped = 0;
        for (int i = end - 1; i >= start; --i) {
            if (arr[i] > arr[i + 1]) {
                int temp = arr[i];
                arr[i] = arr[i + 1];
                arr[i + 1] = temp;
                swapped = 1;
            }
        }
        start++;
    }
}
```
