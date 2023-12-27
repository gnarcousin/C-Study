```C#
int a = 5;
int b = 6;
if ( a + b > 10 )
    Console.WriteLine("The answer is greater than 10.");
```
> `if`의 기능과 `bool` 형식을 보여줌  
> `bool`은 `true` or `false`의 값 중 하나이며 값이 `true`인 경우에만 `if` 뒤의 명령문 실행

```C#
int a = 5;
int b = 3;
if (a + b > 10)
{
    Console.WriteLine("The answer is greater than 10");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
}
```
> **들여쓰기와 공백은 C#에서 중요하게 취급하지 않음** -> `{` 및 `}`을 사용해 블록 표현이 더 중요  
> `if` 또는 `else` 키워드는 조건에 따라 실행되며 일반적으로 모든 `if else` 절에서 중괄호를 사용함

```C#
int a = 5;
int b = 3;
int c = 4;
if ((a + b + c > 10) && (a == b))
{
    Console.WriteLine("The answer is greater than 10");
    Console.WriteLine("And the first number is equal to the second");
}
else
{
    Console.WriteLine("The answer is not greater than 10");
    Console.WriteLine("Or the first number is not equal to the second");
}
```
> `==` 기호는 같음을 의미. `&&` 기호는 `AND`를 의미. `||` 기호는 `OR`을 의미
> `true` 분기에서는 위 조건 모두가 `true`여야 실행함  
> `{` 및 `}`로 문을 엮으면 각 조건부 분기에 여러 문을 지닐 수 있음

```C#
int counter = 0;
while (counter < 10)
{
  Console.WriteLine($"Hello World! The counter is {counter}");
  counter++;
}
```
> `while`문은 조건을 확인하고 뒤의 명령문을 실행해 조건이 `false`가 될 때까지 반복
> `false` 설정이 없을 시 **무한 루프의 위험성**이 있음
> `counter`변수 뒤의 `++`는 증가 연산자를 의미함

```C#
int counter = 0;
do
{
    Console.WriteLine($"Hello World! The counter is {counter}");
    counter++;
} while (counter < 10);
```
> `while` 루프는 뒤의 코드를 실행하기 전에 조건을 테스트함
> `do`...`while` 루프는 코드를 먼저 실행하고 뒤의 조건을 확인함

```C#
for (int counter = 0; counter < 10; counter++)
{
  Console.WriteLine($"Hello World! The counter is {counter}");
}
```
> `for`문에는 **for 이니셜라이저, for 조건, for 반복기**라는 작동 방식 제어가 존재함  
> **for 이니셜라이저** = 루프 변수를 선언, 첫번째 값 지정  
> **for 조건** = `for` 문에 대한 조건 지정  
> **for 반복기** = `for`문 다음 블록을 실행한 후 변수를 수정하는 방법 지정  
>  `foreach`문의 경우 컬렉션과 주로 사용되므로 다음 자습서에서 설명

```C#
for (int row = 1; row < 11; row++)
{
  for (char column = 'a'; column < 'k'; column++)
  {
    Console.WriteLine($"The cell is ({row}, {column})");
  }
}
```
> **루프 중첩**: 한 루프를 다른 루프 안에 중첩하여 쌍을 구성할 수 있음

```C#
int sum = 0;
for (int number = 1; number < 21; number++)
{
  if (number % 3 == 0)
  {
    sum = sum + number;
  }
}
Console.WriteLine($"The sum is {sum}");
```
> `for`문 + `if`문
