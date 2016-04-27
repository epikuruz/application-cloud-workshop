## Create a service key


```bash
# CREATE NEW MARIDB SERVICE
$ cf create-service mariadb small my-mariadb
Creating service instance my-mariadb in org swisscom / space DEV as me@example.com...
OK

Attention: The plan `small` of service `mariadb` is not free.  The instance `mymariadb` will incur a cost.  Contact your administrator if you think this is in error.
```

---

```bash
# CREATE NEW SERVICE KEY
$ cf create-service-key my-mariadb mykey
Creating service key mykey for service instance myservice as me@example.com...
OK
```

---

##  Get credentials for the service key

```bash
# GET CREDENTIALS FOR A SERVICE KEY
$ cf service-key my-mariadb mykey | grep -e password -e user
Getting key mykey for service instance myservice as me@example.com...

 "jdbcUrl": "jdbc:mysql://10.0.20.18:3306/CF_5603C3AB_2336_473A_AD27_2EB0FE37A7E0?user=81M84MGVOd5kPpI8\u0026password=C8EpnZOQXlnxIAn1",
 "password": "C8EpnZOQXlnxIAn1",
 "username": "81M84MGVOd5kPpI8"
```

---

## Open SSH tunnel to this service

```bash
# OPEN TUNNEL TO SERICE ON LOCAL PORT 13000
$ cf service-connector 13000 10.0.20.18:3306:3306
```

---

## Now we can reach this service

localhost:13000


