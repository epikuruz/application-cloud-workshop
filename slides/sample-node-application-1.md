## We are ready to deploy our first application!

---

##  Step: Checkout


```bash
# CLONE FROM GITHUB
$ git clone https://github.com/swisscom/cf-sample-app-node
```

---

## Step: Push to Application Cloud

```bash
# PUSH AND ASK FOR RANDOM ROUTE
$ cf push my-node-app --random-route
```

```bash

# LIST ALL APPS
$ cf apps
# CHECK OUR APP HEALTH AND STATUS
$ cf app my-node-app
```

