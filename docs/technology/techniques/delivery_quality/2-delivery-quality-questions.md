---
sidebar_label: 'Delivery Quality Questions'
---

# Delivery Quality Questions

## Introduction 
These questions are used in Delivery Quality Reviews to help teams assess how well we are doing things on each engagement. Not every question applies to every engagement, and the answers can vary depending on the responsibilities and make-up of the team, but they provide a good, broad overview of what a healthy engagement looks like. (See ‘Delivery Quality Review Process’ for more information on how to run a review.)  

## Scoring
The team scores each area to highlight where they want to focus their efforts.  The scoring scale is as follows:  

| Score | Description |
| ------ | ------- |
| 5 | **Great.** All the right things are happening. |
| 4	| **Good.** Most of the right things are happening. |
| 3	| **Average.** Some improvement is needed. |
| 2	| **Poor.** Moderate improvement is needed. |
| 1	| **Needs Work.** Significant improvement is needed. |

The scores are relative to a shared view of what good looks like and are established by reviewing the questions in this document. These questions have evolved, with many contributors from across the software development and delivery community. They are refined from time to time as improved tools and techniques emerge.  

* Note that the team carries out the review.  It is done ‘done to’ the team.  

## This is a self-assessment  
The Delivery Quality Review is a self-assessment which is done by the team and supported by people form outside the account.  There are some simple points that it is worth emphasising:    
* The review is carried out by the team, not “done to” the team.  
* The emphasis is on discussion, alignment and action, not the scores.  
* Scores help the team to focus their improvement efforts in the right places.  
* Scores can help the team communicate and escalate issues outside the team.  
* Scores cannot be directly compared between teams but can help spot common issues that would benefit from coordinated effort across multiple teams to improve.  

## 1.Goals  
* Are the business goals of the engagement clear and visible to all?  
    - Are the objectives backed by clear business metrics / KPI’s?  
    - Is user feedback gathered and incorporated into the development process?	 
* Are users a key part of the design and development process?  
    - Are the non-functional requirements of the system understood and written down?  

## 2. Plan  
* Is there a plan for the engagement and team for a sensible timeframe (1-2 months)?  
* Is the plan at the right level – a small number of epics per sprint, for example.  
* Are milestones clearly shown on the plan?  
* Is the plan up to date and complete?  
    - Does the team have regular backlog refinement session?  
* Does everyone in the team understand the plan?  
    - Is there a forecast for what is most likely to happen?  
* Does the plan iteratively deliver business value, starting with a walking skeleton?  
* Does the plan take an ‘operations first’ approach?  
    - Does the plan include the right amount of detail for maintainability and operability?  

## 3. Delivery   
* Is there a defined delivery process that everyone sticks to?  
    - Are tasks managed using a shared agile/kanban/process board?  
    - Are there clear definitions of ready and exit criteria for each column of the board, and a clear ‘definition of done’ for each task?  
    - Is analysis and elaboration done prior to implementation?  
* Are stand-ups held and effective?  
* Is functionality delivered in thin vertical slices?  
    - Are items typically delivered in two days or less, from backlog to done?  
    - Is each item able to be demonstrated individually?  
* Does the team use source control, ideally with short-lived feature branches off a long-lived main branch?  
    - Is all code reviewed and do all tests pass before branches are merged?  
    - Can code changes be traced back to business requirements (for example using issue reference numbers in code commits)?  
* Is continuous improvement embedded in ways of working?  
    - Does the team have regular retrospectives?  
    - Do team members look forward to retrospectives?  
    - Are bugs and tech debt dealt with and not left to accumulate?  
* Do stakeholders have good visibility of the team’s progress?  
    - Does the team hold sprint reviews/demos and write sprint reports?  

## 4. Team
These questions cover the entire team.  If you are working with an augmented team that includes customer and potentially third-party staff, add those people into your thinking.  
* Is the team a fun place to be?  
* Do team members trust one another?  
* Do team members go out of their way to help one another?  
* Are team members learning new things?  
* Is the pace of work sustainable?  
* Do people give honest feedback when things aren’t right?  

## 5. Risks and Decisions
* Are risks and issues tracked?  
    - Are risks and issues worked on promptly?  
    - Are risks and issues communicated and escalated effectively?  
