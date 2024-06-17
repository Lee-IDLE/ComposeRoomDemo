Compose에서 Room 사용법을 알기 위한 공부용 데모 프로젝트입니다.

1. Gradle에서 필요한 설정이 뭐가 있는지 확인
 - plugins에서 "androidx.room"과 "kotlin-kapt" 추가
 - dependencies에서 "room-runtime", "room-ktx", "room-livedata"과 annotationProcessor로 "room-compiler"와 kapt로 "room-compiler" 설정
 - 코루틴 사용을 위한 "coroutines-core", "coroutines.android" 설정
 - 컴포즈 ViewModel 사용을 위한 "viewmodel-compose" 설정
2. Entity 파일 생성 (데이터베이스에 있는 하나의 테이블을 클래스로 정의)
3. DB에 insert, delete 등의 기능을 정의한 DAO(Database Access Object) 인터페이스 생성
4. DAO 객체를 만들기 위한 ~Database 파일 생성
  - 어떤 방식으로 만드는지 확인
5. Insert나 Delete등 DB에 직접 데이터를 조작할 때는 메인 스레드에서 하면 안 되므로,
 다른 스레드에서 실행되도록 ~Repository 파일을 준비
 - CoroutineScope을 사용 방식을 확인
 - 검색기능(findProduct)에서 비동기를 위한 await기능 사용 방법 확인
