[
前端js——键盘事件、获取键盘输入、组合按键执行动作](https://blog.csdn.net/qq_41141657/article/details/88653915
)
## Q1 编程实现，班上期末成绩平均分评级，95及以上为卓越；85及以上且小于95为优秀；75及以上且小于85为一般；60及以上且小于75为及格；其余为不合格；请用适当的语句实现上述描述，打印输出评级文字。
代码：
```
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <script type="text/javascript">
    function grade() {
      var input = document.getElementById("value").value;
      if (input >= 95) {
        console.log("卓越");
      } else if (input >= 85 && input < 95) {
        console.log("优秀");
      } else if (input >= 75 && input < 85) {
        console.log("一般");
      } else if (input >= 60 && input < 75) {
        console.log("及格");
      } else if (input < 60) {
        console.log("不合格");
      }

    }

  </script>
</head>

<body>
  <input type="text" id="value" placeholder="请输入成绩" />
  <input type="button" value="等级" onclick="grade()" />
</body>

</html>
```
## Q2 编程实现，有一简易计算器，最终输出结果是：当运算符是+时，为两值相加；当运算符是-时，为两值相减；当运算符是*时，为两值相乘；当运算符是/时，为两值相除；当运算符是%时，为两值相除的余数；请用适当的语句实现上述描述，结果打印输出，假设两值固定为：var x = 10, y = 8;，运算符变量设为 var operator; 。
```
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <script type="text/javascript">
    function grade() {
      var x = 10, y = 8;
      var operator = document.getElementById("value").value;
      switch (operator) {
        case "+":
        document.write(x+y);
        break;
        case "-" :
        document.write(x-y);
        break;
        case "*" :
        document.write(x*y);
        break;
        case "/" :
        document.write(x/y);
        break;
        case "%" :
        document.write(x%y);
        break;
        default :
        document.write("输入运算符有误");
      }

    }

  </script>
</head>

<body>
  <input type="text" id="value" placeholder="请输入运算符" />
  <input type="button" value="结果" onclick="grade()" />
</body>

</html>
```
## Q3 编程实现，求整数1~100的累加值，但要求跳过所有个位为3的数。
结果是`4570`
```
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <script type="text/javascript">
    function grade() {
      var sum = 0;
      for (var i = 1; i < 101; i++) {
        if (!(i % 10 == 3)) {
          sum += i;
        }
      }
      document.write(sum);
    }
  </script>
</head>

<body>
  <label for="result">1~100中除了个数为3的和:</label><br />
  <input type="button" id="result" value="结果" onclick="grade()" />
</body>

</html>
```

## Q4 编程实现，打印输出如下效果：
![image.png](https://upload-images.jianshu.io/upload_images/20166506-047b95f8f81ce798.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <script type="text/javascript">
    for (var i = 0; i < 6; i++) {
      for (var j = i; j < 6; j++) {
        document.write("* ");
      }
      document.write("<br/>");
    }
  </script>
</head>

<body>
</body>

</html>
```
## Q5 编程实现，打印输出 99乘法表，如图：
![image.png](https://upload-images.jianshu.io/upload_images/20166506-3f0c4aa2051a46a8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
<!DOCTYPE html>
<html>

<head>
  <meta charset="UTF-8" />
  <script type="text/javascript">
    for (var i = 1; i <= 9; i++) {
      for (var j = 1; j <= i; j++) {
        document.write(i + "*" + j + "=" + i * j + "&nbsp&nbsp&nbsp&nbsp");
      }
      document.write("<br/>");
    }
  </script>
</head>

<body>
</body>

</html>
```

