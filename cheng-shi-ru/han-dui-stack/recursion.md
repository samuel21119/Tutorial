# 遞迴 \(Recursion\)

遞迴是在函數中呼叫自己的函數，而呼叫者本身會被放進Stack裡面，直到被呼叫者執行完畢，才會繼續執行呼叫者的剩餘程式。

在本章節，由於遞迴較難理解，所以本篇主要以題目來說明，需要花較多時間，請懷著耐心看完本篇。

## 1 + 2 + ... + n

> 題目：
>
> 給定一自然數n，請輸出1 + 2 + ... + n的總和

解題思路：

這題可以利用`for`迴圈跑，也可以利用高斯梯形公式直接算出答案，但是這邊要介紹遞迴的寫法：

```cpp
#include <iostream>
using namespace std;

int sum(int i) {
    if (i < 1)              //如果i不是自然數，則離開函數
        return 0;
        
    return i + sum (i - 1); //回傳i + sum (i - 1)，可以視為i + (i - 1) + (i - 2) + ... 1
}

int main() {
    int n;
    cin >> n;
    cout << sum(n);
    
    return 0;
}
```

> 範例輸入：
>
> 100

> 範例輸出：
>
> 5050

雖然這題雖然可以用看似酷炫的遞迴解決，但是其執行速度不比`for`還來的快，因為先前提到，每呼叫一次自己，就會把自己本身放入stack中，等待被呼叫端執行完畢後，才抽出來再繼續執行，這中間就會牽扯記憶體的管理，增加程式執行時間。而且如果stack存的內容太多，還很可能會造成[stack overflow](https://stackoverflow.com/questions/26158/how-does-a-stack-overflow-occur-and-how-do-you-prevent-it)。

附上另外兩種解法：

{% tabs %}
{% tab title="For迴圈" %}
```cpp
#include <iostream>
using namespace std;

int main() {
    int n, sum;
    cin >> n;
    sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    cout << sum;
    
    return 0;
}
```
{% endtab %}

{% tab title="梯形公式" %}
```cpp
#include <iostream>
using namespace std;

int main() {
    int n, sum;
    cin >> n;
    cout << (n + 1) * n / 2;
    
    return 0;
}
```
{% endtab %}
{% endtabs %}

到目前為止，感覺遞迴沒有什麼用處，但是如果寫得好，反而會比用for迴圈還好理解。

## GCD 最大公因數

> 題目：
>
> 給定x, y，請輸出gcd\(x, y\)

```cpp
//使用輾轉相除法
#include <iostream>
using namespace std;

int gcd(int x, int y) {
    if (y == 0)
        return x;
    return gcd(y, x % y);
}

int main() {
    int x, y;
    cin >> x >> y;
    cout << gcd(x, y);
    
    return 0;
}
```

> 範例輸入：
>
> 10 5

> 範例輸出：
>
> 5

利用遞迴的寫法，輾轉相除法只用了3行就解決，非常簡單明瞭，如果有學過輾轉相除法，一看下去就能理解。

## 費氏數列

> 題目：
>
> 給定一自然數n，請輸出費氏數列第n項  
> 費氏數列： 1 1 2 3 5 ...

```cpp
#include <iostream>
using namespace std;
int Fibonacci(int i) {
    if (i == 1 || i == 2) {
        return 1;
    }
    return Fibonacci(i - 1) + Fibonacci(i - 2);
}
int main() {
    int n;
    cin >> n;
    cout << Fibonacci(n);
    
    return 0;
}
```

> 範例輸入：
>
> 7

> 範例輸出：
>
> 13

{% tabs %}
{% tab title="說明" %}
`return Fibonacci(i - 1) + Fibonacci(i - 2);`

這行非常的直觀，可以知道要回傳 第i - 1項 ＋第i - 2項。

而`if (i == 1 || i == 2) return 1;`這邊非常重要，如果沒有加上這行，則Fibonacci函數會沒有跳脫的條件，導致程式無止境執行下去。

這題也可以是試著用迴圈寫，並比較兩者之間差異。

{% hint style="info" %}
遞迴版的程式雖然看起來較間單，但是執行時間會跟n成指數成長\(2 ^ n\)，可以嘗試輸入大於40的數字看看。

並試著考慮為何n過大時執行時間會很久，詳細解法請到網路上搜尋關鍵字「動態規劃」或是「Dynamic Programming \(DP\)」
{% endhint %}
{% endtab %}

{% tab title="for迴圈版本" %}
```cpp
#include <iostream>
using namespace std;

int main() {
    int sum, n, prev1, prev2;
    prev1 = 0;
    prev2 = 1;
    sum = 1;
    
    cin >> n;
    
    for (int i = 1; i < n; i++) {
        sum = prev1 + prev2;
        prev1 = prev2;
        prev2 = sum;
    }
    cout << sum;

    return 0;
}

```
{% endtab %}
{% endtabs %}

