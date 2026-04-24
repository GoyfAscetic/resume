These charts try to offer flexibility to shipping customer to breakdown contract progress. The three dimensions of customization are: 
## Contract Structure
- **Carriers**, companies that own and operate cargo ships like Hapag Lloyd or MSC
- **Shippers**, companies that buy space on cargo ships measured in TEUs like IKEA or Wayfair
- Contracts progress is the percentage between TEUs used by the shipper divided by the space provided by the carrier 
  - So if a Carrier provides 100,000 TEUs for the Shipper to use in a year but the Shipper only uses 89,000 then the Contract progress is only 89%
- A Contract's **Milestone** is used to answer two questions
  - _Which port_ the TEU needs to reach to count towards Progress
  - The timestamp _when_ a TEU Counts towards Progress
  - Options include
    - When a Cargo Container is **Shipped On Board** the Vessel
    - When a Cargo Container is **Loaded at Port of Load** onto the Vessel
    - When a Cargo Container is **Gated In** the Port of Load
    - When the Vessel that's carrying the Cargo Container has left the **Sailing's Last Port of Load** for its journey
    - When the Vessel that's carrying the Cargo Container has left the **Sailing's First Port of Load** for its journey
- Contract **Frequency** is the _cadence_ and _calendar_ for tracking Contract Progress
  - _Cadence_ include week, month, quarter, year, and each unique **Sailing**
  - _Calendar_ includes Gegorian, ISO, and OPUS
  - Note **Sailing** does not use calendar for its cadence as multiple sailings could sail on the same date
- Another factor is where in the world this cargo space is being provided.
  - For example a shipper getting 100,000 TEUs of space deporting from USA doesn't matter if their factories are in China
- Contract can cover demand from all over the world
- Demand can change over the duration of the Contract
- So **Commitments** are used to break down which locations in world the contract promises TEUs over time
### Commitments
- **Commitments** organize when and where carriers expect to provide TEUs to the shipper
- One Contract has many commitments
- Commitments can start and end at anytime during a Contract's duration
- Commitments have their own **Milestone** and **Frequency** the differ from the Contract
- Commitments are broken down in two different ways
  - 


## Chart Structure

### 1.  Choosing the x-axis

- This can be done by time either weekly, monthly, quarterly, or yearly 

- We needed to support different calendars such as ISO, Gegorian, or OPUS

- Another approach was grouping the contract progress unique commitments

- Finally if the contract commitments were configured to 

### 2. Setting the goal for each bar in the x-axis

- This was determined by how the x-axis is chosen and how the contract was configured

- 
