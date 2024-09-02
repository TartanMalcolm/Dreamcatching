
### 2-Step User Stories

1. **Customer Requests Pickup Change:**
   - **Customer**: "I need to change my next pickup date."
   - **Red Lid Admin**: "I have modified your scheduled run." 
     - **Red Lid Admin** updates the run in the system.


An email comes in from a Customer to the Customer Agent asking for the next pickup to be cancelled, but only that one.  Customer agent has permission to cancel a single change, and notifies the Duty Manager who alters the schedule.  The Driver comes on shift and receives the schedule, with an additional note about the change as it's always good to be obvious when changing routine tasks.  The Accountant is also notified that there's a change for invoicing.  


2. **Driver Assigned to Multiple Runs:**
   - **Red Lid Admin**: "You have been assigned to an additional run."
   - **Driver**: "I will check my updated schedule for the new assignment."
     - **Driver** reviews their manifest to see the updated schedule.

Duty Manager needs to have a Driver do an additional run because a truck is out of order and there's reduced capacity.  The Driver converses with the Duty Manager about whether he can make the additional run.  HR is informed about the proposal, (I'm assuming there's a maximum number of hours allowed, and a contract with the Driver that needs to be honoured.). HR confirmed, Driver confirms, schedule is updated.

3. **Sector Creation and Assignment:**
   - **Red Lid Admin**: "I have created a new sector for better organization."
   - **Red Lid Admin**: "I will assign runs to the new sector."
     - **Red Lid Admin** updates the system with the new sector and assigns runs.

A new customer has asked to sign up, but is outside of the Sectors currently covered.  The Duty Manager has permissions to alter schedules, but not add a new route.  To do that the Accountant, Duty Manager and Commercial Manager needs to interact to decide whether 1. alter the existing Sectors to include the new location. 2. Create a new Sector of one location (ie it might be worth it, maybe not.) 3. Decide whether to take a loss-leader and market to other addresses nearby - as it follows if one new customer is in that area, possibly more could be.  Once a decision is made, either 1. The customer is turned down, and perhaps pointed to another firm. 2. The new/altered Sectors are updated.  If 2. then the schedule needs to be update, the drivers need to be informed, the customer needs to be on-boarded, and possible, contacted again after the first pickup as a nicety. 

4. **Consistent Customer Pickups:**
   - **Customer**: "I want to be added to a regular weekly run."
   - **Red Lid Admin**: "You have been added to a consistent weekly run."
     - **Red Lid Admin** updates the customer’s schedule in the system.

Version 1: A customer is new and is asking for a regular weekly run.  Customer is in an existing sector.  The Customer Agent takes the order and checks against the existing runs to see if there's capacity (NB this is new - need to talk about capacity planning as that's not in RedLid's business rules.). If there is (possibly) allow the Customer Agent to say yes immediately.  If there isn't capacity, then it goes to the Duty Manager to check if the schedules can be moved to accomodate and to check with the Truck Fleet and Drivers to see if there's physical capacity.  If the answer is yes, then Accounts notified, Customer Agent notified, and Customer informed.

Version 2: An existing customer asked for a second weekly run.  As above, but:

	NOTE: current ERD allows for 1:1 for Customer:Pickup.  New rule?  If there is a new rule, super-admin now must add in a new test for that business rule, and re-run the tests in sandbox on the existing state to see if it breaks anything.  Result 1: Nothing breaks, but now perhaps the Customer Record structure needs to be updated to allow for multiple runs.  So Super Admin commits the change.  Result 2: It does break something.  So Super-Admin can either figure out what other business rules it violates, updates those as new tests, re-runs, rinse and repeat until the change can be made or proven that it can't.  However, if it can't, then presumably it's not the system that's at fault, it could be that the business wants to expand.  Therefore delayed decision until business decides.  If yes, then back to the testing cycle, then when tested back to the Customer Agent who informs the Customer.  If no, then back to Customer Agent who informs Customer.  Therefore, need a delayed messaging stack, ie "we'll get back to you." and presumably also a prompt based on time or decision for promises made to customers so that the Customer Agent can keep the customer in the loop.  



5. **Manage Overlapping Runs:**
   - **Red Lid Admin**: "I see we have overlapping runs in the same sector."
   - **Red Lid Admin**: "I will adjust pickup dates to resolve this."
     - **Red Lid Admin** updates the run schedule to avoid overlap.

