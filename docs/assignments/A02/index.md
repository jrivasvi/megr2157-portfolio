# A2 – Truss Stress Analysis


I was given the task of creating a truss that could withstand an external load. A truss is a structure comprised of members connected by joints creating triangles to support many architectural structures like bridges, towers, houses, and roofs.   

<img width="317" height="215" alt="image" src="https://github.com/user-attachments/assets/3bad65ff-365d-45c9-906d-1dc71e89b553" />

This is the initial image I was given. P could be any value from 20 kN to 30 kN. a = .4 m, b = .3 m. Point A is a pin and point B is a roller.

## Initial Thoughts and Setup
<img width="1280" height="835" alt="image" src="https://github.com/user-attachments/assets/59ed76a9-b7d5-4e01-8cbe-15472e062620" />

My initial thoughts were to keep the truss as simple as possible in order to minimize difficulties later on down the line. At first I made a trapezoid that connected all the joints, but I quickly realized that there was no way that structure would hold any type of load. The formula m=2j-3 also confirmed that I would need an extra member for the truss to work. This formula expresses the number of members necessary(m) for a certain number of joints(j). I decided to add a member connecting C and A that would create more triangular patterns and thus be able to carry more load. I also solved for the external forces at the support points. I chose a load of 20kN in order to keep the number even and somewhat small. 


## Internal Forces
<img width="817" height="1024" alt="image" src="https://github.com/user-attachments/assets/8a9ffda3-3f48-4ec8-ab08-9e33ff46d84a" />

I used method of joints to calculate all the individual forces within the members. Some important angles were the angle at B which was 36.87 degrees and the upper angle at A which was 20.56 degrees. 

As you can on the image and below the strongest internal force was the tension in member AD

BA	8.89 kN	(Compression)	

BC	11.11 kN	(Tension)	

CD	26.67 kN	(Tension)

DA	33.33 kN	(Tension)

CA	18.98 kN	(Compression)


## Sizing Truss Elements
<img width="910" height="1024" alt="image" src="https://github.com/user-attachments/assets/92bfef07-80b1-40be-aaa4-1f0e0f165007" />

Like I said previously the largest internal force is 33.33 kN in member AD. The factor of safety is 3.5, and the yield strength is 290 MPa according to https://www.metalsusa.com/a500-grade-steel/ Using all these values I calculated the necessary cross sectional area for the truss members. The total weight using the density of steel according to https://niftyalloys.com/blogs/density-of-steel is 10.9 kg.


## Sizing Pin 
<img width="1024" height="871" alt="image" src="https://github.com/user-attachments/assets/28cf01f5-ed17-4882-9397-c3279b2b6985" />

The given values were yield shear strength of 170 ksi, a density of 0.278 lb/in^3, factor of safety of 4, and single shear connection type. The goal of this step was to calculate the cross sectional area. All pins are the same size and therefore have the same cross sectional area. 

## CAD vs Hand Calculations
<img width="959" height="539" alt="Screenshot 2026-09-03 031857" src="https://github.com/user-attachments/assets/9a8899dc-ce71-4870-921c-d945077f6657" />

This is a overhead view of the truss and the measurements came out the same as the hand calculations. I had some difficulties with the pins, and I realized that I need to brush up on my solid works proficiency. The cross sections all remained the same and equivalent to one another.


## Truss Member Failure

The members in tension(BC,CD,DA) will all fail due to yielding since they will continue to get stretched and eventually reach failure where they snap. A500 steel is ductile meaning that it is less hard and more flexible. An example of a very hard but brittle material would be glass since it is hard to scratch but easy to break. With this in mind A500 steel is the opposite it stretches and deforms but is easier to scratch. All the members having the same cross sectional area is less efficient because the whole structure is limited by whichever member is experiencing the greatest amount of stress. It also distributes reinforcement to areas where it isn't needed while neglecting the areas in need. A fix for this would be to add another member that would split the load.

sources: https://engineeringlibrary.org/reference/trusses-air-force-stress-manual 
https://study.madeeasy.in/ce/design-of-steel-structures/types-of-failure

The members in compression(AB and CA) would fail due to buckling in the real world, but the instructions say "assume elements in compression won't fail in buckling" so they would likely fail due to crushing even though A500 steel is ductile. A fix for this would be to use hollow members instead because they provide a resistance to buckling. 


## Pin Failure

The pins would fail due to shear yielding which is supported by the equation τ = F/A_pin. The material of the pins are also different than that in the truss members. The pins are made of hardened tool steel which is more brittle than A500 steel also meaning that it's harder. This also means that there is less deformation than what you would see with A500 steel. A fix for this would be to utilize a double shear connection since this divides the shear stress in two. 

## Lessons

I learned a lot such as that a lot of thinking goes into even the smallest details of a structure, and that's not even considering the ones that were excluded. I also need to brush up on my CAD skills, and spread my work time better throughout the week. This project took me 7 hours to complete. 









