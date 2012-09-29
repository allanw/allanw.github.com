---
layout: default
published: true
---

http://stackoverflow.com/questions/8937905/how-to-pip-uninstall-with-virtualenv-on-heroku-cedar-stack

heroku labs:enable user_env_compile
heroku config:add CLEAN_VIRTUALENV=true
heroku config:add BUILDPACK_URL=https://github.com/blaze33/heroku-buildpack-python.git

I had celery version 3.0.11, need 2.5.5. Add celery<3.0 to reqs/common.txt then do git push heroku master