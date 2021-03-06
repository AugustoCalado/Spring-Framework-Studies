
## Spring 2.2.7.RELEASE
``` groovy
plugins {

 id 'org.springframework.boot' version '2.2.7.RELEASE'

 id 'io.spring.dependency-management' version '1.0.9.RELEASE'

 id 'java'

}

group =  'augusto.bueno'

version =  '0.0.1-SNAPSHOT'

sourceCompatibility =  '1.8'

configurations {

 developmentOnly

 runtimeClasspath {

 extendsFrom developmentOnly

  }

 compileOnly {

 extendsFrom annotationProcessor

  }

}

repositories {

  mavenCentral()

}

dependencies {

 implementation 'org.springframework.boot:spring-boot-starter-data-jpa'

 implementation 'org.springframework.boot:spring-boot-starter-web'

 compileOnly 'org.projectlombok:lombok'

 developmentOnly 'org.springframework.boot:spring-boot-devtools'

 annotationProcessor 'org.springframework.boot:spring-boot-configuration-processor'

 annotationProcessor 'org.projectlombok:lombok'

  testImplementation('org.springframework.boot:spring-boot-starter-test')  {

 exclude group:  'org.junit.vintage', module:  'junit-vintage-engine'

  }

}

test {

  useJUnitPlatform()

}
```

## Spring 2.3.0.RELEASE
```groovy
plugins {

 id 'org.springframework.boot' version '2.3.0.RELEASE'

 id 'io.spring.dependency-management' version '1.0.9.RELEASE'

 id 'java'

}

group =  'augusto.bueno'

version =  '0.0.1-SNAPSHOT'

sourceCompatibility =  '1.8'

configurations {

 compileOnly {

 extendsFrom annotationProcessor

  }

}

repositories {

  mavenCentral()

}

dependencies {

 implementation 'org.springframework.boot:spring-boot-starter-data-jpa'

 implementation 'org.springframework.boot:spring-boot-starter-web'

 compileOnly 'org.projectlombok:lombok'

 developmentOnly 'org.springframework.boot:spring-boot-devtools'

 annotationProcessor 'org.springframework.boot:spring-boot-configuration-processor'

 annotationProcessor 'org.projectlombok:lombok'

  testImplementation('org.springframework.boot:spring-boot-starter-test')  {

 exclude group:  'org.junit.vintage', module:  'junit-vintage-engine'

  }

}

test {

  useJUnitPlatform()

}
```

[Spring Gradlew = MultiProject](https://stackoverflow.com/questions/54134759/springboot-with-multi-project-gradle-main-class-name-has-not-been-configured)
