## 구현 설명
[[NoticeUI]]
## 메시지 오브젝트 인스펙터
https://docs.google.com/spreadsheets/d/1ggNM4tM3_zZigdZPan29CJD9NnmLdk3iAKksM9TLXM4/edit#gid=2070682695 - Index 부분 참조
Default Notice Identifier : 알림/경고/주의 메시지 Index 부분 나눠서 입력
	공용
		Category - Message
		Object Type - Notice/Warning/Caution
		Sub Type - Index 끝부분
		예시) Message_Warning_Damage_Reload
			Category - Message
			Object Type - Warning
			Sub Type - Damage_Reload
	알림 메시지
		공용 부분 작성 후, Npc Name 작성
		Npc Name은 Grace,Scott,Venus 중 하나 > 스프레드 시트 참조 (Message_Name_NpcName)
	경고 메시지
		공용 부분 작성 후, Npc Name 비워도 상관없음
## 참고
한글은 한글 폰트가 존재하지 않으면 깨짐
오브젝트
	UI Test Scene > Dummy_NoticeObj
Scene
	Assets > Scenes > Develop Scene > UI Test > Notice Canvas
	주의/경고 버튼
		NoticeWarningButton
	해결 버튼
		NoticeWarningDeleteButton
	알림 버튼
		NoticeButton
더미 파일
	Assets > Scripts > UI > Notice > DummyObj_Notice.cs
더미 사용법
	Assets > Scenes > Develop Scene > UI Test > Notice Canvas를 활성화
	공용
		UI Test Scene > Dummy_NoticeObj의 Default Notice Identifier를 변경해서 메시지 생성 및 삭제
	주의/경고 메시지
		Notice(Warning) 클릭
	알림 메시지
		Dummy_NoticeObj의 Npc Name을 입력해야함
		Notice 클릭