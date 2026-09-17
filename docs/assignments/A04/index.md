# A4 – Motor Mount

The goal of this assignment was to create amotor mount for a brushed 24V DC gear motor, attached to a rigid wall and subjected to a 300 N transverse load at the motor shaft. The mount could be thought of as two features, an arm used to hold the motor and the other to attach to the wall. These were both treated as cantilever beams

## Feature 1
<img width="844" height="1024" alt="image" src="https://github.com/user-attachments/assets/3c32401e-4a59-46e9-a452-45b12bef1fb9" />

Firstly I listed out all my knowns and unknowns, but the only unknown was height since I chose a width value of 28 mm. This width value made the process much easier since it gave me a value instead of another variable to consider. I treated the beam as a cantilever fixed at the corner attached to feature 2. I solved for the two height values using the stress formula and the deflection formula. I got two different values but chose the bigger of the two in order to make sure that the structure wouldn't fail due to a lack of height. The bigger value was 20.7 mm, but I also decided to give some more room for margin so the final value was 22mm. 

## Feature 2
<img width="1280" height="981" alt="image" src="https://github.com/user-attachments/assets/e43a0cd4-0f56-4621-b7bb-a53571c4be46" />

Once again I listed out all my knowns and unknowns, and height was the only unknown again. I followed the same process and the two final values were 18.8 mm and 24.3 mm. I took the larger of the two adjusting for margin and got a final value of 25mm. The free body for this feature was a little different as it included the transferred moment from feature 1. 

## Sketch
<img width="2048" height="747" alt="image" src="https://github.com/user-attachments/assets/707cfd9e-9f23-4753-989b-81d5ef65c36c" />

I combined the two separate features into one solid object and used the previously calculated values of h1 and h2. I used Appendix A to get all the hole sizes necessary. 

## CAD Model (Parametric)

I inserted all the values as parameters thus allowing me to quickly change the model if I changed a value. 

<img width="896" height="355" alt="Screenshot 2026-09-17 032301" src="https://github.com/user-attachments/assets/b15cedaa-f0eb-4ee9-9b5f-fc96086d7032" />



<img width="2550" height="1650" alt="A4 Motor Mount_page-0001" src="https://github.com/user-attachments/assets/06bbc7d6-797f-421d-b93a-9eed76a2814c" />


This is the isometric view and it shows all the dimensions of the motor mount and how they coincide with one another. 


<img width="519" height="272" alt="Screenshot 2026-09-17 031406" src="https://github.com/user-attachments/assets/37c14a09-3d4c-4056-9a53-aa4ac5a4ade6" />




CAD Link: https://a360.co/4xqWukP
