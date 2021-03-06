# PHP 运算符

------

本章节我们将讨论 PHP 中不同运算符的应用。

在 PHP 中，赋值运算符 = 用于给变量赋值。

在 PHP 中，算术运算符 + 用于把值加在一起。

------

## PHP 算术运算符

| 运算符 | 名称             | 描述            | 实例                | 结果  |
| :----- | :--------------- | :-------------- | :------------------ | :---- |
| x + y  | 加               | x 和 y 的和     | 2 + 2               | 4     |
| x - y  | 减               | x 和 y 的差     | 5 - 2               | 3     |
| x * y  | 乘               | x 和 y 的积     | 5 * 2               | 10    |
| x / y  | 除               | x 和 y 的商     | 15 / 5              | 3     |
| x % y  | 模（除法的余数） | x 除以 y 的余数 | 5 % 2 10 % 8 10 % 2 | 1 2 0 |
| - x    | 取反             | x 取反          | - 2                 |       |
| a . b  | 并置             | 连接两个字符串  | "Hi" . "Ha"         | HiHa  |

以下实例演示了使用不同算术运算符得到的不同结果：



## 实例



```php
<?php 
$x=10; 
$y=6;
echo ($x + $y); // 输出16
echo '<br>';
echo ($x - $y); // 输出4
echo '<br>';
echo ($x * $y); // 输出60
echo '<br>';
echo ($x / $y); // 输出1.6666666666667 
echo '<br>';
echo ($x % $y); // 输出4 
?>
```





PHP7+ 版本新增整除运算符 **intdiv()**,使用实例：

```php
<?php
var_dump(intdiv(10, 3));
?>
```

以上实例会输出：

```PHP
int(3)
```

------

## PHP 赋值运算符

在 PHP 中，基本的赋值运算符是 "="。它意味着左操作数被设置为右侧表达式的值。也就是说，"$x = 5" 的值是 5。

| 运算符 | 等同于    | 描述                           |
| :----- | :-------- | :----------------------------- |
| x = y  | x = y     | 左操作数被设置为右侧表达式的值 |
| x += y | x = x + y | 加                             |
| x -= y | x = x - y | 减                             |
| x *= y | x = x * y | 乘                             |
| x /= y | x = x / y | 除                             |
| x %= y | x = x % y | 模（除法的余数）               |
| a .= b | a = a . b | 连接两个字符串                 |

以下实例演示了使用不同赋值运算符得到的不同结果：

## 实例

```php
<?php 
$x=10; 
echo $x; // 输出10
echo '<br>';

$y=20; 
$y += 100;
echo $y; // 输出120
echo '<br>';

$z=50;
$z -= 25;
echo $z; // 输出25
echo '<br>';

$i=5;
$i *= 6;
echo $i; // 输出30
echo '<br>';

$j=10;
$j /= 5;
echo $j; // 输出2
echo '<br>';

$k=15;
$k %= 4;
echo $k; // 输出3
?>
```



以下实例演示了使用不同字符串运算符得到的不同结果：

## 实例

```php
<?php
$a = "Hello";
$b = $a . " world!";
echo $b; // 输出Hello world! 
echo '<br>';

$x="Hello";
$x .= " world!";
echo $x; // 输出Hello world! 
?>
```

------

## PHP 递增/递减运算符

| 运算符 | 名称   | 描述                |
| :----- | :----- | :------------------ |
| ++ x   | 预递增 | x 加 1，然后返回 x  |
| x ++   | 后递增 | 返回 x，然后 x 加 1 |
| -- x   | 预递减 | x 减 1，然后返回 x  |
| x --   | 后递减 | 返回 x，然后 x 减 1 |

以下实例演示了使用递增/递减运算符得到的结果：

## 实例



```php
<?php
$x=10; 
echo ++$x; // 输出11
echo '<br>';

$y=10; 
echo $y++; // 输出10
echo '<br>';

$z=5;
echo --$z; // 输出4
echo '<br>';

$i=5;
echo $i--; // 输出5
?>
```



------

## PHP 比较运算符

比较操作符可以让您比较两个值：

| 运算符  | 名称     | 描述                                           | 实例               |
| :------ | :------- | :--------------------------------------------- | :----------------- |
| x == y  | 等于     | 如果 x 等于 y，则返回 true                     | 5==8 返回 false    |
| x === y | 恒等于   | 如果 x 等于 y，且它们类型相同，则返回 true     | 5==="5" 返回 false |
| x != y  | 不等于   | 如果 x 不等于 y，则返回 true                   | 5!=8 返回 true     |
| x <> y  | 不等于   | 如果 x 不等于 y，则返回 true                   | 5<>8 返回 true     |
| x !== y | 不恒等于 | 如果 x 不等于 y，或它们类型不相同，则返回 true | 5!=="5" 返回 true  |
| x > y   | 大于     | 如果 x 大于 y，则返回 true                     | 5>8 返回 false     |
| x < y   | 小于     | 如果 x 小于 y，则返回 true                     | 5<8 返回 true      |
| x >= y  | 大于等于 | 如果 x 大于或者等于 y，则返回 true             | 5>=8 返回 false    |
| x <= y  | 小于等于 | 如果 x 小于或者等于 y，则返回 true             | 5<=8 返回 true     |

