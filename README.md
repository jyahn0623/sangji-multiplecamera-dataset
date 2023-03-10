# 가천대학교 상지 다중카메라 데이터 셋 안내

본 데이터 셋은 가천대학교에서 진행된 실험 중 다중카메라로부터 수집된 데이터입니다.

## 실험 정보

본 실험이 측정된 환경은 아래 그림과 같습니다.

- 실험 환경

![image](https://user-images.githubusercontent.com/43843665/222639437-872a62df-8045-4d50-a206-60bbe6dc2348.png)

- 활용 모델

Mediapipe's Pose https://google.github.io/mediapipe/solutions/pose

- 각도 산출 정보

|구분|사용된 키 포인트|
|---|---|
|우측 팔꿈치 각도|16, 14, 12|
|좌측 팔꿈치 각도|15, 13, 11|
|우측 어깨 각도|14, 12, 24|
|좌측 어깨 각도|13, 11, 23|

![pose_tracking_full_body_landmarks](https://user-images.githubusercontent.com/43843665/222633346-e6948f7e-272c-40cb-a83c-01e701d1658a.png)


## 측정자 정보
|human number|나이|키|성별|
|---|---|---|---|
|1|21살|156cm|여성|
|2|23살|156cm|여성|
|3|23살|162cm|여성|
|4|27살|151cm|여성|
|5|23살|173cm|남성|
|6|24살|176cm|남성|
|7|23살|166cm|여성|
|8|31살|158cm|여성|
|9|23살|170cm|남성|
|10|24살|172cm|남성|
|11|26살|170cm|남성|
|12|24살|166cm|여성|
|13|25살|180cm|남성|

## 측정자세 정보

|position number|측정자세|
|---|---|
|1|어깨 옆으로 올리고 내리기 좌|
|2|어깨 옆으로 올리고 내리기 우|
|3|어깨 앞으로 올리고 내리기 좌|
|4|어깨 앞으로 올리고 내리기 우|
|5|팔꿈치 앞으로 올리고 내리기 좌|
|6|팔꿈치 앞으로 올리고 내리기 우|
|7|고개 앞으로 숙이고 돌아오기|
|8|고개 옆으로 숙이고 돌아오기 좌|
|9|고개 옆으로 숙이고 돌아오기 우|
|10|랫풀다운|
|11|비하인드넥풀다운|
|12|시티드로우 |
|13|체스트프레스|


## DB Table

데이터 셋은 다음과 같은 DB 테이블 형태로 구성되어 있습니다.

Table 이름은 `dataaset`입니다.

| Column name          | Data type | Description |
|----------------------|-----------|-------------|
| Frame count          | INTEGER   |영상 내 프레임 번호|
| human_number          | INTEGER   |측정자 번호|
| position_number          | INTEGER   |측정 자세 번호|
| camera_number          | INTEGER   |카메라 번호|
| right_shoulder_x            | REAL      |우측 어깨 x |
| right_shoulder_y           | REAL      |우측 어깨 y | 
| right_shoulder_z           | REAL      |우측 어깨 z |  
| right_elbow_x         | REAL      |우측 팔꿈치 x |
| right_elbow_y          | REAL      |우측 팔꿈치 y |
| right_elbow_z          | REAL      |우측 팔꿈치 z |
| right_wrist_x            | REAL      |우측 손목 x | 
| right_wrist_y           | REAL      |우측 손목 y | 
| right_wrist_z            | REAL      |우측 손목 z | 
| right_hip_x         | REAL      |우측 엉덩이 x |     
| right_hip_y          | REAL      |우측 엉덩이 y |
| right_hip_z         | REAL      |우측 엉덩이 z | 
| left_shoulder_x            | REAL      |좌측 어깨 x |
| left_shoulder_y           | REAL      |좌측 어깨 y |   
| left_shoulder_z           | REAL      |좌측 어깨 z|
| left_elbow_x          | REAL      |좌측 팔꿈치 x|
| left_elbow_y          | REAL      |좌측 팔꿈치 y|
| left_elbow_z        | REAL      |좌측 팔꿈치 z|
| left_wrist_x            | REAL      |좌측 손목 x|
| left_wrist_y          | REAL      |좌측 손목 y|
| left_wrist_z            | REAL      |좌측 손목 z|
| left_hip_x         | REAL      |좌측 엉덩이 x| 
| left_hip_y         | REAL      |좌측 엉덩이 y|
| left_hip_z         | REAL      |좌측 엉덩이 z|
| right_elbow_angle         | REAL      |우측 팔꿈치 각도|
| left_elbow_angle         | REAL      |좌측 팔꿈치 각도|
| right_shoulder_angle          | REAL      |우측 어깨 각도|
| left_shoulder_angle         | REAL      |좌측 어깨 각도|
| frame width          | INTEGER   |해당 이미지의 넓이|
| frame height         | INTEGER   |해당 이미지의 높이|
| file_name            | TEXT      |해당 이미지 파일명|

## 데이터 수

총 데이터 수는 1,842,545건입니다
| 구분          | 데이터 수 | 
|----------------------|-----------|
| Mediapipe가 분석한 데이터 수 | 1,816,704   |
| Mediapipe가 분석하지 못한 데이터 수  | 25,841   |
| 총 데이터 수           | 1,842,545   |

## 데이터 다운로드

데이터 파일이 큰 관계로 부득이하게 외부에서 다운로드 받도록 열어두었습니다.

1. SQLlite Databse 파일 - 데이터를 DB로 만든 파일입니다.

- [SQLlite Database 다운로드](https://marketian.sharepoint.com/:u:/s/IT/EVuFY6hKiuRPjjcudPUgG4IBkBsrtfM9LWZhKKNdJNrodA?e=MSwby7)

2. .CSV Data 파일 - 데이터를 CSV로 만든 파일입니다.

- [Database .CSV 다운로드](https://marketian.sharepoint.com/:u:/s/IT/ERo5ocZdM9hJuUGEE7r1krMBYuvJnFD48EjVuyW6Mhjmjw?e=nfOeVP)

3. 실험 영상 파일 - 측정자의 실험 원본 영상 파일입니다.

- [실험 영상 파일 다운로드](https://marketian.sharepoint.com/:u:/s/IT/ES1yGolmgN1PuqYBYXQxoEoB50DeXhsZI2LIyrwHp2mvyw?e=naK5yH)

4. 이미지 데이터 - 측정자의 스켈레톤이 추출된 이미지 파일입니다. 

|human number|다운로드|
|---|---|
|1|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EUYKoGkM0qdGnC1JsUZpAYcBg81kz4t0akx9_-Fb8olTnQ?e=K2ydUP)|
|2|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EZ9HLqxMjx1Jim5jAe6SRj8Br3UcBTPnZ1JeehKWZqmUGw?e=sOP8uG)|
|3|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/Ef8wWGcVCQpIo52oKKBnut4BtQW_vnoG-UGhv41yH6tEZA?e=OFw0Dn)|
|4|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EYR8E05Zr2RIgK5rMWqvDUwBRxqNaCLC0QZVW418dUDXEQ?e=WdoFz0)|
|5|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/Ed_x__vM5_RDvpTsFtVhDXQBeBM0UHqWpehT4KsufiWeMQ?e=7CtJgl)|
|6|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EZaaew3TfRpNhZMdlETgtKkBW02i_3F_hIfyYFlkVCAH1w?e=coydTV)|
|7|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EYbZPbA-WDVBsPsnZ2yyR-sBO_GBZ-JQD8IpdJlHogFSXQ?e=ZLI4m5)|
|8|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EeM8uI09q_5Hq2RP2XF-ajcB9Ec5UvR8bt0M7ejfCe89VA?e=P4SzBa)|
|9|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EV-f0414H85JltWIhyRbDNQBYMEE3WYlXDB7dVVu1hN9oQ?e=2402Za)|
|10|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/ER-SWAovNXZNnIt8t_52STgBCINIOJDZbtSKLNOXASfVRw?e=wAJ3O0)|
|11|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EUnvXtYtOPZDgvmzJCsCOusB0NzHcFJOXBSCXzuTBOhKjw?e=GzlIGv)|
|12|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/EXFvZfgA0l1Cl-AYq_9iT5EBiEuMd4JlBp3gBxXsvSQ5Bg?e=NdlGPk)|
|13|[다운로드](https://marketian.sharepoint.com/:u:/s/IT/ESeRbFRrxspLie0rJTGyIOQBIkwo-ouXzbRahW5IW1JyoQ?e=kkqaPh)|

## DB Broswer for SQLite

SQLite로 저장된 Database의 조회 및 관리를 위하여 아래 소프트웨어를 사용했습니다.

[DB Broswer for SQLite](https://sqlitebrowser.org/)

1. DB Broswer 실행 화면
![image](https://user-images.githubusercontent.com/43843665/222322395-9d4aff8e-763b-4f3e-bb7b-2952d44deeba.png)

2. DB 데이터 조회 화면
![image](https://user-images.githubusercontent.com/43843665/222322557-7adef8bf-dff7-4ca0-ade1-f8cd6211f83f.png)

3. DB 데이터 쿼리 화면 (측정자가 1인 경우 테스트)
![image](https://user-images.githubusercontent.com/43843665/222322571-0dcea1fc-09c4-4a4a-b6c5-0606b6f743aa.png)




