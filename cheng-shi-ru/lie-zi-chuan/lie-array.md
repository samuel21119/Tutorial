# 陣列\(Array\)

## 一維陣列

陣列將同一型態同一作用的變數排在一起，宣告時與一般的變數不同，請見以下範例：

```cpp
#include <iostream>
using namespace std;

int main() {
    int array[4];
    
    array[0] = 1;
    array[1] = 10;
    array[2] = 12;
    array[3] = 5;
    
    for (int i = 0; i < 4; i++) {
        cout << array[i] << endl;
    }
    
    return 0;
}
```

> 範例輸出：
>
> 1
>
> 10
>
> 12
>
> 5

可以很清楚的看到，陣列在宣告的時候，變數名稱後面需加上`[n]`，其中n為陣列的長度。

之後在存取的時候，不能只寫 `array = 0;` ，因為陣列是一長串的變數，只是他們的名字都相同，這時候編譯器會不知道我們到底要讀寫哪一個變數，所以在讀寫的時候，必須要加上它們各自的編號。

1號叫做 `array[0]`

2號叫做 `array[1]`

... 以此類推。這裡必需要注意的是，陣列是從「0」開始存取，不是從「1」開始，所以如果我宣告長度為10的陣列 `int a[10];`，我只能從`a[0]`存取到`a[9]`，如果寫成`a[10]、a[-1]`，則會造成記憶體讀取錯誤，這時候我們就會稱作RE\(Runtime Error\)。

### 範例程式

> 題目：
>
> 給定n，接著有n個數字，請用陣列將數字存起來再輸出。

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    int array[n];
    for (int i = 0; i < n; i++) {
        cin >> array[n];
    }
    for (int i = 0; i < n; i++) {
        cout << array[n] << endl;
    }
    
    return 0;
}
```

> 範例輸入：
>
> 5
>
> 1 7 3 4 5

> 範例輸出：
>
> 1
>
> 7
>
> 3
>
> 4
>
> 5

## 多維陣列

上面那小節已經介紹了最基本的陣列了，其會被稱作一維陣列是因為只有一組`[]`。接著將介紹二維陣列：

`int array_2D[2][2];`

如果要存取二為陣列，則兩組`[]`都要填入0~n-1的數字

### 範例程式

> 題目：
>
> 給定n，接著有n × n的矩陣，請用矩陣儲存並輸出

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    
    int array[n][n];
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            cin >> array[i][j];
        }
    }
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            cout << array[i][j];
        }
    }
    
    return 0;
}
```

除了二維陣列，還有三、四...等多維陣列，其差異就只在於`[]`的數目。



Tip: 通常會使用巢狀`for`迴圈來輸入多維陣列