Duty Manager has an unforseen scheduling issue, e.g. a Truck is taken off line.  Duty Manager confers with the system to work out an appropriate one-off change based on how long they think the issue will last.  A suitable new set of schedules that works with Driver work contracts, truck availability and some metric to minimise the impact to customers is decided.  Customer Agent is informed to email the impacted Customers about their pick-up. (Let's assume the customer contract allows for this.)


6. **Address Change Handling:**
   - **Customer**: "I have moved to a new address."
   - **Red Lid Admin**: "Your address has been updated, and your new location falls within an existing sector."
     - **Red Lid Admin** updates the address and assigns the new sector and run.

Customer tells the Customer Agent that they love the service, but are moving house (New House is within the existing Sectors served.). Customer Agent then needs to take the new address, the date they'll be there, and inform Duty Manager.  Duty manager now needs to alter the schedules after the date to avoid a pick-up at the old house, but that's in the future.  Also needs to alter schedules after that date to the new house.  System can handle the schedule shifts, but are tied to the customer address, and now there's two, based on time.  Over to Super Admin to alter the address field to handle two addresses, with date ranges for when valid.  Then, back into the test cycle.


7. **Truck Maintenance Impact on Runs:**
   - **Red Lid Admin**: "We have scheduled truck maintenance."
   - **Red Lid Admin**: "I will reassign runs to available trucks to ensure service continuity."
     - **Red Lid Admin** updates truck assignments in the system.

A Truck is approaching a maintenance cycle that means it will be off the road for 4 days, but the company can say when those 4 days are.  Duty Manager is aware of the maintenance schedule and must 1. Minimise the impact by choosing an appropriate day for it to go into the shop. 2. Trigger the changes to schedule, which may result in one or both of Drivers and Customer Agents being informed (and therefore Customers notified.) 

For exercise, this also looks like a Stuck, so Duty Manager now needs a tool to minimise the impact as the current system can't handle that sort of thing (or is giving shit answers.). Therefore Duty Manager registers a stuck and escrows.  Time passes... [Note: insert Stuck Loop here]. Now Duty Manager has a new tool for the next time this happens.


8. **Red Lid Admin Approving Requests:**
   - **Customer**: "Can I have a one-time bulk pickup?"
   - **Red Lid Admin**: "Your request has been approved, and I have created a special run for your bulk pickup."
     - **Red Lid Admin** schedules the special bulk pickup.

Customer asks Customer Agent for the same pickup date and location, but for double the capacity.  Customer Agent should have access to some kind of capacity tool here that assumes nothing else has changed except doubling the pick-up size for one location on one date.  If this is a stuck, see above.  


9. **Sector Analysis for Efficiency:**
   - **Red Lid Admin**: "I am reviewing sector data to enhance route efficiency."
   - **Red Lid Admin**: "I have made changes to sector boundaries for optimal performance."
     - **Red Lid Admin** updates the sector boundaries and assigns new runs.

Board have asked Duty Manager to ensure that they're scheduling and sector choises are optimal.  Probably another stuck, but I'm guessing that the Duty Manager would give it a go with the existing system in NL.  Assuming that takes a lot of prompting but works.  Duty Manager now wants to use that in the future but not go through the same process of prompting again - ie a bash script.  NOTE: Possible Artifact Function?


10. **Driver License Update:**
    - **Driver**: "I need to update my license details."
    - **Red Lid Admin**: "Your new license information has been verified and approved."
      - **Red Lid Admin** updates the driver’s license information in the system.

Driver contacts HR with an issue with his license.  It's now out of date and needs to be reverified.  HR contacts Duty Manager who reschedules (repeat of above similar to drop in capacity.). HR updates and verifies new license details, contacts Accountant for any revisisions to pay for the Driver, contacts Driver.


### 3-Step User Stories

1. **Adding a New Customer:**
    - **Customer**: "I want to sign up for recycling services."
    - **Red Lid Admin**: "I have added you to the system and scheduled your pickups."
      - **Red Lid Admin** creates a customer profile and assigns a run.
    - **Red Lid Admin**: "You are all set and will receive a notification with your pickup schedule."
      - **Red Lid Admin** sends a notification to the customer.

 [Nothing new here.]

2. **Seasonal Adjustments:**
    - **Red Lid Admin**: "We are adjusting run schedules for the upcoming public holiday."
    - **Driver**: "I will update my route to reflect the new schedule."
      - **Driver** checks the updated manifest.
    - **Approved Red Lid Admin**: "The seasonal adjustments have been approved."
      - **Approved Red Lid Admin** confirms the system updates.

[Adding in a new holiday?]

3. **Financial Processing for Special Services:**
    - **Customer**: "I request a special service that incurs an additional fee."
    - **Red Lid Admin**: "I have scheduled your special service."
      - **Red Lid Admin** adds the special service run.
    - **Approved Red Lid Admin**: "Your payment has been processed, and the account balance updated."
      - **Approved Red Lid Admin** confirms the payment and updates financial records.

4. **Handling Overbooked Runs:**
    - **Customer**: "I want to sign up for your services."
    - **Red Lid Admin**: "I see the run is overbooked, so I will schedule an additional run."
      - **Red Lid Admin** creates a new run.
    - **Red Lid Admin**: "Your service has been scheduled on a new run."
      - **Red Lid Admin** notifies the customer of the new schedule.

5. **Multi-Driver Coordination:**
    - **Red Lid Admin**: "I am assigning multiple drivers to a large run."
    - **Driver**: "I'll coordinate with other drivers to ensure all pickups are done efficiently."
      - **Driver** collaborates with other drivers.
    - **Red Lid Admin**: "The run was completed efficiently with multiple drivers."
      - **Red Lid Admin** updates the manifest to reflect successful completion.

6. **Reviewing and Approving Driver Schedules:**
    - **Red Lid Admin**: "I have created manifests for the upcoming month."
    - **Approved Red Lid Admin**: "I will review and approve these schedules."
      - **Approved Red Lid Admin** validates the schedules.
    - **Driver**: "I have received today’s manifest."
      - **Driver** checks the monthly manifest and prepares.

7. **Addressing Missed Pickups:**
    - **Customer**: "I missed my scheduled recycling pickup."
    - **Red Lid Admin**: "I have scheduled a follow-up run to ensure your items are collected."
      - **Red Lid Admin** updates the schedule with the follow-up run.
    - **Driver**: "I will complete the missed pickup on the next available run."
      - **Driver** performs the follow-up pickup.

8. **Customer Payment Update:**
    - **Customer**: "I want to update my payment details."
    - **Approved Red Lid Admin**: "Your payment information has been updated and verified."
      - **Approved Red Lid Admin** updates the customer’s payment details.
    - **Approved Red Lid Admin**: "Your next billing cycle will reflect these changes."
      - **Approved Red Lid Admin** confirms the change in the system.

9. **New Truck Integration:**
    - **Red Lid Admin**: "We are adding a new truck to the fleet."
    - **Driver**: "I am assigned this new truck and will update my manifest accordingly."
      - **Driver** updates the manifest with the new truck.
    - **Red Lid Admin**: "The assignments have been updated." 
      - **Red Lid Admin** registers new truck and assigns runs.

10. **Sector-Based Reporting:**
    - **Red Lid Admin**: "I will generate a report based on sector performance."
    - **Approved Red Lid Admin**: "I will review the report and make necessary adjustments."
      - **Approved Red Lid Admin** analyzes the report and provides feedback.
    - **Red Lid Admin**: "The sector performance adjustments have been implemented."
      - **Red Lid Admin** makes updates based on feedback. 









1. **Scheduling Emergency Pickups:**
   - **Customer**: "I need an emergency pickup. I have a hazardous item that needs proper disposal."
   - **Red Lid Admin**: "I will create a special run for this emergency pickup." 
     - **Red Lid Admin** creates and schedules a special run in the system.
   - **Driver**: "I see I have been assigned an emergency pickup today."
     - **Driver** reviews the updated manifest and prepares for the pickup.
   - **Approved Red Lid Admin**: "I will ensure the hazardous item is disposed of correctly."
     - **Approved Red Lid Admin** verifies proper disposal procedures are followed.

2. **Customer Upgrades Service Plan:**
   - **Customer**: "I would like to upgrade to the premium recycling service plan."
   - **Red Lid Admin**: "I have updated your profile and service details."
     - **Red Lid Admin** updates the customer profile in the system.
   - **Approved Red Lid Admin**: "I have reviewed and approved the new billing for your premium service."
     - **Approved Red Lid Admin** adjusts the billing information.
   - **Driver**: "I have been informed of the changes and will adjust my pickups accordingly."
     - **Driver** reviews the updated manifest for premium service pickups.

3. **Review and Approve Sector Changes:**
   - **Red Lid Admin**: "I propose a change to the current sector boundaries to balance our routes."
   - **Approved Red Lid Admin**: "I am reviewing and will approve these sector boundary changes."
     - **Approved Red Lid Admin** reviews and approves the proposed sector changes.
   - **Red Lid Admin**: "The new sector boundaries are now in effect."
     - **Red Lid Admin** updates the system with new sector boundaries.
   - **Driver**: "I have received the updated routes based on the new sector boundaries."
     - **Driver** adjusts routes according to changes.

4. **Customer Requests Bulk Pickup:**
   - **Customer**: "I need a bulk pickup for a large quantity of recyclables."
   - **Red Lid Admin**: "I will schedule a special bulk pickup run for you."
     - **Red Lid Admin** schedules a special run for bulk pickup.
   - **Approved Red Lid Admin**: "I have confirmed the special bulk pickup arrangement."
     - **Approved Red Lid Admin** confirms the special run in the system.
   - **Driver**: "I am ready to complete your bulk pickup as per the scheduled run."
     - **Driver** prepares and executes the bulk pickup run.

5. **Handling Driver Substitution:**
   - **Driver**: "I am unable to complete my run today due to illness."
   - **Red Lid Admin**: "I will identify a substitute driver for today."
     - **Red Lid Admin** finds a substitute driver in the system.
   - **Approved Red Lid Admin**: "I have approved the driver substitution."
     - **Approved Red Lid Admin** confirms the substitution.
   - **Substitute Driver**: "I will take over the assigned run for today."
     - **Substitute Driver** carries out the assigned run.

6. **Seasonal Pickup Adjustments:**
   - **Customer**: "Will there be any changes to my recycling pickups during the holidays?"
   - **Red Lid Admin**: "We are adjusting the schedule for the holiday season."
     - **Red Lid Admin** updates the run schedule for holidays.
   - **Approved Red Lid Admin**: "The holiday schedule adjustments are now approved."
     - **Approved Red Lid Admin** confirms the holiday schedule in the system.
   - **Driver**: "I will execute the adjusted pickups for the holiday season."
     - **Driver** performs pickups according to the new holiday schedule.

7. **New Route Implementation:**
   - **Red Lid Admin**: "I have drafted a new pickup route to improve efficiency."
   - **Approved Red Lid Admin**: "The new route has been reviewed and approved."
     - **Approved Red Lid Admin** approves the new route.
   - **Driver**: "I will implement the new route in my daily pickups."
     - **Driver** follows the new route.
   - **Red Lid Admin**: "I will monitor the performance of the new route and gather feedback."
     - **Red Lid Admin** tracks and assesses route performance.

8. **Customer Requests Multiple Bin Pickup:**
   - **Customer**: "I need pickups for multiple bins due to a large volume of waste."
   - **Red Lid Admin**: "I have adjusted the schedule to accommodate your request."
     - **Red Lid Admin** updates the schedule to include multiple bin pickups.
   - **Driver**: "I received the updated schedule and will plan for multiple bin pickups."
     - **Driver** prepares for multiple bin pickups.
   - **Approved Red Lid Admin**: "I will verify that the multiple bin pickups were completed successfully."
     - **Approved Red Lid Admin** confirms completion of pickups.

9. **Driver Performance Review and Feedback:**
   - **Red Lid Admin**: "I am conducting a quarterly review of driver performance."
     - **Red Lid Admin** generates performance reports.
   - **Approved Red Lid Admin**: "I have reviewed the performance reports and provided feedback."
     - **Approved Red Lid Admin** reviews and shares feedback.
   - **Driver**: "I received feedback and will work on areas for improvement."
     - **Driver** implements the feedback.
   - **Red Lid Admin**: "We will provide any necessary training or support based on the feedback."
     - **Red Lid Admin** organizes training or support.

10. **Special Event Recycling:**
    - **Customer**: "We are organizing a community event and need recycling services."
    - **Red Lid Admin**: "I will schedule a special run for your event."
      - **Red Lid Admin** records the event run in the schedule.
    - **Approved Red Lid Admin**: "The event recycling schedule has been reviewed and approved."
      - **Approved Red Lid Admin** validates the event run.
    - **Driver**: "I will complete the pickups for your community event as scheduled."
      - **Driver** carries out the event pickups.

11. **Addressing Customer Complaints:**
    - **Customer**: "My recycling pickup was missed."
    - **Red Lid Admin**: "I will investigate and schedule a follow-up pickup."
      - **Red Lid Admin** investigates and schedules a follow-up run.
    - **Approved Red Lid Admin**: "I have reviewed the resolution process."
      - **Approved Red Lid Admin** validates the resolution process.
    - **Driver**: "I will complete the follow-up pickup and ensure customer satisfaction."
      - **Driver** performs the follow-up pickup.

12. **Introduction of New Recycling Program:**
    - **Customer**: "I am interested in the new recycling program."
    - **Red Lid Admin**: "I will enroll you in the new program and adjust your pickups accordingly."
      - **Red Lid Admin** updates the customer profile with the new program.
    - **Approved Red Lid Admin**: "The new program rollout has been reviewed and approved."
      - **Approved Red Lid Admin** confirms the new program.
    - **Driver**: "I will follow the new program guidelines during pickups."
      - **Driver** executes pickups per the new guidelines.

13. **Handling Overlapping Runs:**
    - **Red Lid Admin**: "I have identified overlapping runs in the schedule."
      - **Red Lid Admin** proposes adjustments to resolve overlaps.
    - **Approved Red Lid Admin**: "The necessary adjustments to eliminate overlap have been approved."
      - **Approved Red Lid Admin** approves the adjustments.
    - **Red Lid Admin**: "The run schedules have been updated."
      - **Red Lid Admin** updates the system with new schedules.
    - **Driver**: "I received the revised schedule and adjusted my routes."
      - **Driver** adjusts routes according to new schedules.

14. **Customer Requests Electronic Invoice:**
    - **Customer**: "I would like to receive my invoices electronically."
    - **Red Lid Admin**: "Your billing preferences have been updated for electronic invoices."
      - **Red Lid Admin** updates billing preferences in the system.
    - **Approved Red Lid Admin**: "The changes to your billing preferences have been approved."
      - **Approved Red Lid Admin** confirms the update.
    - **Customer**: "I will now receive my invoices via email."
      - **Customer** begins receiving emailed invoices.

15. **Implementing Driver Shift Changes:**
    - **Driver**: "I need to change my shift schedule."
    - **Red Lid Admin**: "I will propose shift changes to accommodate your request."
      - **Red Lid Admin** adjusts the shift schedule in the system.
    - **Approved Red Lid Admin**: "The shift changes have been reviewed and approved."
      - **Approved Red Lid Admin** validates the new shifts.
    - **Driver**: "I will follow my new shift schedule as approved."
      - **Driver** adheres to the new schedule.

16. **Driver Overload Management:**
    - **Driver**: "My run is overloaded."
    - **Red Lid Admin**: "I will review and adjust the run distribution."
      - **Red Lid Admin** redistributes runs to manage the load.
    - **Approved Red Lid Admin**: "The redistribution of runs has been approved."
      - **Approved Red Lid Admin** approves the adjustments.
    - **Driver**: "I received the adjusted run schedule to balance the workload."
      - **Driver** follows the new balanced schedule.

17. **New Sector Introduction:**
    - **Red Lid Admin**: "I propose the creation of a new sector to enhance service coverage."
      - **Red Lid Admin** drafts the new sector plan.
    - **Approved Red Lid Admin**: "The new sector has been reviewed and approved."
      - **Approved Red Lid Admin** validates the new sector.
    - **Red Lid Admin**: "Customer locations and runs have been assigned to the new sector."
      - **Red Lid Admin** updates assignments.
    - **Driver**: "I updated my routes to include the new sector."
      - **Driver** adjusts routes accordingly.

18. **Customer Enrollment in Recycling Program:**
    - **Customer**: "I am interested in enrolling in the new recycling program."
    - **Red Lid Admin**: "You have been enrolled in the program and your pickups adjusted."
      - **Red Lid Admin** updates enrollment and pickup schedule.
    - **Approved Red Lid Admin**: "The enrollment and billing adjustments have been verified."
      - **Approved Red Lid Admin** confirms execution.
    - **Driver**: "I will follow the updated pickup schedule reflecting the new program."
      - **Driver** performs pickups according to the updated schedule.

19. **Implementation of a Pilot Program:**
    - **Red Lid Admin**: "We are introducing a pilot recycling program in a small sector."
      - **Red Lid Admin** designs the pilot program.
    - **Approved Red Lid Admin**: "The pilot program has been reviewed and approved."
      - **Approved Red Lid Admin** validates the pilot program.
    - **Driver**: "I received training and instructions for the pilot program."
      - **Driver** undergoes training.
    - **Red Lid Admin**: "We will monitor the pilot program’s progress and gather feedback."
      - **Red Lid Admin** collects feedback and monitors performance.

20. **Waste Sorting Initiative:**
    - **Customer**: "I need more information on how to sort recyclables."
    - **Red Lid Admin**: "Here are the materials and guidelines for waste sorting."
      - **Red Lid Admin** sends the customer an email with materials and guidelines for waste sorting.
    - **Approved Red Lid Admin**: "Distribution of sorting guidelines has been overseen."
      - **Approved Red Lid Admin** confirms distribution.
    - **Driver**: "I will provide feedback on sorting during my pickups."
      - **Driver** offers feedback on waste sorting.

