# Stack

如先前所提到的[堆疊\(Stack\)](../../cheng-shi-ru/han-dui-stack/dui-stack.md)概念，這裡將介紹stack的實際使用方式。

## 使用方式

### 標頭檔

使用stack需要include特殊標頭檔，名為stack：

```cpp
#include <stack>
```

### 宣告

如同一般變數，stack也是需要宣告的，用法如下：

`stack<儲存變數型態>  Stack名稱;` 

所以我們可以這樣宣告：

```cpp
stack<int> stack_int;               // 儲存int形態的stack
stack<char> stack_char;             // 儲存char型態
stack<string> stack_string;         // 儲存string型態
stack< stack<int> > stack_stack_int;// 當然也可以在stack裡面儲存stack;
```

### 基本操作

為了操作我們所宣告的stack，我們需要用到其內建的函數。以下為基本的操作\(函數\)：

| 函數名稱 | 說明 |
| --- | --- | --- | --- | --- | --- |
| push\( 資料 \) | 將資料放進Stack頂端 |
| top\(\) | 回傳最上方的資料 |
| pop\(\) | 移除最上方的資料 |
| empty\(\) | 回傳stack是否為空1: 空0: 有資料 |
| size\(\) | 回傳stack目前有幾筆資料 |

基本操作用法可參照下方的[範例](stack.md#li)，若有不懂之處，可以到以下連結查詢詳細資訊

{% embed data="{\"url\":\"http://www.cplusplus.com/reference/stack/stack/\",\"type\":\"link\",\"title\":\"stack - C++ Reference\",\"icon\":{\"type\":\"icon\",\"url\":\"http://www.cplusplus.com/favicon.ico\",\"aspectRatio\":0}}" %}

## 範例

> 第一行有一個n \(n &lt;= 100000\)
>
> 接下來有n行
>
> 每一行一開始有一個數字，代表哪一種操作
>
> 如果數字為1，代表刪除操作
>
> 如果數字為2，請輸出當前stack的頂端元素
>
> 如果數字為3，請在讀入一個整數丟進堆疊

[Zerojudge b923](https://zerojudge.tw/ShowProblem?problemid=b923)

這裡會以程式碼來說明使用方式：

```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    int n;
    int cmd;
    cin >> n;     //輸入n
    stack<int> MyStack; //宣告stack資料結構
    
    while (n--) { //執行n次，等同於 for(int i = 0; i < n; i++)，請自行思考為何會相等
        cin >> cmd;
        switch (cmd) {
            case 1:
                MyStack.pop();                 // 將最上面的數字刪除
                break;
            case 2:
                cout << MyStack.top() << endl; // MyStack.top()將回傳最上方的數字
                break;
            case 3:
                cin >> cmd;
                MyStack.push(cmd);             // 將「cmd」放到Stack的最上層
        }
    }
    return 0;
}
```

> 範例輸入：
>
> 5
>
> 3 10
>
> 3 15
>
> 2
>
> 1
>
> 2

> 範例輸出：
>
> 15
>
> 10

