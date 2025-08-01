---
date: '2024-11-21T20:16:43.834284Z'
tags:
- autogenerated
- source__claude
- conversation_id__3192c2c3-bfbf-423b-8bab-29fb984f34a0
- msg_c3e19f47-9579-4202-939c-c93b3fff18ad
- msg_6f156f1a-d175-44ce-9cae-a763ae1afa84
- colorclass/information-theory
title: dimensional analysis of information absorption efficiency
---

**USER**

dimensional analysis of η(C)


**ASSISTANT**

# Dimensional Analysis of Information Absorption Efficiency

## Base Units

Let's establish fundamental units:
- [I] = bits (information)
- [C] = FLOPs (computation)
- [t] = seconds
- [E] = joules

## Analysis of η(C)

From definition:
```
dI(θ;D)/dC = η(C) · [I_max - I(θ;D)]
```

Therefore:
```
[η(C)] = [1/C]
       = [FLOP^(-1)]
```

Since η(C) = η₀ · exp(-C/C₀):

1. [η₀] must be [FLOP^(-1)]
2. [C₀] must be [FLOP]

## Alternative Formulation

Through energy:
```
[η(C)] = [dI/dC]·[1/I]
       = [bits/FLOP]·[1/bits]
       = [FLOP^(-1)]
```

## Unit Analysis by Component

### Information Rate
```
[dI/dC] = [bits/FLOP]
```

### Remaining Capacity
```
[I_max - I(θ;D)] = [bits]
```

### Base Efficiency
```
[η₀] = [1/FLOP]
     = [bits/FLOP/bits]  # alternative view
```

## Physical Analogies

1. [[Thermal Conductivity]]:
   ```
   [k] = [W/m/K]  # heat flow per length per temperature
   [η] = [bits/FLOP/bits]  # info flow per compute per info gradient
   ```

2. [[Diffusion Coefficient]]:
   ```
   [D] = [m²/s]  # spatial flow rate
   [η] = [1/FLOP]  # computational flow rate
   ```

## System Implications

For consistent units:
```
[dI/dt] = [η]·[C/t]·[I]
        = [FLOP^(-1)]·[FLOP/s]·[bits]
        = [bits/s]
```

⚠️ **META-NOTE**: This dimensional analysis reveals η(C) as a fundamentally rate-like quantity in computational space, analogous to conductivity or diffusion coefficients in physical systems.

## See Also
- [[Physical Units in ML]]
- [[Information Flow Analysis]]
- [[Computational Metrics]]
- [[Rate Constants]]


---

preceding: [[characteristic compute scale]]  


following: [[[[information absorption efficiency]] compound rate analysis]]

See also: [[information absorption efficiency]]