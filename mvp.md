## MVP

#### Nginx/Ingress

- [ ] 404 Page
- [ ] 500 Page

#### General

- [ ] Logstash / Kibana / Grafana setup
- [ ] Winston logging in all services

#### Gateway

**API Gateway**

- [x] all routes are setup and running
- [x] securing routes with JWT (sessionless)
- [x] role based routes
- [x] company based routes by subdomain
- [x] service communication with côtejs
- [ ] superadmin/internal routes for internal administration
- [ ] hr/admin/owner routes for company admins

**Authentication**

- [x] Users can register/login/logout
- [x] JWT sessionless authentication for api
- [x] authentication service handles authentication for identifier / password
- [x] authentication service instructs email service to send validation email
- [x] authentication generates token on registration and verifies users against

#### Services

**Brownbags**

- [x] brownbag sessions can be added
- [x] brownbag sessions can be updated
- [x] brownbag sessions can be participated
- [x] brownbag sessions can be deleted
- [x] brownbag sessions can be added to local calendar
- [ ] frontend part of brownbags is done
  - displaying list
  - displaying single
  - participate sessions
  - add/edit views for brownbags


**Budgets / Spendings**

- [x] budgets can be added
- [x] budgets can be updated
- [x] budgets can be deleted
- [x] budget spending can be requested
- [x] budget spending can be approved
- [ ] frontend part of budget administration is done
  - displaying list
  - displaying single
  - spending approval view
  - add/edit views for budgets

**Categories**

- [x] categories can be added
- [x] categories can be updated
- [x] categories can be deleted
- [ ] frontend part of category administration is done
  - add/edit views for categories

**Departments**

- [x] departments can be added
- [x] departments can be updated
- [x] departments can be deleted
- [ ] frontend part of department administration is done
  - add/edit views for departments

**Employees**

- [x] employees invitation registation api
- [x] employees can be invited by owner/hr/admins
- [x] employees can be updated
- [x] employees can be deleted by owner/hr/admins
- [ ] frontend part of employee profile is done
- [ ] frontend part of employee administration is done

**Companies**

- [x] companies can be created upon first registration
- [x] companies can be fully deleted with all related data
- [x] company info can be updated
- [x] company valid email domains can be updated
- [ ] frontend part of settings for companies is done
- [ ] frontend part of company administration is done

**Feedbacks**

- [x] feedbacks can be added and attached to training
- [x] feedbacks can be updated
- [x] feedbacks can be deleted
- [ ] frontend part of feedbacks is done

**Trainings**

- [x] trainings can be added
- [x] trainings can be updated
- [x] trainings can be participated
- [x] trainings can be deleted
- [x] trainings can be added to local calendar
- [ ] frontend part of trainings is done

**Emails**

- [x] send employee invite mails
- [x] send auth verification mails