* Are technical and product decisions recorded?  
    - Is there clear ownership, sign-off and accountability for each decision?  

## 6. Skills and Knowledge
* Does the team have all the skills, knowledge, experience and capacity it needs to do a great job?  
* Are skills and knowledge well spread between team members?  
    - Do team members work across all deliverables, in multiple roles and are knowledge silos avoided?  
    - Do the team use a range of approaches to develop new skills and share knowledge?  
* Does the team have good documentation?  
    - Does the documentation cover architecture and operability?  
    - Are the documents kept up to date and accessible?  
* Is the onboarding of new team members quick and easy?  


## 7. Healthy Codebase
* Is the code clean, easy to read, well-structured and safe to work with?  
* Does the code have good unit test coverage?  
* Is source control used for all development artefacts?  
* Are appropriate design patterns and common libraries used?  

## 8. Functional Testing
* Is testing everyone’s responsibility?  
* Is there good, automated test coverage?  
    - Are integration tests quick and effective?  
    - Is there explicit contract testing between components and sub-systems?  
    - Are whole system tests reliable and maintainable?  
    - Is test data valuable, useful and created and managed sensibly?  
* Are tests required to pass before code is merged?  
* Are tests required to pass before releases?  
* Can all tests be run locally?  
* Does the team do effective exploratory testing?  

## 9. Technology and Architecture
* Do the technology stack and architecture choices work well for the team?  
    - Is the developer experience good?  
    - Do tech stack and architecture make testing easy?  
    - Do tech stack and architecture make it east to operate service reliably?  
    - Is the technology something the customer can live with in the long term?  
* Is the technology strategy for the engagement clear?  
    - Is the architecture modern and proven?  
    - If changes are needed to the architecture and tech stack, is there a roadmap in place?  

## 10. Deployment
* Is CI/CD used and does it work well?  
    - Is a release candidate built on every merge of a feature branch?  
    - Is this release candidate progressed through environments rather than built specifically for each environment?  
    - Does each environment have a single, clear purpose?  
    - Is every environment in the deployment pipeline identical?  
    - Are deployments fully automated – can automation create an environment from scratch?  
    - Is it possible to deploy / roll back to any recent version of the solution?  
* Is it easy to release a change all the way to production?  
    - (Ideal) Can changes be released on demand, multiple times per day?  
* (Ideal) Do deployments follow a blue-green / canary pattern, with automated roll back if unhealthy?  

## 11. Security and Compliance
* System design  
    - Is the minimum necessary data handled?  
    - Is the system designed to minimize attack surface?  
    - Does the team consider OWASP Top 10 during design and implementation?  
* Software supply chain	  
    - Is source code access secure, with reliable audit for code changes?  
    - Are static analysis tools used to can code?  
    - Are build-time dependencies scanned for vulnerabilities?  
    - Are run-time dependencies scanned for vulnerabilities (e.g. base containers and VM images)?  
    - Is the running system scanned for vulnerabilities? e.g. using OWASP ZAP)  
    - Do CI/CD triggered deployment use an infrastructure role with minimal permissions?  
    - Are secrets managed securely?  
* Infrastructure  
    - Do cloud user roles have minimum permissions?  
    - Are best practices enforced? (e.g. AWS Config)  
    - Is there audit logging and traceability?  
    - Is there active scanning of hosts, software and running systems? (e.g. Amazon Inspector)  
    - Is all ingress protected appropriately? (e.g. Web Application Firewall WAF)  
    - Is data secured at rest and in transit?  
* People Factors  
    - Is there a process to manage access controls?  
    - Do people have the minimum permissions needed to do their job?  
    - Do the team rehearse security incident responses?  
    - Is there a quick and easy process to remove someone from the system?  

## 12. Observability  
* Are the logs useful and accessible?  
* Is the log retention reasonable?  
* Does the team trust the monitoring? – Is it reliable?  
* Is the monitoring isolated?  
    - Can the team access monitoring during incidents?  
    - Could the monitoring system cause incidents?  
