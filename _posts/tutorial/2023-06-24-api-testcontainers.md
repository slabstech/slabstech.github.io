---
layout: post
title: "Java + SpringBoot : Robust API endpoints with testcontainers"
excerpt: "Validate Features End to End"
categories: tutorial
tags: [ tutorial ]
date: 2023-06-24T08:08:50-04:00

---
* Steps
  * Generate API documentation with OpenAPI spec using
    * 'org.springdoc:springdoc-openapi-ui'
  * Validate models/data with Bean validation 
    * 'org.springframework.boot:spring-boot-starter-validation'
  * Validate API end to end with testcontainers utilising Integration Testing 
    * 'org.testcontainers:junit-jupiter', 
      'org.springframework.boot:spring-boot-testcontainers', 'org.springframework.boot:spring-boot-starter-test'
  * Create test.http with sample inputs for manual verification

 [Code available at](https://github.com/slabstech/tutorials/tree/main/api-testcontainer)
