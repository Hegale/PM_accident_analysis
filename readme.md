

# 전처리

### build_road.ipynb
: linestring 데이터의 '도로폭' 속성을 기반으로 buffer하여 실제 폭 도로 데이터를 파일로 반환한다.

### merge_traffic.ipynb
: 2017년 1월~2019년 12월까지의 도로별 교통량을 병합, 파일로 반환한다.

### area_separate.ipynb
: 용도지역 데이터를 분류 및 도시하고, 사고지점의 분포를 확인한다.

### pm_slope.ipynb
: 사고지점의 경사도 분포를 확인

### point_buff.ipynb
: 버스정류장, 신호등, 횡단보도 데이터에 대해 buffer를 진행

---

### input data

data

├─ road

│  └─ Z_KAIS_TL_SPRD_MANAGE_11000.shp 외 3개 파일

│  └─ Z_KAIS_TL_SPRD_MANAGE_2018 (테이블 정의서)

├─ traffic

│  └─ 2017

│  └─ 2018

│  └─ 2019

├─ PM

│  └─ pm4326.csv


### output data

data

├─ road

│  └─ buffer_road_5181.shp 외 3개 파일

├─ traffic

│  └─ 총 교통량_지점별.csv

│  └─ traffic_by_length

---

# 분석

### build_raster.ipynb
: 역거리 가중치 보간법을 구현하여 포인트 데이터로 래스터 생성

### merge_raster.ipynb
: 도로, 용도지역, 포인트를 래스터화해 합산

### raster_analysis.ipynb
: merge_raster의 산출물과 실제 사고지점을 비교하여 사고발생률 확인

### point_count.ipynb
: 각 포인트 버퍼에 대해 사고지점 분포 확인

### road_analysis.ipynb
: 교통량 데이터와 도로 데이터의 병합, 교통량과 도로폭을 히스토그램으로 확인

### slope_analysis.ipynb
: 경사도 분석 및 사고지점 folium으로 도시

### statistics_PM.ipynb
: 가해운전자 / 피해운전자 연령을 도시

### result_folium.ipynb
: 최종 결과들을 folium으로 도시하여 html로 내보내기
