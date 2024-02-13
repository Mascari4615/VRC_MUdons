# VRC_MUdons

- 왁타버스 VRChat 컨텐츠 맵에 사용하고 있는 기능들을 모았습니다.

- 성능을 일부 포기히고, 개발 편의/재사용에 중점을 뒀습니다.
  -  U#을 사용하지만, Udon 같은 Event (C# 리플렉션/Unity 메시지 브로드캐스트) 기반으로 시스템 구현 
  -  Static 사용에 제한이 있기에, Util 기능을 모아둔 클래스를 직접 상속

- 자유롭게 수정/사용 가능합니다, 피드백 환영합니다 !

## 기능

- MBase : 자주 사용하는 코드 블럭 모음 (직접 상속받아 사용)

- MBool : 동기화되는 Bool 변수의 값 변화에 따른 Event 호출

- MPlayerUdonIndex : 각 플레이어에게 제한된 범위 내의 고유한 Index 할당
  - VRChat에서 제공하는 `PlayerID`는 플레이어가 들어올 때마다 제한없이 계속 커지기 때문에, 플레이어에게 고유한 오브젝트를 할당하는 등의 상황에서 쓰기에 어려움이 있음
 
- MQuiz : 퀴즈 관련 컨텐츠 대부분에 응용될 수 있음

- MScore : 동기화되는 점수판 (자잘한 기능들과 함께)

- MTarget : 특정 플레이어의 `PlayerID`를 UI를 통해 특정하여 동기화

- SendEvent : 각종 이벤트 발생 시 (`Interact`, `OnPlayerTriggerEnter`, ...) 다른 Event 호출 

- 그 외 추가 예정...