```
by_tag_job:
  script: echo "by tag - job"
  only:
    variables:
    - $CI_COMMIT_TAG == /job/
```
