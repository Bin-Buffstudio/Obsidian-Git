## Car.cs
* [[HUD]]에서 OnChangeCarDetailLayer 실행
* **OnChangeCarDetailLayer**
	* 레이어 마다 오브젝트 끄고 켜기
	+ *https://docs.google.com/presentation/d/15FUgGttBdiSQS256ion7H-yEUF1DhyVLN8_fhP9zZG8/edit#slide=id.g2713a008554_2_1125 - 레이어 참조*
	* carDetailStatEffectIcon - 전력 과부화/ 부품 파손 등 상태 효과 아이콘
	* carDetailElectricIcon - 전력 표시 아이콘 - 텍스트로 표시
	* carDetailPowerStone - 초당 동력석 표시 텍스트
	* carDetailElectricInformation - 전력망 정보 (마우스 오버시 표시)
	* Action OnElectricIconMouseEnter, OnElectricIconMouseExit를 추가하여 carDetailElectricInformation을 끄고 키게 구독했다가 끊었다가 함(1번 레이어 일때만)
	* OnMouseEnter, OnMouseExit로 해당 구독된거 Invoke