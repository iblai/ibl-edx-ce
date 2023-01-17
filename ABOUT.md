# ABOUT

## Overview

ibl-edx-ce extends Open edX and Tutor via a fast, secure and extensible layer.

Implements course authoring and delivery on top of MIT's and Harvard's 60M+ learner-backed pedagogy.

## About IBL

IBL Education builds AI-driven skills and analytics learning platforms for some of the world's largest organizations.

* Headquarters: New York, NY
* Open edX (Premier): openedx.org/marketplace/ibl-education
* GitHub: github.com/ibleducation
* Twitter: twitter.com/ibleducation
* AWS: ibleducation.com/aws


# USAGE

## Running image with tutor

## Prequiste

- tutor

Run the following command to set tutor image to use

```bash
tutor config save --set DOCKER_IMAGE_OPENEDX=<aws_ecr_account>/ibl-edx-ce:latest
tutor local stop
tutor local start -d
```

## Running image in non tutor environment e.g ecs

Create an env file for lms and cms with the following variables

```bash
LMS_HOST=
CMS_HOST=
PLATFORM_NAME=
CONTACT_EMAIL=
REDIS_HOST=
REDIS_PORT=
OPENEDX_CELERY_REDIS_DB=
REDIS_USERNAME=
REDIS_PASSWORD=
SMTP_HOST=
SMTP_PORT=
EMAIL_USE_TLS=
LANGUAGE_CODE=
OPENEDX_SECRET_KEY=
OPENEDX_AWS_ACCESS_KEY=
OPENEDX_AWS_SECRET_ACCESS_KEY=
MYSQL_HOST=
MYSQL_PORT=
OPENEDX_MYSQL_DATABASE=
OPENEDX_MYSQL_USERNAME=
OPENEDX_MYSQL_PASSWORD=
SMTP_USERNAME=
SMTP_PASSWORD=
```

Pass lms.env and cms.env when running the lms and cms container respectively