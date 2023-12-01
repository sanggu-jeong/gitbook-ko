## Data & Analytics > DataFlow > 콘솔 사용 가이드

DataFlow는 다음과 같은 순서로 사용할 수 있습니다.

* 서비스 활성화
    1. [프로젝트 관리](https://docs.toast.com/ko/TOAST/ko/console-guide/# _14)를 참고하여 프로젝트를 생성합니다.
    2. 원하는 프로젝트를 선택합니다.
    3. [프로젝트 서비스 활성화 가이드](https://docs.toast.com/ko/TOAST/ko/console-guide/# _18)를 참고하여 DataFlow를 활성화합니다.
* 플로우 실행
    1. 이름과 설명을 입력하여 플로우를 생성합니다.
    2. 필요한 노드를 추가하고, 설정값을 입력하여 각 노드의 동작 방식을 정의합니다.
    3. 노드 연결을 통해 노드들의 동작 순서를 결정하여 플로우를 완성합니다.
    4. 플로우를 실행합니다.
    5. 로그 정보를 확인하여 플로우가 정상적으로 실행되었는지 확인합니다.

## 관리

플로우 메타데이터 정보를 조회하고 관리하는 페이지입니다.
**Data & Analytics > DataFlow > 관리**를 클릭합니다.

![management_main.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/management_main.png)

## 검색

주어진 기준으로 플로우를 검색합니다.

* 플로우 이름을 기준으로 검색하면 이름에 검색어가 포함된 플로우를 검색합니다.

### 필터

주어진 조건으로 플로우를 검색합니다.

* 플로우 상태값에 따른 필터링 옵션을 제공합니다.

### 플로우 목록

조회 결과 플로우를 테이블 형태로 표시합니다.

* 간단한 플로우 메타데이터와 현재 플로우 실행 상태를 표시합니다.
* 최근 수정일을 기준으로 정렬합니다.
* 플로우를 선택하여 플로우 변경, 플로우 상세보기, 플로우 시작 등의 관리 기능을 사용할 수 있습니다.
* 필터 조건 기능을 통해 특정 상태의 플로우만 조회할 수 있습니다.
* 한번 조회된 플로우는 **새로 고침**을 눌러야 조회 결과를 갱신합니다.
* 한 페이지당 12개의 플로우를 조회하며, **이전** 및 **다음**을 클릭해 페이지를 이동할 수 있습니다.

#### 플로우 상태 정보

| 플로우 실행 상태                                         | 설명 |
|---------------------------------------------------| --- |
| <span style="color:black">START\_REQUESTED</span> | 플로우 실행이 요청되었습니다. |
| <span style="color:#880808">START\_FAILED</span>  | 플로우 실행 요청에 실패했습니다. |
| <span style="color:#00ffff">STARTING</span>       | 플로우 실행을 위한 리소스를 파악하는 중입니다. |
| <span style="color:orange">QUOTA\_EXCEEDED</span> | 플로우 실행을 위한 리소스가 부족해 실행에 실패했습니다. |
| <span style="color:#088f8f">PREPARING</span>      | 플로우 실행 준비가 완료되었습니다. |
| <span style="color:#aaff00">RUNNING</span>        | 플로우가 실행 중입니다. |
| <span style="color:red">ERROR</span>              | 플로우 실행 과정에서 통신 장애나 인증 불가 등으로 인해 오류가 발생했습니다. 지속적으로 <b>ERROR</b>가 발생할 경우 고객 센터로 문의하십시오. |
| <span style="color:red">UNKNOWN</span>            | 플로우 실행 과정에서 알 수 없는 원인으로 인해 오류가 발생했습니다. 지속적으로 <b>UNKNOWN</b>이 발생할 경우 고객 센터로 문의하십시오. |
| <span style="color:black">STOP\_REQUESTED</span>  | 플로우 종료가 요청되었습니다. |
| <span style="color:#880808">STOP\_FAILED</span>   | 플로우 종료 요청에 실패했습니다. |
| <span style="color:#ee4b2b">STOPPED</span>        | 플로우가 종료되었습니다. |

### 플로우 생성

플로우를 정의할 메타데이터를 생성합니다.

* 플로우 식별을 위해 이름과 설명을 추가하여 플로우 메타데이터를 생성합니다.
* 플로우 이름은 다른 플로우와 중복이 가능합니다.
* 플로우 템플릿을 지정하여 사용자가 원하는 기능의 플로우를 손쉽게 불러올 수 있습니다.

### 플로우 변경

플로우의 메타데이터를 수정합니다.

* 기존의 플로우 이름과 설명을 수정하여 플로우 메타데이터에 반영합니다.
* 플로우 템플릿은 지정할 수 없습니다.
* 플로우 실행 중에도 플로우 변경이 가능합니다.

### 플로우 복사

기존의 플로우 정의를 가지고 새로운 메타데이터를 생성합니다.

* 기존 플로우의 이름에 `_copy` 문구가 추가된 새로운 메타데이터를 생성합니다.
* 기존 플로우가 가진 플로우 로직을 그대로 복사해 옵니다.
* 실행 중인 플로우도 복사가 가능합니다.
* 실행 중인 플로우는 정지 상태로 복사합니다.
* 플로우의 현재 저장 상태가 임시 저장이라면 기존 플로우의 마지막 저장 버전은 복사하지 않습니다.
* 스케줄러가 등록된 플로우를 복사하더라도 복사한 플로우는 스케줄러가 등록되지 않습니다.
* 복사한 플로우는 기존 플로우와 완전히 별개의 플로우입니다.

### 플로우 삭제

플로우 메타데이터를 삭제합니다.

* 플로우 메타데이터를 완전히 삭제합니다.
* 삭제한 플로우는 복구할 수 없습니다.
* 실행 중인 플로우는 삭제할 수 없습니다.

### 더 보기

플로우를 시작 혹은 중지하는 동작을 제어합니다.

* 정지 상태의 플로우를 시작할 수 있습니다.
* 시작 요청을 전달하여 실행 준비 중이거나 실행 중인 플로우를 중지할 수 있습니다.
* 각 플로우는 동시에 하나만 실행할 수 있습니다.
* 임시 저장한 플로우는 마지막으로 저장한 버전으로 시작합니다.
* 플로우는 반드시 1회 이상 저장해야 시작할 수 있습니다.
* 플로우가 스케줄러에 의해 실행 중이더라도 사용자에 의해 시작한 플로우와 동일하게 플로우를 시작할 수 없습니다.

## 플로우 상세 보기

선택한 플로우의 상세 정보를 확인하는 세부 페이지입니다.
**Data & Analytics > DataFlow > 관리 > 플로우 목록 중 하나**를 클릭합니다.
플로우 목록 영역과 플로우 상세보기 영역 경계를 움직여 화면 비율을 조정할 수 있습니다.
또한 플로우 상세 보기 영역의 오른쪽 상단에 위치한 영역 크기 조절 아이콘을 클릭해 지정된 화면 비율로 조정할 수 있습니다.

### 기본 정보

상세한 플로우 메타데이터를 표시합니다.

![management_basicinfo.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/management_basicinfo.png)

* 플로우 생성 시 입력한 이름과 설명 정보를 표시합니다.
* 플로우 생성 날짜와 생성자 이름을 비롯한 최근 수정일/수정자, 최근 실행일/실행자 정보를 표시합니다.
* 가장 최근에 실행할 당시의 총 실행 시간을 표시합니다.

### 기본 정보 - 최근 로그

* 최근 로그에서 현재 실행 중인 플로우의 로그 정보를 직접 확인할 수 있습니다.
* 최근 15분의 로그를 확인할 수 있습니다.

### 기본 정보 - 전체 로그
![management_basicinfo_lncs_query.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/management_basicinfo_lncs_query.png)
* Log & Crash Search를 연동한 경우 Log & Crash Search에서 플로우 로그를 조회하기 위한 Lucene Query를 복사할 수 있습니다.

### 기본 정보 - 스케줄링

* 스케줄링 기능을 통해 플로우 실행을 예약할 수 있습니다.
* 스케줄러에 등록된 시작 시기가 도래했을 때 만약 플로우가 실행 중이라면 스케줄러에 의한 실행은 실패합니다.
* [알림] 현재는 예약 실행 기능만 지원합니다. 추후 기능을 추가 지원할 예정입니다.

### 플로우 정보

플로우 로직을 정의합니다.

![management_detail.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/management_detail.png)

* 플로우 설정으로부터 노드 유형이나 템플릿으로부터 플로우 구성 요소를 불러와 플로우를 정의합니다.
    * 접기 및 펼치기 아이콘을 클릭해 플로우 화면을 확장하거나 축소할 수 있습니다.
* 플로우 화면을 조작하여 플로우를 정의하고 그래프의 구성을 변경합니다.
    * 각 노드에 적절한 설정값을 입력하여 노드의 동작을 정의합니다.
        * [노드 상세 가이드 링크](https://docs.toast.com/ko/Data%20&%20Analytics/DataFlow/ko/node-config-guide/)
    * 노드 간에 연결선을 연결하여 메시지의 흐름을 정의합니다.
        * 각 플로우는 반드시 하나의 Directed Acyclic Graph(DAG)만 정의할 수 있습니다.
        * 노드의 유형별 카테고리에 맞는 연결이 빠짐없이 정의되어야 저장 가능합니다.
        * 한 노드는 여러 연결을 가질 수 있습니다.
            * 입력 연결이 여러 개인 경우에는 각 연결의 메시지가 단일 흐름으로 처리됩니다.
            * 출력 연결이 여러 개인 경우에는 노드가 출력하는 메시지를 모든 연결에 복제하여 흐름을 생성합니다.
* 배율 조정과 초기화, 화면 조정, 노드 정렬을 통해 플로우가 화면에 잘 보이도록 조정할 수 있습니다.
    * 배율 조정
        * 플로우 그래프가 표시되는 화면의 배율을 조정합니다.
        * 0.5배~2배까지의 배율을 지원합니다.
    * 초기화
        * 배율 조정을 통해 조정한 배율을 1배로 조정합니다.
    * 화면 조정
        * 플로우가 한 화면에 보이도록 배율 및 화면 중심을 조정합니다.
    * 노드 정렬
        * 플로우의 배열을 단계가 잘 드러나도록 정렬합니다.
        * 플로우가 한 화면에 보이도록 배율 및 화면 중심을 조정합니다.
* 편집한 플로우 정의를 취소/저장/임시 저장할 수 있습니다.
    * 취소
        * 편집한 플로우 정의를 마지막으로 저장/임시 저장 당시의 상태로 되돌립니다.
    * 임시 저장
        * 플로우를 미완성 형태로 저장하는 기능을 제공합니다.
        * 임시 저장한 플로우는 시작할 수 없습니다.
        * 플로우를 임시 저장하더라도 마지막 저장 시점으로 되돌릴 수 없습니다.
        * 임시 저장 시 커밋명을 입력하여 어떤 변경이 있었는지 기록할 수 있습니다.
    * 저장
        * 플로우의 완성도를 정적으로 평가하고 저장합니다.
        * 플로우 완성도 평가를 통과하지 못할 경우 저장 요청에 실패하며, 실패 이유를 표시합니다.
        * 저장한 플로우는 시작 요청이 가능합니다.
        * 저장 시 커밋명을 입력하여 어떤 변경이 있었는지 기록할 수 있습니다.

### 수정 이력

플로우를 수정한 이력을 표시합니다.

![management_flowhistory.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/management_flowhistory.png)

* 수정한 날짜와 사용자 정보를 표시합니다.
* 저장/임시 저장 시 입력한 커밋명을 표시합니다.
* 당시 저장된 방식이 저장/임시 저장 중 어떤 방식이었는지 표시합니다.

### 실행 이력

플로우 시작/종료 요청한 이력을 표시합니다.

![management_actionhistory.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/management_actionhistory.png)

* 실행한 날짜와 사용자 정보를 표시합니다.
* 요청한 동작을 표시합니다.
* 요청한 동작으로 인해 플로우가 어떤 상태인지 표시합니다.
* 실행 중인 플로우일 경우 새 창에서 플로우 상세 상태를 확인할 수 있습니다.

## 모니터링

실행 중인 플로우나 노드의 모니터링 정보를 표시합니다.
**Data & Analytics > DataFlow > 모니터링**을 클릭합니다.
플로우 화면 영역과 모니터링 영역 경계를 움직여 화면 비율을 조정할 수 있습니다.
또한 모니터링 영역의 오른쪽 상단에 위치한 영역 크기 조절 아이콘을 클릭해 지정된 화면 비율로 조정할 수 있습니다.

![monitoring.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/monitoring.png)

### 플로우 목록

모니터링 가능한 플로우 목록을 표시합니다.

* 상세한 모니터링 정보를 확인하기 위해 플로우를 선택할 수 있습니다.
* 플로우의 목록 트리를 확장하여 플로우에 포함된 각 노드를 선택하여 상세한 모니터링 정보를 확인할 수 있습니다.
* 목록 접기를 통해 모니터링 상세 페이지 영역을 확장할 수 있습니다.
* **삭제된 플로우도 보기** 버튼을 통해 삭제된 플로우의 모니터링 정보도 확인할 수 있습니다.

### 플로우 화면 영역

플로우의 모양을 표시하는 영역입니다.

* 현재 실행 중인 플로우의 전체적인 그래프를 표시합니다.
* 노드를 선택하여 노드에 특화된 모니터링 정보를 확인할 수 있습니다.
* 전체적인 그래프가 원하는 위치로 오도록 플로우 화면을 조정할 수 있습니다.

### 모니터링 영역

모니터링 차트를 표시하는 영역입니다.

* 선택된 플로우나 노드의 모니터링 정보를 차트로 확인할 수 있습니다.
* 배율 조정과 초기화를 통해 플로우가 화면에 잘 보이도록 조정할 수 있습니다.
    * 배율 조정
        * 플로우 그래프가 표시되는 화면의 배율을 조정합니다.
        * 0.5배~2배까지의 배율을 지원합니다.
    * 초기화
        * 배율 조정을 통해 조정한 배율을 1배로 조정합니다.
* 차트 기간 선택
    * 기간 일괄 조정
        * 버튼 토글을 통해 차트 확대/축소 동작을 모든 차트에 동기화할 수 있습니다.
    * 현재 시간
        * 차트 기간을 현재 시간으로 설정합니다.
    * 기간 선택
        * 모니터링 정보를 확인할 기간을 선택합니다.
        * 새로 고침 설정을 통해 모니터링 정보의 새로 고침 주기를 선택합니다.
        * **취소**를 클릭해 변경할 기간을 적용하지 않을 수 있습니다.
    * 차트
        * 차트의 범위를 지정하여 차트를 확대/축소할 수 있습니다.

## 템플릿

템플릿 메타데이터 정보를 조회하고 생성 및 수정하는 페이지입니다.
**Data & Analytics > DataFlow > 템플릿**을 클릭합니다.

![template_main.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/template_main.png)

### 검색

주어진 기준으로 템플릿을 검색합니다.

* 템플릿 이름을 기준으로 검색하면 이름에 검색어가 포함된 템플릿을 검색합니다.

### 템플릿 조회

조회 결과 템플릿을 테이블 형태로 표시합니다.

* 간단한 템플릿 메타데이터를 표시합니다.
* 최근 수정일을 기준으로 정렬합니다.
* 템플릿을 선택하여 템플릿 변경, 템플릿 상세보기 등의 기능을 사용할 수 있습니다.
* 한번 조회된 템플릿은 새로 고침을 눌러야 조회 결과를 갱신합니다.
* 한 페이지당 12개의 템플릿을 조회하고 **이전** 또는 **다음**을 클릭해 페이지를 이동할 수 있습니다.

### 템플릿 생성

템플릿을 정의할 메타데이터를 생성합니다.

* 템플릿 식별을 위해 이름과 설명을 추가하여 템플릿 메타데이터를 생성합니다.
* 템플릿 이름은 다른 템플릿 이름과 중복이 가능합니다.
* 플로우 템플릿은 지정할 수 없습니다.
* 생성된 템플릿은 플로우 혹은 템플릿 로직 정의 시 노드 유형 목록에서 확인할 수 있습니다.

### 템플릿 변경

템플릿의 메타데이터를 수정합니다.

* 기존의 템플릿 이름과 설명을 수정하여 템플릿 메타데이터에 반영합니다.
* 플로우 템플릿은 지정할 수 없습니다.

### 템플릿 복사

기존의 템플릿 정의를 가지고 새로운 메타데이터를 생성합니다.

* 기존 템플릿 이름에 `_copy` 문구가 추가된 새로운 메타데이터를 생성합니다.
* 기존 템플릿이 가진 플로우 로직을 그대로 복사해 옵니다.
* 복사한 템플릿은 기존 템플릿과 완전히 별개의 템플릿입니다.

### 템플릿 삭제

템플릿 메타데이터를 삭제합니다.

* 템플릿 메타데이터를 완전히 삭제합니다.
* 삭제한 템플릿은 다시 복구할 수 없습니다.

## 템플릿 상세 보기

선택한 플로우의 상세 정보를 확인하는 세부 페이지입니다.
**Data & Analytics > DataFlow > 템플릿 > 템플릿 목록 중 하나**를 클릭합니다.
템플릿 목록 영역과 템플릿 상세 보기 영역 경계를 움직여 화면 비율을 조정할 수 있습니다.
또한 템플릿 상세 보기 영역의 오른쪽 상단에 위치한 영역 크기 조절 아이콘을 클릭해 지정된 화면 비율로 조정할 수 있습니다.

![template_detail.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/template_detail.png)

### 템플릿 정보

템플릿 로직을 정의합니다.

* 템플릿 설정으로부터 노드 유형이나 템플릿으로부터 플로우 구성 요소를 불러와 템플릿을 정의합니다.
    * **접기** 및 **펼치기**를 클릭해 템플릿 화면을 확장하거나 축소할 수 있습니다.
* 템플릿 화면을 조작하여 템플릿을 정의하고 그래프의 구성을 변경합니다.
    * 템플릿은 플로우와 달리 미완성 플로우를 자유롭게 저장할 수 있습니다.
* 배율 조정과 초기화, 화면 조정, 노드 정렬을 통해 플로우가 화면에 잘 보이도록 조정할 수 있습니다.
    * 배율 조정
        * 플로우 그래프가 표시되는 화면의 배율을 조정합니다.
        * 0.5배~2배까지의 배율을 지원합니다.
    * 초기화
        * 배율 조정을 통해 조정한 배율을 1배로 조정합니다.
    * 화면 조정
        * 플로우가 한 화면에 보이도록 배율 및 화면 중심을 조정합니다.
    * 노드 정렬
        * 플로우의 배열을 단계가 잘 드러나도록 정렬합니다.
        * 플로우가 한 화면에 보이도록 배율 및 화면 중심을 조정합니다.
* 편집한 플로우 정의를 취소/저장할 수 있습니다.
    * 취소
        * 편집한 템플릿 정의를 마지막으로 저장/임시 저장 당시의 상태로 되돌립니다.
    * 저장
        * 플로우를 미완성 형태로 저장할 수 있습니다.
        * 저장한 템플릿은 노드 유형의 템플릿 카테고리에서 불러올 수 있습니다.
## 설정
서비스에 필요한 설정을 관리하기 위한 페이지입니다.
**Data & Analytics > DataFlow > 설정**을 클릭합니다.

### Log & Crash Search 설정
사용자의 플로우 로그를 사용자가 설정한 Log & Crash Search로 연동하는 기능입니다.
Log & Crash Search 서비스에 로그를 저장하려면 Log & Crash Search 서비스를 활성화해야 하며 별도 이용 요금이 부과됩니다.


![settings_lncs_v2.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/settings_lncs_v2.png)

① **Log & Crash Search 저장 설정**을 클릭합니다.
② 로그를 저장할 Log & Crash Search **Appkey**키와 저장할 **로그 레벨**을 입력합니다.
③ **저장**을 눌러 설정을 마칩니다.
④ Log & Crash Search 연동 기능을 사용하기 원치 않을 경우, **삭제**를 눌러 저장 정보를 삭제합니다.

* 로그 필드

|             이름 |                              설명 |
|---------------|--------------------------------|
|       logLevel | 로그 레벨(INFO, WARN, ERROR, FATAL) |
|      logSource |                          `Flow` |
|           host |                      `DataFlow` |
|         appkey |                 DataFlow 서비스 앱키 |
|         flowId |                          플로우 id |
| flowInstanceId |                     플로우 인스턴스 id |

### 유효성 검사 설정
![settings_acc.png](http://static.toastoven.net/prod_dataflow/ko/console_user_guide/settings_acc.png)

플로우와 노드의 유효성 검사 사용 여부를 설정할 수 있습니다.
유효성 검사가 **사용 안함**으로 설정할 경우 플로우 저장 시 노드 유효성 검사를 자동으로 수행하지 않으며, 노드별 유효성 검사 기능을 사용할 수 없습니다.