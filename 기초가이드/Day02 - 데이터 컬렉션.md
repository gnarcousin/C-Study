```C#
var names = new List<string> {"<name>", "Ana", "Felipe"};
foreach (var name in names)
{
    Console.WriteLine($"Hello {name.ToUpper()}!");
}
```
> 문자열 목록을 만들어서 해당 목록에 세 개의 이름을 추가하고 출력함  
> 생성한 컬렉션은 List<T> 형식 사용, 요소의 시퀀스를 저장. 꺽쇠 괄호 사이에 요소 형식을 지정함

```C#
