# Node Study

### 3. This
  - 전역공간에서의 this는 전역객체를 의미한다.
    - window, global.
    - 함수 내부에서 this를 호출하면 기본적으로 전역객체가 등장하고 메소드 호출 시 메소드 호출 주체가 호출 됨.

      #### 메소드 호출시)
      ```
      1) var a = {
        b: function() {
            console.log(this);
        }
      }
      a.b();

      1_return)
        Object {b: function}
          b: function ()
          __ proto__ : Object

      2) var a = {
        b: {
          c: function() {
            console.log(this);
           }
        }
      }
      a.b.c();

      2_return)
        Object {c: function}
          c: function ()
          __ proto__ : Object
      ```
      => A.()의 this는 A, a.b.c()의 this는 a.b()

  - 콜백함수에서의 this
    - 콜백함수도 함수이기 때문에 this는 전역객체를 바라본다.
    - 콜백의 제어권을 넘겨받은 함수나 메서드가 다른 곳을 명시하면 전혀 다른 값이 나옴.
    - 생성자 함수에서의 this는 인스턴스

  - 정리
    - 전역공간: window/global
    - 함수 내부: window/global
    - 메소드 호출시: 메도스 호출 주체
    - callback: 기본적으로는 함수내부와 동일
    - 생성자 함수: 인스턴스
  
### 4. Closure
  - Closure란 함수와 그 함수가 선언될 당시의 환경정보 사이의 조합 (SCOPE)
    - 함수 내부에서 생성한 데이터와 그 유효범위로 인해 발생하는 특수한 상태
    - Scope에서 외부에 정보를 제공할 수 있는 유일한 수단은 Return
    - 최초 선언시의 정보를 유지함으로서 접근권한 제어, 지역변수 보호, 데이터 보존 및 활용 가능
    - Scope는 정의될 때 결정.
  - Closure를 이용한 Private Member
    - 1. 함수에서 지역변수 및 내부함수 등을 생성한다.
      2. 외부에 노출시키고자 하는 멤버들로 구성된 객체를 return한다.
        -> return한 객체에 포함되지 않은 멤버들은 private.
        -> return한 객체에 포함된 멤버들은 public
  - 정리
    - 외부에 노출하고자 하는 데이터들만 리턴하면 리턴하지 않은 데이터들은 외부에서의 접근을 제어.
      - 지역변수 보호
      - 외부에서 지역변수의 변경 권한을 부여함으로서 데이터 활용 가능
      
     

