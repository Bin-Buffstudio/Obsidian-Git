## ShopUI.cs
	OnEnable
		풀링으로 ShopItem(Button 상속)인스턴스 3개 생성
		아이템 이름, 가격 모두 더미상태
		AddListener에 SelectItem등록
	SelectItem
		해당 아이템 클릭하면 테두리 하이라이트
		선택 이미지, 이름, 설명 갱신, buyButton에 AddListener BuyItem등록
	BuyItem
		미구현 상태 - 현재는 아이템 이름 출력
## 인스펙터
세부 사항 창
	buyButton, cancelButton, selectItem, selectItemImage
https://docs.google.com/document/d/1cwjw8W0kiE2gzVPLW6CHT8oEXg-p2HxfanoZKcRb9HI/edit#heading=h.8t950ld2wyku - 떠돌이 상인 부분 참고함
## 참고
Scene
	Assets > Scenes > Develop Scene > UI Test > Shop Canvas
