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
        
    
- 
- 랩탑
- 시간
- 열정
- 카페인

### Coverage
- Javascript ES5, ES6
- Javascript core
- AWS EC2, AWS RDS, AWS S3, AWS SQS, AWS rekognition
- RDBMS (MySQL, MariaDB), NoSQL(MongoDB), Redis
- CI/CD

### 최종 세미나 주제
- AWS 인프라를 사용하여 API 서버 구축및 배포하기

### 스터디 방향
- JS의 기초를 학습한다.
- 기초부터 학습하여 간단한 백엔드 외주를 할 정도까지 학습한다
