# 迴圈控制指令

`continue`跟`break`在迴圈裡面非常的好用，可以處理很多煩人的情況，以下會一一介紹

## Continue

如果在一個迴圈中，執行到了一半，而這時候我要重新到迴圈開頭執行，就可以使用`continue`這個指令：

```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 1; i <= 5; i++) {
        if (i == 3)
            continue;
        cout << i << endl;
    }
    
    return 0;
}
```

> 範例輸出：
>
> 1
>
> 2
>
> 4
>
> 5

**解析：**

在`for`迴圈裡面，我加了一個`if`，判斷當`i == 3`時，我要從頭來執行，以便跳過輸出數字3。

這裡要注意的是，`continue`不只會跳回迴圈開頭，如果是`for`迴圈，它會先執行上一章寫到的\(C\)步驟，在上面的程式就是**`i++`。**且無論是`while`還是`for`，接下來都會先判斷\(B\)部分，就是判斷條件，如果條件成立，才會回到迴圈開頭。

## Break

這裡提到的`break`，其實在 [Switch條件判斷](../fen-zhi/switch-jian-pan.md) 就遇過了，運作方式很簡單：

遇到`break`，就跳出。但是只會跳出當層迴圈。例如：

```cpp
for (int i = 1; i < 4; i++) {     //甲迴圈
    for (int j = 1; j < 4; j++) { //乙迴圈
        if (i == 2) {
            break;
        }
        cout << i << ' ' << j << endl;
    }
}
```

當`i == 2 && j == 5`的時候，break只會跳出乙迴圈，不會影響到甲。

> 範例輸出：
>
> 1 1
>
> 1 2
>
> 1 3
>
> 3 1
>
> 3 2
>
> 3 3



