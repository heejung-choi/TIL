Ctrl+shift+v -> Preview 모드로 md 볼수있음

프로그래밍 언어
- 변수
- 조건문
- 반복문
- 함수:이름(인자)

1) 주석
```dart
//메인함수
void main() {
  print('hello world');
  print("hello world 2");
}
//한줄주석
/*
여러줄 주석
*/
```

2) 변수

주요 type
-  int형: 정수
-  double형: 실수
-  String형: 문자열
-  bool형 true 또는 false


```dart 
void main() {
//변수명은 lowerCamelCase 네이밍을 추천
//다른 프로그램의 경우 초기값이 없는 경우도 있는데 flutter가 3.0오면서 null safety가 올 수 있기 때문에 값을 무조건 넣어준다고 생각하고 넣어야 한다. 
  int myAge = 26;
  double myHeight = 181.8;
  String myName = 'Dave Lee';
  bool military = true;

  print(myAge);
  print(myName);  
  
  myName = 'heejung';
  print(myName);
  
  print('my age is $myAge, and my height is $myHeight');
  print('my age is ${myAge}, and my military is ${military}');
  
  //myAge = 100.1
  //int에 double값을 넣으면 자동으로 형변환 해주는 프로그래밍 언어도 있는데 dart의 경우에는 자동형변환을 해주지 않는다.
}
```
 특수타입
- num형: int 형과 double형 모두 대입 가능하다.
- var형: 특정 타입을 지정하지 않고 해당 변수에 대입하는 값을 기반으로 타입이 지정된다. 
    - 동적타입: var 변수명;으로 선언하면 다양한 타입의 값을 대입할 수 있음
    - var 변수명 = 값;으로 선언하면 해당 값에 맞는 타입으로 고정되어, 이후에는 다른 타입의 값을 대입할 수 있음

- dynami형: dynamic으로 선언하면, 모든 타입의 데이터를 대입할 수 있음 처음부터 값을 넣어줘도 다른 타입의 값을 대입 할 수 있다.

```dart 
void main() {
  num myAge = 26;
  myAge =25.1;
  print(myAge);
  
  var no;
  no = 1;
  print(no);
  no = 'hello';
  print(no);
  
  var ex = 1;
  print(ex);
  //ex = 'hello'; 에러 발생

  dynamic non = 1.1;
  non = 1;
  non = 'hello';
  print(non);
}

```

- final, const 키워드
  - 둘다 고정된 값으로 변수를 사용하기 위해 선언
  - final은 런타임 시점에 고정 값이 대입됨 (가능하면 const가 컴파일 시점에 값이 대입되므로 성능상이점이 있음)
  - const는 컴파일 시점에 고정 값이 대입됨
성능상의 이점은 const가 더 있다. 이미 컴파일 때에 고정하고 나서 런을 했기 때문에
그러나 컴파일 시점에 고정값을 넣을 수 없는 경우도 있다.

```dart
void main() {
  num myAge = 26;
  final String myName = 'Dave';
  const String lastName = 'Lee';
  
  bool military = true;
  
  //myName = 'David';
  //final로 선언한 변수는 새로운 값을 대입할 수 없음
  
  //lastName = 'choi';
  //const로 선언한 변수는 새로운 값을 대입 할 수 없음
}
```


```dart
void main() {
  num myAge = 26;
  final String firstname = 'Dave';
  const String lastName = 'Lee';
  
  final name1;
  name1 = 1; //처음 선언한 값으로 타입도 자동지정 가능
  //name1 = 2; final로 선언한 변수는 새로운 값을 대입할 수 없음 
  
  const name2 = 1; //정수로 데이터 타입이 정해짐
  
  print(DateTime.now()); //실행이 되어야 만들어지는 값인데(객체지향의 개념)
  //이럴때는 final만 가능하다.
  
  //const time1 = DateTime.now();
  final time1 = DateTime.now();
  print(time1); 
}
```

연습
```dart
void main() {
  int num1 = 10;
  double num2 = 10.5;
  int num3;
  
  num3 = num1;
  print(num3);
  //num3 = num2;
  print(num3);
  
  
  var num4;
  num4 = 1;
  print(num4);
  num4 = 2.2;
  print(num4);
  num4 = true;
  print(num4);
  
  var data = 'DaveLee';
  //date = 1; var 선언시 값을 대입하면, 해당값에 맞는 타입으로 고정됨
}  

```