# Analysis and Management of Production Systems
# Lesson 01: Formalisms for manufacturing process modeling

---

## Slide n.01 → Title: Analysis and Management of Production System

**Content:**
Course: Analysis and Management of Production System
Lesson 01: Formalisms for manufacturing process modeling
Lecturer: Prof. Giulia Bruno
Department: Department of Management and Production Engineering
Contact: giulia.bruno@polito.it

---

## Slide n.02 → Title: Importance of formalism

**Content:**
- Problem of making customers/colleagues with different backgrounds to understand the process to reach the solution of a problem
- Everyone reasons and expresses concepts according to their own cultural background
  - distance of languages

---

## Slide n.03 → Title: Communication problem

**Content:**
- Metaphor of the swing
- Problem of using words to describe processes
- Importance of being able to formalize a process to have an effective communication

**Image reference:** `images_01/image03_schema.jpg`

**Image description:** 2x3 grid of cartoon-style drawings (the "swing metaphor"). Six trees each with a different swing, labelled: 1) "As proposed by the project sponsor" – swing with multiple stacked platforms; 2) "As specified in the project request" – simple swing; 3) "As designed by the senior analyst" – complex non-functional structure; 4) "As produced by the programmers" – swing with short ropes; 5) "As installed at the user's site" – swing with unstable poles; 6) "What the user wanted" – simple tyre hanging from a branch.

---

## Slide n.04 → Title: Importance of processes in production systems

**Content:**
Processes are used to manage a product during its whole Product Lifecycle:
- Plan
- Design
- Implement
- Support
- Disposal

**Image reference:** `images_01/image04_schema.jpg`

**Image description:** Circular diagram of the Product Lifecycle Management (PLM). The circle is divided into coloured segments (red, yellow, grey, orange) with the phases: "Innovate and Change (Plan)", "Develop and Validate (Define)","Produce and Deliver (Build)", "Service and Support (Assist)", "Phase out and disposal (End of Life)". At the centre the text "PLM" on a dark blue background.

---

## Slide n.05 → Title: Process definition

**Content:**
A process is characterized by a series of activities linked together to provide a certain output given a certain input.
- Representation at various levels of detail
- To represent a process, it is necessary to identify the activities of which it is composed and their sequence
  - Activities may be difficult to be identified or separated from the other related activities

**Image reference:** `images_01/image05_schema.jpg`

**Image description:** Linear diagram with three elements in horizontal sequence: the word "Input" in blue italics, an arrow, a teal rectangle labelled "Process", another arrow, and the word "Output" in blue italics. Represents the basic structure of any process.

---

## Slide n.06 → Title: Types of processes

**Content:**
- **Information processes:** functions that create, manage, process and provide information (e.g. management of a purchase order)
- **Physical processes:** processing activities of physical objects (e.g. material flows within a production system)
- **Functional processes:** functions related to the overall activity of the organization or company (e.g. production of a car, publication of a book, management of an airline)

---

## Slide n.07 → Title: Types of formalism

**Content:**
Depending on the process type, different representation formalism can be used:
- Information flows → Flow chart, UML Activity diagram, BPMN
- Material flows → Flow process chart, Value Stream Mapping
- Functional flows → IDEF0 diagrams

Many variants. The same formalism may be used to represent different process types.

---

## Slide n.08 → Title: Flow chart

**Content:**
Flow chart symbols:
- Green ellipse: Start and End
- Light orange rectangle: Activity
- Pink rhombus: Decision
- Teal parallelogram: Input/output data
- Arrow: Flow control

---

## Slide n.09 → Title: Example: Customer support service

**Content:**
Applied flow chart example for the customer support process (swimlane with three lanes: Customer, Service Desk, Technical Support).

**Image reference:** `images_01/image09_schema.jpg`

**Image description:** Swimlane flow chart with three horizontal lanes (Customer, Service Desk, Technical Support). The flow starts with the customer sending a request; the Service Desk determines the nature of the request, checks if it is a previous incident, creates a new record if necessary, and performs investigation & diagnosis. If the Service Desk cannot resolve the issue, it escalates to Technical Support. The flow ends with Resolution notification, Customer confirmation and Store rating → End.

---

## Slide n.10 → Title: UML Activity Diagram

**Content:**
UML Activity Diagram symbols:
- Filled black circle: Initial state
- Filled black circle with outer ring: End state
- Green rounded rectangle: Activity
- Pink rhombus: Decision
- Thick black bar with multiple arrows: Fork and Join
- Arrow: Flow control

---

## Slide n.11 → Title: Example: order management

**Content:**
UML Activity Diagram example for order management (swimlane: Warehouse, Customer Service, Accounting).

**Image reference:** `images_01/image11_schema.jpg`

**Image description:** UML Activity Diagram with three-column swimlane (Warehouse, Customer Service, Accounting). The flow starts with the initial node in Customer Service → Receive Order → fork: in parallel Fulfill Order (Warehouse, then 24h Shipping) and Send Bill (Customer Service, then Receive Payment in Accounting) → join → Close Order → End state.

---

## Slide n.12 → Title: Business process model and notation (BPMN)

**Content:**
Based on popular graphical flowcharts:
- Core set of notation elements
- Each core element has various subtypes

A BPMN process model is a graph consisting of four types of core elements:
- **Activity:** captures work performed in a process (rounded rectangle)
- **Event (start/end):** represents triggers and outcomes (circle)
- **Gateway:** captures forking and joining paths (rhombus)
- **Sequence flow:** represents the order of execution (arrow)

---

## Slide n.13 → Title: Example Order-to-cash

**Content:**
Applied BPMN example for the Order-to-cash process with pool and swimlanes.

**Image reference:** `images_01/image13_schema.jpg`

**Image description:** BPMN diagram with "Customer" pool at the top and vertical swimlanes for the Seller (Warehouse & Distribution - ERP System, Warehouse Staff, Sales). Flow: customer sends Purchase order → Check stock availability; if available → Confirm order → Ship goods + Emit invoice → Archive order → Order fulfilled; if not available → Reject order → Order rejected. Messages (Purchase order, Order confirmation, Shipment notice, Invoice, Order rejection) are exchanged with the customer via message flows.

