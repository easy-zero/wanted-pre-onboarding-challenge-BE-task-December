## 1-1) 사전과제 진행 가이드

- 아래 총 5 문제에 대한 해설을 작성한 뒤 Pull Request를 날려주세요.
- 문제 해설에 대한 정해진 양식은 없으며, 최대한 자세히 해설해주시면 좋습니다.
- 문제 유형은 해당 코스에서 다룰 주제들을 포함하고 있으니 완벽히 이해하시면 코스를 수강하는데 큰 도움이 될 것입니다.

**문의 사항은 사전 과제 Repository의 Issue로 등록해 주세요.*



## 1-2) 사전 과제

- (1) 동기와 비동기 프로그래밍에 대한 차이점을 설명해주세요.

> - 동기 : 호출한 함수가 완료될 때까지 기다리는 것. 호출한 함수의 리턴값을 받을 때까지 다음 동작을 실행하지 못한다. (직렬적)
> - 비동기 : 호출한 함수가 완료될 때까지 기다리지 않는 것. 함수를 호출할 때 콜백함수를 같이 넘겨주며, 호출한 함수의 완료여부에 상관 없이 다음 동작을 실행한다. (병렬적)

- (2) 블로킹과 논블로킹의 차이점을 설명해주세요.
> - 블로킹 : 함수를 호출할 때 제어권을 함께 넘겨주는 것. 호출한 함수가 끝나고 제어권을 다시 돌려받을 때까지 다음 동작을 실행하지 못한다. (멀티 스레드 - 결과 받을 때까지 현재 스레드 잠금 상태)
> - 논블로킹 : 함수를 호출할 때 제어권을 계속 갖고 있는 것. 호출한 함수의 완료여부에 상관없이 계속 다음 동작을 실행한다. (멀티 스레드 - 결과 받기 전에도 현재 스레드에서 다른 작업 수행 가능)

- (3) 본인이 주로 사용하는 언어에서 비동기 프로그래밍을 사용하는 방법을 설명해주세요.
> - Node.js : 기본적으로 싱글 스레드에 비동기이다. 비동기로 구현 시 콜백함수를 함께 넘겨준다. 동기로 구현 시에는 async/await 이나 promise 를 이용한다.
> - Java : Thread (Thread pool), Future (CompletableFuture) 를 이용하여 멀티 스레드로 구현하며 콜백함수를 함께 넘겨준다.
> - 공통 : MQ (Kafka, RabbitMQ, ..) 를 이용


- (4) 메세지 큐를 쓰는 이유에 대하여 2가지 예시를 서술해주세요.
> - 비동기 처리 유연, 부하 분산 (비동기 처리를 통해 MSA 등에서 Application 간의 결합도를 낮추고 여러 Consumer 를 둠으로써 부하 분산 가능) - ex. 쇼핑몰 서비스에서 주문/결제 프로세스 시 사용자 대기 시간 단축
> - 데이터 손실 방지, FailOver (시스템 장애 시 Consumer 가 메시지 소비하지 못하면 메시지큐에 쌓여있어 데이터 손실 방지 및 유연한 FailOver 가능) - ex. 결제 서비스 장애 시 금전 손실 대비

~~- (5) 본인이 작성한 서버 코드가 있는 github repo 주소를 제출해주세요. (CRUD 기능을 모두 포함하여야 하며, 서버에 대한 설명을 README에 작성해주시면 더욱 좋습니다.)~~  

(6 - Optional) 해당 수업을 통해 꼭 배우고 싶은 주제 또는 지식이 있다면 자유롭게 서술해주세요.
> - 서비스 구축 시 기본적인 인프라 구조 및 그에 적합한 AWS SaaS 에 대해 배우고 싶습니다. 또한 장애 처리와 관련된 부분도 배울 수 있다면 좋을 것 같습니다.
