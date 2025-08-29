# Proyect Introduction 
GRAFCET project created for the pneumatic power course, where we had to select a machine, obtain its sequence, and then use this information to design the machine in Autodesk Inventor CAD software. In addition, the Automotion Studio software was used to present a complete simulation of the machine's operation, the Petri net, the simulation of the connections to the PLC, along with all the LADDER programming of the system.

# Selected Machine and its Operating Sequence
## Machine
This machine is responsible for filling 10 bottles of viscous fluid per section. The four pneumatic pistons used in the machine are marked in yellow and labeled with the letters (A, B, C, D). The bottles to be filled are also shown.
<img width="1920" height="1080" alt="A" src="assets/A.png" />

## Machine Operating Sequence
The sequence of this machine is summarized as follows: [A-B+A+C-D+D-C+B-]. <br>
The machine operates in the following order: Pistons A and C start extended, while pistons B and D start closed. Then, piston A is the first to move, closing to allow the bottles to begin positioning themselves. After this piston is closed, sensor A0 gives the signal for piston B to extend and begin accumulating the bottles to be filled. When sensor B1 indicates that it is fully extended, piston A extends again, which is responsible for ensuring that no more than the specified number of bottles (10) pass through, ensuring that the bottles are ready to be filled. When sensor a1 indicates this, piston C, which is responsible for the cleaning tray, closes to make space available for the filling nozzles. When sensor c0 indicates that it is completely closed, piston D, which is responsible for the filling nozzles, extends so that the bottles can be filled with viscous fluid. When sensor d1 indicates that it is fully extended, a 5-second countdown is performed to show that the bottles are being filled. After this time, piston D closes, indicating that the bottles have been filled, and sensor d0 gives the indication for this. The filled bottles continue their journey, and the machine prepares to start another process. 

# Machine Design in Autodesk Inventor (CAD)
The machine was created from scratch in Inventor, using the image where the sequence was built as a model. In the machine, the pneumatic pistons are blue, and the bottles to be filled are represented by orange vehicle oil bottles. The images show the motor, the cleaning tray, and the filling nozzles next to the connections to the pistons so that the movement of the machine is fully represented.
<img width="1920" height="1080" alt="A" src="assets/machine_inv_1.png" />
<img width="1920" height="1080" alt="A" src="assets/machine_inv_2.png" />
<img width="1920" height="1080" alt="A" src="assets/machine_inv_3.png" />

# machine Simulation in Automotion Studio
The simulation created in Automotion indicates all the elements that are included and necessary for the machine to operate. We will now proceed to describe everything that belongs to the system.
<img width="1920" height="1080" alt="A" src="assets/auto_1.png" />
In the image, we see the four pistons labeled (A, B, C, D), each of which is connected to a 5/2 monostable solenoid valve. In addition, there are two magnetic sensors on the piston skirt, labeled according to the piston on which they are located. These sensors indicate (1,0) depending on whether the piston is extended or closed.


# Selected Machine and its Operating Sequence