## EventUI.cs
Interface IEventDataProvider
	상호작용 가능한 오브젝트(이벤트 노드)는 해당 인터페이스를 상속 받으며 아래의 값 필요
			EventIdentifier defaultEventIdentifier
			EventIdentifier defaultEventCategory
		public string[] GetNextEventIdentifier()
			Assets > Resources > EventTree에 저장되어 있는 값 중 Next Event Node Identifier를 가져옴
		public string GetCurrentEventIdentifier()
			현재 이벤트의 Identifier를 가져옴
		public void SetEventIdentifier(string identifier)
			currentEventIdentifier를 identifier값으로 변경
InitEventUI
	1. provider(상호작용 가능한 오브젝트)의 Identifier를 받아 Database의 [[#^88b8ae|EventData]]의 Dictionary Value(EventDataTuple)를 가져와서 eventData라는 이름으로 선언
	2. m_EventDataProvider에 provider 저장
	3. eventData의 다양한 값을 가져와서 적용 및 선택지와 보상은 풀링 적용
	4. List에 저장된 선택지(EventOptions)의 개수 만큼 선택지 인스턴스 생성(EventOptionItem - Button 상속), 선택지 index가 1이면 무조건 닫기(무시한다) AddListner 등록
	5. 그 외의 선택지는 GetMethod를 이용해 Identifier 이름의 맞는 함수 AddListner 등록
	6. EventRewardIconIndex가 비어 있지 않으면 List에 저장된 개수 만큼 보상 인스턴스 생성(EventRewardItem)
	7. EventRewardIconIndex를 통해 Database의 TextData의 Dictionary Value(TextDataTuple)를 얻어 보상 이름과 설명을 가져옴 ( 마우스 호버 기능을 위함 )
	8. EventRewardQuantity의 값이 음수이면 선택지에 필요한 자원 출력 - 자원이 충분하면 파란색 아니라면 빨간색, 보상 인스턴스 비활성화
InitShop
	상점 열기 (더미)
region EventMethodList
	이벤트 별로(함수 별로) 내용 구현 필요
AttackEvent
	공격 이벤트 공통함수
	현재는 미구현 상태
GetResource
	자원 획득 처리 함수
	현재 미구현(Train만 있으면 됨)
## EventData 구조
	class EventData : Dictionary<string, EventDataTuple>
		EventDataTuple
			string Identifier
			string EventName
			string EventDescription
			List<string> EventOptions
			List<string> EventRewardIconIndex
			List<string> EventRewardQuantity
		List의 값은 csv의 값이 비어있으면 저장하지 않음
^88b8ae

## 선택지에 다음 이벤트가 있는 경우
	m_EventDataProvider의 currentIdentifier를 바꿔서 InitEventUI호출