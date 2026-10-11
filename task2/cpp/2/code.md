# 洛谷题二：五题 C++ 代码

## 1. 苹果 Prologue

```cpp
#include <iostream>
using namespace std;

int main() {
    int m, t, s;
    cin >> m >> t >> s;

    if (t == 0) {
        cout << 0;
    } else {
        int eaten = (s + t - 1) / t;
        int remaining = m - eaten;
        if (remaining < 0) remaining = 0;
        cout << remaining;
    }

    return 0;
}
```

## 2. 数的性质

```cpp
#include <iostream>
using namespace std;

int main() {
    int x;
    cin >> x;

    bool even = (x % 2 == 0);
    bool inRange = (x > 4 && x <= 12);

    cout << (even && inRange) << ' '
         << (even || inRange) << ' '
         << (even != inRange) << ' '
         << (!even && !inRange);

    return 0;
}
```

## 3. 闰年判断

```cpp
#include <iostream>
using namespace std;

int main() {
    int year;
    cin >> year;

    if (year % 400 == 0 || (year % 4 == 0 && year % 100 != 0)) {
        cout << 1;
    } else {
        cout << 0;
    }

    return 0;
}
```

## 4. Apples

```cpp
#include <iostream>
using namespace std;

int main() {
    int x;
    cin >> x;

    cout << "Today, I ate " << x << " apple";
    if (x != 1) {
        cout << 's';
    }
    cout << '.';

    return 0;
}
```

## 5. 洛谷团队系统

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;

    if (5 * n < 11 + 3 * n) {
        cout << "Local";
    } else {
        cout << "Luogu";
    }

    return 0;
}
```
