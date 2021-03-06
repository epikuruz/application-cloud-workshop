##  Let's start with the Cloud Foundry fundamentals

---

##  Every app and service is scoped to a space


---

## Space (#1)

A **space** provides a set of users access to a shared location for application development, deployment, and maintenance.

---

## Space (#2)

Belongs to an **org**


---

## Org (#1)

 An **org** is a development account that an individual or multiple collaborators can own and use.

 All collaborators access an org with user accounts. Each org contains at least one space.

---

## Org (#2)

 Collaborators in an **org** share a resource quota plan, applications, services availability, and custom domains.

---

## User Account (#1)

A **user account** represents an individual person within the context of a Cloud Foundry installation.

---

## User Account (#2)

A **user** can have different roles in different spaces within an org, governing what level and type of access they
have within that space.


---

## The Cloud Foundry fundamentals at a glance

<img src="images/orgs-spaces.png" style="background:none; border:none; box-shadow:none;" />

---

## Complicated?

It is simple! Typically:

* Org = Team
* Space = Environment like "_test_", "_prod_" etc.
* You push your apps and create your services in the given space
