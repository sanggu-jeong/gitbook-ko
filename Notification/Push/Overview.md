## Notification > Push > 개요

Push를 사용하면 다양한 전송 방법으로 메시지를 전송하고 결과를 검색할 수 있습니다.
현지 시간에 맞춰 메시지를 예약 전송할 수 있고, 메시지 전송 결과도 쉽게 확인할 수 있습니다.

Push의 주요 기능은 다음과 같습니다.

### 주요 기능

- Android OS(FCM, ADM), iOS(APNS, Apple Push Notification Service) 기기에 메시지를 통합 발송
- 토큰 관리
- 즉시 전송
- 일반 예약 전송과 현지 시간 예약 발송
- SERVER KEY(FCM), 인증서(APNS), 클라이언트 아이디/시크릿(ADM) 관리
- 전송 결과 성공/실패 지표 제공
- 태그 관리, 토큰 기반 메시지 발송
- 메시지 수신 및 확인 데이터 수집, 통계 제공

### 서비스 용어

| 용어        | 설명                                      |
| --------- | --------------------------------------- |
| 토큰(token) | 애플리케이션이 설치된 기기의 고유 식별자.                 |
| 태그(tag)   | UID를 분류하는 체계. UID에 여러 개의 태그를 붙일 수 있습니다. |

### 구조

다음은 Push 서비스 구조입니다.

![](http://static.toastoven.net/prod_push/21-05-03/overview_ko.png)

#### Console

인증서 관리, API 테스트, 메시지 발송 등 모든 기능을 사용할 수 있습니다.

#### REST API

토큰 등록/조회, 메시지 전송, 피드백 확인 등 Public API를 호출할 수 있습니다.

#### client SDK
토큰 등록/조회 및 푸시 메시지 수신을 편하게 사용할 수 있습니다.

### 기능

#### 알림/홍보성 푸시 메시지 수신 동의 정보 저장 및 자동 필터링

정보통신망법 규정(제50조부터 제50조의 8)에 따라 토큰 등록 시 알림/홍보성/야간홍보성 푸시 메시지 수신에 관한 동의 여부도 함께 입력받습니다. 메시지 발송 시 수신 동의 여부를 기준으로 자동으로 필터링합니다.

[KISA 가이드 바로 가기](https://spam.kisa.or.kr/spam/na/ntt/selectNttInfo.do?mi=1020&nttSn=1171&bbsId=1002)

[법령 바로 가기](http://www.law.go.kr/lsEfInfoP.do?lsiSeq=123210#)

#### 국가 필터링

토큰 등록 시 국가 코드를 입력받고, 메시지 발송 시 발송 국가를 지정할 수 있습니다.

#### 공통 메시지 형식

공통 메시지 형식에 맞게 메시지를 작성하면, 기기 종류에 맞게 메시지가 생성되어 발송됩니다.  
공통 메시지 형식에 맞게 입력받은 언어 코드를 기준으로 메시지를 작성하면, 해당 언어와 기기 종류에 맞게 생성되어 발송됩니다.

#### 광고성 메시지 발송

광고성 푸시 메시지 표시 의무화를 따르고 있습니다.  
광고성 메시지 형식으로 메시지를 발송할 경우, (광고), 연락처, 수신 철회 방법 등 광고 표시 문구를 메시지에 삽입해 발송합니다.
광고 표시 문구 삽입 여부는 기기의 언어 설정을 따릅니다.
언어가 한국어(ko, ko-KR 등 ko로 시작하는 언어 코드)로 설정된 기기만 정보통신망법에 따라 광고 표시 문구가 삽입되어 발송됩니다.

#### 예약 메시지 발송

한 번, 매일, 매주, 매월 등 다양한 예약 발송 유형을 선택할 수 있습니다.
현지 시간에 맞춰 발송할 수 있습니다.

#### 메시지 유효기간 설정

메시지에 유효기간(TTL)을 설정할 수 있습니다. 유효기간이 지나면 실패 처리됩니다.
단, 0은 유효기간이 없는 것으로, 발송 지연으로 인해 실패 처리되지 않습니다.

#### 실시간 모니터링

![](http://static.toastoven.net/prod_push/img_03.png)

**메시지** 탭에서 메시지 발송 상태를 실시간으로 확인할 수 있습니다.

#### 피드백 제공

삭제되거나 잘못된 토큰은 메시지 발송 시 자동으로 삭제되며, 피드백 API로 삭제된 토큰을 조회할 수 있습니다.

#### 인증서 관리

푸시 유형별 인증서 또는 API Key를 관리할 수 있습니다.

#### Public API

토큰 등록, 조회, 메시지 전송, 피드백 확인 API를 사용할 수 있습니다.
**API** 탭에서 Public API를 테스트할 수 있습니다.

* *문서 수정 내역*
    * *(2018.01.25) 광고성 메시지 발송 설명 추가*