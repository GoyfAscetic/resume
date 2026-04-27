# Shipping Industry Overview
## Goal of the Industry
- To enable the purchase, sale, and use of Space on Cargo Ships to ship goods around the world.
## What are the Key Roles in the Industry?
### Carriers
- Companies that own and _sell_ space on cargo ships  like Hapag Lloyd or MSC
- They want to avoid penalties that occur if they fail to _provide_ the space to **Shippers** 
- They want to ensure that **Shippers** are using the Cargo Space provided by their **Contracts**
  - Especially when the Ad-Hoc Cargo Space rates are _lower_ than the Contract Rates
### Shippers
- Companies that _buy_ space on cargo ships like IKEA or Wayfair
- They want to avoid penalties that occur if they fail to _use_ the space given to them by the **Carriers** 
- They want to ensure that **Carriers** are providing the Cargo Space promised by their **Contracts**
  - Especially when the Ad-Hoc Cargo Space rates are _higher_ than the Contract Rates
### NVOs
- Companies that buys cargo space from **Carriers** to resell to **Shippers** that lackm volume to work with **Carriers** directly.
- Examples include DSV and ONE
- They'll agree to **Parent Contracts** with **Carriers** to buy excess Cargo Space
  - NVOs are the **Shipper** of all **Parent Contracts**
- Then they'll agree to **Child Contracts** with **Shippers** to sell the Cargo Space promised by the **Parent Contract**
  - NVOs are the **Carrier** of all **Child Contracts**    
## How is Cargo Shipped?
- For each shipment **requested** by a **Shipper** they will submit a **Booking** to a **Carriers** requesting Cargo Space measured in **TEUs**
  - The **Booking** status becomes **Requested**
- The **Carrier** then decides to confirm or reject the **Booking**  
  - The **Booking** status becomes **Pending**, while the Carrier is deciding
  - The **Booking** status becomes **Rejected**, if the Carrier _declines_ the **Booking** and the shipping process _ends_.
- When the **Booking** is confirmed, the **Carrier** will assign Cargo Container **Equipment** equal to the TEU volume requested
  - The **Booking** status becomes **Confirmed**
- The **Equipment** Containers will **Gate Out Empty** of the **Port of Load** and sent to the **Place of Receipt**
  - The **Booking** status becomes **Gated Out Empty**
  - Each **Equipment** will note the timestamp for when it was **Gated Out Empty**
- Once the **Equipment** reaches the **Place of Receipt** the Shipper will fill up the **Equipment** with the Goods to be shipped
  - The **Booking** status does not change as the Carrier doesn't track this event
  - The **Equipment** does not note this time as the Carrier doesn't track this event
- Then the **Equipment** is returned to the **Port of Load**
  - The **Booking** status becomes **Gated In**
  - Each **Equipment** will note the timestamp for when it was **Gated In**
- Next the **Equipment** is **Loaded** onto the first Vessel of its **Sailing** Voyage
  - The **Booking** status becomes **Loaded at Port of Load**
  - Each **Equipment** will note the timestamp for when it was **Loaded at Port of Load**
- The goods are **shipped** once the first vessel begins it **Sailing** Voyage by leaves the **Port of Load** 
  - The **Booking** status becomes **Shipped on Board**
  - Each **Equipment** will note the timestamp for when it was **Shipped on Board** 
  - The **Sailing** will note the same timestamp as the **First Port of Load Departure**
- The Vessel will then travel to other Ports to Load other goods along its **Service** Loop
  - The **Booking** status does not change as these events are not tied to the Booking
  - The **Equipment** does not note these timestamps as these events are not tied to the Booking
  - The **Sailing** will note just the **Last Port of Load Departure** time of the Vessel
- Once the **Sailing** has left the **Last Port of Load** it'll cross the ocean to discharge goods on the other half of the **Service** Loop
- When the **Sailing** reaches the **Booking's** **Port of Discharge** the Equipment is **Unloaded** off of the **Sailing** Vessel
  - The **Booking** status becomes **Unloaded at Port of Discharge**
  - Each **Equipment** will note the timestamp for when it was **Unloaded at Port of Discharge**
- The **Equipment** Containers will **Gate Out Full** of the **Port of Discharge** and sent to the **Place of Delivery**
  - The **Booking** status becomes **Gated Out Full**
  - Each **Equipment** will note the timestamp for when it was **Gated Out Full**
- Finally, once the **Equipment** reaches the **Place of Delivery** the Shipper will remove the Shipped Goods out of the **Equipment**
  - The **Booking** status does not change as the Carrier doesn't track this event
  - The **Equipment** does not note this time as the Carrier doesn't track this event
## Shipping Risks
- Cargo Space Supply and Pricing can fluxuate heavily based on many real world conditions spanning from the weather to labor strikes 
- A lack of Cargo Space Supply _raises_ TEU pricing and threatens **Shipper** Supply Chain
- A lack of Cargo Space Demand _lowers_ TEU pricing and threatens **Carrier** Revenue
- To manage both risks, **Carriers** and **Shippers** enter into **Contracts** to commit to multiple **Bookings** in advance

## Contract Structure
- A Contract ensure that some Cargo Space (in **TEUs**) will be provided by the Carrier and used by the Shipper
  -  
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
- So **Commitments** are used to break down the total number of TEUs promised by the Contract by both time and Location
### Commitments
- **Commitments** organize when and where carriers expect to provide TEUs to the shipper
- One Contract has many commitments
- Commitments can start and end at anytime during a Contract's duration
- Commitments have their own **Milestone** and **Frequency** the differ from the Contract
- Commitments connect to Bookings in teo different wayss
  - Using **Lanes** using origin/destination port pairs on **Bookings** to connect to TEUs
  - Using **Sailings** using Sailing records to connect between  


## Chart Structure

### 1.  Choosing the x-axis

- This can be done by time either weekly, monthly, quarterly, or yearly 

- We needed to support different calendars such as ISO, Gegorian, or OPUS

- Another approach was grouping the contract progress unique commitments

- Finally if the contract commitments were configured to 

### 2. Setting the goal for each bar in the x-axis

- This was determined by how the x-axis is chosen and how the contract was configured

- 
