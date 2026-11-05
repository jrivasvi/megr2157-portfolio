# A9 – Pulleys

## Initial Setup
This week were tasked with creating a pulley system that underwent differing loads and situations. The certain parameters I chose were a center distance of 5 inches, pulley diameter of 3 inches, friction coefficient of 0.3(comes from polyurethane on aluminum,  rotational speed of 1500 rpm which simplifies to 157.1 radians/sec, belt tension(static) of 5 lbf, a theta value of pi which means that the pulleys are equal and on the same plane,  and a safety factor of 3.

## Belt
The belt is made of polyurethane rubber, and has a yield strength of 3.25 MPa(471 psi) according to the assignment page. I used the same given values and decided values I previously discussed. The goal of this step was to find the tension of the tight side, the tension of the loose side, belt diameter, and the belt length. I assumed that the belt was elastic so the total tension would remain constant. I also assumed no slip which is how I got the T_1/T_2 = e^(mu*theta). I decided on a belt diameter of 1/4 inch since it was the next standard size from 0.242 inches. I selected an outer circumference of 20 in because the calculation came out to be 21 but I wanted there to be some type of stretch, so I went down to the next standard value. With both of these dimensions I landed on 3044K606 round belt on McMaster-Carr.
<img width="720" height="633" alt="image" src="https://github.com/user-attachments/assets/bb36b6ed-3ed5-4b63-85b6-88f7a09db79e" />


## Shaft
I made a conservative assumption of 60 ksi for the yield strength since I couldn't find it in the textbook so I checked Fusion and this was the value I got. The pulley was centered between bearings leaving 1.5 on each side. The load acts at the midpoint therefore splitting it between the bearings. The assignment only accounts for torque in the calculation but I accounted for bending, torsion, and von Mises. This combination increased the minimum diameter and to account for error I chose a diameter of 1/4 in. 
<img width="926" height="633" alt="image" src="https://github.com/user-attachments/assets/3d8c32ac-984d-4db9-9196-ddf884db8dae" />



## Journal Bearing
The journal bearing was in need of a length, pressure(P), velocity(V), and PV. The journal bearing are loaded by 5 lbf each but are offset by the reaction force(N). With all these parameters in mind I decided on oil-impregnated sintered bronze, which is well beyond all limiting values I calculated. The image depicts the end view on the left and the side view on the right.
<img width="815" height="633" alt="image" src="https://github.com/user-attachments/assets/6fa505e9-7004-4869-94fc-5d0c075f757b" />



## Frame
I assumed that the belt pulls the two shafts together, so each shaft pushes inward on the frame leaving it in compression. I calculated the stress on the inner frame walls at the holes, and calculated the necessary force to make it buckle. With both of these in mind I decided to make the frame out of aluminum in order to make sure that there were no complications.
<img width="1122" height="632" alt="image" src="https://github.com/user-attachments/assets/3ee93768-d1b9-4ecb-b110-419639cca731" />


## Lessons Learned
I spent approximately 2.5 hours on this project. I learned that the torsional force a belt can carry is relative to the proportion between the tight side and the looser side. I also learned that just cause you get a final value from a calculation you have to think about how to apply it appropriately, such as when the outer circumference of the belt was 21 inches but I chose a more realistic value of 20 inches allowing the belt to stretch. I learned about the direction of force/torque for a pulley system because I assumed previously that they would go away from each other, but in reality they go towards each other and leave the system in compression.
