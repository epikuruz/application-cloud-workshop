## We are ready to deploy first application!

---

##  Step: Checkout


```bash
# CLONE FROM GIT
$ git clone https://github.com/swisscom/cf-sample-app-node
```

---

## Step: Push to Application Cloud

```bash
# PUSH AND ASK FOR RANDOM ROUTE
$ cf push my-node-app --random-route
```

```bash
# CHECK APP HEALTH AND STATUS
$ cf apps
$ cf app my-node-app
```

