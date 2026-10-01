# 스크린샷 촬영 기록

2026-09-30 작업에서 배포 사이트와 로컬 앱을 직접 열어 JPEG 화면을 촬영했습니다. 2026-10-01에는 사용자가 제공한 도란도란 로그인 화면 PNG 원본을 추가했습니다. 이미지 생성이나 합성은 하지 않았습니다. 캡처는 화면 표시 확인 자료이며, 모든 기능의 정상 동작을 보증하는 테스트 결과는 아닙니다.

| 프로젝트 | 이미지 | 출처 및 확인 범위 |
| --- | --- | --- |
| 도란도란 | [공개 첫 화면](assets/screenshots/doran-doran.jpg), [아이 책방](assets/screenshots/doran-dashboard.png), [동화 읽기](assets/screenshots/doran-reader.png), [독해 문제](assets/screenshots/doran-quiz.png), [어휘 확인](assets/screenshots/doran-vocabulary.png), [스티커북](assets/screenshots/doran-stickerbook.png), [부모 성장 기록](assets/screenshots/doran-parent-dashboard.png) | https://doran-doran-front.vercel.app/ · 공개 첫 화면은 9월 30일 직접 촬영. 로그인 후 화면 6장은 10월 1일 사용자가 제공한 원본이며, 책방과 동화 읽기 화면은 브라우저에서도 확인. 문제 제출·낭독·PDF 저장과 성장 지표의 정확성은 이 캡처로 검증하지 않음. |
| BiddingFlow | [로그인](assets/screenshots/biddingflow-login.jpg) | [프론트엔드 저장소](https://github.com/Uranium10/SKN31-FINAL-front)의 기존 로컬 체크아웃에서 Vite 실행. 로그인 후 작업함은 촬영하지 않음. |
| USD | [시작](assets/screenshots/usd-title.jpg), [거래 화면](assets/screenshots/usd-market.jpg) | https://usd-public.vercel.app/ · 새 게임 → 프롤로그·튜토리얼 건너뛰기 → 정보 없이 진행 → 1일차 시작. 게임 내 가상 자산 화면. |
| 치매정보알리미 | [서비스 소개](assets/screenshots/dementia.jpg) | https://dementia-front.vercel.app/ · 공개 소개 화면 캡처. 상담 세션은 생성하지 않음. |
| apple-online | [게임 보드](assets/screenshots/apple-online.jpg) | https://apple-online.vercel.app/ · 촬영용 닉네임으로 진입 후 혼자 하기. 채팅 전송과 순위 등록 없이 보드 촬영. |
| MDViewer | [리더](assets/screenshots/mdviewer.jpg) | https://md-viewer-drab.vercel.app/ · 직접 작성한 촬영용 Markdown 예시 문서를 붙여 넣음. 공유 기능은 사용하지 않음. |
| HeadHandLeg | [게임 장면](assets/screenshots/head-hand-leg.jpg) | [저장소](https://github.com/Uranium10/HeadHandLeg)의 기존 로컬 프로덕션 빌드를 `next start -p 4311`로 실행. Local Sandbox 첫 장면. 원격 멀티플레이 미검증. |
| 선거 대시보드 | [전국 지도](assets/screenshots/voting-dashboard.jpg) | https://voting-dashboard-front.vercel.app/ · 8회(2022년) 결과 선택. 9회 데이터는 제작 당시 예측값이며 이 이미지에 표시되지 않음. 지도 표시는 확인했으나 서버 상세 조회와 데이터 정확성은 검증하지 않음. 저장소 README는 기본 Vite 안내로, 대체 실행 이미지는 없었음. |
| typo99 | [플레이](assets/screenshots/typo99.jpg) | https://typo99.vercel.app/ · 일반 모드 시작 후 문제·타이머 화면. 순위표에 기록을 제출하지 않음. |
| alkanoid | [지도](assets/screenshots/alkanoid.jpg) | https://alkanoid-rouge.vercel.app/ · 시작 전 지도 영역을 스크롤하여 촬영. 지역 목록과 지도 표시 확인. |
| MiniStudio | [UI 미리보기](assets/screenshots/ministudio-preview.jpg) | [README](https://github.com/Uranium10/MiniStudio#readme)에 안내된 브라우저 미리보기. 새 복제본에서 `npm ci`, Vite 실행. 빈 프로젝트에 악기 트랙을 추가해 타임라인과 패널 촬영. 네이티브 오디오 미연결로 ERROR 표시. |

## MiniStudio 촬영용 복제본 변경

브라우저 환경에서 `getCurrentWebview().onDragDropEvent(...)`가 동기 예외를 내어 전체 UI가 비어 있었습니다. 촬영용 복제본의 `src/App.tsx`에 `isTauri()` 확인을 추가하고, Tauri 환경이 아닐 때 네이티브 드래그앤드롭 등록만 건너뛰었습니다. 변경은 해당 복제본의 `log.txt`에 기록했고, 원본 저장소에는 반영하지 않았습니다. 네이티브 오디오·MIDI·플러그인 동작은 검증하지 않았습니다.

## 화면을 확보하지 못한 프로젝트

- **UranEngine**: 저장소에 README가 없으며 Windows 편집기 실행 파일과 소스·리소스가 존재합니다. 실행 환경 복원과 Direct3D 동작 확인은 이번 촬영 범위에서 완료하지 못했습니다. 게임 리소스 이미지를 실행 스크린샷으로 대체하지 않았습니다. [저장소](https://github.com/Uranium10/UranEngine)
- **DefaultSynth**: README와 기존 로컬 실행 파일을 확인했습니다. 데스크톱 앱 실행 도구의 승인이 만료되어 실제 창을 확보하지 못했습니다. README의 `SYNTH.png`는 목표 디자인이므로 실행 화면으로 사용하지 않았습니다. [README](https://github.com/Uranium10/DefaultSynth#readme)

BiddingFlow·치매정보알리미의 로그인 후 화면, 선거 결과 API, 네이티브 오디오 앱의 실행 화면은 추후 실제 실행 환경이 준비되면 추가할 수 있습니다.
