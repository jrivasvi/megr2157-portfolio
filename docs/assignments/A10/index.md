# A10 – Lead Screw Design Part 1

## Objective- Joel Rivas
This week were tasked with the initial setup for a 2 part project. We had to choose a lead screw using the diameter, rotational speed, and max torque. We also had to choose a nut and flange making sure they supported the load. Lastly, we had to design a crosshead with a max deflection of .1mm. The key constraints for this week were: no electronics, load capacity of 2kN split between the two lead screws, linear speed range of 1-50 mm/min, and a safety factor of 4. 

## Leadscrew Diameter- Joel Rivas
This first step was to calculate the minimum leadscrew diameter. I chose a low carbon steel because it is definitely strong enough, inexpensive, and works well with the bronze nut. McMaster didn't have the exact yield strength so I used the lower bound I found from an online steel properties table( https://us.misumi-ec.com/blog/yield-strength-stress-chart/ ), and this gave me a yield strength of 210 MPa. Using this value I was able to calculate the minimum diameter to be 4.92 mm or 0.194 in. The standard 1/2 in -10 ACME screw has a minor diameter of 10.2 mm which is more than enough according to my hand calculations, but McMaster didn't have an 8mm screw so the safest choice was to settle on the 1/2 in diameter screw. The length of 3 ft is greater than the minimum 18 in required while also making sure to leave space for the nut, thrust bearing, and crosshead. 


<img width="1024" height="758" alt="image" src="https://github.com/user-attachments/assets/fd46322f-af75-4e65-9d99-e94e5a2405e4" />


## Leadscrew Rotational Speed- Joel Rivas
The second step was to calculate the range of rotational speed the lead screw could handle. The knowns for this part were the linear speed range of 1-50 mm/min, pitch of 0.1 in = 2.54 mm, and lead of 0.1in/rev= 2.54 mm/rev. The pitch and lead are the same in this example. The driving formula for this step was V=N*L which I rearranged to be N=V/L in order to be able to get the rotational speed from the lower and upper end of the linear speed range. The final range of rotational speed came out to be 0.39- 19.7 RPM. The bottom range is really slow and would require a gear reduction if it was ran. 

<img width="1024" height="786" alt="image" src="https://github.com/user-attachments/assets/17364e1f-e64d-4bc5-b80c-14fdfc473a10" />


## Leadscrew Torque- Joel Rivas
The final calculation for the leadscrew was the max torque to provide the 2kN tension. The knowns for this part were: load per screw (P)=1000 N, Diameter(d)= 12.7 mm, Pitch(p)/Lead(L)= 2.54mm, Pitch diameter (d_m)= 11.43mm, Friction Coefficient(mu)= 0.15, C= 39.898 mm(using pitch diameter). We had to find the effort force in order to find the max torque per screw. We used the power screw formulas we derived in class which were F=P*((mu*C+L)/(C-mu*L)) and T=F*r. In this part the radius we used was half of the pitch diameter. The first free body diagram is the unwrapped thread as an inclined plane, and the second is the more real world depiction showing the load acting down the screw and the torque being applied at the top. The torque came out to 1.23 N*m. There is also another formula in the handbook which says T_d=(P*L)/(2pi*e) where e is the ball screw efficiency. Plugging in our values gets a max torque of 1.01 N*m which isn't too far from the calculated value we had previously, but it also uses a lower friction coefficient which explains why the value is lower. This value helped confirm that the torque calculation was done correctly.  

<img width="1024" height="794" alt="image" src="https://github.com/user-attachments/assets/bbff224d-5d84-4b2e-b1f9-d7a0c11918fa" />


## Leadscrew Selection- Joel Rivas
The leadscrew we selected is a 1/2 in-10 ACME low carbon steel screw, 3 ft long (McMaster 98935A823). Its minor diameter of ~10mm is around double the minimum diameter of 4.92 mm to carry 1kN per screw with a safety factor of 4. The thread is self-locking, so that will aid holding the crosshead in position while under load. 

<img width="1262" height="455" alt="image" src="https://github.com/user-attachments/assets/baae3b09-a594-4989-bf45-402351298b2e" />



## Nut and Flange Calculations - Drew Wayne
For the nut flange, I first listed the knowns and unknowns. I then drew an FBD to show how the load acts on the nut and screw. After that, I used the equations for bearing stress and thread bending stress and plugged in my values to calculate 14.85 MPa for the bearing stress and 44.56 MPa for the thread bending stress. I ended up choosing a bronze acme flange nut with a thread size of 1/2" - 10 so that it works with our lead screw we chose previously.
![My Image](IMG_1405.jpeg)
![My Image](IMG_1399.jpeg)
## Crosshead Design - Drew Wayne
For the crosshead design, I first listed my knowns and unknowns. The material that I ended up choosing was 6061-T6 aluminum. I then drew a FBD to show the applied load and reaction forces on both ends. I then used the bending moment and section modulus equations to determine the required dimensions. Using my calculated values, I found a maximum bending moment of 400 N * m and a required section modulus of 1.45 x 10^-6 m^3 and a beam height of approximately 17mm. 
![My Image](IMG_1406.jpeg)

For the crosshead deflection, I used the same load, material, and dimensions from my previous calculations to make sure the beam would not deflect more than 0.1mm. I first drew a FBD showing the applied load and reaction forces. I then used the deflection equation to solve for the required moment of inertia, which came out to be 4,83 x 10^-8 m^4. From there, I calculated a minimum beam height of 26.8mm and decided to use final dimensions of 200mm long, 30mm wide, and 40mm high to keep the deflection within the required limit.
![My Image](IMG_1407.jpeg)

For this part, I created a multi-view paper sketch of my crosshead to show how the design would look from the top, side, and front views. I included the main dimensions, such as the overall length of 240mm, the spacing between the holes of 200mm, and the different hole diameters. I also sketched the side and front views to show the height, width, and placement of the different features. This helped me get a better idea of how we need our crosshead to look before modeling it in SolidWorks.
![My Image](IMG_1408.jpeg)



## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Lessons Learned-Joel Rivas
We learned to choose the real/tangible part first, and then take dimensions from that specific part because in the lead screw selection we originally worked out the values for an unavailable screw, and then had to adjust. Tracking units properly is also very important because we almost made a mistake with the torque calculation not converting mm to m. We also learned how to work with a team more effectively, and allowing people to play into their strengths. Communication was paramount in order to get this done to the best of our ability, and to check over one another's work in order to correct any unrecognized mistakes.

