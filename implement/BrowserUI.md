## BrowserUI.cs
* SelectBrwoserOption
	+ 선택지에 따라 해당 창 오브젝트 끄고 켜기, 버튼은 이미지 컬러만 바꿔줌
* CreateAugmentIcons
	+ 증강체 데이터(보유 갯수, Identifier)를 받아와 AugmentIcon(Button 상속) 생성, 생성된 순서가 index
	+ 생성된 index에 따라 SelectAugmentIcon함수 AddListener
* SelectAugmentIcon
	+ 선택된 아이콘 선택 효과 처리, identifier에 따라 데이터를 받아와 텍스트에 넣어줌 (Name, Desc, Stat)
	+ 인덱스가 -1인 경우 초기화
* CreateCarList
	+ 차량 세부 정보 데이터를 받아 텍스트에 출력 (HUDDetailItem.DetailName, DetailValue)
	+ 차량 데이터(identifier, model, stat, 차량 갯수)를 받아 하단 버튼 생성, 생성된 순서가 index
	+ 생성된 index에 따라 SelectCar함수 AddListener
* SelectCar
	+ 선택된 차량 선택 효과 처리, identifier에 따라 데이터를 받아와 텍스트에 넣어줌 (carInformationName, Desc, Stat)