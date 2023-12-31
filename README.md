# 프로젝트명: SpyRobot

## [목차]

### 1. [컨셉](#1)
### 2. [게임 시나리오](#2)
### 3. [게임 시스템 디자인](#3)
### 4. [주차 별 개발 과정](#4)

# [컨셉]<a name='1'></a>

## 메인컨셉: 은밀

- 이 게임은 총기에 반동이 없어 ai가 플레이어를 발견하고 쏠 때 빚 맞힐 일이 극도로 적기에 플레이어들은 자신의 몸을 숨기면서 플레이 하는 것이 중요하다 생각합니다.

### 서브 컨셉1: 반응속도

- fps의 중요한 요소들 중 하나라고 볼 수 있는 반응속도는 적을 발견했을 때 먼저 쏠 수 있는 속도가 되겠습니다.

### 서브 컨셉2: 정확도

- fps장르의 두 가지 큰 핵심을 생각해보라고 한다면 첫 번째는 반응속도이지만 그에 못지않게 중요한 요소는 정확도라 생각합니다. 경우의 수를 생각해보자면 적을 발견하고 내 반응속도가 빨라 먼저 적을 쏘았는데 정확도가 낮아서 맞추지 못하면 아무런 쓸모가 없다 생각했기에 정확도를 서브 컨셉으로 정했습니다.

<br><br>

# [게임 시나리오]<a name='2'></a>

- 로봇들이 군사력의 척도가 된 이 세상에서 로봇들의 인식을 바꾸는 장치를 개발한 어떠한 테러 집단이 장치들을 이용해 로봇들을 적대관계로 바꾸어 버린다. 플레이어는 유일하게 그 장치의 영향을 받지 않는 개체였고 그러한 이유로 장치를 회수하여 이 사태에 대한 대처법을 알아내는 것이 목표다.

<br><br>

# [게임 시스템 디자인]<a name='3'></a>

## 1. 주요 오브젝트

1) 오브젝트 이름: Player

|행동|영문 명칭|설명|
|:----:|:----:|:----:|
|걷기|Move|W,A,S,D의 키를 입력받아 움직이는 행동|
|발사|Shot|좌클릭을 누르면 총알이 발사된다.|
|사망|Die|플레이어의 HP가 0이 될 때 사망한다.|

2) 오브젝트 이름: Enemy

|행동|영문 명칭|설명|
|:----:|:----:|:----:|
|걷기|Move|플레이어를 쫒아 움직이는 행동|
|발사|Shot|자신과 플레이어간의 거리가 일정 거리 내에 진입시 총알을 발사한다.|
|사망|Die|Enemy의 HP가 0이 될 때 사망한다.|

3) 오브젝트 이름: Car

|행동|영문 명칭|설명|
|:----:|:----:|:----:|
|걷기|Move|플레이어를 쫒아 움직이는 행동|
|폭발|Explode|자신과 플레이어간의 거리가 일정 거리 내에 진입 시 폭발한다.|
|사망|Die|Enemy의 HP가 0이 될 때 사망한다.|

## 2.주요 파라미터 및 공식

|이름|영문 명칭|수치|설명|
|:----:|:----:|:----:|:----:|
|최대 생명력|MaxHealth|100|플레이어의 최대 생명력|
|현재 생명력|CurrentHealth|(MaxHealth-Dmg)|캐릭터의 현재 생명력|
|데미지|Dmg|1|플레이어와 적들의 데미지|

|이름|공식|
|:----:|:----:|
|Hit_Head|Dmg = damage * 40|
|Hit_Arm|Dmg = damage * 5|
|Hit_Body|Dmg = damage * 10|
|Hit_Leg|Dmg = damage * 5|
|CurrentHealth|CurrentHealth = MaxHealth - Dmg|

<br><br>

# [주차 별 개발 과정]<a name='4'></a>

## 1주차 개발 내용

캐릭터의 이동 및 카메라 회전 및 조준점 구현

## 2주차 개발 내용

총 발사와 랜덤 스포너 구현

## 3주차 개발 내용

총 발사 사운드 및 파티클 제작

## 4주차 개발 내용

적 Enemy AI패턴 제작

## 5주차 개발 내용

적 Enemy의 플레이어 추적 및 총 발사 제작
 
## 6주차 개발 내용

플레이어와 적 Enemy의 애니메이션 제작

## 7주차 개발 내용

적 Enemy의 기본적인 체력 및 hp바 구현

## 8주차 개발 내용

중간고사

## 9주차 개발 내용

적 Enemy ‘Car’제작 및 플레이어 추적 구현 및 폭발

## 10주차 개발 내용

적Car에 들어갈 폭발 파티클 제작 및 구현 그에 따른 버그 수정(9주차의 폭발 코드 확인)

## 11주차 개발 내용

맵 스테이지 제작

## 12주차 개발 내용

기존의 총알 판정 스크립트 수정(OnCollisionEnter->OnTriggerEnter)

## 13주차 개발 내용

맵에 존재하는 적Enemy가 아닌 일반 맵 오브젝트 자동차를 스폰 및 움직이도록 구현

## 14주차 개발 내용

기존에 만들어두었던 것들에 대해 버그 수정 및 2주차에 만들어두었던 랜덤스포너를 활용해서 맵 필드에서 스폰되도록 설정













