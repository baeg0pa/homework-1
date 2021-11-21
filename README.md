# homework-1

## 1)getopt 명령어

	getopt명령어는 명령줄을 분석하여 옵션을 분리하고 유효한 옵션을 확인

### 사용법
* getopt optstring parameters*

* getopt [options] [--] optstring parameters*

* getopt [options] -o|--options optstring [options] [--] parameters*

### 매개변수
|종류|설명|
|:---|:---|
|-o[옵션]|short option을 의미함.|
||예시: "getopt -o ab:c"=> -a, -b, -c를 옵션으로 가지고, -b는 argument를 가짐. getopts와 비슷함|
|-l[옵션]|long option을 의미함.
||예시: "getopt -l help,path:,name:"(예시)=> help,path,name을 옵션으로 가지고, path와 name은 argument를 가짐. ','(반점)은 구분자|
|$@|주로 이걸로, parameter를 한번에 받아서, while문과 shift를 이용해서 옵션을 구별함|


## 2)getopts 명령어

	명령행 인수를 처리하고 유효한 옵션을 검사
	getopts 명령은 매개변수 리스트에서 옵션 및 옵션 인수를 검색하는 Korn/POSIX 쉘 내장 명령

### 사용법
* getopts OptionString Name [ Argument ...]*

### 매개변수

|종류|설명|
|---|---|
|OptionString|getopts명령이 인식할 옵션 문자를 문자열로 표기. 문자 뒤에 ':'(콜론)이 있을 경우, 해당 옵션은 인수가 있는 것으로 간주됨. 이럴 경우 인수도 제공되어야함.|
|Name|getopts 명령에 의해 발견된 옵션 문자로 설정됨.|
|Argument...|고액으로 분리된 하나 이상의 문자열. getopts명령이 올바른 옵션인지 검사함. 생략 시, 위치 매개변수가 사용됨.|
		
				
## 3)sed 명령어
	
	텍스트를 변환하고 필터링하기위한 편집기

### 사용법
* sed [OPTION] {script-only-if-no-other-script} [input-file]*

**간단예시로 알아보자**

* '-n'옵션은 'p'(print의 약자)와 같이 자주 쓰임.
<img src="https://github.com/baeg0pa/homework-1/blob/main/sed%20%EC%82%AC%EC%9A%A91.png?raw=true" width="600" height="400">
	
	%%hello는 파일명(이 파일에서 내용 읽어옴)%%
	
	* -n '1p'는 첫번째줄만 출력
	* -n '1,3p'는 첫번째줄부터 세번째줄까지만 출력
	* -n '4,$p'는 4번째줄부터 끝까지 출력

* 특정 단어로 시작or포함하는 행들 출력 
<img src="https://github.com/baeg0pa/homework-1/blob/main/sed%20%EC%82%AC%EC%9A%A9%202.png?raw=true" width="600" height="200">

	* -n '/^o/p'는 hello에서 'o'로 시작하는 행만 출력
	* -n '/a/p'는 hello에서 'a'를 포함하는 행만 출력

## 4)awk 명령어
	
	awk = Aho + Weinberger + Kernighan. (A:Alfred V. Aho, W:Peter J. Weinberger, K:Brian W. Kernighan 최초에 awk 기능을 디자인한 사람들의 이니셜을 조합하여 만든 이름.)
	파일로부터 레코드(record)를 선택하고, 선택된 레코드에 포함된 값을 조작하거나 데이터화함.

### 사용법
*awk [OPTION...] [awk program] [ARGUMENT...]*

|기능|사용 방법|
|---|---|
|파일의 전체 내용 출력|awk '{ print }' [FILE]|
|필드 값 출력|awk '{ print $1 }' [FILE]|
|필드 값에 임의 문자열을 같이 출력|awk '{print "STR"$1, "STR"$2}' [FILE]|
|지정된 문자열을 포함하는 레코드만 출력|awk '/STR/' [FILE]|
|특정 필드들의 합|awk '{sum += $3} END { print sum }' [FILE]|
|필드의 연산 수행 결과 출력|awk '{print $1, $2, $3+2}' [FILE]|
|레코드 or 필드의 문자열 길이 검사|awk ' length($0) > 10' [FILE]|
| ... | ... |

**간단예시로 알아보자**

* 파일 전체 내용 출력
<img src="https://github.com/baeg0pa/homework-1/blob/main/awk%20%EC%82%AC%EC%9A%A91.png?raw=true" width="600" height="300">

* 필드 값 출력
<img src="https://github.com/baeg0pa/homework-1/blob/main/awk%20%EC%82%AC%EC%9A%A91.png?raw=true" width="600" height="300">
