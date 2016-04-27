## Application Manifest (#1)

Application manifests tell cf push what to do with applications.

This includes everything from how many instances to create and how much memory to allocate to what services applications should use.

---

## Application Manifest (#2)

A manifest can help you automate deployment, especially of multiple applications at once.

Manifests are written in YAML.


Minimal manifest requires only an application name

```
---
applications:
- name: nifty-gui
```

---

The buildpack attribute
If your application requires a custom buildpack, you can use the buildpack attribute to specify its URL or name:

```yaml
  ---
  ...
  buildpack: buildpack_URL
```

---

## Instances

Use the instances attribute to specify the number of app instances that you want to start upon push:


```yaml
---
  ...
  instances: 2
```

---

## The memory attribute

```yaml
  ---
    ...
    memory: 1024M
```

---

## Services

```yaml
---
  ...
  services:
   - instance_ABC
   - instance_XYZ
```

