## Push your application

Cloud Foundry provides two great ways to run you applications:

* Buildpacks
* Docker Images (NEW!)



```bash
# MAGIC COMMAND:
$ cf push yourapp
```

---

## Buildpacks

Buildpacks provide framework and runtime support for your applications.
When you push your application, the appropriate buildpack needs to be selected.


Almost **any** programming language is supported.

---

## Docker Images


You can push Docker Images from Docker Registries

```bash
# PUSH DOCKER IMAGE:
$ cf push -docker-image user/docker-image-name
```

---

## Staging

During staging executable **droplet** is created either from:
* Application + Buildpack
* Docker Image


<img src="images/buildpack.png" style="background:none; border:none; box-shadow:none;" />

