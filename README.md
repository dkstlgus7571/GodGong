<같공 실행환경과 기능 설명>

실행환경:

-SDK버전: Android 11(R)

sourceCompatibility 1.8
targetCompatibility 1.8
applicationId "com.example.basicdemoapp"
minSdkVersion 23
targetSdkVersion 30
versionCode 1
versionName "1.0"
testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"


기능 설명:

-로그인 기능: Firebase를 통해 UserAccount 정보를 연동시켜 사용자 정보를 저장
하고 불러오는 기능을 수행시킴

-회원가입 기능: Firebase를 통해 UserAccount 정보를 연동시켜 사용자 정보를 저
장하고 불러오는 기능을 수행시키며, 프로필 사진을 지정

-줌 사용 기능 : Zoom 계정 개설을 통해 Zoom SDK android용 API 키를 생성, 애
플리케이션 이름을 지정하고 생성된 SDK key를 확인, 프로젝트에 Zoom SDK를
추가, 프로젝트에 종속성을 추가 Zoom SDK 구현을 위해 인터넷 권한 추가,
Zoom SDK Key추가, Zoom 초기화를 진행. 회의를 만들어서 Meeting number와
meeting password 입력을 통해 회의에 참여

-채팅 기능: 팀프로젝트 채널, 스터디방 채널에서 user가 참가한 방에서 어디에서
든지 채팅기능을 이용할 가능. 채팅하기 버튼을 누르면 채팅이 가능.

-질문 작성 기능: Firebase의 StorageReference를 활용하여 저장된 사용자의 프로필
사진과 정보를 가져와 출력. Post.class를 작성하여 Firebase realtime data에 등록할
질문과 관련된 정보를 구조화하여 저장.

-댓글 작성 기능: Firebase의 StorageReference를 활용하여 저장된 사용자의 프로필
사진과 정보를 가져와 출력. 새로 작성된 댓글은 Firebase realtime data에 저장.
Firebase의 데이터가 변형되어 onDataChange 를 통해 기존 화면에 나타난 모든
댓글들을 제거하고 저장된 댓글들을 차례대로 화면에 나타냄. 게시글 작성과 마
찬가지로 Firebase realtime data에 등록할 댓글을 구조화하여 저장하기 위해
comment.class를 작성.

-프로젝트 참여, 취소 기능: 프로젝트 참여하기 버튼을 누르면 참여 가능하고 취소
버튼을 누르면 RemoveValue()함수를 호출하여 해당 정보를 firebase에서 제거.
스터디 작성 게시판과 줌 연동: 등록하기를 누르면 게시물 작성자가 생성한
zoom에 참여할 수 있음. Zoom Sdk에 appkey와 secret을 입력하여 사용할 준비를
함. Firebase에서 게시물의 내용을 가져와 회의실 ID와 Password를 모듈에 입력으
로 주고 Zoom sdk 모듈에서 이를 실행. Zoom 모듈인 startMeeting을 커스텀하여
회의가 열리는 동시에 firebase에 해당 글과 회의실 아이디 및 비밀번호가 저장.
이글은 추후에 참여자가 입장할 때 사용.

-스터디방의 줌 참여 기능: Firebase에서 게시물의 내용을 가져와 회의실 ID와
Password를 모듈에 입력으로 주고 Zoom sdk 모듈에서 이를 실행.

-Navigation drawer 기능 : Navigation drawer 구현을 위한 DrawerLayout 구현 완
료 및 header, content 구현 완료, 버튼 클릭 시 Main으로 이동하며, Navigation
drawer menu click 시, 해당 menu마다 기능 구현을 실행
