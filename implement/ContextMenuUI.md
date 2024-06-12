## ContextMenuUI.cs
* CreateContextMenuItems
	+ contextMenuData를 받아 해당 개수만큼 ContextItem 생성
	+ 생성 후 생성된 개수에 따라 fillAmount 설정
	+ 생성된 순서에 따라 0~360 사이의 회전 값 설정
	+ SetData를 통해 받은 데이터를 대입함
	+ 캔버스의 크기에서 벗어나서 생성되지 않게 위치를 조정해서 ContextMenuItem의 localPosition 지정
* Update
	+ contextMenuItem이 존재하면 ManualUpdate 계속 호출
	+ Fan 계속 호출
* OpenMenu
	+ 입력받은 screenPos에 CreateContextMenuItems 호출
* Fan 
	+ 회전하면서 생성, 소멸하는 애니메이션 효과
	+ m_OpenedMenu변수를 통해 각각 생성, 소멸 애니메이션
* SetContextMenuDetailItem
	+ 컨텍스트 메뉴 세부정보 활성화
	+ identifier를 받아서 데이터 찾아서 이름, 설명 대입
## ContextMenuItem.cs
* ManualUpdate
	+ 컨텍스트 메뉴 아이템이 활성화 되어있으면 계속 호출
	+ iconImage와 itemName의 위치를 중앙으로 위치시킴
	+ 여러 함수 계속 호출
* UpdateScale
	+ 마우스 호버 상태면 ContextMenuUI의 HoverScale에 따라 크기 변경
* CheckMouseHover
	+ 마우스 위치에 호버 기능 구현
* CheckControllerHover
	+ 컨트롤러 위치에 따라서 호버 기능 구현
* UpdateColorAndClickEvent
	+ 마우스 호버 상태면 색 변경
	+ 클릭시, 이벤트 Invoke
* ResetRotation
	+ 회전 값 보정 및 초기화
* UpdateAngles
	+ fillAmount에 따라 회전 범위 지정
* HandleHoverEvents
	+ 마우스 호버 상태 기능 구현
* Center
	+ fillAmount에 따라 중앙 값 결정
* SetData
	+ ContextMeduData를 받아 각각의 값 지정
* OnHoverEnter
	+ 마우스 호버시 호출 되는 함수
* OnHoverExit
	+ 마우스 호버를 나가면 호출 되는 함수