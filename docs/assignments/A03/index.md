# A3 – Parametric and FEA
## Objective

The goal of this project was to create and design a solid box beam given a tensile force between 300-500 lbsf, max deflection of .009 in, and an aluminum with a young's modulus between 8.5*10^6-11.5*10^6 psi. Using this information and some values I decided for myself the end goal was to find a length value that would satisfy all the conditions using parametric design. 
## Initial Steps

<img width="1280" height="709" alt="image" src="https://github.com/user-attachments/assets/617248be-bf81-45a1-9f60-7bad553dc883" />

I chose for the box to have equal side lengths of 0.2 inches, therefore giving a cross sectional area of 0.04 in^2. I settled on a middle ground value of 400lbf, and I chose 6061-T6 aluminum which has a young's modulus value of 10*10^6 psi. I also used the direct tension elongation equation to create a formula to calculate the length given all the previous values. My calculated length came out to be 9.00 inches.  

Sources: https://arcuscnc.com/6061-t6-aluminum-modulus-of-elasticity/

## Parameters

I inputted all the values into the parameters, and I had a little bit of difficulty with the units for area but besides that it worked smoothly. 

<img width="1792" height="714" alt="image" src="https://github.com/user-attachments/assets/044ec94d-ce7a-43a9-bed1-6e8a914c4599" />


## FEA

<img width="1024" height="791" alt="image" src="https://github.com/user-attachments/assets/a12394f5-e0dc-47e0-be3c-08ae3265126f" />


<img width="1536" height="702" alt="image" src="https://github.com/user-attachments/assets/348daf88-c7d4-4eae-ab85-c5d79fc92368" />


<img width="1536" height="694" alt="image" src="https://github.com/user-attachments/assets/e63333b9-da41-49e5-b87b-b31a37cd35c0" />

These images show the safety factor, the Von Mises Stress map, and a deflection map. The safety factor image indicates that the whole structure is stable and well beyond a permissible factor of safety. The von Mises Stress map shows that there is most stress, 11.3 ksi, at the contact point between the bar and the support, and that the middle of the bar is under the same constant stress of 10ksi. The max stress is 11.3 ksi which is much smaller than the value of 40 ksi which is the strength of aluminum. With this in mind the safety factor would be 40/11.3 which is 3.5, but this value is not a real design limit due to the way that FEA handles supports. Excluding that the max stress would be 10 ksi, and therefore the safety factor would be 4.


## Design Reflection

There is no direct percent difference between my hand calculated value and the FEA when it comes to the stress or deflection. This could be a rounding error or an issue I'm not completely aware of, but the values are very close. The FEA has small spikes in stress at the two ends due to the functionality of the program, while my hand calculations assumed equal stress everywhere throughout the bar. This could be explanation as to why the values differ, but are extremely close to one another. The deflection ramps up the further you get from the support which makes sense because the deflection should increase the length. I trust the hand calculations more since they don't have any meshing error or boundary assumptions/approximations. 


## Pin Hole Problem

I chose a hole with a diameter of 0.08 inches. Using the Peterson curve fit for a hole in a flat bar in tension the Kt value is 2.24. σ_peak = Kt × σ_nom = 2.24 × 10 ksi = 22.4 ksi. 40 ksi /22.4 ksi gives you a safety factor of 1.79 which is still passing so the structure will still hold. 


## Modify Design Parameters

My initial guesses are that if you increase the load the length will decrease, and if you increase the height or width that will increase the overall area therefore increasing the length.

<img width="1641" height="595" alt="image" src="https://github.com/user-attachments/assets/2f0005b7-049e-46ec-8663-7c82e5a80db1" />

My assumptions were correct. 


## Time and Takeaways

I spent about 5 hours on this project over the course of 2 days. I switched to Fusion which I am more comfortable with, and that has allowed me to submit work of a higher quality. I can also be more efficient with the CAD processes. I still need to familiarize myself with the new functions such as parameters, but I am more confident now after this project. 


## Access CAD
https://a360.co/4gMQBtu





