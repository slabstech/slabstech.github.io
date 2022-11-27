---
layout: post
title: "How to migrate project from Monolith to Micro-service"
excerpt: "Step by Step info to help in migration"
categories: blog
tags: [ blog ]
date: 2022-05-27T08:08:50-04:00
---

* Follow how Revive was migrated from monolith to micro-services

* Setting up [Bhoomi](https://mangala.earth) , using [revive](https://github.com/slabstech/revive) project

* Monorepo

| Name                                                                                                    | Repo                                                                                                                                 | Integrated |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|------------|
| [mangala.earth](https://github.com/slabstech/bhoomi)                                                    | [https://github.com/slabstech/bhoomi](https://github.com/slabstech/bhoomi)                                                           | No         |
| [slabstech.com/revive](https://github.com/slabstech/revive)                                             | [https://github.com/slabstech/revive](https://github.com/slabstech/revive)                                                           | Yes        |
| [gaganyatri.com](https://github.com/slabstech/gaganyatri.com)                                           | [https://github.com/slabstech/gaganyatri.com](https://github.com/slabstech/gaganyatri.com)                                           | No         |
| [slabstech.com](https://github.com/slabstech/slabstech.github.io)                                       | [https://github.com/slabstech/slabstech.github.io](https://github.com/slabstech/slabstech.github.io)                                 | No         |
| [slabstech.com/connectthedots.com](https://github.com/slabstech/connectthedots.com)                     | [https://github.com/slabstech/connectthedots.com](https://github.com/slabstech/connectthedots.com)                                   | No         |
| [slabstech.com/ammanaaduge.com](https://github.com/slabstech/ammanaaduge.com)                           | [https://github.com/slabstech/ammanaaduge.com](https://github.com/slabstech/ammanaaduge.com)                                         | No         |
| [slabstech.com/samruddhi.com](https://github.com/slabstech/samrudhi)                                    | [https://github.com/slabstech/samrudhi](https://github.com/slabstech/samrudhi)                                                       | No         |
| [slabstech.com/keeper](https://github.com/slabstech/keeper)                                             | [https://github.com/slabstech/keeper](https://github.com/slabstech/keeper)                                                           | No         |
| [slabstech.com/alemaari.in](https://github.com/slabstech/alemaari.in)                                   | [https://github.com/slabstech/alemaari.in](https://github.com/slabstech/alemaari.in)                                                 | No         |
| [action-deploy-container-to-registry](https://github.com/slabstech/action-deploy-container-to-registry) | [https://github.com/slabstech/action-deploy-container-to-registry](https://github.com/slabstech/action-deploy-container-to-registry) | No         |
| [action-cuda-compiler-python](https://github.com/slabstech/action-cuda-compiler-python)                 | [https://github.com/slabstech/action-cuda-compiler-python](https://github.com/slabstech/action-cuda-compiler-python)                 | No         |
| [action-cuda-compiler](https://github.com/slabstech/action-cuda-compiler)                               | [https://github.com/slabstech/action-cuda-compiler](https://github.com/slabstech/action-cuda-compiler)                               | No         |
| [action-create-ebook](https://github.com/slabstech/action-create-ebook)                                 | [https://github.com/slabstech/action-create-ebook](https://github.com/slabstech/action-create-ebook)                                 | No         |
| [slabstech.com/darktales.com](https://github.com/slabstech/darktales.com)                               | [https://github.com/slabstech/darktales.com](https://github.com/slabstech/darktales.com)                                             | No         |
| [slabstech.com/aachocolates.in](https://github.com/slabstech/aachocolates.in)                           | [https://github.com/slabstech/aachocolates.in](https://github.com/slabstech/aachocolates.in)                                         | No         |
| [slabstech.com/thehdtour.com](https://github.com/slabstech/thehdtour.com)                               | [https://github.com/slabstech/thehdtour.com](https://github.com/slabstech/thehdtour.com)                                             | No         |
| [slabstech.com/ant2Maven](https://github.com/slabstech/ant2Maven)                                       | [https://github.com/slabstech/ant2Maven](https://github.com/slabstech/ant2Maven)                                                     | No         |

### Project Logs

* November 27
  * Bhoomi project
    * Wiki built using Jekyll, Markdown, HTML
    * GitHub Pages, Google Domains, ProtonMail, IntelliJ Idea Ultimate 
    * [Setting up multiple websites - GitHub Pages and Google Domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-a-records-with-your-dns-provider)

* June 7
  * samruddhi-react :
    * Migrating Samruddhi project from Single Markdown Page to ReactJS 
    * ReactJS standalone project is deployed to gh-pages.
    * Created a PreProcessor in Java to convert BookData to Json.data_import directory [Source](https://github.com/slabstech/samrudhi-react)
    * Json Data to be loaded into website using Fetch
  * shop :
    * Made config changes to refactor project from Revive to Shop
    * Removed spring_boot configs and source code directory.

* June 6 
  * revive:
    * Create composite github actions to handle Docker multi-stage build issue with Server(SpringBoot+Dropwizard)
    * Now gradle build is run inside the docker container. Server code is copied to docker container.
    * Build task now runs independently and can run in parallel if build task is successful.

* June 5 
  * revive:
    * Docker push failing as build directory not found in container. Build files are copied from host machine to container.
    * Local push to docker successful, Github actions does not have access to build files from pre-cursor task, Try to build project inside gradle container.
  
* June 4 
  * revive:
    * Add starter code for Dropwizard. Second option for Server. Dropwizard is suitable for micro-services

