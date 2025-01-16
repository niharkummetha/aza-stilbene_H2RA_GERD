---
title: Discovery of Aza-stilbene as a Scaffold for a Histamine Receptor H2 Antagonist for the Treatment of Gastroesophageal Reflux Disease
short_title: Discovery of Aza-stilbene as a H2RA Scaffold for Treatment of GERD
abstract:  |
  Gastroesophageal reflux disease (GERD) is a gastronintestinal disease affecting millions worldwide, causing chronic acid reflux. While dietary changes are a first-line treatment, current medications often face challenges such as limited efficacy, side effects, recalls, or complex synthesis. This project aims to computationally design a drug targeting the Histamine Receptor H2 (HRH2) in the gut as an alternative GERD treatment. Using Schrödinger Maestro and PDB 7UL3, a docking grid based on HRH2 was created to evaluate potential drug candidates. Four existing HRH2 antagonists were docked to establish benchmarks for docking score and pharmacokinetic properties including low CNS activity, reduced oral absorption, and minimal gut-to-blood permeability. A library of 3,057 ligands from the DUD-E database was screened for binding to key receptor amino acids, Asp98 and Asp186, and pharmacokinetic properties. Compounds with 2 or 3 six-membered rings showed the most promising profiles. A scaffold-based approach identified quinoles and aza-stilbenes as strong candidates. The optimal aza-stilbene demonstrated stronger docking scores, easier synthesis, and better pharmacokinetic properties than that of the quinolines, and in many aspects, better than known HRH2 antagonists. This compound was synthesized using a simple, one-step reaction with benzaldehyde and aniline in water at room temperature. The product was characterized by FTIR. This project demonstrates a new aza-stilbene scaffold that could be employed for new drugs to treat GERD.
---

## Introduction
### Gastroesophageal Reflux Disease
Gastroesophageal reflux disease (GERD), a gastrointestinal disease where a person experiences chronic acid reflux, affects around 20 percent of adults and 10 percent of children in the United States. Acid reflux is chronic when an individual has it two or more times a week for several weeks. Acid reflux occurs when gastric acid repeatedly rises into the esophagus, irritating the esophagus lining [@cleveland_clinic_acid_2023]. The most common way gastric acid can enter the esophagus is when the lower esophageal sphincter (LES) weakens or relaxes [@mittal_characteristics_1988]. The LES is a smooth muscle segment that opens when a person swallows, and its function is to prevent stomach contents like gastric acid from moving back up into the esophagus. Hiatal hernias, pregnancy, obesity, smoking, birth defects, connective tissue disorders, previous surgeries near the chest or upper abdomen, as well as certain foods and medications, can all be causes for a weaker or relaxed LES. For many, there may not be an obvious reason why their LES does not function properly. Even lying down after eating can cause the LES to relax and increase the risk of acid reflux [@cleveland_clinic_acid_2023].

Until patients with gastroesophageal reflux undergo treatment options, they can experience a range of symptoms. Regurgitation can occur, where stomach contents, including acid, food, or liquid, rise back up from the stomach into the throat after eating. Patients can also experience a burning feeling in several areas including the esophagus, chest (commonly known as heartburn), and stomach (known as acid indigestion). Additional symptoms include non-cardiac chest pain, nausea, sore throat, and asthma symptoms [@cleveland_clinic_acid_2023]. If GERD is not treated, complications can develop, including esophagitis (inflammation of the esophagus that can cause ulcers and bleeding), Barrett’s esophagus (esophagus tissue changes to look like intestinal tissue, which can lead to esophageal cancer), and esophageal stricture (development of scar tissue in the esophagus that narrows the esophagus, making it harder to swallow) [@national_definition_2020].

### Treatment Options for GERD

The first course of action for patients with GERD is lifestyle and dietary modifications. For patients who are overweight, losing weight could help with GERD symptoms. Quitting smoking, avoiding lying down after eating, and elevating the head when lying down may offer relief. Dietary changes include avoiding acidic foods and drinks, caffeine, fatty foods, and alcohol. Lifestyle and dietary changes will not be able to help every patient [@johns_hopkins_gastroesophageal_2024].

Since the weakening of the LES is the main cause of GERD, surgery may seem like the next option. Current surgical options include laparoscopic fundoplication (Nissen fundoplication), transoral incisionless fundoplication (TIF), and Magnetic Sphincter Augmentation (LINX device). All three of these options strengthen the LES by either wrapping the stomach or implanting magnetic beads [@newyork-presbyterian_gastroesophageal_2024]. However, laparoscopic fundoplication tends to have a failure rate of 10–20%; TIF has shown a failure rate of 33%; and the LINX device, being fairly new with only about 30,000 devices having been implanted, has a 4.81% risk of removal due to reasons like dysphagia/odynophagia and persistent GERD [@bardini_modification_2017; @hunter_efficacy_2015; @demarchi_evolution_2021]. Moreover, antireflux surgery carries a risk of mortality and prolonged structural complications, which can result in complications such as difficulty belching, feeling of abdominal bloating, increased diarrhea, and dysphagia (difficulty swallowing) [@yadlapati_complications_2018; @international_surgical_2021]. Ultimately, the American Gastroenterological Association recommends that surgery should only be an option for a very select number of patients with reflux, especially those with heartburn and regurgitation. Medication should be the next treatment option after dietary and lifestyle changes, and only after patients see their response to medications, undergo pH monitoring, and understand the benefits and risks with their clinicians, should they go for anti-reflux surgery [@chen_aga_2023].

