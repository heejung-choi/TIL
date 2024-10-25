# 조건문

### if
```dart
void main() {
  int data = 1;
  if(data > 0){
    print('0보다큽니다.');
  }else{
    print('0보다작습니다.');
  }
}
```

### switch
```dart
void main() {
  int data = 3;
  switch(data){
    case 1:
      print("1111");
      break;
    case 2:
      print("2222");
      break;
    default:
      print("1과 2가 아니다");      
  }
}
```

### 삼항연산자
(조건식) ? 참일 경우 실행 : 거짓일 경우 실행;
```dart
void main() {
  int data = 10;
  (data > 0) ? print('양수') : print('음수');
  
}```