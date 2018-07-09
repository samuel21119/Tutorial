# While迴圈

先看範例：

```cpp
while ( statement ) {
    ...
}
```

其中 `()`裡面的`statement`是放置判斷式的地方，進入`while`時檢查一次，執行到`while`底部時也會檢查一次，如果再檢查的時候條件不成立，則跳出迴圈。

所以如果我要使用者持續輸入一個數字直到該數字大於100，可以寫成下面這樣：

```cpp
#include <iostream>
using namespace std;

int main() {
    int input = 0;
    
    while (input <= 100) {
        cin >> input;
    }
    cout << input;
    
    return 0;
}
```

> 範例輸入：
>
> 1
>
> 2
>
> 87
>
> 100
>
> 101
>
> 範例輸出：
>
> 101

