# shindap_rullet

신답초등학교 뽑기판. 이름을 붙여넣으면 구슬이 되어 맵을 굴러 내려가고,
먼저 도착한 순서로 당첨을 정한다. 당첨 뽑기, 모둠 짜기, 자리 배치에 쓴다.

https://shindap-rullet.vercel.app

## 만든 방식

`index.html` 한 파일에 화면·소리·물리가 모두 들어 있다. 물리 엔진을 쓰지 않고
원과 선분의 충돌을 직접 계산한다(`collideSegment`, `collideCircle` 등).
바깥에서 불러오는 것은 Pretendard 웹폰트뿐이다.

## 아이디어 출처

구슬을 떨어뜨려 뽑는 형식은 [lazygyu/roulette](https://github.com/lazygyu/roulette)로
널리 알려진 방식이다. 이 프로젝트는 그 저장소를 포크하지 않았고 코드도 가져오지
않았다. 원본은 TypeScript에 Parcel, box2d-wasm 물리 엔진을 쓰지만 여기서는
바닐라 JS로 새로 구현했다.
