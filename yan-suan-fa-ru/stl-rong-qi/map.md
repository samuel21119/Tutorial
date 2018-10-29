# Map

在一個讀取一個陣列的時候，我們必須要透過索引值\(Index\)來讀取我們要的值，但是如果要用字串來當作索引值，或是索引值範圍很大，例如：0 ~ 2^63，就可以使用Map來達成目的。

## 使用方式

### 標頭檔

使用map標頭檔：

```cpp
#include <map>
```

### 宣告方法

這裡需給定兩個變數型態，第一個為index的型態，第二為儲存資料的型態：

```cpp
map<long long int, int> a;
map<string, int> b;
```

### 基本操作

使用方法非常簡單，直接當成陣列存取即可，裡面儲存的變數預設為0，例如：

```cpp
#include <iostream>
#include <map>
using namespace std;

int main() {
    string index;
    index = "123";
    map<string, int> m;
    m[index]++;
    cout << m[index];
    
    return 0;
}
```

輸出為1。

詳細說明可參照以下連結：

{% embed url="http://www.cplusplus.com/reference/map/map/" %}

## 範例

基本操作均使用陣列存取方式即可，以下會示範如何便利輸出，會使用到迭代器：

```cpp
#include <iostream>
#include <map>
using namespace std;

int main() {
    map<string, int> m;
    m["hello"] = 10;
    m["apple"] = 5;
    m["cpp"] = 11;
    for (map<string, int>::iterator it = m.begin();
        it != m.end(); it++) {
        cout << "Index: " << it->first << "   value: "
             << it->second << endl;
     }
     
     return 0;
 }
```

> 範例輸出：
>
> Index: apple value: 5
>
> Index: cpp value: 11
>
> Index: hello value: 10



