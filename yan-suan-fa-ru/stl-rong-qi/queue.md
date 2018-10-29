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

<table>
  <thead>
    <tr>
      <th style="text-align:left">函數名稱</th>
      <th style="text-align:left">說明</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">push( 資料 )</td>
      <td style="text-align:left">將資料放進Queue尾部</td>
    </tr>
    <tr>
      <td style="text-align:left">front()</td>
      <td style="text-align:left">回傳最前方的資料</td>
    </tr>
    <tr>
      <td style="text-align:left">pop()</td>
      <td style="text-align:left">移除最前方的資料</td>
    </tr>
    <tr>
      <td style="text-align:left">empty()</td>
      <td style="text-align:left">
        <p>回傳queue是否為空</p>
        <p>1: 空</p>
        <p>0: 有資料</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">size()</td>
      <td style="text-align:left">回傳queue目前有幾筆資料</td>
    </tr>
  </tbody>
</table>詳細說明可參照以下連結：

{% embed url="http://www.cplusplus.com/reference/queue/queue/" %}

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



