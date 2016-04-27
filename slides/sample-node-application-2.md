## Time for more advances version of our application

We will use NO SQL Database

---

## Let's use MongoDB

```bash
# CREATE NEW "SMALL" MONGODB SERVICE
$ cf create-service mongodb small my-mongodb
Creating service instance my-mongodb in org swisscom / space DEV as me@example.com...
OK

Attention: The plan `small` of service `mongodb` is not free.  The instance `mymmongodb` will incur a cost.  Contact your administrator if you think this is in error.
```

---

## Check it

```bash
# DISPLAY SERVICE INSTACE INFO
$ cf service my-mongodb
```


---

## How do we connect the application to this service?

---

## MongoDB Connection Config

[The Twelve Factors Manifest](http://12factor.net) says
>...
#### III. Config
Store config in the environment
...

**So we will!**

---

## How do we inject config to environment?

Service Biding injects service keys into app environment

---



## Read config in the environment

Switch the branch in git to _final-result_:

```bash
git checkout final-result
```

---

## Read ENV Variables

Code: we can get the DB Url and Credential from ENV

```js
// check if the app is running in the cloud and set the MongoDB settings accordingly
if (process.env.VCAP_SERVICES) {
  const vcapServices = JSON.parse(process.env.VCAP_SERVICES);
  mongoUrl = vcapServices.mongodb[0].credentials.uri;
} else {
  mongoUrl = 'mongodb://localhost/db';
}
```



