# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
google colab
# Program:
```
import numpy as np
import math 
L  = 0
hs = 0
p = []
lk = []
n = int(input("Enter the number of Samples : "))
for i in range (n): 
    pr = float(input(f"Enter the probability of sample values {i + 1}: "))  
    p.append(pr)
for j in range (n): 
    l = float(input(f"Enter the length of the sample values {j + 1}: "))  
    lk.append(l)
# Avg length of the code word
for k in range (n):
    Avg1 = p[k] * lk[k]
    L = L + Avg1
# Entropy
for k in range (n):
    e = p[k] * math.log(1 / p[k], 2)
    hs = hs + e
hs = round(hs,3)
# Efficiency
eff =  hs / L
eff = round(eff,3)
# Redundancy 
red =  round(1 - eff,3) 
# Variance
var = 0
for k in range(n):
    var1 = p[k] * (lk[k]-L)**2
    var = var + var1
var = round(var,3)
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff}")
print(f"Redudancy is : {red}")
print(f"Variance is : {var}") 
```
# Calculation:
<img width="1378" height="1600" alt="WhatsApp Image 2026-07-27 at 8 32 51 AM" src="https://github.com/user-attachments/assets/97fbeaa0-6b16-487e-8a9e-de8cde21def6" />

<img width="1200" height="1600" alt="WhatsApp Image 2026-07-27 at 8 32 52 AM" src="https://github.com/user-attachments/assets/0b169417-9d6d-41d7-876f-442599f4a5a3" />

<img width="1200" height="1600" alt="WhatsApp Image 2026-07-27 at 8 32 52 AM (1)" src="https://github.com/user-attachments/assets/8a4d76f6-4082-479e-806e-e0593d8dffe2" />

# Output

<img width="285" height="88" alt="image" src="https://github.com/user-attachments/assets/a292f8e1-53e4-4578-a0a2-e9a882a75082" />


# Results:
The Huffman and Shannon-Fano coding techniques have been successfully applied to the given source. The average codeword length, entropy, variance, redundancy, and efficiency have been computed.