以下实例演示了使用一些比较运算符得到的不同结果：

## 实例

```php
<?php
$x=100; 
$y="100";

var_dump($x == $y);
echo "<br>";
var_dump($x === $y);
echo "<br>";
var_dump($x != $y);
echo "<br>";
var_dump($x !== $y);
echo "<br>";

$a=50;
$b=90;

var_dump($a > $b);
echo "<br>";
var_dump($a < $b);
?>
```



------

## PHP 逻辑运算符

| 运算符   | 名称 | 描述                                         | 实例                                 |
| :------- | :--- | :------------------------------------------- | :----------------------------------- |
| x and y  | 与   | 如果 x 和 y 都为 true，则返回 true           | x=6 y=3 (x < 10 and y > 1) 返回 true |
| x or y   | 或   | 如果 x 和 y 至少有一个为 true，则返回 true   | x=6 y=3 (x==6 or y==5) 返回 true     |
| x xor y  | 异或 | 如果 x 和 y 有且仅有一个为 true，则返回 true | x=6 y=3 (x==6 xor y==3) 返回 false   |
| x && y   | 与   | 如果 x 和 y 都为 true，则返回 true           | x=6 y=3 (x < 10 && y > 1) 返回 true  |
| x \|\| y | 或   | 如果 x 和 y 至少有一个为 true，则返回 true   | x=6 y=3 (x==5 \|\| y==5) 返回 false  |
| ! x      | 非   | 如果 x 不为 true，则返回 true                | x=6 y=3 !(x==y) 返回 true            |

------

## PHP 数组运算符

| 运算符  | 名称   | 描述                                                         |
| :------ | :----- | :----------------------------------------------------------- |
| x + y   | 集合   | x 和 y 的集合                                                |
| x == y  | 相等   | 如果 x 和 y 具有相同的键/值对，则返回 true                   |
| x === y | 恒等   | 如果 x 和 y 具有相同的键/值对，且顺序相同类型相同，则返回 true |
| x != y  | 不相等 | 如果 x 不等于 y，则返回 true                                 |
| x <> y  | 不相等 | 如果 x 不等于 y，则返回 true                                 |
| x !== y | 不恒等 | 如果 x 不等于 y，则返回 true                                 |

以下实例演示了使用一些数组运算符得到的不同结果：

## 实例

```php
<?php
$x = array("a" => "red", "b" => "green"); 
$y = array("c" => "blue", "d" => "yellow"); 
$z = $x + $y; // $x 和 $y 数组合并
var_dump($z);
var_dump($x == $y);
var_dump($x === $y);
var_dump($x != $y);
var_dump($x <> $y);
var_dump($x !== $y);
?>
```



------

## 三元运算符

另一个条件运算符是"?:"（或三元）运算符 。

### 语法格式

```
(expr1) ? (expr2) : (expr3) 
```

对 expr1 求值为 TRUE 时的值为 expr2，在 expr1 求值为 FALSE 时的值为 expr3。

自 PHP 5.3 起，可以省略三元运算符中间那部分。表达式 expr1 ?: expr3 在 expr1 求值为 TRUE 时返回 expr1，否则返回 expr3。

### 实例

以下实例中通过判断 $_GET 请求中含有 user 值，如果有返回 $_GET['user']，否则返回 nobody：

```php
<?php
$test = 'Jser教程';
// 普通写法
$username = isset($test) ? $test : 'nobody';
echo $username, PHP_EOL;

// PHP 5.3+ 版本写法
$username = $test ?: 'nobody';
echo $username, PHP_EOL;
?>
Jser教程
Jser教程
```

**注意：**PHP_EOL 是一个换行符，兼容更大平台。

在 PHP7+ 版本多了一个 NULL 合并运算符，实例如下：

```
<?php
// 如果 $_GET['user'] 不存在返回 'nobody'，否则返回 $_GET['user'] 的值
$username = $_GET['user'] ?? 'nobody';
// 类似的三元运算符
$username = isset($_GET['user']) ? $_GET['user'] : 'nobody';
?>
```

------

## 组合比较符(PHP7+)

PHP7+ 支持组合比较符，实例如下：

```php
<?php
// 整型
echo 1 <=> 1; // 0
echo 1 <=> 2; // -1
echo 2 <=> 1; // 1

// 浮点型
echo 1.5 <=> 1.5; // 0
echo 1.5 <=> 2.5; // -1
echo 2.5 <=> 1.5; // 1
 
// 字符串
echo "a" <=> "a"; // 0
echo "a" <=> "b"; // -1
echo "b" <=> "a"; // 1
?> 
```