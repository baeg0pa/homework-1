# homework-1

## 1)getopt 명령어

	* getopt명령어는 명령줄을 분석하여 옵션을 분리하고
	  유효한 옵션을 확인

	* 사용법
		* getopt optstring parameters

## 2)getopts 명령어

	* 명령행 인수를 처리하고 유효한 옵션을 검사
	
	* getopts 명령은 매개변수 리스트에서 옵션 및 옵션 인수를 검색하는 Korn/POSIX 쉘 내장 명령

	* 사용법
		* getopts OptionString Name [ Argument ...]

	* 매개변수
		| 종류 | 설명 |
		| OptionString | getopts명령이 인식할 옵션 문자를 문자열로 표기.
				 문자 뒤에 ':'(콜론)이 있을 경우, 해당 옵션은 인수가 있는 것으로 간주됨.
				 이럴 경우 인수도 제공되어야함. |
		| Name | getopts 명령에 의해 발견된 옵션 문자로 설정됨. |
		| Argument... | 고액으로 분리된 하나 이상의 문자열. 
				getopts명령이 올바른 옵션인지 검사함. 
				생략 시, 위치 매개변수가 사용됨. |
## 3)sed 명령어
	
	* 텍스트를 변환하고 필터링하기위한 편집기

	* 사용법
		* sed [OPTION] {script-only-if-no-other-script} [input-file]

## 4)awk 명령어
	
	* awk = Aho + Weinberger + Kernighan. (A:Alfred V. Aho, W:Peter J. Weinberger, K:Brian W. Kernighan)
	  최초에 awk 기능을 디자인한 사람들의 이니셜을 조합하여 만든 이름

	* 파일로부터 레코드(record)를 선택하고, 선택된 레코드에 포함된 값을 조작하거나 데이터화

	* 사용법
		*awk [OPTION...] [awk program] [ARGUMENT...]
