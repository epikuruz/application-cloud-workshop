##  Routes (#1)
HTTP requests are routed to applications pushed to Cloud Foundry by associating an application with a URL, known as a route. This association can be called a mapping. For example, a developer might say, “I mapped route myapp.shared-domain.com to app myapp”.

---

## Routes (#2)
Many apps can be mapped to a single route resulting in load balanced requests
for the route across all instances of all mapped apps.
An individual app can also be mapped to multiple routes, granting multiple URLs access to the app.

---

## Routes (#3)
Routes belong to a **[space]()**, so that only apps in the same space can be mapped to a route.
Routes are **globally unique**, so that member users of one space cannot create a route with the same URL.

---


## Routes (#4)

Blue Green Deployments - piece of cake with Cloud Foundry

<img src="images/green-blue-deployment.jpg" style="background:none; border:none; box-shadow:none;" />
