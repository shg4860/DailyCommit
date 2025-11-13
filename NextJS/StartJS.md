# = Login Logic을 위한 JS의 라이브러리들 = 

Express.js = FastAPI 
Frisma = SQLAlchemy 
Zod (or Joi) = Pydantic
bcryptjs = bcrypt



# Print vs console.log 
Python : 
  print("Hello", 1234, var1)
JS :
  console.log("Hello", 1234, var1) 



# 변수 선언 
const :  상수. 한번 할당하면 그 후로 바꿀 수 없다. 
let : 변수. 나중에 값을 바꿀 수 있다. 

예 ) 
const name = "SHK" ;
let age = 20; 
age = 21;  (바꾸기 가능) 

// name = "송희경"; << !Error!  상수 바꾸기 X 



# 중괄호 vs 들여쓰기
파이썬 : 들여쓰기로 코드블록 
JS : 중괄호로 코드블록 (들여쓰기 필수 X But 가독성을 위해...)



# 함수 선언 (def vs function) 
Python :
  def add(a,b) : 
    return a + b 
JS : 
  fonction add(a,b){ 
    return a + b ;
  }
JS (화살표 함) : 
  const add = (a, b) => {    << const 대신 let을 쓸 수 있지만 함수의 기능이 바뀌면 프로그램이 꼬일 수 있으니 const를 쓴다.
    return a + b ; 
  }



# Dict vs Object 
파이썬의 Dictionary와 똑같은 게 Object
Python : 
  user = { 
  "username" : "희경",  // 파이썬에서 key값으로 못 쓰는 것 : list, dict 같은 mutable type 
  "age" : 30 
  }
  print(user["age"])

  
JS : 
  const keyname = "age"; 
  const user = { 
    username : "희경" ,  // JS에선 Key 값에 따옴표 안 붙여도 됨  
    age : 30 
  }; 
  console.log(user.username);
  console.log(user["username"]); 

 이러면 결과로 { age : 30 } 이 아닌 { username : 30 } / keyname이 변수가 아닌 키 그 자체가 되어버림 
 
 _ 해결법 _ 
   const user = { 
    [username] : "희경" ,  // 괄호로 감싸면 변수로서 사용됨
    age : 30 
  }; 
  혹은 추가할 때 user[keyname] = 30; 쓰기 



# List vs Array 
파이썬의 List는 JS에서의 Array이다. 사용법은 같다.
Python :
  my_list = [1, "hello~", True]   (파이썬의 tuple 안에 변수는 못 들어감 
JS : 
  const my_Array = [10, "Hello~", ture];   

+ )
  Q. 튜플이나 딕셔네리 키 값으로 변수 써도 됨? 
  A. 가능! 변수는 이름표이고 값은 데이터가 담긴 상자(list 등..) 혹은 데이터(str, int, tuple 등..)이다.
     변수가 재할당 되는 것은 이름표가 다른 상자 혹은 데이터에 가서 붙은 것이다.
     다른 데이터에 가서 붙는 것이지 데이터 자체가 바뀌는 건 아니기 때문에 immutable -> 튜플이나 key 값으로 사용 가능
     But list나 Dict는 상자 속 데이터가 바뀔 수 있기 때문에 mutable -> 튜플이나 key 값으로 사용 불가
     애초에 튜플에 변수가 들어가면 그 변수가 가지고 있는 값을 튜플에 넣는 것이다. 


# import (모듈 가져오기) 
Python :
  _ in a.py 
    my_var = 10
  _ in b.py 
    from a import my_var  
JS : 
  _ in a.js 
    export const my_var = 10;
  _ in b.js 
    import {my_var} from './a.js';  




  
  
