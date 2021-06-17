## Data Models and Microservices

### Authentication service
**Data Model**

**Invitiation Data Model**
| Name       | Model                              |
| ---------- | ---------------------------------- |
| _id        |                                    |
| email      |                                    |
| name       |                                    |
| token      |                                    |
| validUntil |                                    |
| company    | [CompanyModel](#Company-service)   |
| invitedBy  | [EmployeeModel](#Employee-service) |
| acceptedAt |                                    |
| createdAt  |                                    |
| updatedAt  |                                    |

**Activation Data Model**
| Name       | Model   |
| ---------- | ------- |
| _id        |         |
| employee   |         |
| token      |         |
| code       |         |
| used       |         |
| createdAt  |         |
| updatedAt  |         |

### Employee service
**Data Model**
| Name          | Model                              |
| ------------- | ---------------------------------- |
| _id           |                                    |
| firstName     |                                    |
| lastName      |                                    |
| company       | [CompanyModel](#Company-service)   |
| roles[]       |                                    |
| department    |                                    |
| email         |                                    |
| identifier    |                                    |
| password      |                                    |
| createdAt     |                                    |
| updatedAt     |                                    |
| gender        |                                    |
| position      |                                    |
| internalEmail |                                    |
| interests[]   | [CategoryModel](#Category-service) |

### Company service
**Data Model**
| Name        | Model                              |
| ----------- | ---------------------------------- |
| _id         |                                    |
| name        |                                    |
| street      |                                    |
| zip         |                                    |
| city        |                                    |
| country     |                                    |
| phone       |                                    |
| domain      |                                    |
| website     |                                    |
| employees[] | [EmployeeModel](#Employee-service) |
| createdAt   |                                    |
| updatedAt   |                                    |

### Training service
**Data Model**
| Name           | Model                              |
| -------------- | ---------------------------------- |
| _id            |                                    |
| createdAt      |                                    |
| updatedAt      |                                    |
| author         | [EmployeeModel](#Employee-service) |
| participants[] | [EmployeeModel](#Employee-service) |
| price          |                                    |
| location       |                                    |
| fromDate       |                                    |
| toDate         |                                    |
| description    |                                    |
| street         |                                    |
| zip            |                                    |
| city           |                                    |
| country        |                                    |
| remote         |                                    |
| website        |                                    |
| categories[]   | [CategoryModel](#Category-service) |
| departments[]  |                                    |
| spots          |                                    |
| company        | [CompanyModel](#Company-service)   |

### Feedback service
**Data Model**
| Name        | Model                              |
| ----------- | ---------------------------------- |
| _id         |                                    |
| createdAt   |                                    |
| updatedAt   |                                    |
| author      | [EmployeeModel](#Employee-service) |
| comment     |                                    |
| training    | [TrainingModel](#Training-service) |
| rating      |                                    |
| learnings[] |                                    |
| recommended |                                    |

### Integration service
**Data Model**
| Name        | Model                            |
| ----------- | -------------------------------- |
| _id         |                                  |
| createdAt   |                                  |
| updatedAt   |                                  |
| company     | [CompanyModel](#Company-service) |
| integration |                                  |

### Email service
**Data Model**
| Name      | Model |
| --------- | ----- |
| _id       |       |
| createdAt |       |
| updatedAt |       |
| subject   |       |
| body      |       |
| status    |       |
| recipient |       |
| sender    |       |

### Receipt service
**Data Model**
| Name      | Model                              |
| --------- | ---------------------------------- |
| _id       |                                    |
| createdAt |                                    |
| updatedAt |                                    |
| filePath  |                                    |
| author    | [EmployeeModel](#Employee-service) |

### Brownbag service
**Data Model**
| Name           | Model                              |
| -------------- | ---------------------------------- |
| _id            |                                    |
| createdAt      |                                    |
| updatedAt      |                                    |
| location       |                                    |
| speaker        | [EmployeeModel](#Employee-service) |
| company        | [CompanyModel](#Company-service)   |
| training       | [TrainingModel](#Training-service) |
| fromDate       |                                    |
| toDate         |                                    |
| title          |                                    |
| description    |                                    |
| participants[] | [EmployeeModel](#Employee-service) |

### Recommendation service
**Data Model**
| Name          | Model                              |
| ------------- | ---------------------------------- |
| _id           |                                    |
| createdAt     |                                    |
| updatedAt     |                                    |
| employee      | [EmployeeModel](#Employee-service) |
| training      | [TrainingModel](#Training-service) |
| recommendedBy | [EmployeeModel](#Employee-service) |

### Notification service
**Data Model**

No Data Model needed, gets Data from ElasticSearch

### Category service
**Data Model**
| Name      | Model                            |
| --------- | -------------------------------- |
| _id       |                                  |
| label     |                                  |
| createdAt |                                  |
| updatedAt |                                  |
| company   | [CompanyModel](#Company-service) |
| color     |                                  |

### Department service
**Data Model**
| Name      | Model                            |
| --------- | -------------------------------- |
| _id       |                                  |
| name      |                                  |
| createdAt |                                  |
| updatedAt |                                  |
| company   | [CompanyModel](#Company-service) |

### Budget service
**Data Model**

**Budget Data Model**
| Name      | Model                              |
| --------- | ---------------------------------- |
| _id       |                                    |
| employee  | [EmployeeModel](#Employee-service) |
| budget    |                                    |
| remaining |                                    |
| fromDate  |                                    |
| toDate    |                                    |
| createdAt |                                    |
| updatedAt |                                    |

**Spending Data Model**

### Search service
**Data Model**
_Streamed by MongoDB of all services_

### Slack service
**Data Model**

No Data Model needed

### Billing service
**Data Model**
| Name                 | Model                            |
| -------------------- | -------------------------------- |
| _id                  |                                  |
| company              | [CompanyModel](#Company-service) |
| plan                 |                                  |
| subscriptionStart    |                                  |
| subscriptionInterval |                                  |
| subscriptionEnd      |                                  |
| name                 |                                  |
| email                |                                  |
| street               |                                  |
| zip                  |                                  |
| city                 |                                  |
| country              |                                  |
| overdue              |                                  |

### Feature service
**Data Model**
| Name        | Model |
| ----------- | ----- |
| _id         |       |
| createdAt   |       |
| updatedAt   |       |
| feature     |       |
| betaRelease |       |
| fullRelease |       |
| enabled     |       |
