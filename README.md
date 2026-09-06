# DustinYTDownloader Releases

`DustinYTDownloader`의 Windows 및 Android 직접 배포 파일과 Windows 자동 업데이트
정보를 제공하는 공개 배포 저장소입니다. 현재 Windows 버전은 **1.6.2**,
Android 버전은 **1.6.6**입니다.

## 바로 다운로드

- **Windows 일반 사용자:** [설치 프로그램 다운로드](https://github.com/DustinJung/forYoujinApp-releases/releases/download/v1.6.2/DustinYTDownloader-Setup-v1.6.2.exe)
- **Windows 무설치:** [포터블 EXE 다운로드](https://github.com/DustinJung/forYoujinApp-releases/releases/download/v1.6.2/DustinYTDownloader-Portable-v1.6.2.exe)
- **Windows 전체 묶음:** [설치형 + 포터블 ZIP 다운로드](https://github.com/DustinJung/forYoujinApp-releases/releases/download/v1.6.2/DustinYTDownloader-v1.6.2-Windows.zip)
- **Android 10 이상 ARM64:** [Android APK 1.6.6 다운로드](https://github.com/DustinJung/forYoujinApp-releases/releases/download/v1.6.6/DustinYTDownloader-v1.6.6-Android-arm64.apk)
- **파일 검증:** [SHA-256 체크섬 다운로드](https://github.com/DustinJung/forYoujinApp-releases/releases/download/v1.6.2/DustinYTDownloader-v1.6.2-SHA256.txt)

Windows는 일반적으로 설치 프로그램을 받으면 됩니다. 설치 없이 사용하려면 포터블
EXE를 선택하세요.

## 배포 파일

- `DustinYTDownloader-Setup.exe`: Windows 설치 및 기존 버전 제자리 업데이트
- `DustinYTDownloader-Portable.exe`: 설치 없이 실행하는 Windows 포터블 앱
- `DustinYTDownloader-v1.6.2-Windows.zip`: 설치형·포터블형·안내·라이선스 통합본
- `DustinYTDownloader-v1.6.6-Android-arm64.apk`: Android 10 이상 ARM64 직접 배포판
- `latest.json`: Windows 앱이 시작할 때 확인하는 최신 버전 및 SHA-256 정보
- `latest-android.json`: Android 앱이 시작할 때 확인하는 최신 버전 및 SHA-256 정보

Windows와 Android 모두 Python을 별도로 설치할 필요가 없습니다. Android판은
현재 직접 배포 MVP이며 실제 기기별 검증 전에는 프리뷰로 취급합니다.
1.6.6 APK 서명 인증서 SHA-256은
`424C3FEEAC971423172D365B7701EEC62F2F6A9DC4DFD7B61BAB4048D131B4F2`입니다.

Android 1.6.3은 다운로드 직후 앱이 홈 화면으로 종료될 수 있던 엔진 결합 구조를
Android 전용 yt-dlp 래퍼로 교체했습니다. 다운로드 진행률과 실패 단계를 표시하고,
MP3는 Android에서 토큰 없이 접근 가능한 호환 스트림을 우선 사용하며 변환 호출을
안전한 인수 배열 방식으로 바꿨습니다. 예상하지 못한 종료가 다시 발생하면 다음
실행 때 마지막 작업 단계를 보여 줍니다.

Android 1.6.4는 내장 yt-dlp를 PC와 동일한 2026.8.19로 올려 확인된 HTTP 403에
대응했습니다. 통합 MP4 형식이 없는 영상은 H.264 영상과 M4A 오디오를 각각
다운로드한 뒤 기기에서 MP4로 병합합니다.

Android 1.6.5는 실행 시 새 버전을 확인해 동의 후 APK를 다운로드하고 SHA-256을
검증한 뒤 설치 화면을 엽니다. 또한 FFmpegKit 필수 런타임 누락으로 MP3 변환에서
`com.arthenica.smartexception.java.Exceptions` 오류가 나던 문제를 수정했습니다.

Android 1.6.6은 MP3 저장 시 오디오 전용 MediaStore가 `Download` 경로를 거부하던
문제를 수정했습니다. MP3와 MP4 모두 Android 공식 Downloads 컬렉션을 사용하며
파일은 기존과 같이 `Download/DustinYTDownloader` 폴더에 저장됩니다.

Windows 1.6.2는 업데이트 안내와 영상 제목을 명시적으로 UTF-8로 처리해 한글
깨짐을 수정했습니다. 이전 앱도 1.6.2 안내를 읽을 수 있도록 이번 업데이트 문구는
ASCII 영문으로 제공합니다.

## 반드시 지켜야 할 이용조건

> **이 앱은 무조건 개인·비상업적·합법적 백업 목적으로만 사용해야 합니다.**

- 본인이 소유했거나 권리자로부터 명시적으로 다운로드 허가를 받은 콘텐츠에만 사용하세요.
- 저작권 침해, 유료·제한 콘텐츠의 무단 저장, 로그인·DRM·접근 제한 우회,
  재배포, 판매, 수익 창출 및 기타 상업적 사용을 금지합니다.
- 사용자는 YouTube 및 콘텐츠 제공자의 이용약관과 관련 법률을 직접 확인하고
  준수할 전적인 책임이 있습니다.
- 제작자는 침해·불법·우회 또는 상업적 목적 없이 합법적 개인 백업의 편의를 위해
  이 앱을 만들었습니다.
- 법률이 허용하는 최대 범위에서 제작자는 사용자의 행위로 발생한 청구, 손해,
  손실, 제재 또는 기타 법적 책임을 부담하지 않습니다.

면책 문구가 사용자의 위법행위를 합법으로 만들거나 법적 책임을 자동으로 없애는
것은 아닙니다. 허가 여부가 불분명하면 다운로드하지 마세요.

## 라이선스

Copyright © 2026 DustinJung. All Rights Reserved.

이 앱과 자체 소스는 `LICENSE`의 **DustinYTDownloader Proprietary Personal-Use
License v1.0**을 적용합니다. 오픈소스가 아니며, 명시된 범위 외 복제·수정·공개·
재배포·판매·서브라이선스·파생작 제작·상업적 이용을 허가하지 않습니다.

Chaquopy, yt-dlp, FFmpegKit, FFmpeg 등 제3자 구성요소는 각자의 라이선스가 그대로
적용되며, 이 독점 라이선스는 제3자 라이선스가 직접 부여한 권리를 제한하지 않습니다.

소스와 개발 문서는 비공개 `forYoujinApp` 저장소에서 관리합니다. 이 공개 저장소에는
인증 토큰, 서명 키, 비밀번호, 브라우저 쿠키 또는 개인 정보를 포함하지 않습니다.
