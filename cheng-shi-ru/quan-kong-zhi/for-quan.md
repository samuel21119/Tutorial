# For迴圈

先看用法

```cpp
for ( (A)一開始要做的 ; (B)判斷條件 ; (C)每到迴圈底部，就執行此動作 ) {
    ...
}
```

`for`迴圈比較複雜一點，相較`while`，`for`多了 \(A\) \(C\)部分，所以如果`for`這樣寫：

```cpp
for ( ; 判斷條件; ) {
    ...
}
```

其實就等於`while`！

`for`的流程是這樣的：

1. 先做\(A\)
2. 檢查\(B\)，如果為非，則跳出
3. 執行迴圈裡面的程式
4. 執行C部分
5. 再回到第2點

所以`for`也可以這樣改寫成`while`，範例在下面：

```cpp
(A)
while (B) {
    ...
    (C)
} 
```

`for`迴圈的具體示範：

> 題目：
>
> 給一自然數n，請依序輸出
>
> 1 2 3 4 ... n - 1 n

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    for (int i = 1; i <= n; i++) {
        cout << i << ' ';
    }
    
    return 0;
}
```

```cpp
//for改編成while版本
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    int i = 1;
    while (i <= n) {
        cout << i << ' ';
        i++;
    }
    
    return 0;
}
```

> 範例輸入1：
>
> 10
>
> 範例輸出1：
>
> 1 2 3 4 5 6 7 8 9 10

> 範例輸入2：
>
> 4
>
> 範例輸出1：
>
> 1 2 3 4

