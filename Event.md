## 구현 설명
	[[EventUI]]
	[[Shop]]
## 상호작용 오브젝트 인스펙터
https://docs.google.com/spreadsheets/d/1ggNM4tM3_zZigdZPan29CJD9NnmLdk3iAKksM9TLXM4/edit#gid=76848005 - Index 부분 참고
Default Event Identifier : 이벤트 Index 부분 나눠서 입력
	Category - Event
	Object Type - Category 다음 부분
	Sub Type - Object Type 다음 부분 전부
	Sub Type은 비워도 상관없음
	예시) Event_Wreck
		Category - Event
		Object Type - Wreck
		Sub Type - 
	예시) Event_Wreck_Attack_Warning
		Cagtegory - Event
		Object Type - Wreck
		Sub Type - Attak_Warning
## 참고
한글은 한글 폰트가 존재하지 않으면 깨짐
오브젝트
	UI Test Scene > Dummy_EventObj
Scene
	Assets > Scenes > Develop Scene > UI Test > Event Canvas
더미 파일
	Assets > Scripts > UI > Event > DummyObj_Event.cs
더미 사용법
	Assets > Scenes > Develop Scene > UI Test > Event Canvas를 활성화
	UI Test Scene > Dummy_EventObj의 Default Notice Identifier를 변경하고 중앙에 Button 클릭
	이벤트 종료후에도 해당 행동 반복가능