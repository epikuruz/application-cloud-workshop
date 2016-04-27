## Manifest for our application


```yaml
---
applications:
- name: my-node-app
  memory: 128MB
  instances: 2
  host: my-random-hostname-PUT_RANDOM_NUMER_HERE
  services:
  - my-mongodb

  env:
    NODE_ENV: production
```

---

## Push the app with this manifest

```bash
$ cf push
```

```bash
# DISPLAY HEALTH AND STATUS FOR APP
$ cf app my-node-app
```

---

## Step: Scale it out

```bash
# INCREASE NUMBER OF INSTANCES
$ cf scale my-node-app -i 4
# DISPLAY HEALTH AND STATUS FOR APP
$ cf app my-node-app
```

```bash
# DECRESE NUMBER OF INSTANCES AND INCREASE AMOUNT OF RAM
$ cf scale my-node-app -i 2 -m 256m
# DISPLAY HEALTH AND STATUS FOR APP
$ cf app my-node-app
```

---

## Step: Add route

```bash
$cf map-route my-node-app scapp.io -n my-random-hostname-123
# DISPLAY HEALTH AND STATUS FOR APP
$ cf app my-node-app
Showing health and status for app my-node-app in org sandbox / space michal as me@example.com
OK

requested state: started
instances: 3/3
usage: 256M x 3 instances
urls: my-random-hostname-122.scapp.io, my-random-hostname-123.scapp.io
last uploaded: Wed Apr 27 20:20:55 UTC 2016
stack: cflinuxfs2
buildpack: node.js 1.5.8
```

---

## Step: Final Cleaning

```bash
# DELETE APP
$ cf delete-app my-node-app
```

```bash
# DELETE SERVICE
$ cf delete-service my-mongodb
```