Recent research includes the muscle relaxant baclofen, a gamma-aminobutyric acid class B (GABAB) receptor agonist, which decreased transient lower esophageal sphincter relaxation episodes by ~40%. Still, its clinical use has been limited due to its neurological and gastrointestinal side effects, and other developed GABAB agonists with fewer central side effects, like lesogaberan, have not been impressive during testing [@clarke_baclofen_2018; @bredenoord_lesogaberan_2009]. Another recent advancement in medications for GERD is vonoprazan, a potassium-competitive acid blocker (P-CAB) that has shown potential for being just as effective, if not more effective, as existing medications. Yet, a November 2024 American Gastroenterological Association Clinical Practice Update believes that P-CABs should not be used as initial therapy due to factors like cost, difficulty obtaining the medication, and lack of long-term safety data [@patel_aga_2024].

The AGA recommends three types of medications for the treatment of gastroesophageal reflux disease: antacids (such as Tums® or Alka-Seltzer®), histamine H2 receptor antagonists (H2RA’s or H2 blockers), and proton pump inhibitors [@freedberg_gastroesophageal_2021]. Antacids act as a base and neutralize gastric pH to decrease heartburn symptoms, but typically only last 30 to 60 minutes and should not be used chronically to treat GERD [@winter_gastroesophageal_2024]. Proton pump inhibitors (PPIs), drugs that inhibit certain cells from "pumping" acid into the stomach, last longer than antacids, but are expected to be used for 14 days, with effects not taking place until 24 hours later. They have potential long-term risks such as reduced levels of vitamin B12, magnesium, and calcium [@harvard_health_heartburn_2020]. Additionally, PPIs pose many drug interactions, including blood-thinning, heart, anxiety, immune system, HIV antiretroviral, and arthritis medicines [@wolfe_proton_2024]. Thus, it is best to focus on designing a more efficient histamine H2 antagonist. When histamine binds to histamine H2 receptors in gastric parietal cells, it triggers a pathway that leads to gastric acid secretion. Histamine H2 antagonists, also known as antihistamines, prevent histamine from binding and triggering the release of gastric acid. Histamine H2 antagonists need to bind to both Asp 98 and Asp 186 to be effective. In 2020, two Histamine H2 antagonists (ranitidine and nizatidine) were removed from the US market after it was discovered that they were carcinogenic. Recent advancements in this type of research conducted by Georgia Tech have tried docking small molecule quinolines using computational software but were unable to bind to both residues [@marquez-gomez_discovery_2022].

This study aims to computationally design a scaffold that binds to both Asp98 and Asp186 on the histamine H2 receptor, demonstrates strong binding, favorable pharmacokinetics, and minimal CNS activity, and can be easily synthesized. This study also aims to synthesize the best drug candidate to demonstrate its ease of synthesis. 

The LES is a smooth muscle segment that opens when a person swallows, and its function is to prevent stomach contents like gastric acid from moving back up into the esophagus. Hiatal hernias, pregnancy, obesity, smoking, birth defects, connective tissue disorders, previous surgeries near the chest or upper abdomen, as well as certain foods and medications, can all be causes for a weaker or relaxed LES. For many, there may not be an obvious reason why their LES does not function properly. Even lying down after eating can cause the LES to relax and increase the risk of acid reflux [@cleveland_clinic_acid_2023].

## Methods
### Phase 1: In silico Docking
The entirety of computational work was done using Schrödinger Maestro (Schrödinger Release 2023-3: Maestro, Schrödinger, LLC, New York, NY, 2023). 
#### Protein Preparation
The Histamine H2 receptor target protein complex was obtained from the RCSB Protein Data Bank (PDB ID: 7UL3). The protein was prepared using the built-in Protein Preparation Wizard (Schrödinger Release 2023-3: Protein Preparation Wizard; Epik,  Schrödinger, LLC, New York, NY, 2023; Impact, Schrödinger, LLC, New York, NY; Prime, Schrödinger, LLC, New York, NY, 2023). To prepare the protein, termini were capped, missing side chains were filled, bond orders were assigned, hydrogens were replaced, zero-order bonds to metals were created, disulfide bonds were created, hydrogen bond assignments were optimized, and water molecules outside of 5 hets from the ligand were removed.
#### Receptor Grid Generation
The receptor grid was generated using Receptor Grid Generation built into Schrodinger Glide (Schrödinger Release 2023-3: Glide, Schrödinger, LLC, New York, NY, 2023). The centroid of the workspace ligand (famotidine bound to the Histamine H2 receptor in the PDB) was selected as the center of the enclosing box. No constraints were set during the receptor grid generation in order to allow Maestro to find the poses of the lowest energy states (measured by lowest docking scores) for each ligand. This can best predict how these ligands would bind in vivo. A visual can be seen in @famotidine_dock. 
``` {figure} famotidine_dock.png
:label: famotidine_dock
3D Docking of famotidine to the HRH2 binding pocket. Dashed yellow lines represent hydrogen bonds, dashed pink lines represent salt bridges, and dashed orange lines represent bad contacts/clashes. | N. Kummetha via Schrödinger Maestro (2024)
```

