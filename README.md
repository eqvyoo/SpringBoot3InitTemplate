기존 mulmagi 프로젝트에서 사용하던 springboot 2버전 init 템플릿을 3버전으로 업그레이드 했습니다.

바뀐점
1. springboot를 기존 2.7.13 버전 -> 3.2.2버전으로 업그레이드했습니다.
    id 'org.springframework.boot' version '2.7.13' -> id 'org.springframework.boot' version '3.2.2'
2. javax dependency를 jakarta로 바꿨습니다.
   import javax.persistence.* -> import jakarta.persistence.*
3. Swagger 사용을 위해 build.gradle에서 springfox를 springdoc으로 바꿨습니다.
   implementation 'io.springfox:springfox-boot-starter:3.0.0' -> implementation 'org.springdoc:springdoc-openapi-starter-webmvc-ui:2.2.0'
4. springdoc을 사용하면서 SwaggerConfiguration.java파일이 필요없어졌습니다.
5. Swagger 어노테이션이 바뀌었습니다.
   예: import io.swagger.annotations.ApiParam -> import io.swagger.v3.oas.annotations.Parameter
   어노테이션을 비롯해 구성도 조금씩 달라졌습니다.다른 어노테이션은 https://springdoc.org/#features 의 9.Migrating from SpringFox를 참고하면 됩니다.

https://springdoc.org/#features 을 참고했습니다.
