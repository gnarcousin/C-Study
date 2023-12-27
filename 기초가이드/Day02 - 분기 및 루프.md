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
