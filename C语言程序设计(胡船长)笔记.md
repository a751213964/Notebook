# C语言程序设计(胡船长)笔记

# 数学运算

**左值 右值**

![1555584688113](/home/zhaohang/haizei/4.Notebook/picture/1555584688113.png)**负数右移最大能得到负一**!

![1555584868542](/home/zhaohang/haizei/4.Notebook/picture/1555584868542.png)

### C语言引入数学函数库<math.h>注意事项

若C语言代码中引入了<math.h>函数库，在终端下无法被编译

解决方法：须在编译命令后面加“-lm”；

例如：gcc daima.c -lm                  编译完成；

### 赋值运算符“=”

1.自增自减只能用在变量上，不能用在常量上

代码执行到下一行 值还存在 说明这个值是一个左值，反之不存在了为右值

“d + e”在这里为一个临时变量，默认为右值；

左值和右值不是靠放在左面或者放在右边来区分的

![1555590397515](../haizei/4.Notebook/picture/1555590397515.png)

### 运算符优先级

说明：

同一优先级的运算符，结合次序由结合方向所决定。

简单记就是：

！(条件运算符) > 算术运算符 > 关系运算符(与或) > && > || > 赋值运算符

### “异或”运算

异或运算可用来进行位运算中的奇偶判断

例1 ^ 1 = 1       1 ^ 0 = 0	0 ^ 0 = 1（有偶数个1值为1，有奇数个1值为0）

异或运算，若c = a ^ b，那么： a = b ^ c, b = a ^ c;

![1555592136610](/home/zhaohang/haizei/4.Notebook/picture/1555592136610.png)代码如下

![1555591603126](/home/zhaohang/haizei/4.Notebook/picture/1555591603126.png)此为运行结果

### “与”“或”运算（“&”“|”运算）

与运算通常当作位运算中的乘法

或运算通常当作位运算中的加法







# 练习：C语言输出X的立方根

```
#include <stdio.h>
#include <math.h>
int main(){
    double x;
    scanf("%lf", &x);
    printf("%lf", pow(x, 1.0 / 3.0));
    return 0;
}
```

![1555585926701](/home/zhaohang/haizei/4.Notebook/picture/1555585926701.png)







# C语言角度值转为弧度值

## 1.写一个程序，读如一个角度值，将角度值转为弧度值：

```
#include <stdio.h>
#include <math.h>

#define PI acos(-1)
int main() {
	double x;
	scanf("%lf", &x);
	printf("%lf", PI / 180.0 * x);
	return 0;
}
```

![1555586299145](/home/zhaohang/haizei/4.Notebook/picture/1555586299145.png)







# <inttypes.h>函数库

在<inttypes.h>函数库中，定义16位参数a一般使用“int16_t a"

但是输入如果用“%d”占位，在C语言中默认是读入32位整型，编译会遇到错误，

因此我们在这里可以用到   “%PRId16”  或   “%”PRId16    这两个占位方式

如：scanf ("%PRId16", &a );

	scanf ("%"PRId16, &a);

![1555588310436](/home/zhaohang/haizei/4.Notebook/picture/1555588310436.png)

![1555588399306](/home/zhaohang/haizei/4.Notebook/picture/1555588399306.png)

### 输出16进制

![1555588509284](/home/zhaohang/haizei/4.Notebook/picture/1555588509284.png)

### 输出64位整型的极小值

（极大值需要将这里MIN换成MAX）

![1555588667575](/home/zhaohang/haizei/4.Notebook/picture/1555588667575.png)

