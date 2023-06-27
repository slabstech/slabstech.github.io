---
layout: post
title: "Java + SpringBoot : Robust API endpoints with testcontainers"
excerpt: "Validate Features End to End"
categories: tutorial
tags: [ tutorial ]
date: 2023-06-24T08:08:50-04:00

---

* Unit Tests
  * cover the logic of a module. It verifies if the features work as expected for valid and invalid
    inputs. It is independent and fast. 
  * Used with Test Driven Development(TDD) for feature addition and refactoring existing code
* Integration Tests
  * Cover the end-to-end flow of an application.
  * It spins up the entire application and verifies the integration of modules

[Code - https://github.com/slabstech/tutorials/](https://github.com/slabstech/tutorials/tree/main/api-testcontainer)


* Steps
  * To verify API with manual tests
    * Use Swagger/OpenAPI to Generate API documentation using
      * Spring 2.x - 'org.springdoc:springdoc-openapi-ui'
      * Spring 3.x - 'org.springdoc:springdoc-openapi-starter-webmvc-ui'
    * Create test.http with sample inputs for manual verification
  * To verify API with Integration Tests
    * Use Testcontainers 
      * 'org.testcontainers:junit-jupiter',
        'org.springframework.boot:spring-boot-testcontainers', 'org.springframework.boot:spring-boot-starter-test'
      * Use different container for each use case. Ex
        * Database tests 
          * PostgreSQL Container - 
        * Kafka Container - 
          * KafkaContainer kafka = new KafkaContainer(DockerImageName.parse("confluentinc/cp-kafka:6.2.1"))
  * To verify Modules with Unit Tests
    * Validate models/data with Bean validation
       * 'org.springframework.boot:spring-boot-starter-validation'


* Reference
  * SpringBoot
    * https://github.com/testcontainers/testcontainers-java/tree/main/examples/spring-boot
  * Database Integration Test
    * https://java.testcontainers.org/modules/databases/postgres/
    * https://www.baeldung.com/spring-boot-testcontainers-integration-test
  * Kafka 
    * https://www.baeldung.com/spring-boot-kafka-testing
  * Docker Compose
    * https://java.testcontainers.org/modules/docker_compose/

<!--
* Task
  * Build a form validation API for User Registration

* Field Types
  * String - Name
  * AlphaNumeric - Username
  * Date - Birth Date
  * Regex Match + AlphaNumeric -  Email , Password 

-->