---

## Slide n.14 → Title: Flow process chart

**Content:**
Many physical and manual processes consist of a sequence of simple actions, such as transport, waiting or inspection. Identifying these simple activities makes it easier to find ways to improve the process.

When to use it:
- To provide a detailed description of a physical process by representing the individual activities in sequence
- To analyze processes to identify and eliminate waste
- To represent process with few decision blocks

Uses the American Society of Mechanical Engineers (ASME) symbols.

---

## Slide n.15 → Title: ASME symbols

**Content:**
- Circle: Activity, changes physical or chemical material characteristics
- Arrow: Transport, movement of people or material (distance measures could be included)
- D-shape: Waiting, for material arrivals or machines availability
- Inverted triangle: Warehouse, for material storage
- Square: Inspection, material quality and quantity control

---

## Slide n.16 → Title: Example: Baking Cookies Factory

**Content:**
A cookie factory decides to analyze how to improve its process. In the current process the cookies are formed after introducing the dough into the mould, then they are baked in the oven, cooled on a cooling belt and inspected on an inspection line. 8.2% of the cookies do not pass the shape control and are discarded, the rest of them are packed for shipping.

---

## Slide n.17 → Title: Flow process chart (cookies example)

**Content:**
Flow process chart structure:
- The main flow follows a vertical line from the top to the bottom
- Alternative flows represented on parallel lines
- Numbers for counting the symbols of the same type
- Description at the right side of the activity

**Image reference:** `images_01/image17_schema.jpg`

**Image description:** Vertical flow process chart of the cookie production process. Top to bottom: Transport (50m) → Introduce the dough into the mould; Activity 1 → Shape the cookies; Transport 2 → Place the cookies in the oven; Waiting 13min → Bake the cookies in the oven; Transport 30m → Take the cookies to the cooling belt; Waiting 30min → Cooling of cookies; Transport 30m → Take the cookies to the inspection line; Inspection 1 → Inspection of cookies; Split: alternative flow (8.2%) → Rejection of flat cookies (transport 20m); main flow Activity 3 → Stacking for packaging; Activity 4 → Wrap the cookies; Warehouse 1 → Place the cookies in the shipping boxes.

---

## Slide n.18 → Title: Observations

**Content:**
- Analyzing the material flow, you can see that the shape quality rejection rate is very high
- A simple improvement could be to introduce an inspection immediately after the manufacture of the cookies, before baking, since the raw dough is easier to re-mix
- With a successive intervention, the mixing and molding processes can be improved to further reduce the rejection rate

---

## Slide n.19 → Title: Example: reengineering comparison

**Content:**
Comparison between Present State and Future State of a re-engineered production process using flow process charts.

**Image reference:** `images_01/image19_schema.jpg`

**Image description:** Two flow process charts side by side: "Present State" (left) with Manufacturing Cycle 349.49 Hours and Customer Order Cycle 101.31, and "Future State" (right) with Re-Engineered Process, Manufacturing Cycle 80.79 Hours and Customer Order Cycle 19.21. Both show parallel flows with ASME symbols for Sales Order, Poly Tube Box/Squeegee and 48" 2-mil Log Roll, highlighting the drastic reduction of activities in the future process.

---

## Slide n.20 → Title: Example: packaging process

**Content:**
Flow process chart example for a packaging process (recycled paper).

**Image reference:** `images_01/image20_schema.jpg`

**Image description:** Vertical two-column flow process chart for the packaging process. Left column top to bottom: Warehouse (Store of waste paper) → Transport (Convey to mixer) → Activity (Pulping and mixing) → Transport (Convey to forming machine) → Activity (Forming/Moulding) → Activity (Drying). Right column: Inspection (Inspecting & counting) → Activity (Stacking) → Activity (Packing) → Transport (Convey to warehouse) → Warehouse (Store at warehouse).

---

## Slide n.21 → Title: Example: chair assembly

**Content:**
Flow process chart example for the assembly of a chair with three parallel components (Legs, Sills, Top) that converge in the final assembly.

**Image reference:** `images_01/image21_schema.jpg`

**Image description:** Flow process chart with three parallel columns for chair assembly. Column 1 - Legs (White Maple): Saw to Rough Length → Joint Two Edges → Plane to Size → Saw to Finished Length → Check Over-All Dimensions → Sand All Over. Column 2 - Sills (Yellow Pine): same operations. Column 3 - Top (White Maple): same operations + Assemble Four Sills to Top. The three columns converge in: Assemble Legs Complete → Inspect Complete → Spray One Coat Clear Shellac → Sand Complete → Spray One Coat Lacquer → Inspect Finish. Each operation has time in minutes and a progressive number.

---

## Slide n.22 → Title: Template

**Content:**
Standard Flow Process Chart template with sections for Location, Activity, Date, Operator, Analyst, Method (Present/Proposed), Type (Worker/Material/Machine), and a Summary table with columns: Event, Present, Proposed, Savings.

**Image reference:** `images_01/image22_schema.jpg`

**Image description:** Completed Flow Process Chart template (Dorben Ad Agency, activity: Preparing Direct Mail Ads, date 1-26-98). Header summary: Operation 4, Transport 4, Delay 4, Inspection 0, Storage 2, Distance 340 ft. Main table with columns: Event Description, Symbol (with 5 ASME symbols), Time (in Minutes), Distance (in Feet), Method Recommendation. Twenty activities are listed including stock room, collating, folding, stapling, addressing and mailing.

---

## Slide n.23 → Title: Exercise: paper factory

**Content:**
The wood is partly purchased from a supplier and partly produced in the company's own forests. The wood is conveyed through an artificial channel to the covered storage area. From there, it is taken to be cut in the chipper, where the dimensions are made uniform to the standard size of 1x1/4 inch. Wood chips that are too large are returned to the previous station, and those that are too small are removed. The chips are then stored in silos.

Lignin is removed from wood chips by boiling them in caustic soda and sodium sulphide solution. Then the chips pass into a low-pressure discharge vat which physically separates the fibres. The wood fibres are then centrifuged and pressed. The pulp produced in this process is finally subjected to bleaching and then put to rest in the warehouse.

