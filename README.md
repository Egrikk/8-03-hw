# Домашнее задание к занятию "`GitLab`" - `Доготер Егор`


### Задание 1

1. `Развернул Gitlab через собственный vagrant файл`
2. `Создал новый проект`
3. `Запустил gitlab-runner`

![Поднятие docker runner](8-03\8-03-hw\img\215611.png)
![Результат в gitlab](8-03\8-03-hw\img\215840.png)

---

### Задание 2

1. `Запушил репозиторий sdvps-homeworks и изменил origin`
2. `Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.`


```
stages:
  - test
  - build

test-job:
  stage: test
  image: alpine:latest
  script:
    - echo "Running tests..."
    - echo "Test completed"
  tags:
    - docker

build-job:
  stage: build
  image: docker:latest
  script:
    - echo "Building image..."
    - echo "Build completed"
  tags:
    - docker

```

![Изминение origin](8-03\8-03-hw\img\221207.png)
![Запушенный .gitlab-ci.yml](8-03\8-03-hw\img\222950.png)
![Отметка об успешном pipline](8-03\8-03-hw\img\230336.png)

---
