# 연산자
### 사칙연산
```dart
void main() {
  print(1 + 2);
  print(1 - 2);
  print(1 * 2);
  print(1 / 2);
  print(5 % 2);//나머지
  print(5 ~/ 2);//몫 
}```


### 증감연산자
```dart
void main() {
  int a = 1;
  a = a + 1;
  print(a);
  
  print(++a);
  print(a++);
  print(a);
  
}```

###할당/비교연산자

```dart
void main() {
  num data = 1;
  data += 5;
  print(data);  
  
  data *= 2;
  print(data);
  
  data /= 2;
  print(data);
  
  data ~/= 4; //~ 몫
  print(data);
  
  if(data == 1){
    print('같습니다');
  }
  
  print(data == 1);
  print(data != 1);
}
```

### 타입 검사 연산자
- is: 객체가 특정 타입이면 ture
- is!: 객체가 특정 타입이면 false

```dart
void main() {
  num data = 1;
  print(data is num);
  print(data is! num);
  
  print(data > 1);
  print(data < 1);
  print(data <= 1);
}```

