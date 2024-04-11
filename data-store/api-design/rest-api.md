---
title: REST API
Type:
tags:
  - API
  - Database
DateStarted: 2023-12-27
DateModified: 2023-12-27
DateDo:
DateDone:
DateDue:
status:
---

### REST API

![](z-Assets/Pasted%20image%2020230308202339.png)

- Representational State Transfer
- Architecture style for designing network application
- Rely on a stateless, **client-server** protocol, almost always HTTP
- Use specific HTTP methods and endpoints
- Fetches all or nothing
- Treat server objects as resources that can be created or destroyed.
- Can be used by virtually any programming language
- JSON as the response type of REST APIs
- Good for CRUD

#### 1. Pros

- Standard method names, arguments and status code
- Utilized HTTP features
- Easy to maintain

#### 2. Cons

- Big payloads
- Multiple HTTP roundtrips (To get the resource and the sub-resource, you have to get each individually, no way to combine the results together)

#### 3. CRUD

- POST
- PUT
- PATCH
- GET
- DELETE

#### 4. NON-CRUD

- Archive
- Deactivate
- Search
- ![](z-Assets/Pasted%20image%2020230315162159.png)
