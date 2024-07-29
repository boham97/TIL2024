# scale up

서버를 증강시켜 성능 증가

수직 스케일링

장점

- 구축, 설계 쉬움

- 네트워크 인프라 비용 X

단점

- 확장성 한계

- 용량 성능 확장 제한

- 비용(성능 증가에 따른 비용 중가 폭 큼)

- 트래픽 부하 -> 장애 영향도 증가

사용하는 이유

- 정합성 유지가 어려운 경우
  
  - 정합성?이란
    
    - **데이터 일관성**: 데이터베이스에서 데이터의 일관성은 동일한 데이터에 대해 여러 사용자가 동일한 시간에 접근했을 때, 동일한 결과를 보장하는 것을 의미합니다. 다시 말해, 데이터는 어떤 시점에서도 정확하고 일관된 상태여야 합니다.
    
    - **분산 시스템에서의 일관성**: 여러 서버에 데이터가 분산되어 있는 경우, 모든 서버 간에 데이터가 일관된 상태를 유지해야 합니다. 즉, 하나의 서버에서 데이터가 업데이트되면 다른 서버에서도 동일한 데이터를 조회했을 때 일관된 결과를 보여야 합니다.
  
  - 예시:
    
    - 분산 트랜잭션 복잡성
    
    - 복제 지연
    
    - 분산환경 네트워크 지연과 오류

- 온라인 트랜잭션 처리

- DB

# scale out

서대의 수를 증가 시켜 처리 능력 증가

수평 스케일

장점

- 지속적 확장성 가능

- 분산 처리 -> 장애 가능성 감소

- 저렴

- 유연성
  
  - 필요한 만큼 서버를 추가할 수 있다

단점

- 설계 구현 복잡
  
  - 관리 비용 증가

- 직렬화 (서버간 통신?)

sharding, NOSQL(하둡?), in memory cache

사용하는 이유

- 병렬성 실현 쉬운 경우

- 메일 게시판, 데이터 읽기 전용 어플리케이션, 웹서버등

SPOF single point of failure

단일 장애점

전체 시스템 중단 -> 높은 신뢰성은 단일 컴포넌트 의존X

