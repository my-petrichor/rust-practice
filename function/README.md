## 函数
### 命名
    和 golang 的驼峰法不同，rust 使用的是 snake case 规范风格，即小写字母和下划线结合命名，例 say_hello
### 声明
    函数声明的时候，类型注解是必须的；又返回值的时候，使用 -> [类型]，表示返回值类型；x + y 是表达式(末尾没有分号)不是语句
    fn sum(x: i32, y: i32) -> i32 {
        x + y
    }
    或
    fn sum(x: i32, y: i32) -> i32 {
        return x + y;
    }
### 语句
    语句是执行一些操作但不返回值，如下
    let x = 8;
### 表达式
    表达式是计算并返回一个值，表达式的结尾没有分号，如
    let x = {
        let a = 1;
        a + 1
    }
