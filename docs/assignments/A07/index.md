# A7 – FEA on Bracket

## The Setup
The goal of this week's project was to use FEA on the bracket we have been working on in order to see how it would work in a real life application, and make the appropriate adjustments to optimize it. The force is a distributed load pointing down across the face of the cylinder. The force in my project came out to 1000lbs force. I constrained all the inner faces of the T slot which came out to be 5 total faces. The material I used was aluminum 6061 which has a yield strength of 39885.378 psi according to fusion. I also used fusion's factor of safety range which is 2-4. The values I used for the element sizes were 10% for the coarse mesh, 5% for the medium mesh, and 1% for the fine mesh. Below is a chart of the extreme values in all the designs, and each individual mesh result will be discussed later.

<img width="1729" height="546" alt="image" src="https://github.com/user-attachments/assets/00cf6292-f672-465d-b8ed-6e4552bdc961" />



## Design 1
<img width="1568" height="709" alt="image" src="https://github.com/user-attachments/assets/6b7da522-6ac2-4d65-9a63-86689a62fce3" />


<img width="1568" height="707" alt="image" src="https://github.com/user-attachments/assets/c8ee5f07-805d-4cb4-9815-dd3e7ae3cdbf" />


<img width="1568" height="701" alt="image" src="https://github.com/user-attachments/assets/68b210d4-1517-48e9-bd16-a248ae25fa40" />

These three images show the fine mesh results of the original design(design 1). Displacement converged but stress did not. Stress increased per mesh adjustment which is most likely due to the stress concentration that occurs at sharp corners. The greatest stress location was where the arm and the cylinder intersected towards the bottom and top. The most displacement occurred at the free end opposite of the arm. None of the mesh results converged within 7% of another.


Design 1 Coarse Mesh:

Safety Factor- 0.051 

Max Deflection- 1.785 in

Max Stress- 784,021 psi

Mass- 43.652 oz

Elements- 2307 



Design 1 Medium Mesh:

Safety Factor- 0.038

Max Deflection- 1.811 in

Max Stress- 1.037*10^6 psi

Mass- 43.652 oz

Elements- 5812 



Design 1 Fine Mesh:

Safety Factor- 0.03

Max Deflection- 1.877 in

Max Stress- 1.334*10^6 psi

Mass- 43.652 oz

Elements- 487307 

## Design 2
<img width="1568" height="710" alt="image" src="https://github.com/user-attachments/assets/5331c8bd-2a1b-4a7c-9e28-b94ad6edfafb" />

<img width="1568" height="705" alt="image" src="https://github.com/user-attachments/assets/fc2e2040-374e-4b62-8508-8a18cfa1887c" />

<img width="1568" height="705" alt="image" src="https://github.com/user-attachments/assets/70af36c2-67b4-45fd-aa03-8887006a7659" />

These are the results of the medium mesh, since it converged with the coarse mesh results within 7%, there was no need to check the fine mesh results. My takeaway from the previous design was that the arm wasn't completely centered with respect to the center of the cylinder, so that was the adjustment I made going into design 2. Looking back at it this didn't change much but the effects did seem significant at the time especially since the values converged. The max stress was on the arm this time and not the contact point. The max deflection was once again at the free end of the cylinder. The hand calculation for the arms bending stress using the 1000lbf, 2.7in, and the 0.338 square section gives a value of about 420,000 psi which closely matches the 440,000 psi the FEA gave.


Design 2 Coarse Mesh:

Safety Factor- 0.091 

Max Deflection- 1.694 in

Max Stress- 436,089 psi

Mass- 43.652 oz

Elements- 2307 



Design 2 Medium Mesh:

Safety Factor- 0.091

Max Deflection- 1.739 in

Max Stress- 440,432 psi

Mass- 43.652 oz

Elements- 5812 



## Design 3
<img width="1568" height="706" alt="image" src="https://github.com/user-attachments/assets/e1999860-fefb-4ebf-a62d-678131578608" />

<img width="1568" height="706" alt="image" src="https://github.com/user-attachments/assets/e7d113e8-623a-48ae-9858-cb6847335a06" />

<img width="1568" height="704" alt="image" src="https://github.com/user-attachments/assets/6f5381f0-349f-482e-a354-a3e153d93091" />

