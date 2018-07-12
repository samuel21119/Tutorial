# 堆疊 \(Stack\)

Stack是具有「Last-In-First-Out」特性的資料結構 \(可以想像成一種裝資料的容器\)。

最早進的最晚出來；最晚進的最早出來。就如疊盤子一樣：

![](../../.gitbook/assets/wzwpmlzizvx0cmyktqxejm1kzmx8soxmdm0ezyvcwbpxgbh9yckf2bsbxdv02bj5con5wztvwaq5yd3d3lvodc0rha%20%281%29.jpg)

一般的Stack，會有以下幾種操作項目：

* Push：把資料放進Stack
  * 疊上一個盤子
* Pop：把「最上面」的資料從Stack移除
  * 拿掉最上面的盤子
* Top：回傳Stack「最上面」的資料
  * 回傳最上面盤子的顏色
* Empty：回傳Stack是否無資料
  * 如果有資料，則回傳0，否則回傳1
* Size：回傳Stack的大小
  * 回傳目前有一個盤子

## 實際演練

![](../../.gitbook/assets/f1.png)

1. Push\(6\)，將6放進Stack。此時Top = 6 ， Size = 1
2. Push\(3\)，將3放進Stack。此時Top = 3 ， Size = 2
3. Push\(7\)，將7放進Stack。此時Top = 7 ， Size = 3
4. Pop\(\)，將最上面的數字丟掉\(7\)。此時Top = 3 ， Size = 2

試說明5、6步驟

{% tabs %}
{% tab title="先不要點答案" %}
點擊**答案**觀看答案
{% endtab %}

{% tab title="答案" %}
5. Push\(7\)，將14放進Stack。此時Top = 14 ， Size = 3

6. Push\(8\)，將8放進Stack。此時Top = 8 ， Size = 4
{% endtab %}
{% endtabs %}

{% hint style="info" %}
這章節只是介紹Stack的結構，之後才會介紹C++裡面的stack資料結構及實作
{% endhint %}



