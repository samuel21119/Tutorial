# 起手式

學習每個程式語言的第一件事情，  
通常就是先做個簡單的程式來運行一下。

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World! << endl;
    return 0;
}
```

## 語法 Syntax

英文有自己的語法，中文也有，如果不按照語法來溝通，就不法達成傳遞訊息的目的，所以在程式語言中也是有事先規定好的語法，以下會一一介紹。

另外請注意，每行程式後面都需要加上「;」分號，除了\#include \#define及{}後面

## 標頭檔 Headers

標頭檔告訴編譯器\(Compiler\)需要用到什麼標頭檔

```cpp
#include <iostream>
```

這句話告訴編譯器說我需要用到名為 iostream 的標頭檔

iostream = input / ouput stream

如果以下程式不只用到iostream，則需要include 多個標頭檔，例如

```cpp
#include <iostream>
...
#include <cmath>
```

## C++命名空間

在上面的範例中，可以看到

```cpp
using namespace std;
```

這個很奇怪的東西，以初學者來說，只需要知道每個程式都需要加上這行即可，因為背後牽扯到很多複雜概念，故省略解釋

## 主程式

在一個完整的程式碼當中，需要告訴程式執行的起點在哪裡，就是下面的main:

```text
int main() {
    ...
}
```

主程式；Main function，程式進入點\(Entry point\)是main\(\)這個函式  
int；執行完畢後回傳整數型態 \(將在函數\(Function\)詳細介紹\)  
\( \)；參數定義 \(將在函數\(Function\)詳細介紹\)  
{ }；程式內容 \(裡面就是這支程式要做的事情\)

## 縮排

```cpp
#include <iostream>
using namespace std;
int main(){
cout<<"Hello World!"<<endl;
}
```

比起上面來講，

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World!" << endl;
}
```

這個看起來會顯得更輕鬆愜意。

