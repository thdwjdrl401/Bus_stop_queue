# Bus Stop Queue — GPS 위치 추적 및 로그 기록 앱

실시간 GPS 좌표를 Google Maps에 표시하고, 위치 이력을 텍스트 파일로 저장하는 Android 앱입니다.

## 주요 기능

- **실시간 위치 추적** — FusedLocationProviderClient로 고정밀 GPS 좌표 수신 (최소 5ms 간격)
- **Google Maps 마커** — 현재 위치를 지도에 실시간 업데이트
- **역지오코딩** — GPS 좌표 → 주소 자동 변환 (Geocoder)
- **GPS 로그 저장** — 버튼 클릭으로 타임스탬프 + 위도/경도 이력을 `.txt` 파일로 저장
- **런타임 권한 처리** — Android 6.0+ 위치 권한 요청 및 GPS 활성화 유도

## 기술 스택

- Java, Android SDK
- Google Maps SDK for Android
- Google Play Services Location (`FusedLocationProviderClient`)
- Geocoder (역지오코딩)

## 시작하기

### 1. Google Maps API 키 설정

`GPS_TEST2/local.properties` 파일에 발급받은 API 키를 추가합니다:

```
MAPS_API_KEY=your_google_maps_api_key_here
```

> Google Cloud Console에서 **Maps SDK for Android**를 활성화한 후 API 키를 발급받으세요.

### 2. 빌드

Android Studio에서 `GPS_TEST2` 폴더를 열고 실행합니다.

## 필요 권한

| 권한 | 용도 |
|---|---|
| `ACCESS_FINE_LOCATION` | 고정밀 GPS 위치 수신 |
| `ACCESS_COARSE_LOCATION` | 네트워크 기반 위치 수신 |
| `WRITE_EXTERNAL_STORAGE` | GPS 로그 파일 저장 |
