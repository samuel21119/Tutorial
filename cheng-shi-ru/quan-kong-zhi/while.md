# While迴圈

先看用法：

```cpp
while ( statement ) {
    ...
}
```

其中 `()`裡面的`statement`是放置判斷條件的地方，進入`while`時檢查一次，執行到`while`底部時也會檢查一次，如果在檢查的時候條件不成立，則跳出迴圈。

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

## 持續輸入

​先前提到的[練習題目a002](../suan-shi-suan-zi/suan-suan.md#mu)，因為題目並未說明總共會有幾筆輸入，所以我們需要用到while迴圈來達成持續輸入的目的：

```cpp
int in;
while (cin >> in) {
    ...
}
```

以上寫法，`while`迴圈的判斷條件放入的是`cin >> in`，它會在程式每重複執行的時候輸入數字到`in`變數裡面，如果遇到測試資料的底部，`cin`會讀到EOF\(End Of File\)，並且回傳0給`while`，這時候就會`while`迴圈判定要跳出迴圈。



