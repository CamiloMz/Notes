# SIZING FROM A CONCEPTUAL SKETCH

As introduction to the design process, this chapter presents a quick method of estimating takeoff weight from conceptual sketch. The simplified method presented can only be used for mission which do not include any combat or payload drops.

## TAKEOFF-WEIGHT BUILDUP

"Design takeoff gross weight" is the total weight of the aircraft as it begins the mission for which it was designed. This is not necessarily the same as the "maximum takeoff weight". Unless specifically mentioned, takeoff gross weight, or "$W_{0}$", is assumed to be the design weight.

Design takeoff gross weight can be broken into crew weight, payload (or passenger) weight, fuel weight, and the remaining (or empty) weight. The empty weight includes the structure, engines, landing gear, fixed equipment, avionics, and anything else not considered a part of crew, payload or fuel.

$\displaystyle  W_{0} = W_{crew} + W_{payload} + W_{fuel} + W_{empty}$ (Eq 3.1)

The crew and payload weights are both known since they are given in the design requirements. The only unknowns are the fuel weight and empty weight. However, they are both dependent o the total aircraft weight.

To simplify the calculation, both fuel and empty weights can be expressed as fractions of the total takeoff weight, i.e., $(W_{f}/W_{0})$ and $(W_{e}/W_{0})$. Thus Eq 3.1 becomes:

$\displaystyle  W_{0} = W_{crew} + W_{payload} + ( \frac{W_{f}}{W_{0}})W_{0} + (\frac{W_{e}}{W_{0}})W_{0}$ (Eq 3.2)

This can be solved for $W_{0}$ as follows:

$\displaystyle  W_{0} - ( \frac{W_{f}}{W_{0}})W_{0} - (\frac{W_{e}}{W_{0}})W_{0} = W_{crew} + W_{payload}$ (Eq 3.3)

$\displaystyle  W_{0} = \frac{W_{crew} + W_{payload}}{1 - (W_{f}/W_{0}) - (W_{f}/W_{0})} $ (Eq 3.34)

Now $W_{0}$ can be determined if $(W_{f}/W_{0})$ and $(W_{e}/W_{0})$ can be estimated.

## EMPTY WEIGHT ESTIMATION

the empty-weight fraction $(W_{e}/W_{0})$ can be estimated statistically from historical trends. Empty-weight fractions vary from about 0.3 to 0.7, and diminish with increasing total aircraft weight.

the type of aircraft also has a strong effect, with flying boats having the highest empty-weight fractions and long-range military aircraft having the lowest. Flying boats are heavy because they need to carry extra weight for what amounts to boat hull.

| $W_{e}/W_{0} = AW_{0}^{C}K_{vs}$  | $A$ | $C$ |
|-----------------------------------|-----|-----|
| sailplane -- unpowered            | 0.86 | -0.05 |
| sailplane -- powered              | 0.91 | -0.05 |
| Homebuilt -- metal/wood           | 1.19 | -0.09 |
| Homebuilt -- composite            | 0.99 | -0.09 |
| General aviation -- single engine | 2.36 | -0.18 |
| General aviation -- twin engine   | 1.51 | -0.10 |
| Agricultural aircraft             | 0.74 | -0.03 |
| Twin turboprop                    | 0.96 | -0.05 |
| Flying boat                       | 1.09 | -0.05 |
| Jet trainer                       | 1.59 | -0.10 |
| Jet fighter                       | 2.34 | -0.13 |
| military cargo/bomber             | 0.93 | -0.07 |
| Jet transport                     | 1.02 | -0.06 |
| $K_{vs} = $ variable sweep constant = 1.04 if variable sweep: = 1.00 if fixed sweep|

The table presents statistical curve-fit equations for the trends. Note that these are all exponential equations based upon takeoff gross weight. The exponents are small negative numbers, which indicates that the empty weight fraction decrease with increasing takeoff weight.

A variable-sweep wing is heavier than a fixed wing, and is accounted for at this initial stage of design by multiplying the empty-weight fraction by about 1.04

## FUEL-FRACTION ESTIMATION

