## Time for more advanced version of our application

We will use a NoSQL Database

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

## Check if it is running

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

## How do we inject the config into the environment?

The service binding injects the service's credentials into your app environment.

---



## Service Binding

Service Biding can be achieved via:

*  Manifest file
* _cf bind-service_ command

---



## Read config from the environment

Switch the branch in git to _final-result_:

```bash
git checkout final-result
```

---

## Read ENV Variables


Code: we can get the DB's URL and credentials from ENV

```js
// check if the app is running in the cloud and set the MongoDB settings accordingly
if (process.env.VCAP_SERVICES) {
  const vcapServices = JSON.parse(process.env.VCAP_SERVICES);
  mongoUrl = vcapServices.mongodb[0].credentials.uri;
} else {
  mongoUrl = 'mongodb://localhost/db';
}
```



