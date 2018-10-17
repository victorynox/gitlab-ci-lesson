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
tags - теги
branches - пуш кода в ветку
pushes - теги и пуш кода в ветку
