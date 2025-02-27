# 컬렉션
컬렉션은 여러 값을 하나의 변수에 저장할 수 있는 타입을 의미함

### 주요컬렉션
- LIST: 여러 값을 순서대로 저장하고, 인덱스 번호로 접근 가능한 컬렉션 타입(파이썬의 리스트와 유사함)
- MAP: '키'와 '값'의 형태로 저장하고 '키'를 기반으로 매칭되는 '값'을 바로 접근 가능한 컬렉션 타입(파이썬의 사전과 유사함)
- Set: 중복된 데이터를 제거하고 데이터를 저장하는 컬렉션 타입(파이썬의 집합과 유사함)

## LIST 
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
## map
- CRUD: Create, Read, Update, Delete

```dart
void main() {
  //create
  //map에 넣을 타입을 키/값 각각 <키타입, 값타임>에 명시
  Map<String, int> myDict = {
    'DaveLee': 1,
    'Funcoding': 2,
    'David': 3      
  };
  
  print(myDict);
  print(myDict.runtimeType);
  myDict['Kate'] = 4;//새로운 키와 값으로 키/값 추가 가능
  
  //Read
  print(myDict['kate']);
  print(myDict.keys);  //키 만 가져오기
  print(myDict.values);//값 만 가져오기
  print(myDict.entries);//키/값 모두 가져오기
  
  var myDictKeys = myDict.keys;
  List<String> myDictKeyList = myDictKeys.toList() ;
  print(myDictKeyList);
  
  //Update
  myDict['DaveLee'] = 4;
  print(myDict);
  
  //Delete
  myDict.remove('DaveLee');
  print(myDict);
}
```

추가자료
```dart
void main() {
  //create
  //map에 넣을 타입을 키/값 각각 <키타입, 값타임>에 명시
  Map<String, int> myDict = {
    'DaveLee': 1,
    'Funcoding': 2,
    'David': 3      
  };
  
  //Map에 특정 키/값이 있는지 확인하는 기능
  print(myDict.containsKey('DaveLee'));
  print(myDict.containsValue(5));
  
  //Map 변수에 또다른 Map 변수 일괄추가
  Map<String, int> myDict2 = {
    'korea' : 1,
    'Japan' : 2
  };
  
  myDict.addAll(myDict2);
  print(myDict);
 
}```

## Set
- CRUD: Create, Read, Update(x), Delete
- 집합은 수정은 안되며, 인덱스 번호로 아이템을 접근할 수 없음

```dart
void main() {
  //create
  Set<String> data = {'a','b','c'};
  
  data.add('d');
  print(data);
  data.add('a');//중복은 안들어감
  print(data);
  
  //Read
  print(data);
  
  //Delete
  data.remove('a');
  print(data);
}```

```dart
void main() {
  //create
  //set에 넣을 타입을 <>에 명시
  Set<String> data1 = {'a','b','c'};
  Set<String> data2 = {'b','c','d'};
  
  print(data1.contains('a'));
  print(data1.containsAll(['a','b']));
  print(data1.containsAll(['a','b','d']));
  print(data1.length);
  
  //교집합
  var data3 = data1.intersection(data2);        
  print(data3);
  //차집합
  var data4 = data1.difference(data2);
  print(data4);
}```