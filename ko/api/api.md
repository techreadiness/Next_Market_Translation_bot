---
metaLinks:
  alternates:
    - https://app.gitbook.com/s/pt4moEMpSf4BGvjJCzQm/api/api
---

# API 목록

## Game ➡️ Next Market

### 인증 및 보안&#x20;

* [서버 시간 체크](undefined-1.md#post-api-v1-server-time)
* [스토어 인증용 원타임 토큰 요청](undefined-1.md#post-api-v1-auth-token)
* [스토어 세션 킥](undefined-1.md#delete-api-v1-account-session-kick)

### B2C 아이템 등록

{% stepper %}
{% step %}
#### 아이템 요청

* [미디어 파일 업로드](undefined-2.md#post-api-v1-media-upload)
* [아이템 등록](undefined-2.md#post-api-v1-item)
* [아이템 변경](undefined-2.md#put-api-v1-item-sku)
* [아이템 조회](undefined-2.md#get-api-v1-item-sku)
* [아이템 목록 조회](undefined-2.md#get-api-v1-item)
{% endstep %}

{% step %}
#### 섹션 요청

* [섹션 등록 ](undefined-3.md#post-api-v1-sale-b2c-section)
* [섹션 변경](undefined-3.md#patch-api-v1-sale-b2c-section-sectionid)
* [섹션 목록 조회](undefined-3.md#get-api-v1-sale-b2c-section)
{% endstep %}

{% step %}
#### 판매 요청

* [판매 등록 ](undefined-4.md#post-api-v1-sale-b2c)
* [판매 변경 ](undefined-4.md#patch-api-v1-sale-b2c-b2csaleid)
* [판매 목록 조회](undefined-4.md#get-api-v1-sale-b2c)
{% endstep %}
{% endstepper %}

### B2C 아이템 판매

* [원타임 토큰 요청](undefined-1.md#post-api-v1-auth-token)
* [판매량 통계 조회](undefined-4.md#undefined-7)
* [판매 등록](undefined-4.md#post-api-v1-sale-b2c)
* [판매 변경](undefined-4.md#patch-api-v1-sale-b2c-b2csaleid)
* [판매 목록 조회](undefined-4.md#get-api-v1-sale-b2c)
* [B2C 판매 삭제](undefined-4.md#delete-api-v1-sale-b2c-b2csaleid)

### C2C 아이템 등록

* [미디어 파일 업로드](undefined-2.md#post-api-v1-media-upload)
* [아이템 등록 ](undefined-2.md#post-api-v1-item)
* [아이템 능력 설정 등록 ](undefined-2.md#post-api-v1-item-ability)
* [아이템 능력 설정 수정](undefined-2.md#put-api-v1-item-ability-code)
* [아이템 능력 설정 목록 조회](undefined-2.md#get-api-v1-item-ability)

### C2C 아이템 판매&#x20;

* [원타임 토큰 요청](undefined-1.md#post-api-v1-auth-token)
* [아이템 배송 이력 조회](undefined-2.md#get-users-api-v1-item-send-item-requestid)
* [C2C 아이템 판매 취소](undefined-4.md#delete-api-v1-sale-c2c-c2csaleid)

### 정산

* [매출 데이터 조회](undefined-5.md#get-api-v1-settlement)

### 미션

* [미션 생성](undefined-7.md#post-api-v1-incentive-mission)
* [미션 수정](undefined-7.md#put-api-v1-incentive-mission-missionid)
* [미션 제거](undefined-7.md#delete-api-v1-incentive-mission-missionid)
* [업적 달성 기록 요청](undefined-7.md#post-api-v1-incentive-mission-achieve)
* [미션 보드 조회](undefined-7.md#get-api-v1-incentive-mission)



## Next Market ➡️ Game

### B2C 아이템 구매

* [계정 상태 조회](undefined-6.md#undefined)
* [아이템 배송](undefined-2.md#undefined-16)
* [아이템 배송 결과 조회](undefined-2.md#undefined-18)

### C2C 아이템 구매

* [실링](undefined-2.md#undefined-20)
* [언실링 ](undefined-2.md#undefined-22)
* [계정 상태 조회](undefined-6.md#undefined)
* [아이템 검증](undefined-4.md#c2c-verify)
* [아이템 교환](undefined-2.md#undefined-24)

### 계정&#x20;

* [게임 계정 상태 조회](undefined-6.md#undefined)
