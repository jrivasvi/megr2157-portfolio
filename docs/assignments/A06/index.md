# A6 – Bracket Drawings Part 1

This week the task was to take last week's bracket design and use parametric expressions to size it, and get a engineering drawing. 

## Parametric Design

<img width="844" height="64" alt="Screenshot 2026-09-30 232222" src="https://github.com/user-attachments/assets/550bf306-59e8-4472-8d33-301d902f6e2a" />


<img width="860" height="391" alt="Screenshot 2026-09-30 232157" src="https://github.com/user-attachments/assets/a0ba4823-e528-4fa1-9026-81eb3ab3bfc1" />


These images show all the parametric expressions I used for the bracket and all the dimensions were governed by stress calculations. Last week I inserted the values directly but this week they were automatically calculated using the parameter table. The first values I entered were the ones in the first image and then the order continues in the second picture. Parametric entries are helpful because if any input is changed then the output is automatically updated as well which isn't possible with directly inputted values. One expression that gave me difficulty was the cylinder's radius, r_cylinder= ( ( ( ( 2 * ( F_load * 2 ) * l_strap ) / ( 3.14159265 * Sigma_allow ) ) / ( 1 in^3 ) ) ^ ( 1 / 3 ) ) * 1 in, fusion struggles with values to the one third power especially because it asks for the unit before the expression is complete. I realized that I had to go around it and put inch values into the expression itself. 

## Drawing

This week the mating dimensions of the T Beam use sliding fits which is different than how they were last week, so I had to make sure to re-classify all three of the dimensions. The multiview drawing was generated from the complete model using parametric expressions. This means that all the dimensions are tied to the parameters and if any need to be adjusted it will automatically do it. The tolerance block is included breaking down the tolerances. 


<img width="2481" height="1755" alt="test drawing A6_page-0001" src="https://github.com/user-attachments/assets/0c6889d7-dc6a-4ede-ab93-51368d95af5c" />



## Reflections

I spent a total of 5 hours on this project and the hardest part was getting the accurate expressions in the parameter table since fusion has difficulty understanding units to any power besides 1. I applied a tight tolerance to the T-slot mating dimensions because this is where the strap load passes through; these dimensions ensure that there is no extra play. The block width and length had a loose tolerance since they are non-critical dimensions. A tighter tolerance in a real case scenario would lead to unnecessary machining and costs. Like I stated earlier the radius of the cylinder, r_cylinder, was driven by the strength equation. This equation sets up the model because that is the first part that I completed and effects the other parts as well. 


## 2157 Content

<img width="855" height="135" alt="image" src="https://github.com/user-attachments/assets/03c3b46b-b2d5-453f-b416-32759778b2b6" />

The expression d_hole_A= d_cylinder+0.01 in makes the link parametrically sound with respect to the bracket. Reflecting on this I realized that tolerancing is the idea that ensures that parts coincide with one another correctly and accurately. Before this week I believed dimensions to just be a number used to size things, but now I know that dimensions along with tolerances explain why a part is the size it is. Tight tolerances meant that the part is critical and a loose tolerance means that the part isn't paramount to holding a load or that it is cosmetic. 


Fusion Link: https://a360.co/4hbSYWL

