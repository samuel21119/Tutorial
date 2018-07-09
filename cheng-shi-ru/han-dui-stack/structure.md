# 結構 \(structure\)

在程式設計中，常常會遇到一組變數需要一起宣告的，例如 姓名 學號 成績 排名，全部都是用來描述一個學生的：

```cpp
char name[7];
char id;
float score;
int rate;
```

但是這樣分開宣告非常麻煩，而且不方便管理，所以我們可以把它們黏在一起，就是這邊要介紹的結構 \(structure\)。

定義方法如下：

```cpp
struct student {
    char name[7];
    char id;
    float score;
    int rate;
};
```

這個時候，我們只是定義了student這個資料型態，類似我們熟悉的`int`、 `char`。

如果我要使用這個資料結構，就要這樣宣告：

```cpp
student stu1;
```

或是在定義`structure`的後面：

```cpp
struct student {
    char name[7];
    char id;
    float score;
    int rate;
}stu1, stu2;
```

現在已經完成宣告了，如果要存取structure裡面的東西，需要這樣表示：

`變數名稱.結構成員`

### 實作範例：

```cpp
#include <iostream>
using namespace std;

struct student {
    char name[20];
    char id[7];
    float score;
    int rate;
}stu;

int main() {
    cin >> stu.name;
    cin >> stu.id;
    cin >> stu.score;
    cin >> stu.rate;
    
    cout << stu.name << endl;
    cout << stu.id << endl;
    cout << stu.score << endl;
    cout << stu.rate << endl;
}
```

> 範例輸入：
>
> John
>
> 060123
>
> 70.5
>
> 15

> 範例輸出：
>
> John
>
> 060123
>
> 70.5
>
> 15

當然，structure也可以使用陣列的宣告方式

```cpp
#include <iostream>
using namespace std;

struct student {
    char name[20];
    char id[7];
    float score;
    int rate;
}stu[2];

int main() {
    for (int i = 0; i < 2; i++) {
        cin >> stu[i].name;
        cin >> stu[i].id;
        cin >> stu[i].score;
        cin >> stu[i].rate;
    }
    cout << stu[1].name << endl;
    cout << stu[1].id << endl;
    cout << stu[1].score << endl;
    cout << stu[1].rate << endl;
}
```

> 範例輸入：
>
> John  060123  70.5  15
>
> Blake  069487  67.3  25

> 範例輸出：
>
> Blake
>
> 069487
>
> 67.3
>
> 25