The paper is produced starting from the pulp in a dedicated machine, in which the pulp is deprived of part of its content in water and compressed in steam-heated cylinders. Then it is wrapped in large reels and stored. When delivered to the customer it is cut and rewound into smaller reels.

---

## Slide n.24 → Title: Solution (paper factory)

**Content:**
Solution of the flow process chart for the paper factory with two parallel input branches (Forest and Supplier) and continuation for paper production.

**Image reference:** `images_01/image24_schema.jpg`

**Image description:** Handwritten flow process chart of the paper factory in two parts. Left part: two input branches (FOREST with warehouse and transport; SUPPLIER with transport) converging into WOOD STORAGE AREA (warehouse) → CUTTING (activity 1, with inspection CHIP INSPECTION → split: SMALL CHIPS DISCARDED; main flow continues) → SILOS (warehouse) → BOILING (activity 2) → FIBRE SEPARATION (activity 3) → CENTRIFUGE (activity 4) → PRESSING (activity 5) → BLEACHING (activity 6). Right part (continuation): RESTING IN THE WAREHOUSE (waiting) → DRYING (activity) → COMPRESSION (activity) → WRAPPING (activity) → REEL STORAGE (warehouse) → CUTTING (activity) → REWINDING (activity) → DELIVERY TO CUSTOMER (transport).

---

## Slide n.25 → Title: Value Stream Mapping (VSM)

**Content:**
Value Stream Mapping was introduced in 1980 by Taiichi Ohno and Shigeo Shingo, as part of the Toyota Production System, through which the Japanese company has implemented a policy of reducing waste in production processes.

It is composed by a set of activities and processes necessary for the realization of a product, starting from the supplier to the delivery of the finished product.

Activities are divided in two groups: **value-added activity** and **non value-added activity**.

The VSM Objective is to identify and reduce any non-value-added activity (waste), highlighting the points of improvement of the process.

---

## Slide n.26 → Title: Introduction (VSM)

**Content:**
Value Stream Mapping is a tool that analyses the **current state** of a production process.

- Allows to **visualize in a clear and concise way** the current production situation by drawing the material and information flows in order to decrease the inventory and the production time and to eliminate the overproduction
- It allows to identify each part of the production flow to **reengineer** it
- It describes the **flow of materials/components** of a given product inside the manufacturing (or logistic) system, providing a descriptive visual representation of each phase
- It highlights the points of **material accumulation** (i.e. raw material stocks, finished products and WIP) along the production process, as well as the causes of this accumulation

---

## Slide n.27 → Title: Introduction (VSM) - Advantages

**Content:**
Advantages of using Value Stream Mapping:
- Shows the process flow as a whole, without detailing individual processes
- Allows to identify waste and the causes that determine it
- Is a common international language to talk about the production process
- Helps to define how the production flow should look like and lays the foundation for a Lean implementation plan
- Shows the link between material flows and information flows
- Is a qualitative tool that describes how the plant should operate to produce value

---

## Slide n.28 → Title: VSM Diagram

**Content:**
Complete VSM example with information flows, material flows and lead time ladder.

**Image reference:** `images_01/image28_schema.jpg`

**Image description:** Complete VSM with three zones: upper zone (Information flows) with Supplier, Production control, Customer connected by communication arrows (Weekly order, Monthly order); middle zone (Material flows) with weekly truck → warehouse (1783 pcs) → Process A (C/T=300s, C/O=60min, Uptime=80%, 2 shifts, 27000s avail.) → warehouse (1202 pcs) → Process B (C/T=45s, C/O=10min, Uptime=90%) → warehouse (733 pcs) → Process C (C/T=300s, C/O=240min, Uptime=100%) → warehouse (593 pcs) → Shipping → monthly truck; lower zone (Lead time ladder): 6 days/300sec → 4 days/45sec → 1 day/240sec → 3 days. Production lead time = 14 days, Processing time = 585 sec.

---

## Slide n.29 → Title: Formalism (VSM symbols)

**Content:**
The manufacturing process mapping is performed using a series of simple unified icons. These icons can represent both physical flows and information flows of the production planning system (e.g., an MRP system).

**Image reference:** `images_01/image29_schema.jpg`

**Image description:** Complete table of VSM symbols in two columns. Left column "Flow symbols (physical, informational, temporal)": Physical flow (thick arrow), Electronic information (lightning arrow), Manual information (simple arrow), Physical flow in/out of company (diamond), Time Line. Internal/external process symbols: Process Box (rectangle), Multiple-process Box (striped rectangle), Generic Process Box, External supplier/customer (factory silhouette), Process Box information (lined rectangle), Warehouse (triangle), Operator (circle with head), MRP process (rectangle). Right column "Process improvement symbols": Kaizen objective (star), Supermarket, Kanban post, Kanban flow, Production kanban, Withdrawal kanban, Signal kanban, FIFO lane, U-shaped production cell, Buffer warehouse, Safety stock.

---

## Slide n.30 → Title: Factory (VSM symbol)

**Content:**
It is the symbol used to represent external sources: Clients, Suppliers, Outsourced Process.

Factory + Data Box contains: shipping frequency per shift, information about the material handled, purchase lot size, average demand per time bucket. For suppliers: parts/day, tray capacity, On Time Delivery. For customers: products ordered/day, turnover, OTD. In the case of services, the concepts are similar, it remains only to identify the appropriate measurements.

**Image reference:** `images_01/image30_schema.jpg`

**Image description:** Two VSM elements: at the top the Factory symbol (factory silhouette with jagged roofline) labelled "ABC COMPANY"; below the Customer symbol (silhouette with data box) with fields: 18400 parts/month, 12000 Left side, 6400 Right side, Shelf = 20 parts, 2 shifts.

---

## Slide n.31 → Title: Production process (VSM symbol)

**Content:**
It is the symbol used to represent the production process (a machine, a process, a factory).

