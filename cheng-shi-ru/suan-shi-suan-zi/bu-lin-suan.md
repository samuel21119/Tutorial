---
description: 非零即為真。
---

# 布林運算

在前面 [變數－Bool 布林值](../ji-ben-fa/ji-chu-ru.md#bool-bu-lin-zhi) 時有提過：0代表False；1代表True。

而在這裡還要再補充一點，只要不是0，就是真，例如：

```cpp
bool b1 = 2;
bool b2 = -1;
cout << b1 << endl << b2 << endl;
```

> 範例輸出：
>
> 1
>
> 1

## 關係運算子

| 運算子 | 意思 | 範例 |
| --- | --- | --- | --- | --- | --- | --- |
| `>` | 大於 | `A > B` |
| `>=` | 大於等於 | `A >= B` |
| `<` | 小於 | `A < B` |
| `<=` | 小於等於 | `A <= B` |
| `==` | 等於 | `A == B` |
| `!=` | 不等於 | `A != B` |

### 來看Code吧

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 5;
    int c = 10;
    
    cout << (a > b) << endl;
    cout << (c < b) << endl;
    cout << (a != c) << endl;
    
    return 0;
}
```

> 範例輸出：
>
> 1
>
> 0
>
> 0

## 邏輯運算子

| 運算子 | 意思 | 範例 |
| --- | --- | --- | --- |
| `||` | 或\(OR\) | `A || B` |
| `&&` | 且\(AND\) | `A && B` |
| `!` | 非\(NOT\) | `!A` |

### 範例程式

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int b = 10;
    int c = 5;
    
    cout << ((a == b) || (a == c)) << endl;
    cout << !((a == b) || (a == c)) << endl;
    cout << ((a < b) && (a == c)) << endl;
    
    return 0;
}
```

> 範例輸出：
>
> 1
>
> 0
>
> 1



