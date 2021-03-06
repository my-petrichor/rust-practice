## 变量
    使用 let 声明的变量默认情况下是不可变的(immutable)
    使用 let mut 声明变量是可变的(mutable)

## 常量 
    const 关键字声明常量
    注意：const 声明常量时必须指明类型

## 为何如此设计
    想象以下场景，在一段程序中我们声明了一个变量，并且预测它之后不会再改变。但是另一段使用此变量的程序有时会将变量值更改，
    这种情况下就会出现 bug,而且由于是有时会更改变量，debug 的难度更大,所以 rust 默认是声明 immutable 变量

## 数据类型
### 整数型
    默认为 int32，isize 和 usize 长度跟随系统架构变化，32 位就是 i32 或 u32，64 位就是 i64 或 u64
|长度|有符号|无符号|
|----|----|----|
|8-bit|i8|u8|
|16-bit|i16|u16|
|32-bit|i32|u32|
|64-bit|i64|u64|
|128-bit|i128|u128|
|arch|isize|usize|

### 整型字面值
|数字字面值|例子|
|----|----|
|Decimal(十进制)|98_111|
|Hex(十六进制)|0xff|
|Octal(八进制)|0o77|
|Binary(二进制)|0b1111_0000|
|Byte(u8)|b'A'|

### 浮点型
    只有单精度 f32 和双精度 f64，默认为 f64

### 布尔型
    bool 和 false

### 字符类型
    char 类型，单引号包裹，占 4 字节

### 元组类型
    多种类型的一个聚合，使用 () 表示
#### 声明
    let tup: (i32, f64) = (200, 4.1);
    或
    let tup = (200, 4.1);
#### 解构
    let tup = (200, 4.1);
    let (x, y) = tup;
#### 访问元组元素
    使用点号(.)后跟索引访问值
    let tup = (200, 4.1);
    let first_value = tup.0;
    let second_value = tup.1;

### 数组类型
    相同类型的一个聚合，使用 [] 表示
#### 声明
    let array: [i32, 3] = [1, 2, 3]；
    或
    let array = [1, 2, 3];
    
#### 访问数组元素
    let array = [1, 2, 3];
    let first = array[0];
    let second = array[1];
    