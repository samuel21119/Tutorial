# Queue

Queue，中文為「佇列」，就像是排隊買東西，只能從後面排，然後從頭出來。

![](../../.gitbook/assets/image%20%287%29.png)

## 使用方式

### 標頭檔

使用queue標頭檔：

```cpp
#include <queue>
```

### 宣告方法

與Stack一樣：

```cpp
queue<int> queue_int;
queue<string> queue_string;
```

### 基本操作

| 函數名稱 | 說明 |
| --- | --- | --- | --- | --- | --- |
| push\( 資料 \) | 將資料放進Queue尾部 |
| front\(\) | 回傳最前方的資料 |
| pop\(\) | 移除最前方的資料 |
| empty\(\) | 回傳queue是否為空1: 空0: 有資料 |
| size\(\) | 回傳queue目前有幾筆資料 |

## 範例

```cpp
#include <iostream>
#include <queue>
using namespace std;

int main() {
    queue<int> que;
    
    que.push(1);
    que.push(2);
    
    cout << que.front() << endl;
    
    que.push(3);
    
    que.pop();
    
    cout << que.front() << endl;
    cout << que.front() << endl;
    
    que.pop();
    
    cout << que.front() << endl;
    
    return 0;
}
```

> 範例輸出：
>
> 1
>
> 2
>
> 2
>
> 3



