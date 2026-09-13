# Ar tonelico 한국어 패치

PlayStation 2 일본판 **Ar tonelico: Sekai no Owari de Utai Tsuzukeru Shoujo**를 위한 비공식 한국어 패치입니다.

- 현재 버전: `v.0.9.0`
- 대상 시리얼: `SLPS-25604`
- 대상 버전: 일본판 `1.03`
- 배포 형식: xdelta 차분 패치
- 원본 게임 데이터와 ISO는 이 저장소에 포함하지 않습니다.

## 다운로드

저장소의 **Releases** 페이지에서 `Ar_tonelico_Korean_Patch_v.0.9.0.xdelta`를 받으세요.

## 적용 대상

반드시 수정되지 않은 일본판 ISO를 사용해야 합니다.

| 항목 | 값 |
|---|---|
| 원본 ISO 크기 | `3,783,163,904` bytes |
| 원본 ISO SHA-256 | `E35BAA27F64B60F05E9ABB532B89FCE19AEDC1A3466C0D5329C77359BCC8CB0E` |
| 패치 후 ISO SHA-256 | `5A489C74B8B98B9CF5AC79733C8A6C3FF35D74A84EBB43A097F6CE73FD5A954C` |
| xdelta SHA-256 | `38182D149EC54A4896AC89C0F6745EEC9C4C5BB5C6893D98B4487535C49716B5` |

이미 패치된 ISO, 다른 지역판, 압축 이미지 또는 다른 덤프에는 적용하지 마세요.

## 적용 방법

xdelta3 또는 호환 GUI에서 다음 파일을 지정합니다.

1. Source file: 위 SHA-256과 일치하는 원본 일본판 ISO
2. Patch file: `Ar_tonelico_Korean_Patch_v.0.9.0.xdelta`
3. Output file: 새로 만들 한국어판 ISO

명령행 예시:

```text
xdelta3 -d -s "original.iso" "Ar_tonelico_Korean_Patch_v.0.9.0.xdelta" "Ar_tonelico_Korean_v.0.9.0.iso"
```

## 패치 범위

- 일본어 원문 기반 활성 텍스트 `40,218`행 한국어화
  - 이벤트/EVD `25,346`행
  - 실행 파일/ELF `14,872`행
- 한국어 비트맵 폰트 및 화자명 표시
- 대사 공백·줄바꿈·오버플로 대응
- 확인된 이미지형 UI 컨테이너 `109`개 한국어화 및 무결성 검사
- 메뉴·상태·전투·상점·지도·설정·도움말 등 주요 UI
- 실행 파일에 패킹된 하단 조작 범례 `56`개 한국어화
- 시작 및 인카운트 도움말 이후 프리징 관련 데이터/제어 흐름 보수

자세한 항목과 제외 범위는 [PATCH_SCOPE.md](PATCH_SCOPE.md)를 확인하세요.

## `v.0.9.0` 주의사항

- 전체 시나리오를 처음부터 끝까지 플레이하는 실기 검수는 아직 진행 중입니다.
- 동영상·사전 렌더링 연출에 포함된 일본어 자막은 이번 버전의 완전 보장 범위가 아닙니다.
- 텍스트 여부가 불확실했던 이미지 후보 `7`개는 확정 UI 범위에서 제외했습니다.
- 문제 제보 시 발생 장소, 직전 대사, 사용한 저장 파일 종류와 화면을 함께 남겨 주세요.

## 검증

릴리스 패치는 xdelta3 `3.2.0`으로 생성했으며, xdelta3 `3.1.0`으로 원본 ISO에 다시 적용해 패치 후 ISO SHA-256이 위 값과 정확히 일치하는 것을 확인했습니다.

이 프로젝트는 권리자와 무관한 비공식 팬 번역입니다.
