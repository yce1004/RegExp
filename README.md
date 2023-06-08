# 정규표현식 (RegExp)
정규식 , Regular Expreession


## 역할
-문자 검색(search)
-문자 대체(replace)
-문자 추출(extract)

## 테스트 사이트
https://regexr.com/

### 졍규표현식 작성 방법
1. 생성자 함수 방식
```js
new RegExp('표현식','옵션')
new RegExp('[a-z]','gi')
```

2.리터럴(Literal) 방식
```js
/표현식/옵션
/[a-z]/gi
```

## 예제문자
```js
const str = `
010-1234-5678
thececond@gmali.com
https://www.omdbapi.com/?apikey=4a27f4b6&s=frozen
The quick brown fox jump over the lazy dog.
addccddd
hxyps
table
http://localhost:1234
동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리 나라만세
`
```

## 메소드
메소드 | 문법 | 설명
--|--|--
test | '정규식.test(문자열)' | 일치 여부 (Boolean) 반환
match | '문자열.match(정규식)' | 일치하는 문자를 배열(Array) 반환
replace | '문자열.replace(정규식, 대문자)'| 일치하는 문자를 대체

## 플래그
플래그 | 설명
--|--
g| 모든 문자열 일치(global)
i| 영어 대소문자 구분하지 않고 일치(ignore case)
m| 여러 줄 일치(multi line)

## 패턴(표현)

패턴1|설명
--|--
^ab | 줄(line) 시작에 있는 ab와 일치
ab$ | 줄(line) 끝에 있는 ab와 일치
. | 임의의 한 문자와 일치
a&verbar;b | a또는 b와 일치
ab? | ab가 없거나 ab와 일치(일회성)

패턴2|설명
--|--
{3} | 3개 연속 일치
{3,} | 3개 이상 연속 일치
{3,5} | 3개 이상 5개 이하 일치

패턴3 | 설명
--|--
[abc] | a 또는 b 또는 c 일치
[a-z] | a 부터 z사이의 문자 구간에 일치(영어소문자)
[A-Z] | A 부터 Z사이의 문자 구간에 일치(영어대문자)
[0-9] | 0 부터 9사이의 문자 구간에 일치(숫자)
[가-힣] | 가 부터 힣 사이의 문자 구간에 일치(한글)

패턴4 | 설명
--|--
\w | 63개 문자 (word,대소문자 52 + 숫자 10개 + _)에 일치
\b | 문자경계를 표현하며 문자와 공백
\d | 숫자에 일치
\s | 공백(space, tap 등)에 일치

패턴5 | 설명
--|--
(?=) | 앞쪽 일치
(?<=) | 뒤쪽 일치