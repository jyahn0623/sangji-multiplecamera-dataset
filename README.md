# 가천대학교 상지 다중카메라 데이터 셋 안내

본 데이터 셋은 가천대학교에서 진행된 실험 중 다중카메라로부터 수집된 데이터입니다.

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
| left_hip_z         | REAL      |측 엉덩이 z|
| right_elbow_angle         | REAL      |우측 팔꿈치 각도|
| left_elbow_angle         | REAL      |좌측 팔꿈치 각도|
| right_shoulder_angle          | REAL      |우측 어깨 각도|
| left_shoulder_angle         | REAL      |좌측 어깨 각도|
| frame width          | INTEGER   |해당 이미지의 넓이|
| frame height         | INTEGER   |해당 이미지의 높이|
| file_name            | TEXT      |해당 이미지 파일명|

## 데이터 수

총 데이터 수는 1,842,545건입니다

## 데이터 다운로드

데이터 파일이 큰 관계로 부득이하게 외부에서 다운로드 받도록 열어두었습니다.

1. SQLlite Databse 파일 - 데이터를 DB로 만든 파일입니다.

- [SQLlite Database 다운로드](https://marketian.sharepoint.com/:u:/s/IT/EVuFY6hKiuRPjjcudPUgG4IBkBsrtfM9LWZhKKNdJNrodA?e=MSwby7)

2. .CSV Data 파일 - 데이터를 CSV로 만든 파일입니다.

- [Database .CSV 다운로드](https://marketian.sharepoint.com/:u:/s/IT/ERo5ocZdM9hJuUGEE7r1krMBYuvJnFD48EjVuyW6Mhjmjw?e=nfOeVP)

3. 실험 영상 파일 - 측정자의 실험 원본 영상 파일입니다.

- [실험 영상 파일 다운로드](https://marketian.sharepoint.com/:u:/s/IT/ES1yGolmgN1PuqYBYXQxoEoB50DeXhsZI2LIyrwHp2mvyw?e=naK5yH)

## DB Brower for SQLite

SQLite로 저장된 Database의 조회 및 관리를 위하여 아래 소프트웨어를 사용했습니다.

[DB Brower for SQLite](https://sqlitebrowser.org/)