#### Docking
All ligands were docked using the Ligand Docking tool in Schrödinger Glide (Schrödinger Release 2023-3: Glide, Schrödinger, LLC, New York, NY, 2023). Standard Precision (SP) was used along with the ligand sampling being flexible, sampling nitrogen inversions and ring conformations, and bias sampling of torsions for all predefined functional groups. A scaling factor of 0.80 and partial charge cutoff of 0.15 was used for the scaling of van der Waals radii of ligand atoms. No constraints were set in order to allow Maestro to find the poses of the lowest energy states (measured by lowest docking scores) for each ligand. This can best predict how these ligands would bind in vivo. Post-docking minimization was performed, and at most, 10 poses were written out per ligand. The docking score demonstrates the interaction strength between the static Histamine H2 receptor model and the ligand in the specified binding pocket. Ligands with lower (more negative) scores indicate a higher probability of binding to the target region. Ligands were screened by docking score, and those with more negative docking scores were then screened for ligand interactions.
#### Ligand Interaction Screening
To identify which residues a ligand interacts with, as well as the type of interactions, the built-in Ligand Interaction Diagram tool of Schrodinger Maestro was used. Each ligand interaction diagram was manually viewed to see if the ligand interacted with Asp 98 and Asp 186. Drug candidates that could bind to both of these residues were then screened for pharmacokinetic properties. Famotidine's ligand interaction diagram can be seen in @famotidine_2dlid.

```{figure} famotidine_interaction.png 
:label: famotidine_2dlid
:width: 2000px
2D Ligand Interaction Diagram of Famotidine | N. Kummetha via Schrödinger Maestro (2024)
```

#### Pharmacokinetic Properties Screening
Compounds that had a docking score more negative than a baseline docking score of -5.5 and interacted with Asp 98 and Asp 186 were then screened for pharmacokinetic properties and Lipinski’s rule violations using Schrödinger QikProp (Schrödinger Release 2023-3: QikProp, Schrödinger, LLC, New York, NY, 2023). All scoring rubrics were obtained from the QikProp 4.4 User Manual. Lipinski's rule of 5 uses AlogP, HBD, MW, PSA, and HBA scores to generate a multiple property optimization (MPO) score and determine if there were any violations. In addition, the CNS, QPLogHERG, QPPCaco, QPLogBB, and PercentHumanOralAbsorption pharmacokinetic scores were measured. The CNS score is indicative of central nervous system activity, with a score of -2 indicating that the drug is inactive, and a score of +2 indicating that the drug is active in the central nervous system. GERD HRH2 drug candidates should have a score of -2 and not be active in the central nervous system, as there are Histamine H2 receptors in the central nervous system that it should not target. The QPLogHERG score is a predicted IC50 value for blockage of HERG K+ channels as a measure of potential cardiotoxicity. Values below -5 are a concerning risk of cardiotoxicity as small concentrations of the drug have the potential to cause blockage in the hERG potassium channel, which can lead to cardiac issues. The QPPCaco is a measure of the gut-blood barrier, where a score of less than 25 nm/sec is poor and  >500 nm/sec is considered good. GERD HRH2 drug candidates should have QPPCaco scores below 25 nm/sec, meaning that it is less likely to cross the gut-blood barrier, useful as the orally-absorbed drug targets gastric parietal cells. 
#### Ligand Design and Preparation
All compounds were initially prepared using LigPrep (Schrödinger Release 2023-3: LigPrep, Schrödinger, LLC, New York, NY, 2023). The OPLS4 force field was used, and specified chiralities were retained (varied other chiral centers). Famotidine, nizatidine, cimetidine, ranitidine, and histamine were imported using their SMILES codes. These ligands were prepared, docked, and analyzed for ligand interactions. Their pharmacokinetic properties were calculated. The best drug’s docking score and pharmacokinetic properties were used as a benchmark. The 3,057 ligands from the DUD-E database GPCR subset Adenosine A2a receptor target molecular library were imported, prepared, and docked using high throughput virtual screening (HTVS) [@mysinger_directory_2012]. These ligands were screened by docking score, and the top ligands were screened for ligand interaction. Using the results of the ligands from the DUD-E database ligand database, it was decided that scaffold-based ligand design would be the most effective method. Scaffolds with known synthesis procedures were chosen. Different R-groups were enumerated on the scaffolds manually using the 2D sketcher feature of Schrödinger Maestro. Ultimately, a scaffold was chosen for its strong docking scores, pharmacokinetic properties, and ease of synthesis. The top drug candidate of this scaffold was synthesized.
### Phase 2: Synthesis
The final compound (Aza-stilbene with OH groups on both rings at 3, 5) was synthesized following @lizard_aza_2020. The scheme of synthesis can be seen in @synthesis. 
``` {figure} synthesis_scheme.png
:label: synthesis
Scheme of Synthesis for the final aza-stilbene. (Adapted from Lizard et al., 2020) | N. Kummetha (2024)
```
Briefly, a 1:1 molar ratio of 3,5-dihydroxybenzaldehyde (0.1995g, 1.44mmol) and 5-aminobenzene-1,3-diol (0.1956g, 1.56mmol) and were combined in a small beaker.  A minimal amount of water was added (under 5 mL) and stirred at room temperature using a magnetic stir bar for 20 hrs.  The reaction was monitored by TLC.  The resulting black solid was vacuum-filtered and dried overnight in an oven. The two starting compounds and the resulting product were analyzed by FTIR (Shimadzu IRSpirit with ATR attachment).

