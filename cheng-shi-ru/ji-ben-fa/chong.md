# 補充

對於先前提到的`using namespace std;`，這裡將作進一步的解釋。

首先，我們最基本的程式第一行是`#include <iostream>`，因為如果要進行輸出輸入，需要用到`cout`、`cin`，不過最原始的用法並不是`cout << "Hello World";`。

`<iostream>`裡面定義的`cout`\(`cin`也是一樣\)，其實是定義在一個名叫「std」命名空間的下面。舉個例子：學校要找「1年1班王小明」到學務處，但廣播的時候只說要找「王小明」，並沒有說是在哪一個班級的「王小明」，所以這時候就找不到學校真正要找的那位「王小明」\(假設有多個王小明，且位於不同班級\)。那這時候就要指明說是「1年1班的王小明」。

換句話說，例子裡面的「王小明」就是`cout`，但是C++不允許我使用重複定義的指令，所以我就要明確指定是位於`std`班級裡面的`cout`。

講解先到這裡，來看看最原始的寫法長怎樣：

```cpp
#include <iostream>

int main() {
    int a;
    std::cout << "Hello World!" << std::endl;
    std::cout << "No 'using namespace std;'" << std::endl;
    std::cin >> a;
    return 0;
}
```

由上面的程式可明確看到，如果我沒有加上`using namespace std;`這行，每一次的`cout`、`cin`及`endl`都要加上`std::`，這樣才能明確指定是在std這個班級\(命名空間\)下面。但是因為每次都要加上`std::`非常麻煩，所以我們才會在程式開頭加上`using namespace std;`。

