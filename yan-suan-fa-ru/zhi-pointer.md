# 指標 \(Pointer\)

在[變數](../cheng-shi-ru/ji-ben-fa/ji-chu-ru.md)章節裡面有提過，變數會佔用到記憶體的儲存空間，所以每個變數會有不同的「記憶體地址\(位置\)」，如果我們有它的地址，就可以透過不同的方式存取它了！

如果要擷取該變數的記憶體位置，需使用&符號：

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    
    cout << "變數a的值: " << a << endl;
    cout << "變數a的記憶體位置: " << &a << endl;
    
    return 0;
}
```

> 範例輸出：
>
> 變數a的值: 5
>
> 變數a的記憶體位置: 0x7ffeee673978

其中上面的0x7ffeee673978是變數a的記憶體位置，**每次程式執行結果均不同**。

上述程式中，已經成功擷取變數的記憶體位置，那接下來我們要用到「指標」來將記憶體存起來：

```cpp
int a = 1;
char b = 'a';

int *pointer_a = &a;
/* 或是:
 * int *pointer_a;
 * pointer_a = &a;
 */
char *pointer_b = &b;
```

宣告方式為`type *名稱`，這裡的`type`代表這個指標要存的記憶體位置存的是何種型態的值。

由第7行可看出，pointer只是一種變數，儲存的不是int char等等，而是變數的記憶體位置。



如果要存取指標指向的變數，需使用`*`來操作：

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int *p = &a;
    /* 或是:
     * int *p;
     * p = &a;
     */
     
    cout << "變數a的值: " << a << endl;
    cout << "透過pointer讀取變數a的值: " << *p << endl << endl;
    
    a = 6;
    cout << "變數a的值(a = 6): " << a << endl;
    cout << "透過pointer讀取變數a的值: " << *p << endl << endl;
    
    *p = 7;
    cout << "變數a的值(*p = 7): " << a << endl;
    cout << "透過pointer讀取變數a的值: " << *p << endl;
    
    return 0;
}
```

> 範例輸出：
>
> 變數a的值: 5
>
> 透過pointer讀取變數a的值: 5
>
>
>
> 變數a的值\(a = 6\): 6
>
> 透過pointer讀取變數a的值: 6
>
>
>
> 變數a的值\(\*p = 7\): 7
>
> 透過pointer讀取變數a的值: 7

到目前為止，就是指標的簡單介紹。



以下會講解如何利用[函數](../cheng-shi-ru/han-dui-stack/han-function.md)和指標來達成兩數字互換

```cpp
#include <iostream>
using namespace std;

void swap(int a, int b) {
    int t = a;
    a = b;
    b = t;
}
int main() {
    int x, y;
    x = 5;
    y = 6;
    swap(x, y);
    cout << x << ' ' << y;
    return 0;
}
```

> 範例輸出：
>
> 5 6

在上述程式中，明明執行過swap函數了，但是x和y並沒有互換，原因是因為當呼叫swap\(x, y\)時，它只是傳x和y的「值」進去，也就是說swap裡面的x和main\(\)裡面的x是不同的變數，所以不管怎麼改都沒有用。

那我們可以利用指標的特性還達成swap的目的：

```cpp
#include <iostream>
using namespace std;

void swap(int *a, int *b) {
    int t = *a;
    *a = *b;
    *b = t;
}
int main() {
    int x, y;
    x = 5;
    y = 6;
    swap(&x, &y);
    cout << x << ' ' << y;
    return 0;
}
```

首先：13行呼叫swap的時候，是傳x, y的位置進去

接著看到第四行`int *a`將接收main裡面的x位置，所以swap裡面的`a = main函數x的記憶體位置`

接下來我們「更改指標指向的變數」，以間接存取變數的方法達到swap的目的。

