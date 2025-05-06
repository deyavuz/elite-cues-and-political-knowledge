## 🧠 Political Knowledge and Elite Cue Effects: A Meta-Analytic Investigation

**Author**: Defne Ece Yavuz

This repository contains all analysis code, figures, and supplementary materials for the Independent Research Project titled:

> **“Prepared to Choose Wisely?”: Elite Cues, Political Knowledge, and the Boundaries of Democratic Decision-Making**
> 
> BSc Psychological and Behavioural Science, The London School of Economics and Political Science

## 📘 Project Description

This study investigates how political knowledge moderates the magnitude and variability of party elite cue effects on public policy attitudes. Drawing on heuristic processing and motivated reasoning frameworks, it uses location-scale meta-analytic modelling to analyse data from 1,730 U.S. adults exposed to elite cue treatments across 34 political issues (originally collected by Tappin, 2023).

In addition to a confirmatory test of knowledge as a moderator, the study includes an exploratory analysis examining the influence of partisanship on elite cue responsiveness.

## 💻 Replicating the Code

Requirements:
- R (≥ 4.1.0)
- RStudio (recommended)

1) Install all dependencies with:

```r
install.packages(c("tidyverse", "metafor", "broom", "ggplot2"))
```

2) Clone the repository
   
```bash
git clone https://github.com/yourusername/elite-cue-knowledge-meta.git
```

3) Open the .Rds file

RStudio/VSCode > Open File > 2 - Data Analysis and Visualisation.Rmd

4) Replace the readRDS() path with the location of your own copy of data_party_cues.rds.

## 📖 Codebook, as adapted from Tappin (2023)
Variables description:

pid
> Subject id

Finished
> Did Qualtrics record the subject as finishing the survey? 1 = yes, 0 = no

continue_check
> Did the subject say they would complete the survey (a pre-treatment question)? 1 = no, 2 = yes

word_captcha
> Pre-treatment attention check, "ehllo" is the correct response

age
> In years

gender
> 1 = male, 2 = female, 3 = other

education
> 1 = No formal schooling

> 2 = Left school before 12th grade (did not graduate)

> 3 = Graduated high school

> 4 = Attended college but did not graduate

> 5 = Graduated college with Associate (2-year) degree

> 6 = Graduated college with Bachelor's (4-year) degree

> 7 = Graduated college with Master's degree

> 8 = Graduated college with Doctoral degree

> 9 = Other

ethnicity
> 1 = White/Caucasian

> 2 = Black or African American

> 3 = Asian

> 4 = American Indian or Alaska Native

> 5 = Native Hawaiian or Pacific Islander

> 6 = Latino or Hispanic

> 7 = Other

pol_party
> 1 = Strong Democrat

> 2 = Democrat

> 3 = Lean Democrat

> 4 = Independent/Don't know

> 5 = Lean Republican

> 6 = Republican

> 7 = Strong Republican

party_forced
> If they had to choose, which party out of Republican and Democrat would the subject prefer to be in power in the US?

> Question was only asked if pol_party == 4

> 1 = Democratic Party

> 2 = Republican Party

party_bin
> Binary variable for Democrat/Republican preference

obamatrump
> Preference for Barack Obama versus Donald Trump
> 1 = Definitely Obama

> 2 = Obama

> 3 = Probably Obama

> 4 = Neither/Don't know

> 5 = Probably Trump

> 6 = Trump

> 7 = Definitely Trump

item
> Policy item index

item_text
> Policy item text

cue
> Randomization of party elite cue on this item; 0 = no cue, 1 = cue

obama_binary
> Position of Barack Obama on the item, according to isidewith.com

trump_binary
> Position of Donald Trump on the item, according to isidewith.com

policy_group
> Policy domain of item, according to isidewith.com

policy_item_order
> Order in which the subject saw their policy items

outcome 
> The scale anchor depended on the specific item

> 1 = Definitely Not; Definitely Decrease; Definitely Less; Definitely Pro-life

> 2 = No; Decrease; Less; Pro-life

> 3 = Probably Not; Probably Decrease; Probably Less; Probably Pro-life

> 4 = Not sure / Need more information

> 5 = Probably Yes; Probably Increase; Probably More; Probably Pro-choice

> 6 = Yes; Increase; More; Pro-choice

> 7 = Definitely Yes; Definitely Increase; Definitely More; Definitely Pro-choice

outcome_recode
> outcome is recoded such that all party elite cue ATEs are expected >0

outcome_recode_01
> outcome_recode scaled to lie from 0 to 1

item_label
> Abbreviated policy issue name for plotting

order_variable
> The order in which the policy issue item was answered

pk_sum
> 7 questions on US politics, participants scaled from 1-7 based on correct responses

> pk1. Whose responsibility is it to decide if a law is constitutional or not? = The President; Congress; The Supreme Court

> pk2. Whose responsibility is it to nominate judges to Federal Courts? = The President; Congress; The Supreme Court

> pk3. Who is the current leader of the Conservative Party of Great Britain? Is it: = David Cameron; Jeremy Corbyn; Tony Hayward; Boris Johnson

> pk4. Do you know what job or political office is currently held by Nancy Pelosi? Is it: = Speaker of the House; Treasury Secretary; Senate Majority Leader; Justice of the Supreme Court; Governor of New Mexico

> pk5. Do you know what job or political office is currently held by Steve Mnuchin? Is it: = Attorney General; Justice of the Supreme Court; Treasury Secretary; House Republican Leader; Secretary of State

> pk6. Do you know what job or political office is currently held by Neil Gorsuch? Is it: = Senator; Justice of the Supreme Court; Solicitor General; Head of the EPA

> pk7. How many years is one full term for a U.S. Senator? = 4 years; 6 years; 5 years; 2 years

nfc_mean
> Need for cognition, adapted from Cacioppo et al., 1984

## 👩‍🎓 Acknowledgements
Thank you to my project supervisor Dr Ben Tappin for his continuous support and intellectual guidance;

Thank you to the LSE Department of Psychological and Behavioural Sciences for three amazing undergraduate years;

Thank you to my flatmate Olivia and friend Hannah, for their brutal proof-reading and motivating presence;

And finally, thank you to my mom, İlknur, and dad, Murat, for always supporting, loving, and being there for me. I couldn't have done it without you guys!
