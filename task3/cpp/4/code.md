# 洛谷题4：五题 C++ 代码

## 1. P1428 小鱼比可爱

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    int a[105];
    for (int i = 0; i < n; i++) {
        cin >> a[i];
    }
    for (int i = 0; i < n; i++) {
        int cnt = 0;
        for (int j = 0; j < i; j++) {   // 只看左边的鱼
            if (a[j] < a[i]) cnt++;      // 比自己不可爱的，计数+1
        }
        if (i > 0) cout << " ";          // 数字之间空格隔开
        cout << cnt;
    }
    cout << endl;
    return 0;
}
```

## 2. P1427 小鱼的数字游戏

```cpp
#include <iostream>
using namespace std;

int main() {
    int a[105];
    int n = 0;
    int x;
    while (cin >> x && x != 0) {   // 读入数字，遇到0就停
        a[n++] = x;
    }
    for (int i = n - 1; i >= 0; i--) {  // 从后往前输出
        if (i < n - 1) cout << " ";     // 数字之间空格
        cout << a[i];
    }
    cout << endl;
    return 0;
}
```

## 3. P5727 【深基5.例3】冰雹猜想

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cin >> n;
    int a[1000] = {0};
    int cnt = 0;
    while (true) {
        a[cnt++] = n;           // 把当前数字存进数组
        if (n == 1) break;      // 到1了，停止
        if (n % 2 == 1) {       // 奇数：乘3加1
            n = n * 3 + 1;
        } else {                // 偶数：除以2
            n = n / 2;
        }
    }
    for (int i = cnt - 1; i >= 0; i--) {  // 倒序输出
        if (i < cnt - 1) cout << " ";
        cout << a[i];
    }
    cout << endl;
    return 0;
}
```

## 4. P5728 【深基5.例5】旗鼓相当的对手

```cpp
#include <iostream>
#include <cmath>
using namespace std;

int main() {
    int n;
    cin >> n;
    int a[1005][3];   // a[i][0]=语文, a[i][1]=数学, a[i][2]=英语
    int sum[1005];
    for (int i = 0; i < n; i++) {
        cin >> a[i][0] >> a[i][1] >> a[i][2];
        sum[i] = a[i][0] + a[i][1] + a[i][2];  // 算总分
    }
    int cnt = 0;
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {      // 枚举每一对(i,j)，i<j避免重复
            if (abs(a[i][0] - a[j][0]) <= 5 &&  // 语文分差≤5
                abs(a[i][1] - a[j][1]) <= 5 &&  // 数学分差≤5
                abs(a[i][2] - a[j][2]) <= 5 &&  // 英语分差≤5
                abs(sum[i] - sum[j]) <= 10) {   // 总分分差≤10
                cnt++;
            }
        }
    }
    cout << cnt << endl;
    return 0;
}
```

## 5. P1047 [NOIP2005 普及组] 校门外的树

```cpp
#include <iostream>
using namespace std;

int main() {
    int l, m;
    cin >> l >> m;
    bool tree[10005];
    for (int i = 0; i <= l; i++) tree[i] = true;  // 初始每个点都有树
    for (int i = 0; i < m; i++) {
        int u, v;
        cin >> u >> v;
        for (int j = u; j <= v; j++) {
            tree[j] = false;   // 这个区间的树移走
        }
    }
    int cnt = 0;
    for (int i = 0; i <= l; i++) {
        if (tree[i]) cnt++;    // 数还剩多少棵
    }
    cout << cnt << endl;
    return 0;
}
```
