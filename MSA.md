## MSA Orchestration

#### Microservice Orchestration Workflow Engine
- [Netflix Conductor](netflix.md) : https://netflix.github.io/conductor/
- [Camunda Zeebe](zeebel.md) : https://docs.camunda.io/docs/guides/
- [Temporal](temporal.md) : https://temporal.io/
  - Microservice Orchestration with temporal : https://www.youtube.com/watch?v=6T6zVZHU7_Q
- Zoral

| F/W | Lisence | Spring Integration | 주요 기능 |
|----|----|----|----|
| Netflix Conductor | Apache License 2.0 | 사용가능 | -프로세스를 일시 중지/재개 및 다시 시작하는 기능<br> - workflow 추적 및 관리<br> - 프로세스 흐름을 시각화하기 위한 사용자 인터페이스<br> - HTTP/gRPC와 같은 여러 프로토콜 전송 기능|
| Camunda Zeebe | Zeebe Community License 1.1<br> Apache License 2.0 | 사용가능 | - END-TO-END WORKFLOW 가시성 제공<br> - 마이크로서비스 오케스트레이션<br> - 수평적 확장성<br> - ISO 표준 BPMN 2.0에서 모델링된 시각적 워크플로우  |
| Temporal | Apache License 2.0 | 사용가능 | - 애플리케이션의 일부가 실패하면 항상 일관된 상태로 복구<br> - 워크플로 실행 이벤트 루프에 대한 명확한 가시성을 제공<br> - 프로세스 흐름을 시각화하기 위한 사용자 인터페이스 |

#### Saga implementation frameworks
- [Narayana LRA](narayana.md) : https://github.com/eclipse/microprofile-sandbox/tree/master/proposals/0009-LRA
- [Axon framework](axon.md) : https://www.axoniq.io/
- [Eventuate.io](eventuate.md) : https://eventuate.io/

| F/W | Lisence | Spring Integration | 주요 기능 |
|----|----|----|----|
| Narayana LRA | Apache License 2.0 | 사용가능 | - 서비스 간 강력한 결합 없음<br> -  비즈니스 방법이 보상을 수행하는 방식에 있어 매우 유연 |
| Axon framework | Apache License 2.0 | 사용가능 | - 도메인 주도 설계<br> - 이벤트 소싱<br> - CQRS<br> - 마이크로서비스 아키텍처 지원<br> - Orchestration 방식의 Saga 패턴을 지원<br> - Axon Server없이 Axon Framework 사용가능함. <br> 단 Axon Server 대신 Event Store(예: 선택한 RDBMS)를 구성해야 함. <br> 마이크로서비스를 사용하려면 Axon의 JGroups 또는 Spring Cloud Extension을 사용하여 분산 명령 버스도 구성해야 함|
| Eventuate | Apache License 2.0 | 사용가능 | - Sagas를 활용한 데이터 정합성 유지<br> - CQRS<br> - 다중 언어와 프레임워크 지원 |