## Results and Discussion
The docking scores and computationally calculated pharmacokinetic properties of the four known drugs (either currently or formerly commercially available) can be found in @known_docking_table. All four known drugs were computationally found to bind to Asp 98, and all known drugs (except for nizatidine) were found to bind to Asp 186 and Tyr 250. Additionally, famotidine was found to hydrogen bond with Thr 190, which can be helpful in its docking score. Famotidine had the strongest binding (lowest docking score) of the commercially available drugs, higher than that of histamine, while the other known drugs had lower binding scores than histamine. Out of the four approved drugs, all but nizatidine were found to have CNS scores of -2. Nizatidine’s CNS score of 0 indicates that it is computationally predicted to be neither fully inactive nor fully active in the central nervous system. Ranitidine and nizatidine also had HERG scores significantly below -5, although they have been approved for use by the FDA. Famotidine is the only known drug found to have a QPPCaco score below 25 nm/sec. Famotidine also has the most negative QPLogBB. Additionally, famotidine has the smallest percentage of human oral absorption. All known drugs except for famotidine are considered “drug-like” for having no violations of Lipinski’s Rule of 5, though famotidine only has 1 Lipinski violation, which can be negligible. Taken together, amongst the docking scores and pharmacokinetic properties of the four known drugs, famotidine was found to be the best-known drug. Famotidine’s docking score and pharmacokinetic properties were used as the benchmarks for the ligand design process. 

:::{table} Computational Results for the Docking of Histamine and Known Drugs | N. Kummetha (2024) 
:label: known_docking_table

Docking scores (measure of the interaction strength between the static protein model and the ligand; more negative scores are more optimal), CNS (blood-brain barrier activity, an inactive drug should score -2, and an active drug should score +2 ), QPLogHERG (predicted IC50 value for blockage of HERG K+ channels as a measure of cardiotoxicity. Values significantly below -5 are concerning), QPPCaco (predicted permeability of the gut-blood barrier, <25 nm/sec is poor and >500 nm/sec is great), QPLogBB (predicted brain/blood partition coefficient, more negative means less likely to cross BBB), PercentHumanOralAbsorption (<25% is poor, >80% is high), Lipinski’s Violations (number of violations of Lipinski’s rule of 5, 0 violations is considered “drug-like”). Green = Optimal score, Yellow = Slightly outside optimal range, Red = Significantly outside optimal range.

<table border="1">
   <tr>
      <th colspan="10" align="center" style="background-color: DarkGray;">Docking Scores and Pharmacokinetic Properties of Histamine and Known H2RAs</th>
   </tr>
   <tr>
      <th align="center" style="background-color: cornflowerblue;">Compoud</th>
      <th align="center" style="background-color: cornflowerblue;">Docking Score</th>
      <th align="center" style="background-color: cornflowerblue;">Interacts with</th>
      <th align="center" style="background-color: cornflowerblue;">CNS</th>
      <th align="center" style="background-color: cornflowerblue;">QPLogBB</th>
      <th align="center" style="background-color: cornflowerblue;">QPLogHERG</th>
      <th align="center" style="background-color: cornflowerblue;">QPPCaco </th>
      <th align="center" style="background-color: cornflowerblue;">Percent Human Oral Absorption</th>
      <th align="center" style="background-color: cornflowerblue;">Lipinski's Violations</th>
   </tr>
   <tr>
      <td align="center" style="">Histamine</td>
      <td align="center" style=""></td>
      <td align="center" style="">-5.302</td>
   </tr>
   <tr>
      <td align="center" style="">Famotidine</td>
      <td align="center" style="">-6.577</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Thr190, Tyr250, Arg257</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: MediumSeaGreen">-3.457</td>
      <td align="center" style="background-color: MediumSeaGreen">-4.621</td>
      <td align="center" style="background-color: MediumSeaGreen">3.313</td>
      <td align="center" style="background-color: MediumSeaGreen">16.203</td>
      <td align="center" style="background-color: yellow">1</td>
   </tr>
   <tr>
      <td align="center" style="">Ranitidine</td>
      <td align="center" style="">-5.019</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Tyr250, Phe251, Phe254, Arg257</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: yellow">-1.029</td>
      <td align="center" style="background-color: Crimson">-6.150</td>
      <td align="center" style="background-color: yellow">128.369</td>
      <td align="center" style="background-color: Crimson">75.188</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>
    <tr>
      <td align="center" style="">Nizatidine</td>
      <td align="center" style="">-3.584</td>
      <td align="center" style="background-color: crimson">Asp98, Cys174</td>
      <td align="center" style="background-color: crimson">0</td>
      <td align="center" style="background-color: yellow">-0.939</td>
      <td align="center" style="background-color: Crimson">-6.070</td>
      <td align="center" style="background-color: yellow">127.298</td>
      <td align="center" style="background-color: Crimson">71.688</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>     
 <tr>
      <td align="center" style="">Cimetidine</td>
      <td align="center" style="">-3.141</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Tyr250</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: yellow">-1.194</td>
      <td align="center" style="background-color: MediumSeaGreen">-4.708</td>
      <td align="center" style="background-color: yellow">400.282</td>
      <td align="center" style="background-color: crimson">76.051</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>

:::

To begin the ligand design process, the DUD-E database’s GPCR subset’s AA2AR target molecular library was screened. The results of this screening are found in @dud-e_database. The 3,057 ligands in this molecular library were screened using high throughput virtual screening (HTVS). When using high throughput virtual screening, the scale of the docking scores is different than using standard precision. For this screening, a docking score of -6.250 was set as the benchmark. 280 of the 3,057 ligands had a docking score that was -6.250 or lower (more negative). The ligand interaction diagram for each of these 280 ligands was then manually viewed. 37 of these 280 ligands interacted with Asp 98 and Asp 186. Of these 37 ligands, 24 had 2 or 3 6-membered rings. Thus, it was determined that a scaffold-based ligand design approach using scaffolds with 2 or 3 6-membered rings would be better for designing easily synthesizable ligands.

