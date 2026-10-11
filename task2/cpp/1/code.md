# 洛谷题一：五题 C++ 代码

## 1. Hello,World!

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello,World!";
    return 0;
}
```

## 2. 字符三角形

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    char c;
    cin >> c;

    for (int i = 0; i < 3; i++) {
        cout << string(2 - i, ' ');
        cout << string(2 * i + 1, c) << '\n';
    }

    return 0;
}
```

## 3. 输出字符菱形

```cpp
#include <iostream>
#include <string>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        int row = i < 3 ? i : 4 - i;
        cout << string(2 - row, ' ');
        cout << string(2 * row + 1, '*') << '\n';
    }

    return 0;
}
```

## 4. 苹果采购

```cpp
#include <iostream>
using namespace std;

int main() {
    int applesPerPerson, classmates;
    cin >> applesPerPerson >> classmates;

    cout << applesPerPerson * classmates;
    return 0;
}
```

## 5. 字母转换

```cpp
#include <iostream>
using namespace std;

int main() {
    char c;
    cin >> c;

    cout << char(c - 'a' + 'A');
    return 0;
}
```
