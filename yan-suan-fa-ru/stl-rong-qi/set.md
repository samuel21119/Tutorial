# Set

Set是一個集合，所以set不會包含重複的元素，這就是和vector之間的差別。其中，裡面的元素會按照大小排序，如：{1, 2, 10}、{apple, banana, orange}。

## 使用方式

### 標頭檔

使用set標頭檔：

```cpp
#include <set>
```

### 宣告方法

與Stack一樣：

```cpp
set<int> a;
set<string> b; // 將採用字典順序方法排序
```

### 基本操作

| 函數名稱 | 說明 |
| --- | --- | --- | --- | --- | --- |
| insert\( 資料 \) | 將資料新增到set裡面 |
| erase\( 資料 \) | 將資料從set中移除 |
| begin\(\) | 回傳set一開始的迭代器\(iterator\) |
| end\(\) | 回傳set尾部的迭代器 |
| a.find\(資料\) | 群找資料，並回傳該資料的迭代器，若不存在則回傳end\(\) |

詳細說明可參照以下連結：

{% embed data="{\"url\":\"http://www.cplusplus.com/reference/set/set/\",\"type\":\"link\",\"title\":\"set - C++ Reference\",\"icon\":{\"type\":\"icon\",\"url\":\"http://www.cplusplus.com/favicon.ico\",\"aspectRatio\":0}}" %}

## 範例

### 程式碼

```cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    set<int> s;
    
    s.insert(-1);
    s.insert(3);
    s.insert(1);
    s.insert(5);
    s.insert(7);
    s.insert(9);
    
    if (s.find(0) != s.end()) {            //檢查0是否存在
        cout << "0 is in set!" << endl;
    }else {
        cout << "0 isn't in set!" << endl;
    }
    
    for (set<int>:iterator it = s.begin(); it != s.end(); it++) { //輸出set裡的資料
        cout << *it << ' ';
    }
    
    return 0;
}
```

> 範例輸出：
>
> 0 isn't in set!
>
> -1 1 3 5 7

### 範例說明

在第21行那可以看到一串很詭異的東西，這裡將作進一步的講解：

`set<int>::iterator`這裡是定義變數`it`的型態，其型態叫做：儲存int的set的迭代器。簡單來說，就是set的「指標」。

`it = s.begin()`將使it設為s一開始的迭代器，可以視為指到set第一元素的指標

`cout << *it << ' ';`這裡輸出set的元素，因為迭代器可以視為是指標，所以存取方式也是一樣，需要加上`*`才可以存取。

`it++`會令`it`指到下一個元素的位置，從第一個指到第二個，第二個指到的三個...以此類推

`it != s.end()`如果`it`到達尾部，也就是全部的元素均存取完畢，`it`會等於`s.end()`，所以當`it != s.end()`時，代表還有元素沒有存取到

