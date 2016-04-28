##  Let's start with Cloud Foundry fundamentals

---

## Orgs (#1)

 An **org** is a development account that an individual or multiple collaborators can own and use.
   
 All collaborators access an org with user accounts. Each org contains at least one space.

---

## Orgs (#2)

 Collaborators in an **org** share a resource quota plan, applications, services availability, and custom domains.

---

## User Accounts

A **user account** represents an individual person within the context of a Cloud Foundry installation.
A **user** can have different roles in different spaces within an org, governing what level and type of access they
have within that space.


---

## Space

A space provides a set of users access to a shared location for application development, deployment, and maintenance.



---

<img src="images/orgs-spaces.png" style="background:none; border:none; box-shadow:none;" />

Every application and service is scoped to a space!


---

## Complicated?

It is simple. Typically:

* Org = Team
* Space = Environment like "_test_", "_prod_" etc.
