# Santa Attic · 1인칭

크리스마스 산타 배쓰밤 XR 게임의 다락방 공간을 1인칭으로 걸어다닐 수 있게 만든 버전이에요.
기존 프로토타입(`Dear-Stranger-from-Santa`)은 그대로 두고 따로 복제해서 작업해요.

## 조작
- 데스크톱: 화면 클릭 = 시점 잠금, 마우스 = 둘러보기, WASD = 걷기, Shift = 빠르게, C = 웅크리기, Esc = 해제
- 시점 잠금 중 왼쪽 클릭은 화면 가운데 조준점 기준으로 식물/머그와 상호작용
- 모바일: 왼쪽 아래 조이스틱 = 걷기, 화면 드래그 = 둘러보기
- VR: 왼쪽 스틱 = 걷기(충돌 포함), 오른쪽 스틱 = 30° 회전
- HUD의 `1인칭 걷기` 버튼을 누르면 충돌 없는 `자유 비행`(Q/E 위아래)으로 바뀌어요

## 파일
- `index.html` 메인 페이지 (three.js 0.169 + WebXR, 충돌은 three-mesh-bvh)
- `room.glb.js` 다락방 모델(base64). 대신 `room.glb`를 두어도 돼요
- `modules/herbs.js`, `modules/mug.js` 허브/머그 상호작용 (없으면 건너뜀)

## 로컬 실행
`python3 -m http.server` 후 http://localhost:8000 (VR은 HTTPS 필요: GitHub Pages 사용)
