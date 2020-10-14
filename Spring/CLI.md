- 단순히 프로젝트를 생성하는 용도로 공부하려고 했다.
- [문서](https://docs.spring.io/spring-boot/docs/current/reference/html/spring-boot-cli.html)를 읽었다.
- `run`으로 groovy 파일을 실행하는 것이 `init` 보다 먼저 나온다
  - 단순작업용 스크립트처럼 사용하기 좋아보인다.
    - import 구문이 없다는게 스크립팅에서는 필수조건인데 나름 잘 구현했다.
    - **TODO** 하지만 실제로 어떻게 활용하고 있는지는 찾아봐야 알 수 있을듯
      - [sample groovy script](https://github.com/spring-projects/spring-boot/tree/v2.3.4.RELEASE/spring-boot-project/spring-boot-cli/samples) 참고
- 목표 : eureka project 생성하기
  - 결론 : `spring init help`, `spring init --list`만 보면 바로 사용할 수 있다. 아주 쉬움.
  - install spring cli
    ```bash
    $ brew tap pivotal/tap
    $ brew install springboot
    ```
  - init eureka project
    ```bash
    spring init --build=gradle --dependencies=cloud-eureka --artifactId=eureka --description=study,spring-cli,cloud,eureka --groupId=bk.study.spring --java-version=11 eureka-project`
    ```
