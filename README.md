# 🏔️ 산악 안전을 위한 위치/건강 모니터링 및 긴급 구조 시스템  
 
> 실시간 생체 정보와 위치 추적을 통해 산악 사고 시 신속한 구조를 지원합니다.



---



## 📘  1. 프로젝트 개요

#### 1-1. 프로젝트 소개
- 프로젝트명 : 산악 안전을 위한 위치/건강 모니터링 및 긴급 구조 시스템
- 프로젝트 정의 : 산악 사고 시 등산객의 위치와 생체 정보를 모니터링하여 구조를 지원하는 산악 안전 지원 서비스

#### 1-2. 개발 배경 및 필요성
- 산악 지역은 지형적 특성과 불안정한 통신 환경으로 인해 사고 시 구조 요청이 원활하지 않은 문제가 있습니다. 이에 따라 조난자의 위치와 생체 정보를 실시간으로 파악할 수 있는 시스템이 필요합니다.
- 사고 발생 직후 신속한 위치 파악과 건강 상태 모니터링은 생존율 향상에 큰 영향을 미칩니다. 기존 구조 요청 방식의 한계를 극복하고, 긴급 상황에서 구조 신호를 정확하게 전달할 수 있는 기술적 보완이 요구됩니다.
- 따라서 위치·건강 모니터링 기반의 산악 안전 긴급 구조 시스템 개발이 필수적입니다.

#### 1-3. 프로젝트 특장점
- 웨어러블 센서를 통한 사용자의 위치 및 심박수 등 생체 데이터를 일정 간격으로 수집·분석하여 사용자의 건강 상태와 위험 여부를 실시간 판단
- 저전력·장거리 통신이 가능한 LoRa 기반 통신 기술을 활용해 통신 환경이 불안정한 산악 지역에서도 구조 요청 신호를 안정적으로 전송
- 자동 위험 감지 및 경고 시스템으로 낙상, 등산로 이탈 등 이상상황 발생 시 즉시 사용자에게 경고하고, 필요시 즉시 구조 요청을 전송
- 우선순위 구조 알고리즘을 적용해 다수의 구조 요청 발생 시 긴급도와 위험도를 고려한 효율적 구조 지원
- 통신·데이터·알고리즘을 통합한 지능형 산악 안전 관리 플랫폼으로 신속하고 체계적인 구조 대응 구현

#### 1-4. 주요 기능
- 실시간 위치 및 생체 정보 모니터링
- LoRa 기반 긴급 구조 신호 전송
- 자동 위험 감지 및 긴급 경고
- 우선순위 구조 판단 알고리즘
- 통합 관리 및 구조 지원 대시보드

#### 1-5. 기대 효과 및 활용 분야
- 기대 효과 : 주변 위험 예측과 통신이 어려운 지역에서도 실시간 모니터링으로 안전 관리 효율 향상
- 활용 분야 : 산악, 캠핑 야외 활동 및 소방 시스템과 같은 재난 대응 등 다양한 구조 서비스로 확장 가능

#### 1-6. 기술 스택
<!-- 백엔드 기술 스택 FastAPI -> Flask로 수정했습니다! -by. 서현 -->
- 프론트엔드 : React
- 백엔드 : Python(Flask), Node.js
- AI/ML : OpenAI API
- 데이터베이스 : PostgreSQL, DBeaver
- 클라우드 : NHN Cloud
- 배포 및 관리 : GitHub Actions



## 👩‍💻  2. 팀원 소개
#### 2-1. 팀장 : 방서현
- 역할 : 개발총괄, 하드웨어
#### 2-2. 팀원1 : 이채림
- 역할 : iOS 버전 애플리케이션
#### 2-3. 팀원2 : 송채린
- 역할 : Android 버전 애플리케이션
#### 2-4. 팀원3 : 김수아
- 역할 : 데이터베이스, 서버
#### 2-5. 멘토1 : 박진산
- 역할 : 프로젝트 총괄
#### 2-6. 멘토2 : 신의섭
- 역할 : 프로젝트 총괄, 하드웨어



