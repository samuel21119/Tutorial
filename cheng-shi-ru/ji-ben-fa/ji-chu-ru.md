# 變數

在程式語言裡面，我們需要一個容器來儲存各種不同的值，而這個容器名叫變數\(Variable\)，它會利用記憶體的空間來儲存資料。

如果要使用，則需要先宣告變數，宣告變數分成兩部分，分別為「變數型態」及變數名稱。

最基本的變數型態分成以下4種：

## Integer

Integer 中文名叫整數，故此變數存放整數型態的值，例如：

```cpp
int a = 1;
int b = -100;
int I_am_integer = 9487;
```

因為記憶體的限制，int型態範圍只到 -2^31 ~ 2^31-1

如果還需要更大，則需要宣告為`long long`型態 \(-2^63 ~ 2^63-1\)

```cpp
long long a = 9223372036854775807;
long long b = -9223372036854775807;
```

## Char

char 全名為character，中文叫做「字元」，可以儲存ASCII表上所有的字元

![](../../.gitbook/assets/asciifull.gif)

![](../../.gitbook/assets/extend.gif)

這時我們可以這樣宣告：

```cpp
char a = 'a';
char b = 'b';
char ch = '1';
char ch2 = 'Z';
char ch3 = '%';
```

## Float / Double 浮點數

如果要儲存有小數點的數字，而不是整數，則必須使用float 或 double型態來儲存  
其中double可以儲存的數字範圍較float大，有關浮點數的詳細資訊請參照[IEEE754](https://zh.wikipedia.org/zh-tw/IEEE_754)

```cpp
float f1 = 1.0;
float f2 = 1.234;
double pi = 3.1415926;
```

## Bool 布林值

布林為Boolean的音譯，代表True或False，所以`bool`型態變數只能儲存0或1。

0代表False；1則代表True：

```cpp
bool b1 = true;
bool b2 = 1;
bool b3 = false;
bool b4 = 0;
```

