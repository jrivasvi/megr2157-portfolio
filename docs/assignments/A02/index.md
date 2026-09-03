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