Process + Data box contains: Cycle Time (C/T), Setup Time (C/O), Production Rate per hour/shift, Machine downtime/uptime/waiting time, Waste and Rework, % of Value added activities.

**Image reference:** `images_01/image31_schema.jpg`

**Image description:** Two VSM elements: at the top the generic Process Box (rectangle labelled "PROCESS"); below the filled example "WELDING" with operator symbol (circle with head, n=2) and data box: C/T = 39 sec, C/O = 10 Min, Uptime = 100%, 2 Shifts, 27600 sec. of availability.

---

## Slide n.32 → Title: Inventory (VSM symbol)

**Content:**
It shows the accumulation of products between processes. It can be expressed in terms of WIP or time; in services and offices it can be understood as pending files, emails to be processed, etc. Traditionally the icon is a triangle, as it represents a significant danger in terms of waste.

**Image reference:** `images_01/image32_schema.jpg`

**Image description:** VSM Inventory symbol: triangle with the letter "I" at the centre, with label below showing quantity (300 pieces) and time (2 days). The triangle represents the accumulation of material (WIP) between two processes.

---

## Slide n.33 → Title: Safety Stock and Truck Shipment

**Content:**
**Safety Stock:** represents the presence of voluntary stocks; must always be distinguished from the involuntary accumulation of WIP generated by the production system.

**Truck Shipment:** represents the transportation adopted; internally the frequency of supplying and/or delivery is brought.

**Image reference:** `images_01/image33_schema.jpg`

**Image description:** Two VSM symbols: at the top the Safety Stock (rectangle with two internal horizontal lines, representing stacked stock); below the Truck Shipment (truck with wheels on a rectangle, labelled "1 x day") indicating the daily delivery frequency.

---

## Slide n.34 → Title: Material Flow (VSM symbols)

**Content:**
**Striped arrow:** represents the material flow between two stations; indicates a "Push" type flow.

**White arrow:** represents the movement of raw materials from suppliers or the movement of finished products towards customers.

**Image reference:** `images_01/image34_schema.jpg`

**Image description:** Two VSM material flow symbols: at the top the striped arrow (arrow with black-striped body and black tip) for push flow between stations; below the white arrow (hollow arrow with black border) for movements to/from suppliers and customers.

---

## Slide n.35 → Title: Information Flow (VSM symbols)

**Content:**
**Straight arrow:** Manual information flows (fax, e-mail, telephone, etc.)
**Lightning arrow:** Electronic information flows.
**Information Label:** specifies the type of information, shown above the information flow arrows.

**Image reference:** `images_01/image35_schema.jpg`

**Image description:** Three VSM information flow symbols: at the top the Straight arrow (thin arrow with filled tip, pointing left) for manual flows; in the middle the Lightning arrow (arrow with a zigzag break) for electronic flows; below a label rectangle "Weekly scheduling" as an example of the Information Label.

---

## Slide n.36 → Title: Operator (VSM symbol)

**Content:**
- Indicates whether a process is automated or needs operators
- Reports the number of operators required

**Image reference:** `images_01/image36_schema.jpg`

**Image description:** VSM Operator symbol: circle with an arc at the bottom representing a stylised human head. It is placed inside the Process Box to indicate the number of operators assigned to the process.

---

## Slide n.37 → Title: Timeline (VSM)

**Content:**
The Timeline shows the overall Lead Time given by the sum of the processing, handling and waiting times.
-  The low line means that the product is within the process, and it will be worked for different time (it is the time in which the product is processed on the machine)
- The high parts of the line represent the waiting times

**Image reference:** `images_01/image37_schema.jpg`

**Image description:** VSM Timeline with a stepped line: the horizontal base line represents process times (value-added), the high steps represent waiting/storage times. On the right, two summary boxes: Production Lead Time = 23.5 days and Value-Added Time = 184 sec.

---

## Slide n.38 → Title: VSM design – Step 1: Process flow identification (Data box)

**Content:**
Step 1: Identification and mapping of the main phases with data collection for the Data Box.

**Image reference:** `images_01/image38_schema.jpg`

**Image description:** First VSM design step: row of process boxes with data boxes for the Acme case (storage → stamping → welding → welding → assembly1 → assembly2 → shipping). Distances between processes: 120m, 80m, 30m, 180m, 20m, 60m. Each process box has 1 operator and a data box with: C/T, C/O, Uptime, FTY, 2 shifts. Specific data: Stamping C/T=1s, C/O=60min, Uptime=80%, FTY=0.9; Welding1 C/T=39s, C/O=10min, Uptime=90%, FTY=0.9; Welding2 C/T=46s, C/O=10min, Uptime=80%, FTY=0.85; Assembly1 C/T=62s, Uptime=95%, FTY=0.95; Assembly2 C/T=40s, Uptime=95%, FTY=0.95. Shipping warehouse with 2700L/1440R.

---

## Slide n.39 → Title: VSM design – Step 2: Material flow identification

**Content:**
Step 2: Material flow from supplier to customer.

**Image reference:** `images_01/image39_schema.jpg`

**Image description:** Second VSM step with addition of material flows: supplier (150 ft coils, deliveries Mon+Wed) and customer (18400 pcs/month, 12000L/6400R, 1 Tray=20 pieces, 480 min available per shift) connected by trucks. Between the process boxes WIP warehouses are added with quantities: 4600L/2400R after stamping, 1100L/600R after welding1, 1600L/850R after welding2, 1200L/640R after assembly1, 2700L/1440R in shipping. Push arrows (striped) connect the processes. The initial warehouse holds 1 day of coils.

---

## Slide n.40 → Title: VSM design – Step 3: Time information (Timeline)

**Content:**
Step 3: Timeline Design – Cycle Time, Waiting Time and Lead time.

**Image reference:** `images_01/image40_schema.jpg`

**Image description:** Third VSM step with the addition of the timeline at the bottom. The stepped line shows: 5 days (initial coils) / 1s (stamping) → 7.6 days / 39s (welding1) → 1.8 days / 46s (welding2) → 2.7 days / 62s (assembly1) → 2.0 days / 40s (assembly2) → 4.5 days. Summary boxes: W/T: 23.6 d (total Wait Time) and P/T: 188 s (total Processing Time = Value Added Time).

