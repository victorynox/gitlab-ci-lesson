# README

```
image: docker:latest
services:
- docker:dind

by_tag_job:
  script: echo "by tag - job"
  only:
    variables:
    - $CI_COMMIT_TAG == /job/
    
by_message:
  script: echo "by message RUN TEST"
  only:
    variables:
    - $CI_COMMIT_MESSAGE == /RUN TEST/    
```

## only
* tags - когда создаешь теги
* branches - push код в ветку
* pushes - push тегов и кода в ветку

run test

hotfix
