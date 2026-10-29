# 洛谷题6：五题 C++ 代码

## 1. P5735 距离函数

```cpp
#include <cmath>
#include <iomanip>
#include <iostream>
using namespace std;

int main() {
    double x1, y1, x2, y2, x3, y3;
    cin >> x1 >> y1 >> x2 >> y2 >> x3 >> y3;

    double perimeter = hypot(x1 - x2, y1 - y2)
                     + hypot(x2 - x3, y2 - y3)
                     + hypot(x3 - x1, y3 - y1);

    cout << fixed << setprecision(2) << perimeter;
    return 0;
}
```

## 2. P5736 质数筛

```cpp
#include <iostream>
using namespace std;

bool isPrime(int x) {
    if (x < 2) {
        return false;
    }

    for (int i = 2; i * i <= x; i++) {
        if (x % i == 0) {
            return false;
        }
    }

    return true;
}

int main() {
    int n;
    int a[100];

    cin >> n;

    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }

    int count = 0;

    for (int i = 0; i < n; i++) {
        if (isPrime(a[i])) {
            a[count] = a[i];
            count++;
        }
    }

    for (int i = 0; i < count; i++) {
        cout << a[i];
        if (i < count - 1) {
            cout << ' ';
        }
    }

    return 0;
}
```

## 3. P5737 闰年展示

```cpp
#include <iostream>
using namespace std;

bool isLeapYear(int year) {
    if (year % 400 == 0) {
        return true;
    }

    if (year % 4 == 0 && year % 100 != 0) {
        return true;
    }

    return false;
}

int main() {
    int x, y;
    cin >> x >> y;

    int count = 0;

    for (int year = x; year <= y; year++) {
        if (isLeapYear(year)) {
            count++;
        }
    }

    cout << count << '\n';

    bool first = true;

    for (int year = x; year <= y; year++) {
        if (isLeapYear(year)) {
            if (!first) {
                cout << ' ';
            }

            cout << year;
            first = false;
        }
    }

    return 0;
}
```

## 4. P5738 歌唱比赛

```cpp
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    double best = 0;

    for (int i = 0; i < n; i++) {
        int sum = 0;
        int highest = 0;
        int lowest = 10;

        for (int j = 0; j < m; j++) {
            int score;
            cin >> score;

            sum += score;

            if (score > highest) {
                highest = score;
            }

            if (score < lowest) {
                lowest = score;
            }
        }

        double average = static_cast<double>(sum - highest - lowest) / (m - 2);

        if (average > best) {
            best = average;
        }
    }

    cout << fixed << setprecision(2) << best;
    return 0;
}
```

## 5. P5739 计算阶乘

```cpp
#include <iostream>
using namespace std;

int factorial(int n) {
    if (n == 1) {
        return 1;
    }

    return n * factorial(n - 1);
}

int main() {
    int n;
    cin >> n;

    cout << factorial(n);
    return 0;
}
```
