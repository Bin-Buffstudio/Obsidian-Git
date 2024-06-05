## GameResultUI.cs
* public struct GameResultData
	+ 더미 데이터
* public struct GameResultItem
	+ public TextIdentifier identifier
		+ 해당 항목의 identifier
	+ public TextMeshProUGUI name
		+ 해당 항목의 제목
	+ public TextMeshProUGUI value
		+ 해당 항목의 값
* public struct GameResultOption
	+ public TextIdentifier identifier
		+ 해당 선택지의 identifier
	+ public TextMeshProUGUI name
		+ 해당 선택지의 제목
	+ public Button button
		+ 해당 선택지의 버튼
* Awake
	+ 리플렉션을 통해 GameResultItem을 전부 가져와 리스트에 넣음
* ConvertMinutesToHourMinuteString
	+ 시간/분 나눠서 출력
* ShowGameResult
	+ GameResultItem 리스트의 Identifier를 가져와서 TextData에 있는지 검사 후 name(제목) 선언
	+ value(값 또는 내용)부분 gameResultData(더미) 받아서 처리
## 고려사항
* GameResultItem을 리스트화 하면 보기 불편한지
* Identifier를 Field에서 정의하지 말고 코드로 정의하지 않은 이유? > TextData가 바뀌면 코드를 또 바꿔줘야 하기 때문