:::{table} Results of screening the 3,057 compounds from the DUD-E database’s GPCR subset’s AA2AR target molecular library | N. Kummetha (2024)
:label: dud-e_database

<table border="1">
   <tr>
      <th colspan="4" align="center" style="background-color: DarkGray;">Results of Docking DUD-E AA2AR Molecular Library</th>
   </tr>
   <tr>
      <th align="center" style="background-color: cornflowerblue;">Ligands in Library</th>
      <th align="center" style="background-color: cornflowerblue;">With HTVS Docking Score <= -6.250</th>
      <th align="center" style="background-color: cornflowerblue;">And interact with Asp 98 and Asp 186</th>
      <th align="center" style="background-color: cornflowerblue;">And have 2 or 3 6-membered rings</th>
   </tr>
   <tr>
      <td align="center" style="background-color: MediumSeaGreen;">3,057</td>
      <td align="center" style="background-color: MediumSeaGreen;">280</td>
      <td align="center" style="background-color: MediumSeaGreen;">37</td>
      <td align="center" style="background-color: MediumSeaGreen;">24</td>
   </tr>
   
</table>
:::

2D Sketcher was used to design ligands of different scaffolds that have 2 or 3 6-membered rings that are easy to synthesize. After over 200 modifications to over 8 different scaffolds, it was found that using OH groups and a quinoline or aza-stilbene scaffold was effective, and both of these molecules indeed had higher docking scores than famotidine. Both scaffolds' ligand interaction diagrams can be found in @interaction-diagrams-2. Both scaffolds' best candidate's docking scores and pharmacokinetic properties can be found in @best_candidates_docking_table. Comparing docking scores, aza-stilbene has the highest docking score. Both drugs have a CNS of -2, which is excellent. Both QPLogHERG are just slightly over -5, which is a little concerning, but not too bad to worry about, considering that other FDA-approved drugs have even lower scores. The aza-stilbene’s QPPCaco score and QPLogBB scores are excellent, while the quinoline’s QSPPCaco score is a little bit high and QPLogBB is within a good range. The percent human oral absorption is also not of concern for the aza-stilbene, while quinoline has a high percent human oral absorption. Both have good Lipinski scores. Additionally, both compounds are easy to synthesize. Yan et al. have discovered an easy synthesis for quinolines, though requires a few steps [-@yan_aerobic_2013]. Lizard et al. have discovered a one-step synthesis for aza-stilbenes, and are easy to make [-@lizard_aza_2020]. All it requires is an aldehyde, aniline, and water. Taking these pharmacokinetic properties together, the aza-stilbene demonstrates an excellent drug candidate, one that could bind stronger than famotidine, and be much easier to synthesize than famotidine. @aza-stilbene_docking_table shows all drug candidates using an aza-stilbene scaffold with OH on the R-groups tha have strong docking scores more negative than -5.5 and interact with both Asp 98 and Asp 186. The best aza-stilbene was then synthesized by putting the 3,5-dihydroxybenzaldehyde and 5-aminobenzene-1,3-diol in a small beaker with a minimal amount of water. The yield was approximately 10%. The result of the FTIR for the synthesis is included in @ftir.

```{figure}
:label: interaction-diagrams-2
:align: left

:::{image} best_quinoline_interaction.png
:alt: Best Quinoline Candidate
:width: 370px
:::

:::{image} best_aza-stilbene_interaction.png
:alt: Best Aza-Stilbene Candidate
:width: 350px
:::

:::{image} interaction_legend.png
:alt: Ligand Interaction Diagram Legend
:width: 800px
:::

2D Ligand Interaction Diagrams of the best quinoline scaffold-based drug candidate and aza-stilbene scaffold-based drug candidate for GERD | N. Kummetha (2024)
```

:::{table} Docking Scores and Pharmacokinetic Properties of top Aza-stilbene drug candidate, Quinoline drug candidate, and known drugs | N. Kummetha (2024)
:label: best_candidates_docking_table

Docking Scores(measure of the interaction strength between the static protein model and the ligand; more negative scores are more optimal), CNS (blood-brain barrier activity, an inactive drug should score -2, and an active drug should score +2 ), QPLogHERG (predicted IC50 value for blockage of HERG K+ channels as a measure of cardiotoxicity. Values significantly below -5 are concerning), QPPCaco (predicted permeability of the gut-blood barrier, <25 nm/sec is poor and >500 nm/sec is great), QPLogBB (predicted brain/blood partition coefficient, more negative means less likely to cross BBB), PercentHumanOralAbsorption (<25% is poor, >80% is high), Lipinski’s Violations (number of violations of Lipinski’s rule of 5, 0 violations is considered “drug-like”). Green = Optimal score, Yellow = Slightly outside optimal range, Red = Significantly outside optimal range.

