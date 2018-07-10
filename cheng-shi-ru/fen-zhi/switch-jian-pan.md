# Switch條件判斷

`switch`只能比較特定變數是否為某一數值或字元，不能像上回的`if`是使用判斷式

直接看範例：

```cpp
#include <iostream>
using namespace std;

int main() {
    int a;
    cin >> a;
    
    if (a == 1) {
        cout << "a = 1";
    }else if (a == 2) {
        cout << "a = 2";
    }else {
        cout << "a != 1 && a != 2";
    }
    return 0;
}
```

可以將`if - else if - else`判斷式改成以下這樣：

```cpp
switch (a) {
    case 1:
        cout << "a = 1";
        break;
    case 2:
        cout << "a = 2";
        break;
    default:
        cout << "a != 1 && a != 2";
        break;
}
```

> 範例輸入1：
>
> 2
>
> 範例輸出1：
>
> a = 2

> 範例輸入2：
>
> -1
>
> 範例輸出2：
>
> a != 1 && a != 2

若`case`內都沒有相符的則會執行`default`內的內容，但是`default`本身並不一定要存在，這部分跟`if else`中，其實可以不要寫`else`是一樣的。

{% hint style="warning" %}
在`switch`裡面，每一個`case`結束時都要加上`break;`，要不然會一直往下執行：
{% endhint %}

```cpp
switch (a) {
    case 1:
        cout << "a = 1" << endl;
    case 2:
        cout << "a = 2" << endl;
    default:
        cout << "a != 1 && a != 2" << endl;
}
```

> 範例輸入1：
>
> 2
>
> 範例輸出1：
>
> a = 2
>
> a != 1 && a != 2

> 範例輸入2：
>
> 1
>
> 範例輸出2：
>
> a = 1
>
> a = 2
>
> a != 1 && a != 2

