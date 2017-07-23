## Cloud Foundry Overview
- Do you understand Cloud Foundry concepts like spaces, organizations, routes, services, domains, users, quotas?

> **spaces** - every application and service is scoped to a space. Each org contains at least one space. A space provides users with access to a shared location for application development, deployment, and maintenance. Each space role applies only to a particular space.

> **organizations** - an org is a development account that an individual or multiple collaborators can own and use. All collaborators access an org with user accounts. Collaborators in an org share a resource quota plan, applications, services availability, and custom domains.

> **routes** - define how to get to an application
-- a unique route exists to each application in every space
-- domain can be mapped to multiple spaces
-- route can only be mapped to one space
-- same application can be deployed in multiple spaces
-- each must have a different, unique URL
-- development space route: http://myapp-test.cfapps.io
-- production space route: http://myapp.cfapps.io

> **services** - any type of add-on that can be provisioned along side your apps
-- database, messaging, mail, third-party SaaS provider
-- services are usually bound to 1 or more applications
-- connection info and credentials are put in an environment variable: `VCAP_SERVICES`

> **domains** - define routes to apps

> **users** - a user account represents an individual person within the context of a PCF application. A user can have different roles in different spaces within an org, governing what level and type of access they have within that space.

> **quotas** - restrict resources for orgs and spaces
-- total memory
-- total number of routes
-- max application instance size
-- total number of services

- How do you login to Cloud Foundry?
> `cf login [-a API_URL] [-u USERNAME]`

- How do you deploy an application? What are three activities involved?
> `cf push APP_NAME`
> 1. Upload
> 2. Stage
> 3. Start

- Can you remember the steps Cloud Foundry goes through when deploying applications? What components are involved?

- What is the difference between a public, private and hybrid cloud?

- What infrastructure does Cloud Foundry runs on?

- What is BOSH? Why is it useful?

- What is staging? What does it do?

- Do you know the difference between restarting, restaging and redeploying and application? How does each of these affect the services, environment-variables available on an application?

- What is meant by ephemeral? What are the design implications for an application?
> ephemeral -> temporary
> virtual machines and containers are temporary
> immutable infrastructure - updates to systems and applications are not done in-place
> new, updated instances are created instead

- What are the 12 Factor Design patterns? Could you list each one from memory?

> 1. Processes
Execute the app as one or more stateless processes

> 2. Concurrency
Scale out via the process model

> 3. Disposability
Maximize robustness with fast startup and graceful shutdown

> 4. Logs 
Treat logs as event streams

> 

- Why does Cloud Foundry rely on environment-variables?
- Can you manage environment-variables manually? If so how?
- Can you name two predefined environment-variables available to any application?