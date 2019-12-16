---
title: Immersive Petroleum
# TODO: use variables to run calculations
---
*Author's Note: this guide is intended for Immersive Petroleum v1.1.9 for Minecraft v1.12.2; tested specifically with FTB Revelations v3.2.x and 2.7.x*

***

## Part I: Pumpjacks, or "How much power are we talkin'?"
[Pumpjacks (IP)]() tap oil reservoirs and run at a maximum pace of 1,024 RF/t. From the ground, they pump <a>Crude Oil [TODO]</a>, which can be refined in many different ways. The most efficient method found so far converts <a>Crude Oil [TODO]</a> to <a>Naphtha [TODO]</a> to <a>Refined Fuel [TODO]</a>. Pumpjacks are placed on Fluid Reservoirs, as detected by <a>Core Samples [TODO]</a> (see section TODO for more information). Fluid Reservoirs have a limited capacity before they are "drained", which greatly decreases Pumpjack output within the chunk. The numbers referenced in this section are calculated from running one Pumpjack at full speed (1,024 RF/t).

### Crude Oil Pumping Speed
- **Undrained Crude Oil Reservoir:** 15mB/t @ 1,024 RF/t = 14.65uB/t per RF/t input
- **Drained Crude Oil Reservoir:** 6mB/t [TODO: unverified] @ 1,024 RF/t = 5.86uB/t per RF/t input

If you have a certain level of power production in mind (which you should!), this will be relevant to your calculations. A Pumpjack will accept *up to* 1,204 RF/t, but can accept any level of power between 0 and 1,024 RF/t. *Use this to your advantage! Do not pump large amounts of oil to the surface so you can gawk at it! We are here to make power, not fill a bunch of tanks! Get in there! Do some math! Burn that oil! Keep your systems lean! Know your power needs and set your oil production accordingly!* A Pumpjack can (and will) run, even if there's nowhere to pump to. If there is no demand, it will simply waste power, not oil, too [TODO: unverified].

So you're ready to pull Crude Oil from the ground, huh? Not so fast - we need to talk about refining. The most efficient system we've found requires two [Fractionating Stills (TE)]() and can scale nicely in parallel. Fractionating Stills can use the [Reflux Column (TE)]() Augment, which increases yield, but requires more power [TODO: unverified].

### Fractionating Still Refining Speed
#### Without Reflux Columns
- 200mB Crude Oil to 150mB Naphtha for 5 kRF
- 150mB Naphtha to 100mB Refined Fuel for 5 kRF
- 2B Crude Oil to 1B Refined Fuel for 100 kRF

#### With Reflux Columns
- 200mB Crude Oil to 200mB Naphtha for 10 kRF
- 200mB Naphtha to 200mB Refined Fuel for 10 kRF
- 1B Crude Oil to 1B Refined Fuel for 100 kRF

Refined Fuel can be spent with Water in [Compression Dynamos (TE)]() for 1,500 kRF/B. With the use of the [Ignition Plugs (TE)]() Augment, this rises to 2,250 kRF/B. This augmented version should always be preferred. There is more setup cost to this system, but the power increase is *large* and *tangible*. Additionally, this resource pipeline is specialized enough that you should not be mixing the Refined Fuel in your Compression Dynamos with other (usually weaker) fuels. Using the Ignition Plugs prevents the use of other specialization augments, including the [Closed-Loop Cooling (TE)]() augment and the [Agitative Manifold (TE)]() augment, which is not relevant here.

Summing up our costs, we can find that the Pumpjack, even operating on a drained Reservoir, seems to be energetically profitable! 🎉 Full details below:

### Energy Profit Margin (per Bucket):
#### Undrained, without Reflux Columns
- **Pumping:** 14.65uB/t per RF/t = 68 kRF/B Crude Oil = **137 kRF/B** Refined Fuel
- **Refining:** 100 kRF/2B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel = **2,013 kRF/B** excess or **9.5:1** output:input

#### Undrained, with Reflux Columns
- **Pumping:** 14.65uB/t per RF/t = 68 kRF/B Crude Oil = **68 kRF/B** Refined Fuel
- **Refining:** 100 kRF/1B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel = **2,082 kRF/B** excess or **13.4:1** output:input

#### Drained, without Reflux Columns
- **Pumping:** 5.86uB/t per RF/t = 171 kRF/B Crude Oil = **341 kRF/B** Refined Fuel
- **Refining:** 100 kRF/2B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel = **1,809 kRF/B** excess or **5.1:1** output:input

#### Drained, with Reflux Columns
- **Pumping:** 5.86uB/t per RF/t = 171 kRF/B Crude Oil = **171 kRF/B** Refined Fuel
- **Refining:** 100 kRF/1B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel = **1,979 kRF/B** excess or **8.3:1** output:input

***

## Part II: Core Sampling, or "Oil Dowsing 101"

[TODO]

***

## Part III: Equipment Load, or "How much stuff do I set up?"

[TODO]

***

## Part IV: Tuning the Pumpjack, or "I'm givin' 'er all she's got, captain!"

[TODO]

***

## Part V: A Few Notes on Refining and Augments

[TODO]
