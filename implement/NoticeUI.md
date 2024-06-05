## NoticeUI.cs
* m_ActiveNoticeWarningItems
	+ Dictionary<string,NoticeWarningItem>으로 key값에 Identifier값이 들어가서 삭제할 때 key값을 검색해 해당 Identifier와 일치하는 부분 삭제
* interface INoticeDataProvider
	+ 알림/경고/주의 메시지를 생성하는 오브젝트는 해당 인터페이스를 상속 받으며 아래의 값 필요
		+ NoticeIdentifier defaultNoticeIdentifier
		+  NoticeIdentifier currentNoticeIdentifier
	+ public string GetCurrentNoticeIdentifier()
		+ 현재의 Identifier값을 받아온다.
* OnNoticeWarningReceived
	+ 경고/주의 출력 알림을 받았을 때 호출되는 함수
		1. provider의 Identifier를 받아 Database.TextData의 Dictionary Value(TextDataTuple)를 가져와서 noticeName, noticeDesc라는 이름으로 선언
		2. NoticeWarningItem 생성 후 매개 변수로 받은 time, noticeType 및 앞에 정의한 noticeName, noticeDesc 각각 할당
		3. NoticeWarningItem은 string 타입 Action OnDeleteRequest가 존재하고 생성한 인스턴스는 DeleteNoticeWarningItem 등록
		4. time이 있으면 NoticeWarningItem의 코루틴 시작
		5. ReOrderWarningNotice함수를 통해서 경고/주의 메시지 정렬 (NoticeWarningItem의 Value(NoticeType)에 의해 정렬)
* OnNoticeReceived
	+ WarningReceived와 같으나 NoticeItem 인스턴스를 생성 (알림 메시지), 설명 부분이 없음, notifier라는 매개변수를 받아 notifierName 정의
* DeleteNoticeWarningItem
	+ 매개변수로 받은 Identifier랑 일치하는 NoticeWarnningItem가 있으면 삭제
* DeleteNoticeItem
	+ 매개변수로 받은 NoticeItem 삭제
* GetNoticeWarningItem
	+ NoticeIdentifier와 일치하는 NoticeWarningItem return, 경고/알림 메시지 삭제를 위한 함수
* ReOrderWarningNotice
	+ NoticeWarningItem 정렬 함수
## TextData구조
```
	class TextData : Dictionary<string, TextDataTuple>
		TextDataTuple
			string Identifier
			string korean
			string english
```