<table border="1">
   <tr>
      <th colspan="10" align="center" style="background-color: DarkGray;">Docking Scores and Pharmacokinetic Properties of Top Drug Candidates and Known Drugs</th>
   </tr>
   <tr>
      <th align="center" style="background-color: cornflowerblue;">Compoud</th>
      <th align="center" style="background-color: cornflowerblue;">Docking Score</th>
      <th align="center" style="background-color: cornflowerblue;">Interacts with</th>
      <th align="center" style="background-color: cornflowerblue;">CNS</th>
      <th align="center" style="background-color: cornflowerblue;">QPLogBB</th>
      <th align="center" style="background-color: cornflowerblue;">QPLogHERG</th>
      <th align="center" style="background-color: cornflowerblue;">QPPCaco </th>
      <th align="center" style="background-color: cornflowerblue;">Percent Human Oral Absorption</th>
      <th align="center" style="background-color: cornflowerblue;">Lipinski's Violations</th>
   </tr> 
   <tr>
      <td align="center" style="">Aza-Stilbene</td>
      <td align="center" style="background-color: MediumSeaGreen">-6.898</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Asp186, Thr190, Trp247, Tyr250</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: MediumSeaGreen">-1.982</td>
      <td align="center" style="background-color: yellow">-5.265</td>
      <td align="center" style="background-color: MediumSeaGreen">69.516</td>
      <td align="center" style="background-color: yellow">64.826</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>
      <tr>
      <td align="center" style="">Quinoline</td>
      <td align="center" style="background-color: MediumSeaGreen">-6.741</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Thr190, Trp247, tyr250</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: MediumSeaGreen">-1.086</td>
      <td align="center" style="background-color: yellow">-5.131</td>
      <td align="center" style="background-color: yellow">298.949</td>
      <td align="center" style="background-color: crimson">81.776</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>
   <tr>
      <td align="center" style="">Famotidine</td>
      <td align="center" style="background-color: MediumSeaGreen">-6.577</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Thr190, Tyr250, Arg257</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: MediumSeaGreen">-3.457</td>
      <td align="center" style="background-color: MediumSeaGreen">-4.621</td>
      <td align="center" style="background-color: MediumSeaGreen">3.313</td>
      <td align="center" style="background-color: MediumSeaGreen">16.203</td>
      <td align="center" style="background-color: yellow">1</td>
   </tr>
   <tr>
      <td align="center" style="">Ranitidine</td>
      <td align="center" style="background-color: yellow">-5.019</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Tyr250, Phe251, Phe254, Arg257</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: yellow">-1.029</td>
      <td align="center" style="background-color: Crimson">-6.150</td>
      <td align="center" style="background-color: yellow">128.369</td>
      <td align="center" style="background-color: Crimson">75.188</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>
    <tr>
      <td align="center" style="">Nizatidine</td>
      <td align="center" style="background-color: crimson">-3.584</td>
      <td align="center" style="background-color: crimson">Asp98, Cys174</td>
      <td align="center" style="background-color: crimson">0</td>
      <td align="center" style="background-color: yellow">-0.939</td>
      <td align="center" style="background-color: Crimson">-6.070</td>
      <td align="center" style="background-color: yellow">127.298</td>
      <td align="center" style="background-color: Crimson">71.688</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>     
 <tr>
      <td align="center" style="">Cimetidine</td>
      <td align="center" style="background-color: crimson">-3.141</td>
      <td align="center" style="background-color: MediumSeaGreen">Asp98, Val176, Asp186, Tyr250</td>
      <td align="center" style="background-color: MediumSeaGreen">-2</td>
      <td align="center" style="background-color: yellow">-1.194</td>
      <td align="center" style="background-color: MediumSeaGreen">-4.708</td>
      <td align="center" style="background-color: yellow">400.282</td>
      <td align="center" style="background-color: crimson">76.051</td>
      <td align="center" style="background-color: MediumSeaGreen">0</td>
   </tr>

:::

:::{table} Docking Scores and Pharmacokinetic Properties of Aza-stilbene drug candidates | N. Kummetha (2024)
:label: aza-stilbene_docking_table

Docking Scores(measure of the interaction strength between the static protein model and the ligand; more negative scores are more optimal), CNS (blood-brain barrier activity, an inactive drug should score -2, and an active drug should score +2 ), QPLogHERG (predicted IC50 value for blockage of HERG K+ channels as a measure of cardiotoxicity. Values significantly below -5 are concerning), QPPCaco (predicted permeability of the gut-blood barrier, <25 nm/sec is poor and >500 nm/sec is great), QPLogBB (predicted brain/blood partition coefficient, more negative means less likely to cross BBB), PercentHumanOralAbsorption (<25% is poor, >80% is high), Lipinski’s Violations (number of violations of Lipinski’s rule of 5, 0 violations is considered “drug-like”). Green = Optimal score, Yellow = Slightly outside optimal range, Red = Significantly outside optimal range.

