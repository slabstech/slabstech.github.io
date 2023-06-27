---
layout: post
title: "Rate Limiter API with Spring Security and OAuth"
excerpt: "Usage + Site Reliability"
categories: tutorial
tags: [ tutorial ]
date: 2023-06-25T08:08:50-04:00

---

For Subscription based SaaS, features are provided to users based on tiers.
* Free tier with basic features and limited access
* Standard tier with most features 
* Pro tier with all features

Availability is handled between tiers using Rate Limiter API.

Based on number of users and usage, Cloud services can be provisioned based on metrics.

* Main concepts
  * OAuth
  * Retry Mechanism
  * Api Key
  * Session Management

* Reference
  * https://reflectoring.io/rate-limiting-with-springboot-resilience4j/
  * https://resilience4j.readme.io/docs/ratelimiter
  * https://www.baeldung.com/spring-bucket4j
  * https://spring.io/blog/2021/04/05/api-rate-limiting-with-spring-cloud-gateway