## 🧩 3. 시스템 구성도
#### 3-1. 서비스 구성도
<!-- 최신 구성도 이미지 업로드&수정했습니다! -by. 서현 -->
![service.png](https://github.com/S2ua4/geongangro/blob/main/readImage/service2.png)
- front-end
	- 사용자 앱 : 위치·건강 확인, 수동 구조 요청, 경고 수신
	- Node-RED 대시보드 : 지도 기반 실시간 모니터링·마커 색상 변화
 	- 구조대 앱 : 구조 대상 위치·건강 확인, 우선순위 결과 수신
- back-end
	- 웨어러블로 위치·건강 데이터 주기적 수집
 	- Flask 기반 API서버로 클라우드 연동
	- Node-RED로 분석 경고·구조 요청 처리
	- PostgreSQL를 이용하여 산악 지역의 지역·위치 데이터를 저장 및 백업

#### 3-2. 기능 처리도 (기능 흐름도)
<!-- 이미지 하나 선택할 것! -->
![flowchart](https://github.com/S2ua4/geongangro/blob/main/readImage/flowchart.png)
<!-- ![flowchart2](https://github.com/S2ua4/geongangro/blob/main/readImage/flowchart2.png) -->
- 사용자 앱–관제실 서버–구조대 앱 간의 통신 과정을 LoRa·Wi-Fi 네트워크 기반으로 시각화한 서비스 아키텍쳐

#### 3-3. 사용자 모바일 앱 메뉴 구성도
![userMenu.jpg](https://github.com/S2ua4/geongangro/blob/main/readImage/userMenu.jpg)

#### 3-4. 구조대 모바일 앱 메뉴 구성도
![secureMenu.jpg](https://github.com/S2ua4/geongangro/blob/main/readImage/userMenu.jpg)

#### 3-5. ERD
![erd.jpg](https://github.com/S2ua4/geongangro/blob/main/readImage/erd.png)

#### 3-6. 테이블 정의서
- users Table
![userTable.jpg](https://github.com/S2ua4/geongangro/blob/main/readImage/userTable.jpg)
- rescuer Table
![rescuerTable.jpg](https://github.com/S2ua4/geongangro/blob/main/readImage/rescuerTable.jpg)
- gpssLogs Table & healthLogs Table
![logsTalbe](https://github.com/S2ua4/geongangro/blob/main/readImage/logsTable.jpg)
- Mountain_locations Table & bukhansan_trails Table 
![loactionTable](https://github.com/S2ua4/geongangro/blob/main/readImage/locationTable.jpg)

#### 3-7. 구조 우선순위 판단 알고리즘 명세서
![algorithm.png](https://github.com/S2ua4/geongangro/blob/main/readImage/algorithm.png)
##### 시나리오 개요
- 등산 중 3명의 사용자가 동시에 구조 요청을 보낸 상황을 가정합니다. 서버는 각 사용자의 심박수, 위치 데이터를 기반으로 위험 점수를 계산하여 구조 우선순위를 자동으로 산출합니다.
- 서버는 계산된 위험 점수를 기반으로 구조 우선순위 리스트를 생성하고 이를 구조대 단말기에 전송하여 구조 진행 순서를 결정합니다.

| 사용자 | 상태 요약 | 위험 점수 | 우선순위 |
|:--|:--|:--|:--|
| **이 대리** | 고심박(160bpm), GPS 이탈 6m, 3분 무반응 | +85점 | 1순위 |
| **박 부장** | 심박 145bpm, GPS 이탈 8m, 2분 무반응 | +60점 | 2순위 |
| **김 사원** | 정상 심박, 경로 유지, 반응 있음 | +0점 | 3순위 |
    
##### 주요 처리 단계
1. 이상 징후 판단
2. 위험 요소별 점수 계산
   - 심박수 150bpms 초과 시 가중치 부여
   - GPS 경로 이탈 시 가중치 부여
   - 움직임 없음(무반응) 시 가중치 부여 
3. 종합 위험도 산출 : 개별 점수 합산하여 총 위험도 계산
4. 우선순위 정렬 및 전송 : 종합 점수 순으로 구조대 단말기에 리스트 전송


## 4. 작품 소개영상
[![[2025 한이음 드림업 공모전] 산악 안전을 위한 위치/건강 모니터링 및 긴급 구조 시스템 - 프로젝트 소개 영상](https://i9.ytimg.com/vi_webp/67kj4Bfilcw/mqdefault.webp?v=68eda575&sqp=COCCt8cG&rs=AOn4CLBWJMtC0PVxaeyaakqBJyEt7RIJxQ)](https://youtu.be/67kj4Bfilcw?si=imEq-6aMxHYZTWLK)

## 5. 핵심 소스코드
#### 5-1. 산악 안전 웨어러블 송신기 
- 본 송신기 코드는 MAX30102·GPS 센서 데이터를 주기적으로 수집하여 LoRa 네트워크로 서버에 전송하며, SOS 버튼을 통해 긴급 구조 신호를 전송할 수 있도록 설계함
##### 1. 센서 데이터 수집 (MAX30102 + GPS)
```cpp
void readSensors() {
  for (byte i = 0; i < MY_BUFFER_SIZE; i++) {
    while (!particleSensor.check()) {}
    redBuffer[i] = particleSensor.getRed();
    irBuffer[i] = particleSensor.getIR();
  }

  maxim_heart_rate_and_oxygen_saturation(
    irBuffer,러블 수신기
- 송신기가 보낸 데이터를 수신기가 받아 데이터베이스에 저장하는 역할
##### 1. LoRa 및 wi-fi 초기화
- LoRa 수신기를 초기화하여 송신기로부터 데이터 패킷 수신
- wi-fi 연결을 통해 서버와 통신 준비 완료
``` cpp
SPI.begin(5, 19, 27, LORA_SS);
LoRa.setPins(LORA_SS, LORA_RST, LORA_DIO0);
LoRa.begin(LORA_FREQ);

WiFi.begin(ssid, password);
while (WiFi.status() != WL_CONNECTED) delay(500);
```
##### 2. LoRa 패킷 수신 및 데이터 파싱
- LoRa로 들어온 문자열 데이터를 수신
``` cpp
if (LoRa.parsePacket()) {
  String incoming = "";
  while (LoRa.available()) incoming += (char)LoRa.read();

  int bpm, spo2;
  float lat, lon;
  sscanf(incoming.c_str(), "HR=%d,SpO2=%d,Lat=%f,Lon=%f", &bpm, &spo2, &lat, &lon);
}

```
##### 3. DB 서버 전송
- 수신 데이터를 JSON 형식으로 변환
- 서버 측에서는 PostSQL DB에 사용자별 생체 및 위치 데이터를 저장
``` cpp
String jsonData = "{";
jsonData += "\"user_id\":1,";
jsonData += "\"latitude\":" + String(lat, 6) + ",";
jsonData += "\"longitude\":" + String(lon, 6) + ",";
jsonData += "\"bpm\":" + String(bpm) + ",";
jsonData += "\"spo2\":" + String(spo2);
jsonData += "}";

HTTPClient http;
http.begin(serverUrl);
http.addHeader("Content-Type", "application/json");
http.POST(jsonData);

```

//#### 5-2. 중계기?

#### 5-3. 수신한 데이터를 Flask 서버로 전송
- wi-fi를 통해 Flask 서버와 통신하고 PostgreSQL로 업로드하는 중간 게이트웨이 역할
##### 1. Wi-Fi 연결 및 OLED 상태 표시
- 장치가 Wi-Fi 네트워크에 연결될 때까지 대기
- OLED에 연결 상태와 IP 주소 표시
```cpp
WiFi.begin(ssid, password);
while (WiFi.status() != WL_CONNECTED) {
  delay(500);
  Serial.print(".");
}
Serial.println("WiFi connected");
u8g2.print("WiFi Connected!");
```
##### 2. JSON 데이터 생성 (센서 측정값 → 전송 포맷 변환)
- Flask API 서버가 처리 가능한 포맷으로 구성
``` cpp
StaticJsonDocument<200> doc;
doc["user_id"] = 1;
doc["device_id"] = "TTGO_LORA32_TEST";
doc["bpm"] = random(60, 100);
doc["spo2"] = random(95, 100);
doc["latitude"] = 37.5 + (random(-50, 50) / 1000.0);
doc["longitude"] = 126.9 + (random(-50, 50) / 1000.0);

String jsonString;
serializeJson(doc, jsonString);
```
##### 3. 서버로 데이터 전송 (TCP 소켓 or HTTP POST)
``` cpp
if (client.connect(serverHost, serverPort)) {
  client.println(jsonString);
  Serial.println("Data sent!");
} else {
  Serial.println("Connection failed!");
}
```

