# 洛谷题3：五题 C++ 代码

## 1. P5718 【深基4.例2】找最小值

```cpp
#include <iostream>
#include <algorithm>
using namespace std;

int main() {
    int n;
    cin >> n;
    int minVal = 1001;  // 因为 ai ≤ 1000，初始值设为比 1000 大即可
    for (int i = 0; i < n; i++) {
        int x;
        cin >> x;
        if (x < minVal) minVal = x;
    }
    cout << minVal << endl;
    return 0;
}
```

## 2. P5719 【深基4.例3】分类平均

```cpp
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int n, k;
    cin >> n >> k;
    int sumA = 0, cntA = 0;  // A类：k的倍数
    int sumB = 0, cntB = 0;  // B类：不能被k整除
    for (int i = 1; i <= n; i++) {
        if (i % k == 0) {
            sumA += i;
            cntA++;
        } else {
            sumB += i;
            cntB++;
        }
    }
    cout << fixed << setprecision(1);
    cout << (double)sumA / cntA << " " << (double)sumB / cntB << endl;
    return 0;
}
```

## 3. P5720 【深基4.例4】一尺之棰

```cpp
#include <iostream>
using namespace std;

int main() {
    long long a;
    cin >> a;
    int day = 1;          // 第一天就是初始长度 a
    while (a > 1) {
        a = a / 2;        // 整数除法自动向下取整
        day++;
    }
    cout << day << endl;
    return 0;
}
```

## 4. P5721 【深基4.例5】数字直角三角形

```cpp
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int n;
    cin >> n;
    cout << setfill('0');   // 不足2位时用0填充
    int t = 1;              // 当前要输出的数字，从1开始
    for (int i = 1; i <= n; i++) {          // 第i行
        for (int j = 1; j <= n - i + 1; j++) {  // 这一行输出几个数
            cout << setw(2) << t;           // 占2位，不够补前导0
            t++;
        }
        cout << endl;
    }
    return 0;
}
```

## 5. P5722 【深基4.例11】数列求和

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    cout << sum << endl;
    return 0;
}
```
