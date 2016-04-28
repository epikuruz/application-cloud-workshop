##  Routes (#1)
HTTP requests are routed to applications pushed to Cloud Foundry by associating an application with a URL, known as a route.

This association is called a mapping.

---

## Routes (#2)
Many apps can be mapped to a single route resulting in load balanced requests
for the route across all instances of all mapped apps.

---

## Routes (#3)

An individual app can also be mapped to multiple routes, granting multiple URLs access to the app.

---

## Routes (#4)
Routes belong to a **space**, so that only apps in the same space can be mapped to a route.
Routes are **globally unique**, so that member users of one space cannot create a route with the same URL.

---


## Routes (#5)

[Blue Green Deployments](http://martinfowler.com/bliki/BlueGreenDeployment.html) - a piece of cake with the [Cloud Foundry](https://gist.github.com/mastertinner/3eb3c0e2e5e3558d56d1)

<img src="images/green-blue-deployment.jpg" style="background:none; border:none; box-shadow:none;" />
