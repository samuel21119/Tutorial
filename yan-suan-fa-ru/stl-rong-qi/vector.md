# Vector

Vector類似一般常見的陣列\(Array\)，但是陣列在宣告的時候就需要給定長度，但是如果宣告的時候不清楚之後會用到多少個，這時候vector就派上用場了！

## 使用方式

### 標頭檔

使用vector標頭檔：

```cpp
#include <vector>
```

### 宣告方法

與Stack一樣：

```cpp
vector<int> vector_int;
vector<string> vector_string;
vector< vector<int> > vector_2D; // vector裡面再存一個vector，達到2D陣列的效果
```

### 基本操作

| 函數名稱 | 說明 |
| :--- | :--- |
| push\_back\( 資料 \) | 將資料新增到Vector尾部 |
| \[ 元素位置 \] | 讀寫「元素位置」的資料，可視為array的操作方法 |
| size\(\) | 回傳vector目前有幾筆資料 |

詳細說明可參照以下連結：

{% embed data="{\"url\":\"http://www.cplusplus.com/reference/vector/vector/\",\"type\":\"link\",\"title\":\"vector - C++ Reference\",\"icon\":{\"type\":\"icon\",\"url\":\"http://www.cplusplus.com/favicon.ico\",\"aspectRatio\":0}}" %}

## 範例

```cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec;
    vec.push_back(5);
    vec.push_back(4);
    vec.push_back(3);
    vec.push_back(2);
    vec.push_back(1);
    
    cout << vec.size() << endl;
    for (int i = 0; i < vec.size(); i++) {
        cout << vec[i] << ' ';
    }
    vec[1] = -1;
    for (int i = 0; i < vec.size(); i++) {
        cout << vec[i] << ' ';
    }
    
    return 0;
}
```

> 範例輸出：
>
> 5
>
> 5 4 3 2 1
>
> 5 -1 3 2 1



