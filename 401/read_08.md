# 401_Read_08 - Access Control (ACL)

- [5 Steps to RBAC](#5-steps-to-rbac)
  - [Answers.1](#answers1)
- [RBAC Wiki](#rbac---wiki)
  - [Answers.2](#answers2)
- [RBAC Tutorial](#rbac-tutorial---videos)
  - [Answers.3](#answers3)
- [Things to Learn More About](#things-to-learn-more-about)

## [5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)

Role-Based Access Control is all about giving a user permissions based on their job role rather than manually configuring each permission on a per user and scenario basis.

### Answers.1

1. What is Role Based Access Control (RBAC) and why do we care?
    - RBAC is an authorization system where permissions are assigned to roles, and users are in turned assigned those roles / added to those groups.
    - Least privilege is adhered under this system. A user only has permissions for what they need to do and access, no more.
2. Describe a Role/Permission heirarchy that you might implement using RBAC.
    - Master Baker - able to view and modify recipe, see client orders and contact info, ingredient stock and shipments, etc.
    - Delivery - Able to see clients orders, and address; recipe and ingredients not needed.
    - Client - only able to read products, not modify; only read what they need (price, ingredients, not recipe, profit, etc.), their order and only theirs, not others.
3. What approach might you take to implement RBAC?
    - Identify protected resources (client info, modify-type permissions, etc.)
    - Divide permissions among job roles based on what they need to complete their tasks and duties.
    - Store roles assigned to users in DB.
    - Once a user authenticates, an authoriz middleware check is ran to check role and permission to run protected route.
    - Review roles and permissions regularily, especially in times of re-structuring and employee movement.

## [RBAC - wiki](https://en.wikipedia.org/wiki/Role-based_access_control)

### Answers.2

1. If Authentication is "you are who you say you are," what is Authorization?
    - Authporization is 'what you are allowed to do', based on 'who you are'.
2. Name three primary rules defined for RBAC.
    - Role assignment - permission is granted to a user after and only when they have an assigned and/or active role that allows them to carry out their aim or goal.
    - Role authorization - roles are activated by a user only if they authorized to have said roles.
    - Permission authorization - depending on a user's active role; a user may perform actions that align with said role.
3. Describe RBAC to a non-technical friend.
    - Back to bread and bakers. Everyone is allowed to see price and ingredients (hopefully). Only bakers are allowed to see baking recipe and various clients order and info, only the master baker can alter and modify the recipe, see ingredient order, and other high level info not relevant to other roles.

## [RBAC tutorial - [Videos]](https://www.youtube.com/watch?v=C4NP8Eon3cA)

### Answers.3

1. What are access rights associated with? The User or The Role? Explain.
    - Access are associated with the **role**; users receive permissions based on the role they are assigned to.
2. Access Rights, or Authorization, is activated after a user successfully does what?
    - Activated after the user authenticates their identity.
3. Explain how RBAC might benefit a business.
    - Protect data by limiting access to only what is needed by certain roles.
    - Makes onboarding, position changes, and offboarding a more seamless process.

## Things to Learn More About

- Incorporating RBAC to express app,
- the structure to the middleware,
- RBAC relation with JWT,
- determiantion o routes to be public, subject to suthentication, or restricted to certain roles.
