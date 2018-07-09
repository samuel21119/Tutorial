# 標準輸出輸入

## 輸出

如果一個程式，跑了半天，卻沒有輸出任何東西，是不是等於白跑了？

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!";
    return 0;
}
```

在以上程式，我們使用了 `cout << "Hello World!";`來輸出 "Hello World!"。

其中可以把 cout 想成是螢幕，然後我們順著 `<<` 的方向將 "Hello World"這串字丟到螢幕上面。

那如果輸出的時候需要換行，該怎麼辦呢？

很簡單，只要把`endl`這串東 西送上去就好，所以如果我要輸出：

> Hello
>
> World!

就可以寫成

```cpp
cout << "Hello" << endl << "World!";
```

### 輸出變數

```cpp
#include <iostream>
using namespace std;

int main() {
    int v1 = 100;
    int v2 = 9487;
    return 0;
}
```

如果要將整數形態變數的值輸出，則可以寫成

```cpp
int main() {
    int v1 = 100;
    int v2 = 9487;
    cout << v1 << endl << v2;
    return 0;
}
```

> **輸出結果：**
>
> 100
>
> 9487



當然，我們也可以輸出`float`、`double`、`char`

```cpp
int main() {
    float f = 123.456;
    double pi = 3.14159;
    char c = '*';
    cout << f << endl << pi << endl << c;
    return 0;
}
```

> 輸出結果：
>
> 123.456
>
> 3.14159
>
> \*

## 輸入

如果每次程式都沒有給予輸入，那每次出來相同的結果也顯得有點無趣，所以這裡會教大家如何輸入值到變數裡面

```cpp
#include <iostream>
using namespace std;

int main() {
    int i;
    cin >> i;
    cout << i;
    return 0;
}
```

我們使用了`cin >> i;`來輸入數字到i變數，接著再將輸入的值輸出出來

這裡可以把`cin`當作鍵盤，順著`>>`的方向把數字丟到i裡面

> 範例輸入：
>
> 1234

> 範例輸出：
>
> 1234

同理，也可以透過 `cin`來達成輸入浮點數、字元的功能

```cpp
int main() {
    int i;
    float f;
    char c;
    cin >> i >> f >> c;
    cout << i << endl << c << endl << f;
    return 0;
}
```



> 範例輸入：
>
> 1234
>
> 3.14159
>
> h

> 範例輸出：
>
> 1234
>
> h
>
> 3.14159



