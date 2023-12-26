# MS C# 자습서

```C#
Console.WriteLine("Hello World");
/*
C#의 기본 출력은 Console.WriteLine으로 이루어짐
Console = 콘솔 창을 나타내는 형식
WriteLine = 텍스트를 해당 텍스트 콘솔에 출력함
*/

string aFriend = "Bill";  // 문자열 자료형 변수 지정
Console.WriteLine(aFriend);
aFriend = "Maira";        // 선언한 변수에 여러 값을 할당 가능함. 이 때 변수의 선언과 초기 할당은 유지되어야 함.
Console.WriteLine(aFriend);
Console.WriteLine("Hello" + aFriend); // +를 이용해 변수 및 상수 문자열 추가 가능
Console.WriteLine($"Hello {aFriend}");
/*
문자열 보간 = { 및 } 문자 사이에 변수를 배치해 텍스트를 변수 값으로 바꾸도록 함
문자열의 여는 따옴표 앞에 $를 추가해 중괄호 사이 문자열 안에 변수 포함 가능
*/

string firstFriend = "Maria";
string secondFriend = "Sage";
Console.WriteLine($"My friends are {firstFriend} and {secondFriend}"); // 중괄호 사이에는 단일 변수로 제한되지 않음

Console.WriteLine($"The name {firstFriend} has {firstFriend.Length} letters.");
Console.WriteLine($"The name {secondFriend} has {secondFriend.Length} letters.");
/*
Length = 문자열의 길이를 찾음, 문자열의 속성이며 해당 문자열의 문자 수를 반환함
*/

string greeting = "     Hello World!        ";
Console.WriteLine($"[{greeting}]");

string trimmedGreeting = greeting.TrimStart(); //
Console.WriteLine($"[{trimmedGreeting}]");

trimmedGreeting = greeting.TrimEnd();
Console.WriteLine($"[{trimmedGreeting}]");

trimmedGreeting = greeting.Trim();
Console.WriteLine($"[{trimmedGreeting}]");

/*
문자열에서 공백을 잘라내는 것 = Trim 사용. 이때 TrimStart나 TrimEnd를 지정할 수 있는데
각각 좌측의 공백이나 우측의 공백을 지워주는 역할을 함. 지정 안하면 둘 다 지워줌
Trim은 새 문자열을 만들어 반환하나 원래 메시지를 변경하진 않음
*/

string sayHello = "Hello World!";
Console.WriteLine(sayHello);
sayHello = sayHello.Replace("Hello", "Greetings");
Console.WriteLine(sayHello);

Console.WriteLine(sayHello.ToUpper());
Console.WriteLine(sayHello.ToLower());

/*
Replace 메소드는 두 매개 변수를 사용해 검색할 텍스트, 바꿀 텍스트 순으로 작성
ToUpper, ToLower를 활용하면 대소문자 작성에 편리
*/

string songLyrics = "You say goodbye, and I say hello";
Console.WriteLine(songLyrics.Contains("goodbye"));
Console.WriteLine(songLyrics.Contains("greetings"));

Console.WriteLine(songLyrics.StartsWith("You"));
Console.WriteLine(songLyrics.StartsWith("goodbye"));

Console.WriteLine(songLyrics.EndsWith("hello"));
Console.WriteLine(songLyrics.EndsWith("goodbye"));

/*
Contains는 검색한 문자열을 찾았는지에 대한 bool값을 반환해줌
StartsWith, EndsWith으로 비슷한 작동이 가능하다
*/
```
