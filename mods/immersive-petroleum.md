---
title: Immersive Petroleum
# TODO: use variables to run calculations
---
*Author's Note: this guide is intended for Immersive Petroleum v1.1.9 for Minecraft v1.12.2; tested specifically with FTB Revelations v2.7.x and v3.2.x*

***

## Part I: Pumpjacks, or "How much power *can* we make?"
[Pumpjacks (IP)]() tap oil reservoirs and run at a maximum pace of 1,024 RF/t. From the ground, they pump <a>Crude Oil [TODO]</a>, which can be refined in many different ways. The most efficient method found so far converts <a>Crude Oil [TODO]</a> to <a>Naphtha [TODO]</a> to <a>Refined Fuel [TODO]</a>. Pumpjacks are placed on Fluid Reservoirs, as detected by <a>Core Samples [TODO]</a> (see section TODO for more information). Fluid Reservoirs have a limited capacity before they are "drained", which greatly decreases Pumpjack efficiency within the chunk. The numbers referenced in this section are calculated from running one Pumpjack at full speed (1,024 RF/t).

### Crude Oil Pumping Speed
- **Undrained Crude Oil Reservoir:** 15mB/t @ 1,024 RF/t = 14.65uB/t per RF/t input
- **Drained Crude Oil Reservoir:** 6mB/t [TODO: unverified] @ 1,024 RF/t = 5.86uB/t per RF/t input

If you have a certain level of power production in mind (which you should!), this will be relevant to your calculations. A Pumpjack will accept *up to* 1,024 RF/t, but can accept any level of power between 0 and 1,024 RF/t. *Use this to your advantage! Do not pump large amounts of oil to the surface so you can gawk at it! We are here to make power, not fill a bunch of tanks! Get in there! Do some math! Burn that oil! Keep your systems lean! Know your power needs and set your oil production accordingly!* A Pumpjack can (and will) run, even if there's nowhere to pump to. If there is no demand, it will simply waste power, not oil, too [TODO: unverified].

So you're ready to pull Crude Oil from the ground, huh? Not so fast - we need to talk about refining. The most efficient system we've found requires two [Fractionating Stills (TE)]() and can scale nicely in parallel. Fractionating Stills can use the [Reflux Column (TE)]() Augment, which increases yield, but requires more power [TODO: unverified].

### Fractionating Still Refining Speed
#### Without Reflux Columns
- 200mB Crude Oil to 150mB Naphtha for 5 kRF input
- 150mB Naphtha to 100mB Refined Fuel for 5 kRF input
- 2B Crude Oil to 1B Refined Fuel for 100 kRF input

#### With Reflux Columns
- 200mB Crude Oil to 200mB Naphtha for 10 kRF input
- 200mB Naphtha to 200mB Refined Fuel for 10 kRF input
- 1B Crude Oil to 1B Refined Fuel for 100 kRF input

Refined Fuel can be spent with Water in [Compression Dynamos (TE)]() for 1,500 gross kRF/B. With the use of the [Ignition Plugs (TE)]() Augment, this rises to 2,250 gross kRF/B. This augmented version should always be preferred. There is more setup cost to this system, but the power increase is *large* and *tangible*. Additionally, this resource pipeline is specialized enough that you should not be mixing the Refined Fuel in your Compression Dynamos with other (usually weaker) fuels. Using the Ignition Plugs prevents the use of other specialization augments, including the [Closed-Loop Cooling (TE)]() augment and the [Agitative Manifold (TE)]() augment, which is not relevant here.

Summing up our costs, we can find that the Pumpjack, even operating on a drained Reservoir, seems to be energetically profitable! 🎉 Full details below:

### Energy Profit Margin (per Bucket):
#### Undrained, without Reflux Columns
- **Pumping:** 14.65uB/t per RF/t = 68 kRF/B Crude Oil = **137 kRF/B** Refined Fuel
- **Refining:** 100 kRF/2B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** **2,250 kRF/B** Refined Fuel
- 2,250 gross kRF/B - 137 kRF/B - 100 kRF/B = **2,013 net kRF/B** or **89.5%** conversion

#### Undrained, with Reflux Columns
- **Pumping:** 14.65uB/t per RF/t = 68 kRF/B Crude Oil = **68 kRF/B** Refined Fuel
- **Refining:** 100 kRF/1B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel
- 2,250 gross kRF/B - 68 kRF/B - 100 kRF/B = **2,082 net kRF/B** or **92.5%** conversion

#### Drained, without Reflux Columns
- **Pumping:** 5.86uB/t per RF/t = 171 kRF/B Crude Oil = **341 kRF/B** Refined Fuel
- **Refining:** 100 kRF/2B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel
- 2,250 gross kRF/B - 341 kRF/B - 100 kRF/B = **1,809 net kRF/B** or **80.4%** conversion

#### Drained, with Reflux Columns
- **Pumping:** 5.86uB/t per RF/t = 171 kRF/B Crude Oil = **171 kRF/B** Refined Fuel
- **Refining:** 100 kRF/1B Crude Oil = **100kRF/B** Refined Fuel
- **Burning:** 2,250 kRF/B Refined Fuel
- 2,250 gross kRF/B - 171kRF/B - 100 kRF/B = **1,979 net kRF/B** or **88.0%** conversion

*Author's note: If you come across a method with a better yield than Crude Oil to Naphtha to Refined Fuel, or a more efficent way to implement this method, please let me know. I'll be happy to include the method and give you some well-deserved credit!*

***

## Part II: Core Sampling, or "Oil Dowsing 101"

[TODO]

***

## Part III: Fine Tuning, or "How much power *should* we make?"

If you're looking to run your Pumpjack at full speed, more power to you. Keep in mind, we're looking to produce *enough* power here, not to pump the oil up to a tank endlessly. If you have the space or desire to fill big tanks with Crude Oil, ignore me and pump away. If you overfill a tank, it does not seem to waste any oil, only power. If you have a set amount of power you want to produce, enter it below.

<div class="input with-suffix">
  <label for="part-3-production-RF" markdown="1">
    **Desired Excess RF/t:**
  </label>
  <input id="part-3-RF-excess"/>
  <div class="suffix">RF/t</div>
</div>

#### Undrained, without Reflux Columns
* 2,250 kRF/B output (net) : **2,013 kRF/B output** (excess) : **137 kRF/B input** (pumping)
* <span class="part-3 undrained no-reflux out">2,250</span> RF/t output (net) : **<span class="part-3 undrained no-reflux excess">2,013</span> RF/t output** (excess) : **<span class="part-3 undrained no-reflux in">137</span> RF/t input** (pumping)

***

## Part IV: Equipment Load, or "How much setup?"

[TODO]

***

## Part V: A Few Notes on Refining and Augments

[TODO]