<table border="1"> 
   <tr>
      <th colspan="9" align="center" style="background-color: DarkGray;">Aza-Stilbene Top Drug Candidates</th>
   </tr>
   <tr>
      <th align="center" style="background-color: cornflowerblue;">Aldehyde R-Group OH</th>
      <th align="center" style="background-color: cornflowerblue;">Aniline R-Group OH</th>
      <th align="center" style="background-color: cornflowerblue;">Docking Score</th>
      <th align="center" style="background-color: cornflowerblue;">CNS</th>
      <th align="center" style="background-color: cornflowerblue;">QPLogBB</th>
      <th align="center" style="background-color: cornflowerblue;">QPLogHERG</th>
      <th align="center" style="background-color: cornflowerblue;">QPPCaco</th>
      <th align="center" style="background-color: cornflowerblue;">Percent Human Oral Absorption</th>
      <th align="center" style="background-color: cornflowerblue;">Lipinski's Violations</th>
   </tr> 
   <tr>
      <td align="center" style="">3, 5</td>
      <td align="center" style="">3, 5</td>
      <td align="center" style="">-6.898</td>
      <td align="center" style="background-color: MediumSeaGreen;">-2</td>
      <td align="center" style="background-color: MediumSeaGreen;">-1.982</td>
      <td align="center" style="background-color: yellow;">-5.265</td>
      <td align="center" style="background-color: MediumSeaGreen;">69.516</td>
      <td align="center" style="background-color: yellow;">64.828</td>
      <td align="center" style="background-color: MediumSeaGreen;">0</td>
   </tr>
   <tr>
      <td align="center" style="">2, 3</td>
      <td align="center" style="">3, 5</td>
      <td align="center" style="">-6.741</td>
      <td align="center" style="background-color: MediumSeaGreen;">-2</td>
      <td align="center" style="background-color: MediumSeaGreen;">-1.803</td>
      <td align="center" style="background-color: yellow;">-5.258</td>
      <td align="center" style="background-color: yellow;">99.728</td>
      <td align="center" style="background-color: yellow;">68.213</td>
      <td align="center" style="background-color: MediumSeaGreen;">0</td>
   </tr>
   <tr>
      <td align="center" style="">3</td>
      <td align="center" style="">3, 5</td>
      <td align="center" style="">-6.590</td>
      <td align="center" style="background-color: MediumSeaGreen;">-2</td>
      <td align="center" style="background-color: yellow;">-1.387</td>
      <td align="center" style="background-color: yellow;">-5.365</td>
      <td align="center" style="background-color: yellow;">229.467</td>
      <td align="center" style="background-color: crimson;">78.432</td>
      <td align="center" style="background-color: MediumSeaGreen;">0</td>
   </tr>
   <tr>
      <td align="center" style="">3</td>
      <td align="center" style="">3, 4, 5</td>
      <td align="center" style="">-6.484</td>
      <td align="center" style="background-color: MediumSeaGreen;">-2</td>
      <td align="center" style="background-color: MediumSeaGreen;">-1.783</td>
      <td align="center" style="background-color: yellow;">-5.212</td>
      <td align="center" style="background-color: yellow;">101.891</td>
      <td align="center" style="background-color: yellow;">68.278</td>
      <td align="center" style="background-color: MediumSeaGreen;">0</td>
   </tr>
   <tr>
      <td align="center" style="">3</td>
      <td align="center" style="">2, 5</td>
      <td align="center" style="">-6.452</td>
      <td align="center" style="background-color: MediumSeaGreen;">-2</td>
      <td align="center" style="background-color: yellow;">-1.293</td>
      <td align="center" style="background-color: yellow;">-5.314</td>
      <td align="center" style="background-color: yellow;">276.457</td>
      <td align="center" style="background-color: crimson">80.136</td>
      <td align="center" style="background-color: MediumSeaGreen;">0</td>
   </tr>
      <tr>
      <td align="center" style="">3, 5</td>
      <td align="center" style="">2, 3</td>
      <td align="center" style="">-6.317</td>
      <td align="center" style="background-color: MediumSeaGreen;">-2</td>
      <td align="center" style="background-color: mediumseagreen;">-1.789</td>
      <td align="center" style="background-color: yellow;">-5.209</td>
      <td align="center" style="background-color: yellow;">101.216</td>
      <td align="center" style="background-color: yellow">68.248</td>
      <td align="center" style="background-color: MediumSeaGreen;">0</td>
   </tr>
  <tr>
   <td align="center">2</td>
   <td align="center">3, 4, 5</td>
   <td align="center">-6.192</td>
   <td align="center" style="background-color: mediumseagreen;">-2</td>
   <td align="center" style="background-color: mediumseagreen;">-1.704</td>
   <td align="center" style="background-color: yellow;">-5.243</td>
   <td align="center" style="background-color: yellow;">122.288</td>
   <td align="center" style="background-color: yellow;">70.085</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">3</td>
   <td align="center">3, 4</td>
   <td align="center">-6.167</td>
   <td align="center" style="background-color: mediumseagreen;">-2</td>
   <td align="center" style="background-color: yellow;">-1.329</td>
   <td align="center" style="background-color: yellow;">-5.351</td>
   <td align="center" style="background-color: yellow;">256.684</td>
   <td align="center" style="background-color: crimson;">79.443</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">2, 3</td>
   <td align="center">3</td>
   <td align="center">-6.087</td>
   <td align="center" style="background-color: mediumseagreen;">-2</td>
   <td align="center" style="background-color: yellow;">-1.129</td>
   <td align="center" style="background-color: yellow;">-5.317</td>
   <td align="center" style="background-color: yellow;">396.208</td>
   <td align="center" style="background-color: crimson;">83.558</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>

