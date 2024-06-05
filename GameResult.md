## 구현 설명
[[GameResultUI]]
## 게임 결과창 인스펙터
https://docs.google.com/spreadsheets/d/1ggNM4tM3_zZigdZPan29CJD9NnmLdk3iAKksM9TLXM4/edit#gid=2070682695 - Index 부분 참고
Game Result Name Field
	Success Identifier - 성공 Index 나눠서 입력
		Category - Result
		Object Type - Success
		Sub Type - 빈칸
	Fail Identifier - 실패 Index 나눠서 입력
		Category - Result
		Object Type = Success
		Sub type - 빈칸
Game Result Item Panel
	각각 Identifier만 바꿔주기
		Category - Result
		Object Type - Result 다음 부분 (스프레드 시트 Index 참조)
		Sub Type - 빈칸(Num,Text 부분은 현재 쓰지 않음)
Game Result Options Field
	각각 Identifier만 바꿔주기
		Category - Result
		Object Type - Result 다음 부분 (스프레드 시트 Index 참조)
		Sub Type - 빈칸
## 참고
한글은 한글 폰트가 존재하지 않으면 깨짐
현재 더미 상태로 구현
Scene
	Assets > Scenes > Develop Scene > UI Test > Game Result Canvas
## 추후 수정 사항
게임 결과 데이터 불러오기