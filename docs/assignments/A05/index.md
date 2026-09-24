# A5 – Bracket Design

## Objective
This week I was given the task to design a bracket that could withstand the horizontal force of by a strap outline. The initial options were to choose an applied load in between 500 lbf < F < 800 lbf, and choose one of three metals, aluminum 6061 T6, Steel (ASTM A36), or Titanium (Ti-6Al-V4). I chose an applied load of 500lbf and Aluminum 6061 T6. 


## Feature A

<img width="1024" height="675" alt="image" src="https://github.com/user-attachments/assets/22ca6095-3416-4c3e-b7b7-dd5d1aac8fd7" />


<img width="2048" height="784" alt="image" src="https://github.com/user-attachments/assets/6e0d44f2-efd1-4977-80f0-fc76e6ec653a" />

The cylinder was the first feature that I tackled since it is the origin of the loads in the design. The strap wraps around the cylinder applying the distributed load across 5.75". A diameter of 1.49" was the governing measurement which came from the stress calculation. and the stiffness calculation only required a diameter of 1". 


## Feature B

<img width="1536" height="653" alt="image" src="https://github.com/user-attachments/assets/5cd8ce81-f539-4a15-ba1f-1f153977ea2b" />

<img width="2048" height="719" alt="image" src="https://github.com/user-attachments/assets/6d7e8a93-f58e-4f13-becd-599c5465fbc2" />

Feature B came next and carries all the reaction load from the cylinder but as an axial force. I decided on a square cross section bar.

## Feature C


<img width="581" height="640" alt="image" src="https://github.com/user-attachments/assets/251dc23b-cf6e-4438-a106-8b51f6ed337e" />

Next was feature C and it is a simply loaded beam with a concentrated load at the center. 

## Feature D

<img width="572" height="640" alt="image" src="https://github.com/user-attachments/assets/7e397d51-88b0-4539-8983-bc33f1298e9f" />

Feature D carries the entirety of the reaction force at it's tip since I drew it as a cantilever.

## Feature E

<img width="581" height="640" alt="image" src="https://github.com/user-attachments/assets/013e8b81-fe8d-45a2-94a1-c6aa5ad875b9" />

The lip is meant to block pull out movement. With this in mind I decided to model it for half of the total strap tensile force(500 lbf). 

## Link Feature


<img width="575" height="640" alt="image" src="https://github.com/user-attachments/assets/15748a37-2d6a-4ef4-83ae-8947cb40ddb9" />

The link connects the cylinder of Feature A to a shaft while being able to carry the same load as the rest of the bracket. I modeled it as a two force axial member.

## Lessons Learned
Stress governed the necessary dimensions over stiffness in all features. One specific example was feature D where the stress calculation called for a height of 0.370 in while the stiffness calculation called for 0.113 in. The initial reaction force in feature A is used in feature B and so on, so if there was an error at that point is would ruin everything after. I used the wrong strap width initially but fixing it saved me a lot of time if I had not noticed. An assumption I made regarding feature E was that its role was to prevent pulling out, so I halved the force applied to it. If this assumption was incorrect my dimensions would be half of what they were supposed to be. 

## CAD File
https://a360.co/4hbSYWL
