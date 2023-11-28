# 컬렉션
컬렉션은 여러 값을 하나의 변수에 저장할 수 있는 타입을 의미함

### 주요컬렉션
- LIST: 여러 값을 순서대로 저장하고, 인덱스 번호로 접근 가능한 컬렉션 타입(파이썬의 리스트와 유사함)
- MAP: '키'와 '값'의 형태로 저장하고 '키'를 기반으로 매칭되는 '값'을 바로 접근 가능한 컬렉션 타입(파이썬의 사전과 유사함)
- Set: 중복된 데이터를 제거하고 데이터를 저장하는 컬렉션 타입(파이썬의 집합과 유사함)

### LIST 
- CRUD:Create, Read, Update, Delete

```dart
void main() {
  //Create(생성)
  //리스트에 넣을 타입을 <>에 명시
  List<String> myList = ['Dave', 'FunCoding'];
  print(myList);
  
  myList.add('David');//add() 아이템 추가
  print(myList);
  
   //Read
  print(myList);
  print(myList[0]);
  
  //update
  myList[0] = 'heejung choi';
  print(myList);
  
  //delete
  myList.remove('David');
  print(myList);
  print(myList[1]);
  myList.removeAt(1);
  print(myList);
  
  //사이즈 확인
  print(myList.length);
}  
```
```dart
void main() {
  List<int> myList = [10,20,30,40];
  //myList.removeRange(0,2); //0부터 시작해서 -1에 해당하는 것까지 삭제(10,20)삭제
  //print(myList);
  
  //조건에 맞는 아이템만 가져오는 기능
  //리스트변수.where((각아이템을 저장할 변수) => 조건)
  print(myList.where((item) => item >30)); //(40)
  
  //리스트변수.removeWhere((각아이템을 저장할 변수)=>조건)
  //조건에 맞는 아이템만 삭제하는 기능
  myList.removeWhere((item) => item < 15);
  print(myList);
  
  //리스트변수.map((각아이템을 저장할 변수) => 각아이템변경구문)
  //각 아이템을 일괄적으로 변경하고 싶을 때 유용하게 활용 가능
  //단, 리턴값은 리스트가 아닌 Iterable 클래스
  //Iterable클래스는 컬렉션 공통클래스로 리스트로 변환하려면 toList()로 사용해야함
  //타입을 특정하지 않는 var/final로 리턴값을 받아서 저장가능
  var myList2 = myList.map((item) => item + 15); 
  print(myList2.toList());//toList로 저장한다고 해서 리스트가 된것은 아니다. 아래 List3처럼 리스트로 변환해줘야 한다.
  print(myList2);
  
  List<int> myList3 = myList2.toList();
  print(myList3);
  
  //리스트변수.clear()
  //리스트에 들어 있는 전 아이템 삭제
  myList.clear();
  print(myList);
}
```