---

## Slide n.41 → Title: VSM design – Step 4: Add Information Flows

**Content:**
Step 4: Addition of information flows to the complete VSM.

**Image reference:** `images_01/image41_schema.jpg`

**Image description:** Complete VSM with information flows added: Customer sends "90/60/30 day Forecasts" and "Daily Order" to Production Planning & Control; the latter sends "6-week Forecast" + "faxback" to the Supplier and "Weekly production plan" (via MRP) to all process boxes (stamping, welding1, welding2, assembly1, assembly2); "Daily Ship Schedule" is also added for shipping. Information flows are represented by straight arrows (manual) and lightning arrows (electronic). Total: D/T: 23.6 d, P/T: 188 s.

---

## Slide n.42 → Title: Example (VSM – Acme Spa)

**Content:**
**FIRM:** Acme Spa pressed steel steering arms. The firm produces 2 types of products: L (left side) and R (right side). Each month has 20 working days, in 2 shifts of 8 hours each and two breaks of 10 minutes for each shift.

**CLIENT:** Client demand 18,400 p/month: L → 12,000 [p/month], R → 6,400 [p/month]. Shipments to customers are made 1 time per day.

---

## Slide n.43 → Title: Example (VSM – Acme Spa) – Production Control & Supplier

**Content:**
**PRODUCTION CONTROL:** MRP provides forecasts at 90, 60 and 30 days. Every day the customer provides orders. Production managed through a weekly schedule. MRP forecasts with 6-month horizon sent to supplier. Acme sends orders to the supplier weekly.

**SUPPLIER:** Supplies 500 feet long steel coils twice a week by truck. Coils allow 5 days of stock in the initial warehouse.

---

## Slide n.44 → Title: Example (VSM – Acme Spa) – Processes (Stamping & Welding 1)

**Content:**
Push flow between all production phases. 6 processes:

**Stamping:** Process time = 1 s, Setup time = 1 h, Uptime = 85%, Observed warehouse = 4600 L and 2400 R.

**Welding 1:** Process time = 38 s, Setup time = 10 m, Uptime = 100%, Observed warehouse = 1100 L and 600 R.

---

## Slide n.45 → Title: Example (VSM – Acme Spa) – Processes (Welding 2 & Assembly 1)

**Content:**
**Welding 2:** Process time = 45 s, Setup time = 10 m, Uptime = 80%, Observed warehouse = 1600 L and 850 R.

**Assembly 1:** Process time = 61 s, Setup time = 10 m, Uptime = 100%, Observed warehouse = 1200 L and 640 R.

---

## Slide n.46 → Title: Example (VSM – Acme Spa) – Processes (Assembly 2 & Shipment)

**Content:**
**Assembly 2:** Process Time = 39 s, Setup time = 0, Uptime = 100%, Observed Warehouse = 2700 L and 1440 R.

**Shipment:** After assembly the product is shipped to the customer.

---

## Slide n.47 → Title: Example - solution (Operator Availability)

**Content:**
Each month has 20 working days, 2 shifts of 8 hours each, two breaks of 10 minutes per shift.
- 1 shift: 8×60×60 = 28,800 [s/shift]
- Two breaks: 2×10×60 = 1,200 [s/shift]
- Available time: 28,800 - 1,200 = **27,600 s/shift**

---

## Slide n.48 → Title: Example - solution (Supplier & Customer icons)

**Content:**
Insert the Supplier and Customer icons, with the relative Data Boxes containing the total quantities to be supplied for a given period and calculate the necessary daily production and the load unit type/characteristics.

**Image reference:** `images_01/image48_schema.jpg`

**Image description:** First step of the Acme VSM solution: on the left the Supplier symbol "Michigan Steel Co." with data box "500 ft coils"; on the right the Customer symbol "State Street Assembly" with data box: 18,400 pcs/mo, -12,400 "L", -6,400 "R".

---

## Slide n.49 → Title: Example - solution (Process boxes & Data boxes)

**Content:**
Draw, from left to right, the Process boxes and the corresponding Data Boxes related to the internal operations/stations of the component under analysis (e.g., the production flow of the component).

**Image reference:** `images_01/image49_schema.jpg`

**Image description:** Second step: row of process boxes with data boxes for all Acme processes. From left: coils warehouse (5 days) → STAMPING (1 op, C/T=1s, C/O=1h, Uptime=85%, 27000s) → WIP 4600L/2400R → S. WELD#1 (1 op, C/T=38s, C/O=10min, Uptime=100%, 27000s) → WIP 1100L/600R → S. WELD#2 (1 op, C/T=45s, C/O=10min, Uptime=80%, 27000s) → WIP 1600L/850R → ASSEMBLY#1 (1 op, C/T=61s, C/O=Ø, Uptime=100%, 27000s) → WIP 1200L/640R → ASSEMBLY#2 (1 op, C/T=39s, C/O=Ø, Uptime=100%, 27000s) → WIP 2700L/1440R → SHIPPING (Staging).

---

## Slide n.50 → Title: Example - solution (Complete VSM with information flows)

**Content:**
Draw the icons for the external handling connections (raw material and finished products) from the warehouse to the Customer and from the Supplier. Represent the mode of transport used (e.g., Truck shipment) and indicate the frequency of shipments (daily, etc.). Draw the icons representing manual and/or electronic information and communication flow, describing the function/content with the Information icon.

**Image reference:** `images_01/image50_schema.jpg`

**Image description:** Complete Acme VSM with information flows: Customer → "90/60/30 day Forecasts" and "Daily Order" → Production Control; Production Control → "6-week Forecast" and "weekly fax" → Michigan Steel Co.; Production Control (MRP) → "Weekly Schedule" → all processes; Shipping → "Daily Ship Schedule" → Customer. Material flow: truck Tues.+Thurs. from supplier; truck 1x Daily to customer. Push arrows between all processes.

---

## Slide n.51 → Title: Example - solution (Warehouse related time)

**Content:**
Stock time = Quantity of stock pieces / daily customer demand.

