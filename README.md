---

# 과제 설명

로컬스토리지를 DB처럼 사용하는 회원가입 form을 구현해주세요. 회원 가입 과정에서 유효성 검사가 필요하고, 검사를 통과하면 로컬스토리지에 저장합니다.

## 기술 스택 제약 사항

- form 상태 관리 라이브러리(formik, react-hook-form…), 유효성 검사 라이브러리(joy, yup…)는 사용하지 않고 직접 구현해주세요. 필요하다면 다른 라이브러리는 사용하셔도 괜찮습니다.

---

# 구현 요구사항

아래 내용을 만족하는 회원가입 form을 만들어주세요. 각 필드는 유효성 검사를 통과해야합니다.

### 유효성 검사

| field name | 유효한 입력 |
| --- | --- |
| id | 필수 입력, 최소 5자 이상, 최대 15자 이하 |
| name | 필수 입력 |
| email | email 형식 준수 |
| password | 필수 입력, 영문과 숫자만 허용, 최소 8자 이상, 최대 20자 이하 |
| password-confirm | 필수 입력, 영문과 숫자만 허용, 최소 8자 이상, password와 같은 값이어야 함 |
- 하나라도 유효하지 않은 입력이 있을 경우, 에러메세지를 화면에 표시합니다.
- 메세지 내용은 아래와 같습니다.

### 에러메세지

- 필수값 미입력시 "값을 입력해주세요." 라는 메세지를 표시합니다.
- 최소 글자수 미만시 "최소 N자 이상 입력해주세요." 라는 메세지를 표시합니다.
- 최대 글자수 초과시 "최대 N자 이하로 입력해주세요." 라는 메세지를 표시합니다.
- email 형식 문제시 "이메일 형식에 맞게 입력해주세요." 라는 메세지를 표시합니다.
- password와 password-confirm 불일치시 "비밀번호가 일치하지 않습니다." 라는 메세지를 표시합니다.
- password에 영문, 숫자 외의 문자 입력시 "영문과 숫자만 입력해주세요." 라는 메세지를 표시합니다.
- 유효성 검사는 제출 버튼을 누르는 시점에 진행해주세요.

### 회원 정보를 로컬스토리지에 저장

- users를 Key로 하여 user 정보 배열 형태로 저장해주세요.
- [이 사이트](https://video-world-pi.vercel.app/sign-up) 동작 참고(로컬 스토리지에 저장하는 부분만 참고 해주세요.)

## 추가 구현

이 부분은 시간이 남으면 구현해주세요.

- 이미 존재하는 이메일로 회원가입이 되지 않게 막아주세요.
- 비밀번호를 저장할때 보안처리를 해주세요([참고](https://www.npmjs.com/package/bcryptjs))
