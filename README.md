# Cyber-Metro
Cyber Systems - Assignment 1

Defined Variables:

Doors (D): Can be either open or closed.
Train Movement (TM): Has the states stationary, accelerating, cruise, and decelerating.
Station Status (SS): Indicates whether the train is waiting (at a station) or in transit.
Emergency Signals:
Fire Alarm (FA): A boolean indicator that, when activated, immediately stops the train and opens the doors.
Emergency Button (EB): A boolean signal that, when pressed, triggers the process to complete the current cycle and then stop at the next station, awaiting further instructions.
System Operation Description:

Initially, the FSMD is set with the doors in the open state and the train stationary (parked and waiting for the train driver’s command). In this idle state, the system continuously monitors for both a departure command and any emergency signals, ensuring that no two conditions can be true at the same time.

Once the operator authorizes departure and if no emergency is signaled, the system transitions to the next phase: the doors are closed and the train begins to accelerate. During this accelerating phase, the metro increases its speed until it reaches a steady cruise state. In the cruise state, the train maintains a constant speed as it moves between stations.

As the train approaches its next stop, the system initiates the decelerating state by applying the brakes. This controlled braking process ensures the train slows down appropriately before arriving at the station. When the train comes to a full stop at the station, it enters a waiting state where the doors are reopened and remain open until the scheduled departure time.

After the waiting period, when departure clearance is confirmed (and assuming no emergency signals are active), the doors close again, and the sequence from acceleration to station arrival repeats.

Emergency Handling:

At any point during normal operation, if the Fire Alarm (FA) is activated, the FSMD immediately overrides any ongoing process. The train is brought to an instant stop, and the doors are opened to facilitate safe evacuation. This emergency state has the highest priority, ensuring that no other state (like accelerating or cruising) is active when FA is true.

Similarly, if the Emergency Button (EB) is pressed—typically in response to an onboard accident—the system will allow the train to continue its current operation until it safely reaches the next station. Once there, the train stops and waits for further instructions, with normal operations suspended until the emergency condition is resolved.

By defining these variables at the outset and designing mutually exclusive state transitions, the FSMD model guarantees that at any given moment, only one process condition is true. This logical sequencing and exclusive condition checking are crucial to ensuring safe and predictable control of the subway metro system.
