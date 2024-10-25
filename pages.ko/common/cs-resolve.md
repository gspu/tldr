# cs resolve

> 해결은 다른 종속성의 전이적 종속성을 나열.
> 더 많은 정보: <https://get-coursier.io/docs/cli-resolve>.

- 두 가지 종속성의 정의적 종속성 목록을 해결:

`cs resolve {{그룹_아이디1}}:{{아티팩트_아이디1}}:{{아티팩트_버전1}} {{그룹_아이디2}}:{{아티팩트_아이디2}}:{{아티팩트_버전2}}`

- 종속성 트리를 통해 패키지의 전이적 종속성 목록을 확인:

`cs resolve --tree {{그룹_아이디}}:{{아티팩트_아이디}}:{{아티팩트_버전}}`

- 종속성 트리를 역순으로 해결 (종속성에서 종속성으로):

`cs resolve --reverse-tree {{그룹_아이디}}:{{아티팩트_아이디}}:{{아티팩트_버전}}`

- 특정 라이브러리에 의존하는 모든 라이브러리를 출력:

`cs resolve {{그룹_아이디}}:{{아티팩트_아이디}}:{{아티팩트_버전}} --what-depends-on {{검색된_그룹_아이디}}:{{검색된_아티팩트_아이디}}`

- 특정 라이브러리 버전에 의존하는 모든 라이브러리를 출력:

`cs resolve {{그룹_아이디}}:{{아티팩트_아이디}}:{{아티팩트_버전}} --what-depends-on {{검색된_그룹_아이디}}:{{검색된_아티팩트_아이디}}{{검색된_아티팩트_버전}}`

- 패키지들 간의 최종 충돌 결과를 출력:

`cs resolve --conflicts {{그룹_아이디1:아티팩트_아이디1:아티팩트_버전1 그룹_아이디2:아티팩트_아이디2:아티팩트_버전2 ...}}`