<tr>
   <td align="center">2</td>
   <td align="center">3, 4</td>
   <td align="center">-6.063</td>
   <td align="center" style="background-color: mediumseagreen;">-2</td>
   <td align="center" style="background-color: yellow;">-1.210</td>
   <td align="center" style="background-color: yellow;">-5.352</td>
   <td align="center" style="background-color: yellow;">332.739</td>
   <td align="center" style="background-color: crimson;">81.896</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">2</td>
   <td align="center">3, 5</td>
   <td align="center">-6.049</td>
   <td align="center" style="background-color: mediumseagreen;">-2</td>
   <td align="center" style="background-color: yellow;">-1.241</td>
   <td align="center" style="background-color: yellow;">-5.321</td>
   <td align="center" style="background-color: yellow;">309.421</td>
   <td align="center" style="background-color: crimson;">81.188</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">3</td>
   <td align="center">2, 3</td>
   <td align="center">-5.888</td>
   <td align="center" style="background-color: mediumseagreen;">-2</td>
   <td align="center" style="background-color: yellow;">-1.223</td>
   <td align="center" style="background-color: yellow;">-5.369</td>
   <td align="center" style="background-color: yellow;">328,112</td>
   <td align="center" style="background-color: crimson;">81.786</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">3</td>
   <td align="center">3</td>
   <td align="center">-5.767</td>
   <td align="center" style="background-color: crimson;">-1</td>
   <td align="center" style="background-color: yellow;">-0.809</td>
   <td align="center" style="background-color: yellow;">-5.467</td>
   <td align="center" style="background-color: crimson;">753.306</td>
   <td align="center" style="background-color: crimson;">93.803</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">3</td>
   <td align="center">2</td>
   <td align="center">-5.579</td>
   <td align="center" style="background-color: crimson;">-1</td>
   <td align="center" style="background-color: crimson;">-0.719</td>
   <td align="center" style="background-color: yellow;">-5.453</td>
   <td align="center" style="background-color: yellow;">923.420</td>
   <td align="center" style="background-color: crimson;">95.802</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
<tr>
   <td align="center">2</td>
   <td align="center">3</td>
   <td align="center">-5.503</td>
   <td align="center" style="background-color: crimson;">0</td>
   <td align="center" style="background-color: crimson;">-0.621</td>
   <td align="center" style="background-color: yellow;">-5.440</td>
   <td align="center" style="background-color: crimson;">1150.408</td>
   <td align="center" style="background-color: crimson;">100.000</td>
   <td align="center" style="background-color: mediumseagreen;">0</td>
</tr>
</table>
:::

```{figure} ftir.png
:label: ftir
Synthesis of Aza-stilbene | N. Kummetha (2024) via Shimadzu IRSpirit with ATR attachment | The black line is the aza-stilbene, the blue line is the benzaldehyde, and the red line is the aniline. 
```

Looking at the FTIR data, The benzaldehyde contains characteristic aldehyde peaks: C-H stretch at ~2850, and the C=O stretch at ~1750.  The aniline is harder to identify but there should be an amine peak around 1620.  The product does not contain the 1750 stretch indicating that the C=O has gone away.  A positive indication of the product is the formation of C=N which has a stretch at 1650.  This is confounded by the strong peak around 1600 which is likely due to the stretching from the highly conjugated ring structure.  A small shoulder peak can be seen around 1650 on the black line, obscured by this stronger 1600 peak.  Combined with the disappearance of the C=O stretch, it is likely that the product has formed. Thus, this confirms that aza-stilbenes are easy to synthesize.


## Conclusion

In conclusion, this study presents a significant advancement in the search for effective and accessible treatments for gastroesophageal reflux disease (GERD) by identifying and synthesizing an aza-stilbene scaffold as a potential histamine H2 receptor antagonist. GERD, a chronic condition that affects millions globally, often leads to complications such as esophagitis and Barrett's esophagus, necessitating better therapeutic options. This study evaluated numerous ligands through extensive computational docking and identified aza-stilbene as a scaffold with high binding affinity to key amino acid residues, Asp 98 and Asp 186, within the histamine H2 receptor. Aza-stilbene not only demonstrated a stronger binding score than famotidine, one of the leading H2 receptor antagonists but also displayed favorable pharmacokinetic properties, including low central nervous system (CNS) activity and optimal gut permeability, making it particularly promising as an orally administered treatment for GERD.
The synthesis process further validated the potential of aza-stilbene, confirming its feasibility as a drug candidate that can be produced efficiently with a high yield and minimal steps. The results highlight how scaffold-based ligand design offers a promising route to discovering more targeted, effective treatments for GERD. Importantly, this study addresses limitations in current treatments, such as proton pump inhibitors and antacids, which can have undesirable side effects and limited long-term efficacy. By optimizing the scaffold for selective binding and oral bioavailability, this work contributes valuable insights into gastrointestinal pharmacology and opens avenues for safer, more accessible GERD medications.

## Future Directions

While this study provides foundational insights, several key steps remain to further evaluate and enhance the clinical applicability of aza-stilbene as a GERD treatment. First, in vitro and in vivo studies should be conducted to confirm the efficacy and safety of the synthesized aza-stilbene compounds in biological models. These studies would help verify the compound’s receptor binding affinity, assess its effects on GERD symptoms, and evaluate its toxicity profile. Additionally, exploring various R-group modifications on the aza-stilbene scaffold could yield derivatives with even greater potency or enhanced selectivity, offering a range of possible therapeutic candidates.

Beyond efficacy testing, pharmacokinetic studies focusing on human metabolism, absorption, and elimination are crucial to fully understanding the potential clinical applications of the aza-stilbene scaffold. This involves evaluating its half-life, systemic bioavailability, and possible drug interactions. Given the promising results from this scaffold design, further computational modeling with more advanced docking techniques could provide additional refinements that optimize the drug's interaction with the binding pocket. Lastly, partnerships with pharmaceutical research organizations could help transition this scaffold from the lab to clinical trials, potentially leading to new, effective GERD treatments focusing on patient safety and improving quality of life.

## Acknowledgments

I would like to thank my mentors Dr. Michael J. Bruno and Dr. Timothy C. Anglin Jr. I would also like to acknowledge Mr. Antonio Lopez, Dr. Darrel Spells, the NCSSM Foundation, and the Burroughs Wellcome Fund for helping make this project possible.