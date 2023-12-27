```C#
var names = new List<string> {"<name>", "Ana", "Felipe"};
foreach (var name in names)
{
    Console.WriteLine($"Hello {name.ToUpper()}!");
}
Console.WriteLine();
names.Add("Maria");
names.Add("Bill");
names.Remove("Ana");
foreach (var name in names)
{
    Console.WriteLine($"Hello {name.ToUpper()}!");
}
```
> 문자열 목록을 만들어서 해당 목록에 세 개의 이름을 추가하고 출력함  
> 생성한 컬렉션은 `List<T>` 형식 사용, 요소의 시퀀스를 저장. 꺽쇠 괄호 사이에 요소 형식을 지정함  
> `List<T>` 형식은 늘리거나 줄여 요소를 추가하거나 제거할 수 있음

```C#
Console.WriteLine($"My name is {name[0]}.");
Console.WriteLine($"I've added {name[2]} and {name[3]} to the list.");

Console.WriteLine($"The list has {names.Count} people in it");
```
> `List<T>`를 사용하면 인덱스별로 각 항목을 참조하는 것도 가능  
> `[` 및 `]` 토큰을 사용해 항목에 액세스하며 목록 끝을 지나서 액세스는 불가능  
> `Count` 속성을 사용해서 목록의 길이 확인 가능  
> C#의 인덱스는 0부터 시작하며, 가장 큰 유효 인덱스는 목록의 항목 수보다 하나 작음

```C#
var index = names.IndexOf("Felipe");
if (index != -1)
{
  Console.WriteLine($"The name {names[index]} is at index {index}");
}
var notFound = names.IndexOf("Not Found");
Console.WriteLine($"When an item is not found, IndexOf returns {notFound}");
```
> `IndexOf` 메서드는 항목을 검색하고 항목의 인덱스를 반환
> 목록에 항목이 없으면 `IndexOf`는 `-1`을 반환

```C#
names.Sort();
foreach (var name in names)
{
  Console.WriteLine($"Hello {name.ToUpper()}!");
}
```
> `Sort` 메서드는 일반적인 순서로 목록의 모든 항목을 정렬

```C#
var fibonacciNumbers = new List<int> {1, 1};
```
> 정수 목록을 만들고 처음 두 정수를 값 1, 1로 설정

```C#
var fibonacciNumbers = new List<int> {1, 1};

while (fibonacciNumbers.Count < 20)
{
    var previous = fibonacciNumbers[fibonacciNumbers.Count - 1];
    var previous2 = fibonacciNumbers[fibonacciNumbers.Count - 2];

    fibonacciNumbers.Add(previous + previous2);
}
foreach(var item in fibonacciNumbers)
{
    Console.WriteLine(item);
}
```
> **피보나치 수열 예시**