Customer demand = 18,400 [pcs/month] / 20 [working days] = **920 pcs/day**

- After stamping: (4600+2400)/920 = **7.6 days**
- After welding 1: (1100+600)/920 = **1.8 days**
- After welding 2: (1600+850)/920 = **2.7 days**
- After assembly 1: (1200+640)/920 = **2 days**
- After assembly 2: (2700+1400)/920 = **4.5 days**

---

## Slide n.52 → Title: Example - solution (Final VSM with Timeline)

**Content:**
Compute the total Value Added Time and Production Lead Time.

**Image reference:** `images_01/image52_schema.jpg`

**Image description:** Final complete Acme VSM with timeline at the bottom: 5 days/1s (coils+stamping) → 7.6 days/38s (welding1) → 1.8 days/45s (welding2) → 2.6 days/61s (assembly1) → 2 days/39s (assembly2) → 4.5 days. Summary box: Production Lead Time = 23.5 days; Value-Added Time = 184 sec. The VSM shows all material flows (push), information flows (MRP, weekly schedule, daily order, forecasts) and the complete lead time ladder.

---

## Slide n.53 → Title: Exercise (VSM – TWI)

**Content:**
**FIRM:** TWI produces components for tractors, in particular steering arms. Each month has 20 working days, 2 shifts of 8 hours each, two breaks of 15 minutes per shift.

**CUSTOMER:** Demand of 24,000 pcs/month. Shipments to customers 1 time a day by trucks.

---

## Slide n.54 → Title: Exercise (VSM – TWI) – Production Control & Supplier

**Content:**
**PRODUCTION CONTROL:** Customer provides 60-day purchase forecast and precise order schedule 2 weeks before delivery. Production managed through weekly schedule via MRP. Daily delivery plan generated for shipping department.

**SUPPLIER:** Steel bars and raw joints purchased from Michigan Steel and Indiana Castings. Both deliver 2 times/month with 20 days initial stock. Bar cutting and joint trim run in parallel, then components are welded.

---

## Slide n.55 → Title: Exercise (VSM – TWI) – Process Data

**Content:**
- **Bar cutting:** 1 op, CT=15s, C/O=1h, Reliability=100%, Warehouse: 5 days
- **Finishing:** 1 op, CT=30s, C/O=2h, Reliability=100%, Warehouse: 5 days
- **1st Welding:** 1 op, CT=30s, C/O=1h, Reliability=90%, Warehouse: 3 days
- **2nd Welding:** 1 op, CT=30s, C/O=1h, Reliability=80%, Warehouse: 3 days
- **Deburring:** 1 op, CT=30s, C/O=1h, Reliability=100%, Warehouse: 5 days
- **Painting (outsourcing):** Lead-Time=2 days, Warehouse: 6 days (TWI)
- **Assembly:** 6 op, CT=195s, C/O=10min, Reliability=100%, Warehouse: 4 days
- **Shipping**

---

## Slide n.56 → Title: Solution (VSM – TWI) – Operator availability

**Content:**
Each month has 20 working days, 2 shifts of 8 hours each, two breaks of 15 minutes per shift.
- 1 shift: 8×60×60 = 28,800 [s/shift]
- Two breaks: 2×15×60 = 1,800 [s/shift]
- Available time: 28,800 - 1,800 = **27,000 s/shift**

---

## Slide n.57 → Title: Solution (VSM – TWI) – Complete VSM

**Content:**
Complete VSM of the TWI exercise with information flows, material flows and timeline.

**Image reference:** `images_01/image57_schema.jpg`

**Image description:** Complete TWI VSM. Information flows: Customer → "60 days forecasts" and "Precise orders 2 weeks delivery" → Production control (MRP); Production control → "Weekly orders" → Michigan Steel and Indiana Castings; Production control → "Weekly planning" → all processes; Production control → "Daily scheduling of shipments" → Shipping. Material flow: two suppliers (twice a month) → warehouse 20d; two parallel branches: Bar cutting (1 op, CT=15s, C/O=1h, Uptime=100%, 27000s) with WIP 5d + Finishing (1 op, CT=30s, C/O=2h) with WIP 5d → converge into 1st Welding (WIP 3d) → 2nd Welding (WIP 3d) → Deburring (WIP 5d) → Painting (external, WIP 2d) → Assembly (6 op, CT=195s, C/O=10min, WIP 4d) → Shipping → once a day. Timeline: 20d/30s → 5d/30s → 3d/30s → 3d/30s → 5d/2d/6d → 4d/195s. LT = 48d, VA = 315s.

---

## Slide n.58 → Title: IDEF diagram

**Content:**
ICAM project (Integrated Computer Aided Manufacturing):
- **IDEF0:** for the generation of functional models
- **IDEF1:** for the generation of information models
- **IDEF1X:** for the semantic modelling of data
- **IDEF2:** for the generation of dynamic models

---

## Slide n.59 → Title: IDEF0 diagrams

**Content:**
- Method designed to represent the activities of an organization or system (constraints and controls between activities)
- Based on the organic and systematic combination of graphic and textual components
- The components are related through a multilevel hierarchical structure

---

## Slide n.60 → Title: Diagram layout (IDEF0)

**Content:**
"Box and arrow" graphics. Function represented by a box whose sides enter or exit arrows with different meanings.
- **Node:** identification of the represented node (A-0 overview, A0 general activity, A1/A2/A3 first level, A11/A12/A21 second level)
- **Title** of the diagram
- **Number** of the diagram
- **Short description** of the diagram

**Image reference:** `images_01/image60_schema.jpg`

**Image description:** Generic IDEF0 schema with a single box "Activity name A0": an arrow enters from the left (Input), an arrow exits to the right (Output), an arrow enters from the top (Controls), an arrow enters from the bottom (Resources/Mechanisms). Below the box is the diagram footer with fields Node, Title, and diagram number.

---

## Slide n.61 → Title: Hierarchy of diagrams (IDEF0)

**Content:**
Hierarchical structure of IDEF0 diagrams: from level A-0 (overview) to level A0 (general activity) down to detail levels A1, A2, A3, A4 and further decompositions (A42).

