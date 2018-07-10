# 字串 \(String\)

如果題目說要輸入一串英文字\(例如：`Hello、abcdefghjkl`\)，我們要怎麼接收？

## Char 陣列

這時候就要利用`char`型態陣列來幫忙了，宣告方法跟前面一樣，只是型態改變而已：

```cpp
#include <iostream>
using namespace std;

int main() {
    char input[100];
    
    cin >> input;
    cout << input;
    
    return 0;
}
```

> 範例輸入：
>
> hello!
>
> 範例輸出：
>
> hello!

而且我們也可以讀取及寫入的時候第n位置的字元是什麼：

```cpp
cout << input[0] << endl; //h
input[0] = 'H';

cout << input[1] << endl; //e
input[1] = 'E';

cout << input << endl;    //輸出結果：HEllo
```

上面分別是輸出第一個字元和第二個。

## String 變數型態

從上面的範例可以發現，可以讀取字串的長度事先就已經限制好了\( `char input[100];`在宣告的時候已經固定長度\)。而且在字串相加 \(Ex: Hello + world = Helloworld\) 的時候會變得非常麻煩。這時候我們可以使用C++內建的String\(字串\)變數：

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    string s;
    
    cin >> s;
    cout << s << endl;
    
    return 0;
}
```

> 範例輸入：
>
> hello!

> 範例輸出：
>
> hello!

在上面的程式碼中，可以看到 `#include <string>`這串，這是因為`string`變數型態是定義在string這個標頭檔，所以我們要把它include進來，要不然編譯會發生錯誤。

而且`string`也可以當作`char`陣列讀取，例如：

```cpp
cout << s[0]; //h
cout << s[1]; //e
```

{% hint style="warning" %}
使用此方法只能讀取，不能寫入，如：

```cpp
s[0] = 'a';
```

會造成編譯錯誤。
{% endhint %}

另外，補充一些常用用法：

```cpp
int len = s.length(); // 字串s的長度（若s為"Hello"，則回傳5）

string s1 = s;        //指派s的內容給s1
                      
string s2 = s + s;    //字串相加（若s為"Hello"，則s2為"HelloHello"）

if (s == "Hello") {   //若字串s等於Hello，則...
    ...
}

char char_array[100];
cin >> char_array;
string s3(char_array);//可以在s3宣告的時候，把char_array儲存的字串寫入s3
                      //此做法可以視為 char陣列 轉 string的做法
```

{% hint style="warning" %}
以上用法只適用於`string`型態，如果用`char`陣列儲存字串，使用以上指令將會造成編譯錯誤！
{% endhint %}

## 練習題目

[Zerojudge a001](https://zerojudge.tw/ShowProblem?problemid=a001)

