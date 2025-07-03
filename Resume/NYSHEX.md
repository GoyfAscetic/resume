

# NVO Migration
## Staff Engineer
- Architechted a plan to combine account data across 40 databases with a strategy to rollback all changes without trancations
- Experience the entire platform through one account instead of two

# Engineerined a new Data pipeline to improve Contract Progress Accuracy for over 1 million transactions

# Migrating All Customers to new Contract Progress Platform
## Team Lead
- Inherited ownership of a project that was far behind schedule
- Filled in the leadership vaccum created by the departure of the Engineering Manager and Product Manager

# Merging two Microservices to stablize Contract Progress Platform
## Situation
- All 9 Contract Progress Endpoints were consistently crashing due to the processing taking too long
## Task
- My team needed to reduce the runtime of these endpoints espeically for Larger contracts
## Action
### Staff Engineer
- Indentified that the runtime logic was spread between two microservices connected by an API call with large request and response payloads
- Discovered that one of these microservices only communicated with the other
- So I architeched a plan to merge the two microservices
  - I noticed that since all the data for the TBD (To be Deprecated) Microservice was provided by Kafka streams
  - Also we already had the ability to replay all past Kafka events
  - So to merge them all we need to is duplicate the code and db schema from the TBD microservice to the host microservice
  - Then replay all the events
- With both listening to the same events the data in the two DBs would typically stay in sync
- Therefore the data in their respective endpoints would stay in sync providing a clear toward validating the success of the 
- By keeping both microservices up during the we can test the merge without risking user impact if there are issues
### Team Lead
- Tailored the strategy to best to align with a Senior engineer on my team
- Presented the situation, task and action to successfully secure buy-in from Engineering Leadership
- Explained to the CTO how the plan would address each and every concern he raised
## Results
- The merge was completed by one engineer in just two weeks
- Deployment the merged service and deprecation of the other service took  less than 24 hours
- No disruption to both Microservices
- All 9 endpoints worst case runtimes dropped from over a minute to a couple of seconds

# AMT Report
## Situation
- One of the last blockers to migrate a third of our customers to the Contract Progress Platform was a Report that took six month to build in the previous platform
## Task
- Build a Report that would show Progress for all Contracts 

# Accelerating Contract Progress Platform response time with Precomputation

# Consolidated 13 different versions of the same Contract Progress logic into one place improving accuracy in most charts while reducing runtime by 63.2%

# Pioneered new approach to test and rollout refactors n production while providing the option to rollback

# Added 