**Image reference:** `images_01/image61_schema.jpg`

**Image description:** Three IDEF0 diagrams connected by dashed lines showing hierarchical decomposition: top right is the A-0 diagram with a single box "0/A0"; centre-left is the A0 diagram with 4 boxes in sequence (1, 2, 3, 4/A4) with flow arrows; bottom right is the A4 diagram that decomposes box 4/A4 into 3 boxes (1, 2/A42, 3). Dashed lines indicate which box is expanded in the lower-level diagram.

---

## Slide n.62 → Title: Activity (IDEF0)

**Content:**
The main component of the diagram is the activity: represented by a rectangle, labelled with a noun or verb, identified by a number in the lower right corner. Maximum 6 activities per diagram; if more are needed, an additional level of detail must be introduced.

---

## Slide n.63 → Title: Arrows (IDEF0)

**Content:**
The meaning of the arrows depends on their position with respect to the activity:
- **Left side (Input):** the inputs entered (what is processed during the activity)
- **Right side (Output):** the outputs produced (results of the activity)
- **Top (Control):** constraints that regulate or affect the execution of the activity
- **Bottom (Mechanism/Call):** resources (physical tools or people) that make it possible to carry out the activity

**Image reference:** `images_01/image63_schema.jpg`

**Image description:** IDEF0 schema with "Activity" box at the centre: on the left an arrow "INPUT" with label "LABEL"; on the right an arrow "OUTPUT"; at the top a downward arrow "CONTROL"; at the bottom an upward arrow "MECHANISM" and a downward arrow "CALL" with labels. The schema visually illustrates the positional meaning of the four types of arrows.

---

## Slide n.64 → Title: Parallel operations (IDEF0)

**Content:**
Once the output of activity 1 is available, both activities 2 and 3 can start simultaneously.

**Image reference:** `images_01/image64_schema.jpg`

**Image description:** IDEF0 diagram on grid paper with three boxes (Process Name 1, 2, 3). Box 1 receives an input from the left and a control from the top; its output splits towards box 2 (as control) and box 3 (as input). Box 2 and box 3 each produce an output to the right. A note explains "Once the output of 1 is available, both the activities 2 and 3 can start".

---

## Slide n.65 → Title: Difference between input and control (IDEF0)

**Content:**
- **Physical flow → input:** the material being transformed enters from the left (e.g. blank plate → Drilling → Drilled plate → Polishing → Polished plate)
- **Logical flow → control:** information that guides/regulates the activity enters from the top (e.g. Requirements → Design → Work plan; Work plan controls → Production → Finished product)

**Image reference:** `images_01/image65_schema.jpg`

**Image description:** Two IDEF0 examples side by side. Example 1 (Physical flow - input): "Blank plate" enters from the left into "Drilling A1" (mechanism: Drilling machine, control: Work cycle), produces "Drilled plate" which goes into "Polishing A2" (mechanism: Polisher), produces "Polished plate". Example 2 (Logical flow - control): "Template" enters from the left into "Design A1" (control: Requirements), produces "Work plan" which controls from the top "Production A2"; "Raw materials" enters from the left into "Production A2" (mechanism: Equipments), produces "Finished product".

---

## Slide n.66 → Title: Example: production management (IDEF0)

**Content:**
IDEF0 diagram example for production management (Node A1, Title: Production, N.: 1).

**Image reference:** `images_01/image66_schema.jpg`

**Image description:** Complete IDEF0 diagram with 5 sequential activities: A11 "Raw material inventory" (input: Current warehouse inventory + Transport document; control: Customer order; mechanism: Warehouse department) → A12 "Production planning" (input: Updated warehouse inventory; control: Customer production plan; mechanism: Planning department; output: Updated warehouse inventory + Update employee load) → A13 "Assembly" (control: Drawings/BOMs/Assembly plans/Control plans/Tuning procedure; mechanism: Production department; output: Assembly report) → A14 "Quality check" (control: Test procedure; mechanism: Quality department; output: Certificate of conformance) → A15 "Packaging and delivery" (output: Delivery note). Initial input: Current employee load. Footer: Node A1, Title, Production, N.: 1.

---

## Slide n.67 → Title: Observation (IDEF0 – no decisions)

**Content:**
In IDEF0 there are no decisions, only flows.

**Image reference:** `images_01/image67_schema.jpg`

**Image description:** Comparison between two representations of the same process. Left: flow chart with decision "Shipment OK?" (Yes/No): Receive shipment → Compare shipment with purchase order → decision diamond → [No] Return to vendor / [Yes] Catalogue book. Right: equivalent IDEF0 without decision: "Books ordered" as control from the top → "Receive each book" → two outputs: "Returned book" (right) and "Book, book information" (lower right) → "Catalogue book". In IDEF0 the decision logic is implicit in the output flow.

---

## Slide n.68 → Title: Characteristics (IDEF0)

**Content:**
- Provides a reference architecture for business analysis, information engineering and resource management
- Allows the management of large and complex projects
- The cost of a function can be computed based on the costs attributed to its component activities
- Diagrams are easy to read even by non-technical people
- Top-down decomposition, elimination of choices

---

## Slide n.69 → Title: Example: breakfast distribution

**Content:**
A breakfast is served every morning in a hospital department. Breakfast consists of liquid food (milk, tea, coffee), dry food (cookies, croissants, etc.), jams and sugar packets.Breakfast is brought to the patients using special wheeled cabinets. The preparation of the cabinets takes place in two phases: in the evening, the workers fill the cabinets with dry food, sugar and jams; in the morning, they heat the hot food using the tools in the kitchen and place them into the thermos on the cabinets.
Breakfast is distributed by the distribution staff. The cabinets are transported from the kitchen to the departments using an elevator. The staff deliver the breakfasts to the patients and then bring the cabinets back to the kitchen. In the kitchen the cabinets are washed to be ready for a new use.
Represent the process using the IDEF0 diagram using no more than two levels of detail.


---

## Slide n.70 → Title: Solution (A-0) – breakfast distribution

