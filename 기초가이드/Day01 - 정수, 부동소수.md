```C#
int a = 18;
int b = 6;
int c = a + b;
Console.WriteLine(c);

int c1 = a - b;
int c2 = a * b;
int c3 = a / b;
```
> `int` 형식은 정수를 의미함  
> `+`, `-`, `*`, `/` 사용은 다른 언어와 일치

```C#
int a = 5;
int b = 4;
int c = 2;
int d = a + b * c;
Console.WriteLine(d);

int d1 = (a + b) - 6 * c + (12 * 4) / 3 + 12;
```
```C#
int a = 7;
int b = 4;
int c = 3;
int d = (a + b) / c;
Console.WriteLine(d)
```
> 수학 연산은 연산 규칙에 따름

```C#
int a = 7;
int b = 4;
int c = 3;
int d = (a + b) / c;
int e = (a + b) % c;
Console.WriteLine($"quotient: {d}");
Console.WriteLine($"remainder: {e}");
```
> `%` 연산을 통해 나머지를 얻을 수 있음

```C#
int max = int.MaxValue;
int min = int.MinValue;
Console.WriteLine($"The range of integers is {min} to {max}");

int what = max + 3;
Console.WriteLine($"An example of overflow: {what}");
```
> C# 정수 형식, `int` 형식에는 **최소 한도**와 **최대 한도**가 존재함  
> 계산이 해당 한도를 초과하게 되면 **언더플로**나 **오버플로** 발생

```C#
double a = 5;
double b = 4;
double c = 2;
double d = (a + b) / c;
Console.WriteLine(d);
```
```C#
double a = 19;
double b = 23;
double c = 8;
double d = (a + b) / c;
Console.WriteLine(d);
```
> `double`: **부동 소수점 수**: 아주 크거나 정수가 아닌 수를 나타낼 때 유용함  
> **배정밀도**: 값을 저장하는 데 사용되는 **이진 자릿수를 설명**하는 상대 용어  
> 배정밀도의 이진 자릿수는 **단정밀도의 2배**  
> 단정밀도 숫자는 `float` 키워드로 선언됨

```C#
double max = double.MaxValue;
double min = double.MinValue;
Console.WriteLine($"The range of double is {min} to {max}");
```
> `double`의 값의 범위는 정수 값보다 훨씬 크기에 많은 수 표현이 가능함  
> 큰 값은 과학적 표기법으로 출력됨  
> `E` 좌측 숫자 -> **유효 숫자**, 오른쪽 숫자는 **지수이며 10의 배수**임

```C#
double third = 1.0 / 3.0;
Console.WriteLine(third);
```
> 수학 10진수와 마찬가지로 C#에서 `double`에는 **반올림 오류**가 발생할 수 있음

```C#
decimal min = decimal.MinValue;
decimal max = decimal.MaxValue;
Console.WriteLine($"The range of the decimal type is {min} to {max}");
```
> `decimal` : 범위가 작지만 `double`보다 **전체 자릿수**가 큼

```C#
double a = 1.0;
double b = 3.0;
Console.WriteLine(a / b);

decimal c = 1.0M;
decimal d = 3.0M;
Console.WriteLine(c / d);
```
> 소수점 형식으로 사용하는 수학에는 소수점 오른쪽에 더 많은 숫자가 존재함  
> 숫자의 `M` 접미사로 상수가 `decimal` 형식을 사용해야 한다고 알림. 없을 시 컴파일러는 `double` 형식으로 인지함

```C#
double radius = 2.50;
double area = Math.PI * radius * radius;
Console.WriteLine(area);
```
> 반지름이 2.5센티미터인 원의 면적 계산  
> .NET 형식의 VS 파일에는 `Math.PI`라는 PI 상수가 포함되어 있음  
> `Math.PI`는 `System.Math` 네임스페이스와 마찬가지로 `double` 값임  
> 그러므로 `decimal` 대신 `double` 사용
