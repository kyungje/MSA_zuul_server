# MSA_zuul_server

**msa-architecture-zuul-server**는 마이크로서비스 아키텍처(Microservices Architecture)에서 API Gateway 역할을 수행하기 위한 Spring Cloud Netflix Zuul 기반의 서버입니다.

## 주요 기능

- API Gateway 역할 수행
- 요청 라우팅 및 필터링
- 마이크로서비스 간 통신 관리를 위한 엔트리 포인트 제공
- 인증, 로깅, 모니터링 등의 필터링 기능 지원

## 기술 스택

- **언어**: Java
- **프레임워크**: Spring Boot, Spring Cloud Netflix Zuul

## 설치 및 실행

1. 저장소를 클론합니다:
   ```bash
   git clone https://github.com/kyungje/MSA_zuul_server.git
   ```
2. 프로젝트 디렉토리로 이동합니다:
   ```bash
   cd MSA_zuul_server
   ```
3. 필요한 의존성을 설치하고 애플리케이션을 실행합니다:
   ```bash
   ./mvnw spring-boot:run
   ```

## 사용 방법

1. Zuul 서버를 설정합니다.
   - `application.yml` 파일에서 라우팅 규칙과 기본 설정을 정의합니다.
   - 예:
     ```yaml
     zuul:
       routes:
         service-name:
           path: /service-name/**
           url: http://localhost:8080
     ```
2. 클라이언트 애플리케이션에서 Zuul 서버를 통해 요청을 라우팅합니다.
3. 필요한 경우 커스텀 필터를 구현하여 추가적인 기능을 제공합니다.

## 기여

기여를 환영합니다! 이 프로젝트에 기여하려면 다음 단계를 따라주세요:

1. 이 저장소를 포크합니다.
2. 새로운 브랜치를 생성합니다:
   ```bash
   git checkout -b feature/새로운기능
   ```
3. 변경사항을 커밋합니다:
   ```bash
   git commit -m "추가: 새로운 기능 설명"
   ```
4. 브랜치를 푸시합니다:
   ```bash
   git push origin feature/새로운기능
   ```
5. Pull Request를 생성합니다.

## 라이센스

이 프로젝트는 MIT 라이센스를 따릅니다. 세부사항은 [LICENSE](LICENSE) 파일을 참조하세요.

## 참고 자료

- [Spring Cloud Netflix Zuul 공식 문서](https://cloud.spring.io/spring-cloud-netflix/)
- [마이크로서비스 아키텍처 개요](https://martinfowler.com/articles/microservices.html)
```

이 파일을 프로젝트 루트 디렉토리에 `README.md`로 저장하시면 됩니다. 추가적인 요구 사항이 있다면 알려주세요!