**Content:**
A-0 diagram (overview) of the hospital breakfast distribution process.
- PURPOSE: Hospital breakfast distribution process
- VIEWPOINT: Responsible for managing hospital meals

**Image reference:** `images_01/image70_schema.jpg`

**Image description:** IDEF0 A-0 diagram with a single box "Breakfast preparation A0": Input (left): Dry food, Liquid food, Jams, Sugar packets; Control (top): Preparation, transportation and delivery instruction; Output (right): Breakfasts served, clean cabinets; Mechanisms (bottom): Wheeled cabinets, Hospital workers, Kitchen tools, Freight elevator, Dishwasher. Footer: Node A-0, Title, Breakfast distribution process, N.: 1.

---

## Slide n.71 → Title: Solution (A0) – breakfast distribution

**Content:**
A0 diagram (first level of detail) with 3 activities: Preparation, Distribution, Washing.

**Image reference:** `images_01/image71_schema.jpg`

**Image description:** IDEF0 A0 diagram with 3 boxes in diagonal sequence: A1 "Preparation" (input: Liquid food, Dry food, Sugar packets, Jams; control: Preparation instructions; mechanisms: Wheeled cabinets, Preparation staff, Kitchen tools; output: Cabinets with breakfast) → A2 "Distribution" (control: Distribution instructions; mechanisms: Freight elevator, Distribution Staff; output: Breakfasts served + Cabinets to clean) → A3 "Washing" (control: Washing instruction; mechanisms: Dishwasher, Washing staff; output: Clean cabinets). Footer: Node A0, Title, Breakfast distribution, N.: 2.

---

## Slide n.72 → Title: Solution (A1) – breakfast distribution

**Content:**
A1 diagram (second level of detail) decomposing the Preparation phase into 2 sub-activities: Dry food arrangement (A11) and Liquid food arrangement (A12).

**Image reference:** `images_01/image72_schema.jpg`

**Image description:** IDEF0 A1 diagram with 2 boxes: A11 "Dry food arrangement" (input: Dry foods, Sugar packets, Jams; control: Preparation instructions; mechanisms: Wheeled cabinets, Preparation Staff; output: Cabinets with dry food) → A12 "Liquid food arrangement" (input: Cabinets with dry food + Liquid food; mechanisms: Kitchen tools; output: Cabinets with breakfasts). The output arrow of A11 feeds as input into A12. Footer: Node A1, Title, Preparation, N.: 2.

---

## Slide n.73 → Title: Exercise: Car repair shop (IDEF0)

**Content:**
The customer requests an offer for the production of a specific mechanical component. The formulation of the offer involves two company functions: the technical sector and the administrative sector. The technical sector provides a general description of the manufacturing process, from which the administrative sector defines the costs and define the amount of the offer. The customer evaluates the offer received and if he considers it valid, sends an 
explicit order to activates the production.
From this moment the company is formally engaged in the fulfillment of the order and starts the appropriate administrative and technical procedures. In particular, the technical sector define the process plan with the list of operations that must be performed to transform the raw material into a finished product. On the basis of the process plan, the administration arranges to order the raw materials. Production planning is also carried out from the information contained in the process plan, giving rise to the production plan.
Once the raw materials have been received and the production plan is ready, processing is carried out. At the end of the processing, a quality control of the product is carried out with which the compliance with the project specifications is established. The process ends with the invoice emission and the payment of the customer.

---

## Slide n.74 → Title: Solution (A-0) – Car repair shop

**Content:**
A-0 diagram (overview) of the mechanical workshop.

**Image reference:** `images_01/image74_schema.jpg`

**Image description:** IDEF0 A-0 diagram with a single box "Order fulfilment A0": Input (left): Raw materials; Control (top): Customer request, Customer order; Output (right): Finished product, Invoice; Mechanisms (bottom): Technical department, Administrative department, Equipments. Footer: Node A-0, Title, Mechanical shop, N.: 1.

---

## Slide n.75 → Title: Solution (A0) – Car repair shop

**Content:**
A0 diagram (first level of detail) with 2 macro-activities: Offer formulation (A1) and Production (A2).

**Image reference:** `images_01/image75_schema.jpg`

**Image description:** IDEF0 A0 diagram with 2 boxes: A1 "Offer formulation" (control: Customer request; mechanisms: Technical department, Administrative department; output: Offer) → A2 "Production" (control: Customer order; input: Offer + Raw materials; mechanisms: Technical department, Administrative department, Equipments; output: Finished product, Invoice). Dashed lines indicate that both boxes share the mechanisms. Footer: Node A0, Title, Order fulfilment, N.: 2.

---

## Slide n.76 → Title: Solution (A1) – Car repair shop

**Content:**
A1 diagram (second level) decomposing the Offer formulation phase into 3 sub-activities.

**Image reference:** `images_01/image76_schema.jpg`

**Image description:** IDEF0 A1 diagram with 3 boxes: A11 "Process definition" (control: Customer request; mechanism: Technical department; output: Process plan) → A12 "Costs definition" (input: Process plan; mechanism: Administrative department; output: Costs plan) → A13 "Offer formulation" (input: Costs plan; mechanism: Administrative department; output: Offer). Footer: Node A1, Title, Offer formulation, N.: 3.

---

## Slide n.77 → Title: Solution (A2) – Car repair shop

**Content:**
A2 diagram (second level) decomposing the Production phase into 6 sub-activities.

**Image reference:** `images_01/image77_schema.jpg`

**Image description:** IDEF0 A2 diagram with 6 sequential boxes: A21 "Process definition" (input: Offer + Customer order; mechanism: Technical department; output: Process plan) → A22 "Production planning" (input: Process plan; mechanism: Technical department; output: Production plan) → A23 "Raw materials order" (input: Process plan; mechanism: Administrative department; output: Raw materials order) → A24 "Processing" (input: Raw materials; control: Production plan; mechanisms: Technical + Administrative department + Equipments; output: Product) → A25 "Quality control" (input: Product; mechanism: Technical department; output: Finished Product) → A26 "Invoicing" (mechanism: Administrative department; output: Invoice). Footer: Node A2, Title, Production, N.: 4.
