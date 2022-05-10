---
layout: default
title: 5. Phage enrichment
parent: Lab Protocols
nav_order: 5
published: true
authors: [Natalia Quinones-Olvera]
sphages_credit: True
---

# Phage enrichment
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


## Objective
{: .no_toc }
To amplify phages from environmental samples.

## Rationale
{: .no_toc }
There are different ways to isolate phages from environmental samples. [Direct plating](./protocol_directplating.html) works well when the phages we're looking for are in enough abundance that we expect to find them in a small volume of our sample. If the phage is present at a lower concentration, using a larger volume of sample and doing an <mark>enrichment</mark>, increases our chances of finding it. _Enrichment_ is a technique in which we provide favorable conditions for a certain organism to grow. In this case, we provide phage in the sample an opportunity to replicate in a specific bacterial host. 

In this protocol, we filter a large volume of environmental sample to get rid of all the bacteria from the environment, keeping the phages. Then, we mix the filtrate with a culture of our host bacteria. Phages in the sample that can replicate in the provided host bacteria will lyse the cells they infect, and go through several rounds of infection, effectively "amplifying" the number of phages present in the culture. We then can filter this culture again, and test for the presence of an amplified phage by adding the filtrate on top of bacterial lawns.

This technique is useful, because even if there was only a single phage particle of interest in the sample, we would be able to capture it _after_ this amplification. Some things to consider: 1) The sample *for sure* contains *many* other phages for different bacteria, so even if we can’t see these phages because they can’t replicate in the bacterial host we’re using, we should be careful when handling the samples! 2) A sample might contain more than one type of phage that is able to infect our host, so we might be amplifying more than one phage during an enrichment. Therefore, it is very important to purify it later on! ([See: Protocol 6](./protocol_purification.html))

---

## Setting up enrichment

### Before you start:
{: .no_toc }
- You need a growing liquid culture of your bacterial host(s).
- Retrieve your **filtered** sample(s) from the 4 ℃ fridge.
    + _They should have been processed as specified in:_ [_3.1 Sample processing_](./protocol_03-sampling.html#sample-processing)

### Materials for enrichment
{: .no_toc }
- 2 mL of of each filtered sample.
- Culture tubes (as many tubes as samples + 1 for a _no-sample control_)
- 2 mL of appropriate 2X liquid media per tube.
- 2 labeled microcentrifuge tubes per tube.
- serological pipettes

### Procedure for enrichment
{: .no_toc }

#### Day 1
{: .no_toc }

1. Set out as many culture tubes as sampled you will be enriching and label the tubes. Add an extra tube for the *no-sample* control.
1. ➕ Add 2 mL of 2X LB to a culture tube using 10 mL serological pipettes.
1. 🪵 Inoculate the culture tubes with bacterial liquid culture, at a 1:1000 ratio.
- {: .label .label-red }Team Coryne:
- {: .fs-3 } 4 μL of _C. glu_
- {: .label .label-purple } Team plasmid-dependent: 
- {: .fs-3 } 2 μL of _E. coli_ + 2 μL of _P. putida_ 
1. ➕ Add 2 mL of filtered sample to the same culture tubes. (You will have just over 4 mL of liquid in the tube.)
1. 🌡️ Incubate your enrichment at 30℃, shaking at 220 rpm, overnight.

#### Day 2
{: .no_toc }

1. Fetch your enrichment from the incubator.
1. ➕ Transfer 1000 uL into a microcentrifuge tube. Transfer another 1000 uL into a second microcentrifuge tube.
1. 💫 Spin both of your tubes in the microcentrifuge, at maximum speed, for 1 minute. This will pellet the bacteria.
> We pellet the bacteria, because if we try to pass to many of them through the filter, it will clog it!
1. 💉 [Filter](./protocol_basictech.html#using-syringe-filters) the supernatant through a 0.22 µm filter, into new, clean, and *labeled* microcentrifuge tubes.
1. 🗑️ Appropriately dispose of the remaining enriched culture.
1. 📥 Store your filtered enrichment in the 4℃ fridge.
1. You may continue with the [Spot Assay]() as explained below, or keep your filter enrichment and do the Spot Assay later on.

## Spot assay

### Before you start:
{: .no_toc }
- You need a growing liquid culture of your bacterial host(s).
- Retrieve your filtered enrichment(s) from the 4℃ fridge.
- You need to have pre-melted molten top agar in your bead bath.

### Materials for spot assay
{: .no_toc }
- Processed filtered enrichment(s).
- LB agar plates (you will use about 1 plate per each 6 enrichments you are processing)
- Culture tubes (as many tubes as plates)
- LB top agar
- Serological pipettes

### Procedure for spot assay
{: .no_toc }

#### Day 1
{: .no_toc }
1. 🖊️  Label LB agar plates with today's date, your name, your host bacteria.
1. 🖊️  Mark 6 well spaced dots, as shown in the picture, and label each dot with a different **sample ID** corresponding to the enrichment you are testing.
1. 🧪 Set out as many culture tubes as plates you labeled.
1. ➕ Add the appropriate bacterial host culture(s) to each of the sample tubes.
- {: .label .label-red }Team Coryne:
- {: .fs-3 } **250** µL of _C. glu_
- {: .label .label-purple } Team plasmid-dependent: 
- {: .fs-3 } **100** µL of _E.coli_ - pK2
- {: .fs-3 } **100** µL of _P. putida_ - pK2
1. ➕ Using a sterile serological pipette, gently add 3 mL molten top agar supplemented with CaCl<sub>2</sub> to a single tube, and immediately suck up the top agar/sample/bacteria mixture and transfer it to the appropriately labeled plates.
1. ↔️↔️ Quickly tilt the plate in multiple directions until the top agar mixture evenly coats the agar plate. Once top agar has totally coated the surface, cover the plates with the lid and leave to set.
1. ⏳ Let the plates sit undisturbed for 5 minutes on the benchtop to allow the top agar to fully solidify.
1. ➕ Once the top agar is set, remove the lid of the plate and carefully pipette a 10 µL drop of filtered enrichment on top of the corresponding labeled dot.
1. Repeat this for every enrichment you're testing.
1. ⏳ Close the lid and let the plates unidisturbed until the drops dry.
1. 🌡️ Incubate the plates overnight in the appropriate incubator.
- {: .label .label-red }Team Coryne: **30℃**
- {: .label .label-purple } Team plasmid-dependent: **37℃**

#### Day 2
{: .no_toc }
1. Retrieve your plates from the incubator.
1. Check if any of your enrichments produced clearings in the lawn. If any of them did, use those enrichments and 
[▶ Continue to Protocol 6: Phage purification - Serial dilution of phages for plaque assays](./protocol_06-purification.html#serial-dilution-of-phages-for-plaque-assays){: .btn }




