### Deployment

Vibora is not a WSGI compatible framework because of its async nature.
It ships with its own battle-tested http server so deployment is far easier
than with other frameworks because there is no need for Gunicorn/uWSGI.

One may argue that Gunicorn/uWSGI are battle proven solutions and that's true
but they also bring different application behaviors between dev/prod
environments and still need a battle-tested server such as Nginx
in front of them.

The recommended approach to freeze a Vibora app is using docker.
This way you can build a frozen image locally in your machine, test it
and upload to wherever you host. This way you skip
all python packaging problems that you'll find trying to build
reproducible deployments between different machines.
