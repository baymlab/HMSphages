---
layout: default
title: 6. Phage enrichment
parent: Lab Protocols
nav_order: 6
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
There are different ways to isolate phages from environmental samples. [Direct plating](./protocol_directplating.html) works well when the phages we're looking for are abundant enough that we expect to find them in a small volume of our sample. If the phage is present at a lower concentration, using a larger volume of sample and doing an <mark>enrichment</mark>, increases our chances of finding it. _Enrichment_ is a technique in which we provide favorable conditions for a certain organism to grow. In this case, we provide any phage in the sample an opportunity to replicate on a specific bacterial host.

Previously, we filtered a large volume of environmental sample to get rid of all the bacteria, keeping only the phages. Now, we will mix the filtrate with a culture of our host bacteria and provide growth media for the bacteria to grow. Phages in the sample that can replicate in the provided host bacteria will lyse the cells they infect, and go through several rounds of infection, effectively "amplifying" the number of phages present in the culture. We then can filter this culture again, and test for the presence of an amplified phage by adding the filtrate on top of bacterial lawns.

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
- 20 mL tube of 2X LB.
- 2 labeled microcentrifuge tubes per tube.
- serological pipettes

### Procedure for enrichment
{: .no_toc }

#### Day 1
{: .no_toc }

1. Set out as many culture tubes as samples you will be enriching and label the tubes. Add an extra tube for the *no-sample* control.
1. Add 400 μL CaCl<sub>2</sub> to the 20 mL tube of 2X LB. The final enrichment will contain 10mM CaCl<sub>2</sub>
1. 🪵 Inoculate the 2X LB with bacterial liquid culture, at a 1:1000 ratio.
- {: .fs-3 } 20 μL of _C. glu_
1. ➕ Add 2 mL of inoculated 2X LB to a culture tube using a 10 mL serological pipettes.
1. ➕ Add 2 mL of filtered sample to the same culture tube. To the *no sample* control tube a 2 mL of sterile water (You will have just over 4 mL of liquid in the tube.)
1. 🌡️ Incubate your enrichment at 30℃, shaking, overnight.

#### Day 2
{: .no_toc }

1. Fetch your enrichment from the incubator.
1. ➕ Transfer 1000 µL of your enrichment into a microcentrifuge tube.
1. 💫 Spin your tube in the microcentrifuge, at maximum speed, for 1 minute. This will pellet any bacteria that have grown in the enrichment. Make sure the centrifuge is *balanced* before you start it.
> We pellet the bacteria because if we try to pass too many of them through the filter, they will clog it!
1. 💉 Without disturbing the pellet, pipette 800 µL of the clarified enrichment into a syringe filter and [Filter](./protocol_basictech.html#using-syringe-filters) the supernatant into a new, clean, and *labeled* microcentrifuge tube.
1. 🗑️ Appropriately dispose of the remaining enriched culture.
1. 📥 Store your filtered enrichment in the 4℃ fridge.
1. You may continue with the [Spot Assay]() as explained below, or store your filtered enrichment in the 4℃ fridge and do the Spot Assay later on.

## Spot assay

### Before you start:
{: .no_toc }
- You need a growing liquid culture of your bacterial host(s).
- Retrieve your filtered enrichment(s) from the 4℃ fridge.
- You need to have a tube of molten LB top agar in your bead bath.

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
1. 🖊️  Mark 6 well spaced dots, and label each dot with a different **sample ID** corresponding to the enrichment you are testing.
1. 🧪 Set out as many culture tubes as plates you labeled.
1. ➕ Add the appropriate bacterial host culture(s) to each of the culture tubes.
- {: .fs-3 } **250** µL of _C. glu_
1. ➕ Using a sterile serological pipette, gently add 4 mL molten top agar supplemented with CaCl<sub>2</sub> to a single tube, and immediately suck up the top agar/sample/bacteria mixture and transfer it to the appropriately labeled plates.
1. ↔️↔️ Quickly tilt the plate in multiple directions until the top agar mixture evenly coats the agar plate. Once top agar has totally coated the surface, cover the plates with the lid and leave to set.
1. ⏳ Let the plates sit undisturbed for 5 minutes on the benchtop to allow the top agar to fully solidify.
1. ➕ Once the top agar is set, remove the lid of the plate and carefully pipette a 10 µL drop of filtered enrichment on top of the corresponding labeled dot.
1. Repeat this for every enrichment you're testing.
1. ⏳ Close the lid and let the plates sit unidisturbed until the drops dry. It may be necessary to dry the drops underneath a lit bunsen burner.
1. 🌡️ Incubate the plates overnight in the 30℃ incubator.

#### Day 2
{: .no_toc }
1. Retrieve your plates from the incubator.
1. Check if any of your enrichments produced zones of clearing in the lawn. If any of them did, use those enrichments and
[▶ Continue to Protocol 6: Phage purification - Serial dilution of phages for plaque assays](./protocol_06-purification.html#serial-dilution-of-phages-for-plaque-assays){: .btn }
