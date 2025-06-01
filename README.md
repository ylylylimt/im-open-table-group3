# im-open-table-group3
Finding restaurants nearby(OpenTable) - Panagiotis - Group 3 Project Group

This repository contains the formal models (transition systems and Petri nets) for the “Open Table” restaurant‐reservation project. You will find both customer‐side and staff‐side draw.io files, as well as PNML files.

## Repository Structure & Contents
- *README.md*  
  This file. Provides an overview of the repository’s contents and how everything is organized.

- *Transition Diagram for Customer (User)*  
  The transition system diagram for the *customer (user) side* of the reservation process. It shows each user‐action (select restaurant, choose table, make reservation, payment success/failure, modify/cancel, etc.) as a box, with arrows indicating possible state changes.

- *Transition Diagram for Restaurant (Stuff)*  
  The transition system diagram for the *restaurant (staff) side* of the process. It includes steps such as receiving reservation requests, checking availability, notifying the customer, handling cancellations, and managing the waiting list.

- *restaurant.pnml*  
  A PNML‐formatted Petri net representing the *restaurant‐side* model. This file encodes all places (e.g. Idle, RequestReceived, TablesAvailable, OnWaitingList, etc.) and transitions (e.g. receive_request, check_availability, add_on_waiting_list, etc.) of our project. You can import this into https://pes.vsb.cz/ PNML‐compatible tool to simulate, and analyze invariants or reachability.

- *user.pnml*  
  A PNML‐formatted Petri net representing the *customer‐side* model. It defines places such as Idle, RestaurantSelected, ReservationSubmitted, PaymentFailed, ReservationConfirmed, etc., and transitions like select_restaurant, make_reservation, retry_payment, and cancel_reservation. Load it into a PNML viewer to generate the reachability graph and verify properties (boundedness, liveness, reversibility).

## How to Use

1. *Load the PNML Files*  
   - In a PNML‐capable tool (https://pes.vsb.cz/), import restaurant.pnml or user.pnml.  
   - You can then visualize the net, simulate token flows using Simultaion Mode.
   - You can perform property analysis (boundedness, liveness, deadlock freedom, etc.) using Analysis.
