# cleanact
Describe work progress on clean act study

자료: KOSIS
	
  - 가계동향조사 : 현재 게시된 자료는 제품 분할이 너무 조악하고 분기별 자료로 되어 있어 직접 사용이 어려움. 마이크로 데이터 월별자료가 필요(돈이 필요)
	
  - 서비스업 동향조사 (음식, 숙박/도매, 소매)- 산업별 서비스 생산지수 : 월별자료 직접 이용 가능
	
  - 농림축산화훼: 일단 경작/양육에 시간이 걸리는 곡물생산/축산의 물리적 생산은 크게 영향이 없을 것
	
    ○ 축산: 가축동향조사 (분기)
		
    ○ 농작물 생산조사(연)
		
    ○ 어업생산동향조사(월)
		
    ○ 임업: 임업서베이 가장 최근 자료는 2015년 => 해당 자료 없음
		
    ○ 화훼의 경우 꽃집 매출을 보는게 더 좋을 것. (있으면..) => 재배 면적 자료 2015년이 최근 (2016년 작성 중?)
	
  - 고용: 산업별 고용은 경제활동인구조사를 활용하면 추세 분석 가능.
	
  ○ 경제활동인구조사 자료 게시는 2017년 2월까지. 

자료: ECOS

  - 경제활동별 GDP/GNI : 2016 4분기까지 존재  ( Is 2016 4th quarter is different from others?
	
  - 생산자물가지수 2017년 2월까지 월별 자료 존재 ( Any price depression for three industries?)

분석 방법: Event Study.
	
  1. 월별 자료를 이용해서 3개월 window moving average를 구함 
  
  => 김영란법 발표 전후에 3개월 smoothing을 살아 남는 shock이 있는지 관찰  
  
  => 가격 depression 이나 소비 depression이  있는 산업/상품 파악 (Clustering)
	
  2.  DID with pre-determined cluster.
	
  3. 자료는 2013-2016년 4분기 .2017년 2월까지
	
  4. 잠재적 포인트는 제정 15년 3월/시행이 16년 10월 
	
  5.  분기자료 ARIMA
  
  2016 3분기까지 자료를 이용해서 ARIMA. Specified time series model 구축
  
  2016년 4분기가 추세에서 어느정도 벗어나는지 파악. 95% confidence interval 을 벗어나는 outlier 일 경우에는 shock 이 있었다고 파악.  
  
  Single Series identification would be enough, given that we don't have a lot of data points.
	
  6. Control business cycle and ship bankruptcy. 
		
    a. Business cycle: Compare sector specific shocks with general shocks. Take the difference
		
    b. Ship bankruptcy : Can we take ship industry from analysis? Small VAR and Impulse response? 
			i. Take the size of shock to this industry from shipbuilding. Shock the system with demand shock only. 
	
  8. Structural break wouldn't work. Only one data point after break. 
	
  9. What else???