These are the fine results of design 3. My thoughts going into this one were to increase the contact distance between the arm and the cylinder. Initially it was 0.338 in but I tripled it and ended with 1.014 in. The max stress issue in design one reappeared and it was once again at the contact points between the arm and the cylinder. The max deflection was still at the free end of the cylinder. This small adjust made stress decrease by 2.9 times, and the arm's stiffness improved because deflection decreased by 2.8 times. The updated hand estimate was about 140,000 psi which is in the range of the three mesh results. The mesh results did not converge within 7%




Design 3 Coarse Mesh:

Safety Factor- 0.286 

Max Deflection- 0.592 in

Max Stress- 139,282 psi

Mass- 45.681 oz

Elements- 2976 



Design 3 Medium Mesh:

Safety Factor- 0.266

Max Deflection- 0.621 in

Max Stress- 149,895 psi

Mass- 45.681 oz

Elements- 6105 



Design 3 Fine Mesh:

Safety Factor- 0.185

Max Deflection- 0.649 in

Max Stress- 215,317 psi

Mass- 45.681 oz

Elements- 520691


## Design 4
<img width="1568" height="702" alt="image" src="https://github.com/user-attachments/assets/60ce5160-96ef-4fae-89b3-97f640c6a386" />

<img width="1568" height="709" alt="image" src="https://github.com/user-attachments/assets/b8099dbe-6743-43e3-9c6a-69c6d57f9af2" />

<img width="1568" height="702" alt="image" src="https://github.com/user-attachments/assets/f9cf0cfb-3e56-4aa2-89e9-df6fc9bb142f" />

These images are the fine mesh results of design 4. The last touches I needed to complete were to reach the safety factor interval between 2-4. The best way I could get this to be achieved was to increase the volume of the arm by extending the face to be closer to the free end of the cylinder. The initial length was 0.338 in but after the extension it became 1.338 in. I also added a 0.1 in fillet at all the contact edges between the arm and the cylinder. The max stress of this design was the outer edge of the arm's base. Once again the max displacement took place at the free end of the cylinder. The medium and fine mesh results did converge within 7%



Design 4 Coarse Mesh:

Safety Factor- 2.018 

Max Deflection- 0.011 in

Max Stress- 19,766 psi

Mass- 47.318 oz

Elements- 4903 



Design 4 Medium Mesh:

Safety Factor- 2.372

Max Deflection- 0.011 in

Max Stress- 16,817 psi

Mass- 47.318 oz

Elements- 10,054 



Design 4 Fine Mesh:

Safety Factor- 2.263

Max Deflection- 0.011 in

Max Stress- 17,627 psi

Mass- 47.318 oz

Elements- 635,686


## Reflections/Mistakes

This project taught me that even the smallest adjustments can have a large impact on the overall functionality of the part. I also learned the importance of mesh size and the extra work that is required with smaller sizes. I'm getting more familiar with the applications of FEA and CAD in general. I spent a total of 5.5-6 hours on this project, and it definitely could've been less if not for the solve times with the lower element sizes. A very noticeable mistake was that the arm wasn't completely centered with respect to the center of the circle and this cause unnecessary stress in design 1. I also had the three parts of the bracket as individual bodies instead of one combined figure. My initial calculations in assignment 5 used the widely accepted value of 35,000 psi for yield, but fusion uses a higher value of 39,885 psi. Changing the geometry of the design had a different effect depending which axis it changed about. In design 2 I moved a part and that did help but, not much compared to design 3 and 4. In design 3 and 4 more material was added in two different directions. In design 3 I added more material to the outside of the original arm which cut stress by almost 3 times, and same for deflection. Increasing its depth into the cylinder(design 4) lowered the stress from an already much lower value 215,317 psi , compared to design 2, to 17,627 psi. This taught me a valuable identity that bending resistance grows with the square of the depth. The ratio of increase in mass to increase in safety factor was also very noticeable because the mass only increased from 43.652 oz to 47.318 oz, while the safety factor increased from 0.03 to 2.26. If I were to do more optimization to this I would remove some material from the cylinder.

## CAD Link
https://a360.co/4i7CbmV