* Do the right people have access to the monitoring?  
* Are system dependencies monitored?  
* Is the monitoring data storage resilient, with an appropriate retention policy?  
* Are alerts in place?  
    - Are alerts relevant, with few false alarms or gaps?  
    - Can the impact and priority of an incident easily be determined?  
    - Do the right people get alerted?  
    - Is alerting based on business KPIs (e.g. shopping basket abandonment rates, new customer sign-ups, customer enquiries waiting for response)?  
* Has distributed tracing been put in place, if relevant?  

# 13. Performance and Scalability  
* Are performance and scalability requirements clearly understood?  
    - Are there constraints imposed by the systems this solution depends on?  
* How does the team verify performance and scalability requirements are met?  
    - How regularly does the team carry out performance testing?  
    - Is testing efficient and automated?  
    - Is the team aware of performance bottlenecks?  
        - In which components do bottlenecks occur?  
        - Which resources are bottlenecked?  CPU, Memory or network?  
    - Have stakeholders signed off on performance and capacity?  
* Does the system scale automatically when needed?  
    - Does it scale without impacting availability?  
    - Does it do so quickly enough to meet spikes in demand?  
    - Are the right metrics used to trigger scaling up and down?  
    - Are safe minimum and maximum scaling limits known and configured?  
    - Can the system scale without major re-engineering?  

## 14. Availability  
* Are the availability requirements defined and understood?  
    - Are there availability constraints imposed by systems the solution depends upon?  
* Is the system reliable?  
    - Is it resilient and does it self-heal?  
    - Is it fault tolerant?  
    - Where is data stored in the system and where is it mastered?  
    - Is possible data loss understood and accepted?  
* Is the systems reliability tested?  
    - Are these tests automated?  

# 15. Cost  
* Are the solutions costs well understood?  
    - Is cost tracking in place?  
    - Is cost attributable?  
* Is the system cost effective?  
    - Does the chosen tech stack provide value for money?  
    - Are cost control measures in place and are costs predictable as the system scales or experiences spikes in use?   

# 16. Operability and Operations  
* What is the team’s involvement in support of the production system?  
    - Does this include out of hours support?  
* How is the team informed about incidents from alerts and user reports?  
    - Are issues detected and prevented before users report them?  
    - Are Service Level Objectives used to determine incident severity?  
    - Are response and communication agreements clear for each level of severity?  
* Is the Incident Management / Incident Resolution process smooth and efficient?  
    - Does the team know the target Mean Time to Recovery (MTTR)?  
    - Does the team have defined on-call roles and procedures?  
    - Is problem diagnosis and resolution structured, easy and effective?  
    - Is communication and collaboration smooth and effective?  
    - Are run-books in place and working well?  
* Does the team learn from incidents using blameless post-mortems?  
* Does the technology being used in the solution make operations easy?  
    - Are vendor support agreements in place?  
* Are support processes well-rehearsed and regularly tested?  
    - Game Days  
    - Chaos Engineering  
    - Pagerduty incident response documentation and process  

# 17. Go-Live Readiness  
Are you planning on an initial release or a significant change that will affect users? If not, then this section can be skipped.    

* Do you have an established acceptance into service criteria?  
    - Have these criteria been met?  
* How will business processes have to change to accommodate this release?  
    - Are people ready for the necessary changes?  
* How will the team know how users have been affected by the change?  
    - Will there be monitoring, alerting, analytics or user feedback mechanisms in place?  
    - Are external go-live dependencies and pre-requisites understood, being tracked and actioned?  
    - Is any data migration needed?  
    - Will there be dual-running or a hard switch-over?  
    - How can the go-live deployment be rolled back if necessary?  
    - How will users be migrated or onboarded?  
    - How does the migration affect dependent systems?  
    - Will there be a service outage during release?  
    - Is there a warranty period?  
    - How will the solution be supported in operation?  

## Further Reading  
The Delivery Quality Review process was inspired by the Quality Views process that was pioneered by engineering teams at Netflix. The approach has matured a lot since its inception and will undoubtedly change again as we learn more about what we need to do to best support teams that are delivering amazing outcomes for our customers.     
The Delivery Quality Review process is closely associated with the Account Summary process, as well as the Account Planning process at Robiquity. Together these three processes give us a great insight into what we are doing with a customer, why we are doing it, how we are doing it and whether we are doing it well. Check out those other process to learn more about each in detail and get a good overview of how they all fit together.  




