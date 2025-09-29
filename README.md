pip install mecab-python3 jamdict jaconv
==> CMD에서 패키지 다운로드 필수로 하기.

권한 문제:
설치 중 권한 문제가 발생하면 --user 옵션을 추가하거나 관리자 권한으로 실행해야
Bash
코드 복사
pip install --user mecab-python3 jamdict jaconv

한자로 변환 하는 이유 = 일본현지에서는 히라가나 가타가나보단 한자가 글자수를 더 적게 잡아 먹어서 한자로 많이 쓴다고 함

とりあつかいせつめいしょ= 取扱説明書 = toriatsukai setsumei sho = 취급설명서 (예시)

일본으로 유학/이민 갈 상황이 있는 사람들도 있으니 만들어둠(사실 파파고같은거 쓰는게 더 빠르긴함 ㅎㅎ;)

JAMDICT=> 일본어 사전 데이터 베이스
MECAP => 일본어 형태소 분석기, 일본어 텍스트를 단어 단위로 쪼개고 품사 태깅 해줌
JACONV=> 일본어 텍스트 변환 도구. 가타가나 <=>히라가나 변환
전각문자<=>반각문자
로마자<=>일본어


# 히라가나 → 가타카나 변환
print(jaconv.hira2kata('こんにちは'))  # コンニチハ

# 가타카나 → 히라가나 변환
print(jaconv.kata2hira('コンニチハ'))  # こんにちは

# 전각 숫자 → 반각 숫자 변환
print(jaconv.z2h('１２３４５６７８９０'))  # 1234567890

# 반각 숫자 → 전각 숫자 변환
print(jaconv.h2z('1234567890'))  # １２３４５６７８９０

# 로마자 → 히라가나 변환 (기본적인 변환)
print(jaconv.alphabet2kana('konnichiwa'))  # こんにちは (대략적)

# 카타카나 → 알파벳 변환 (로마자)
print(jaconv.kata2alphabet('コンニチハ'))  # konnichiha
