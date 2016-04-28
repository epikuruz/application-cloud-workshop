## Application Manifest (#1)

An application manifest tell _cf push_ what to do with the application.

This includes everything from how many instances to create and how much memory to allocate to what services applications should use.

---

## Application Manifest (#2)

A manifest can help you automate deployment, especially of multiple applications at once.

Manifests are written in [YAML](http://yaml.org).


A minimal manifest requires only an application's name

```
---
applications:
- name: nifty-gui
```

---

## Manifest: Buildpack Attribute

If your application requires a custom buildpack, you can use the buildpack attribute to specify its URL or name:

```yaml
  ---
  ...
  buildpack: buildpack_URL
```

---

## Manifest: Instances Attribute

Use the instances attribute to specify the number of app instances that you want to start upon push:


```yaml
---
  ...
  instances: 2
```

---

## Manifest: Memory Attribute

```yaml
  ---
    ...
    memory: 1024M
```

---

## Manifest: Services Attribute

Defines binding to services such as databases, messaging, and key-value stores.

```yaml
---
  ...
  services:
   - instance_ABC
   - instance_XYZ
```

