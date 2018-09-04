# Node Study

### 3. This
- 전역공간에서의 this는 전역객체를 의미한다.
  - window, global
  - 함수 내부에서 this를 호출하면 기본적으로 전역객체가 등장하고 메소드 호출 시 메소드 호출 주체가 호출 됨
  
  #### ex)
  ```
  var a = {
    b: {
      c: function() {
        console.log(this);
       }
    }
  }
  a.b.c();
  ```
  #### return
  ``` return
  Object { c: function}
    c: function ()
    __ proto__ : Object
  ```
        
    
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
