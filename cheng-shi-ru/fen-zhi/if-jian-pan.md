# If條件判斷

`if`可以分成`if`和`if-else`：

```cpp
if (判斷條件) { //if
    ... //如果
}

if (判斷條件) { //if-else
    ... //如果
}else {
    ... //否則
}
```

所以我們可以透過`if-else`判斷成績是否及格：

```cpp
#include <iostream>
using namespace std;

int main() {
    int score;
    cin >> score;
    
    if (score < 60) {
        cout << "待加強" << endl;
    }else {
        cout << "及格！" << endl;
    }
    
    return 0;
}：
```

> 範例輸入1：
>
> 78
>
> 範例輸出1：
>
> 及格！

> 範例輸入2：
>
> 59
>
> 範例輸出2：
>
> 待加強！

另外，if裡面的判斷條件同樣也適用於先前提到的「非零即為真」的概念：

```cpp
int a, b, c, d;
a = 1;
b = 0;
c = -2;
d = 100;
if (a) {
    cout << "a" << endl;
}
if (b) {
    cout << "b" << endl;
}
if (c) {
    cout << "c" << endl;
}
if (d) {
    cout << "d" << endl;
}
```

> 範例輸出：
>
> a
>
> c
>
> d

## 巢狀if

誰說`if`不能只放一個的？我們來看看如果`if`裡面也放`if`會怎麼樣

```cpp
#include <iosteam>
using namespace std;

int main() {
    int score;
    cin >> score;
    
    if (score >= 60) {
        if (score >= 70) {
            if (score >= 80) {
                if (score >= 90) {
                    cout << "A+";
                }else {
                    cout << "A";
                }
            }else {
                cout << "B";
            }
        }else {
            cout << "C";
        }
    }else {
        cout << "F";
    }
    
    return 0;
}
```

@@上面到底在寫什麼？

* 首先會進入第一個判斷，判斷`score >= 60`
  * 如果成立
    * 繼續判斷是否`>=70`、`>=80`...
  * 否則
    * 輸出成績等級 \(C、B、A、A+\)
* 否則
  * 輸出F

## if - else if - else條件判斷

以上面輸出成績等級的範例來看，感覺有點過於複雜，我們可以將它改寫成以下這樣

```cpp
if (score < 60) {
    cout << "F";
}else if (score < 70) {
    cout << "C";
}else if (score < 80) {
    cout << "B";
}else if (score < 90) {
    cout << "A";
}else {
    cout << "A+";
}
```

檢查順序會由上到下，如果所有條件都不符合，才會到最下面`else`那裡

當然，也可以不用寫最後面的`else`

```cpp
if (score < 60) {
    cout << "F";
}else if (score < 70) {
    cout << "C";
}else if (score < 80) {
    cout << "B";
}else if (score < 90) {
    cout << "A";
}else if (score <= 100) {
    cout << "A+";
}
```

如果這樣寫的話，當`score > 100`就不會輸出任何東西

> 範例輸入1：
>
> 56
>
> 範例輸出1：
>
> F

> 範例輸入2：
>
> 70
>
> 範例輸出2：
>
> B

> 範例輸入3：
>
> 87
>
> 範例輸出3：
>
> A

## 練習題目

[Zerojudge a003](https://zerojudge.tw/ShowProblem?problemid=a003)

[Zerojudge a004](https://zerojudge.tw/ShowProblem?problemid=a004)

[Zerojudge a006](https://zerojudge.tw/ShowProblem?problemid=a006)

