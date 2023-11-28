# A/B Testing in Healthcare

A pharmaceutical company has just completed a randomized controlled drug trial. To promote transparency and reproducibility of the drug's outcome.

The dataset provided contained five adverse effects, demographic data, vital signs, etc. The organization is primarily interested in the drug's adverse reactions. It wants to know if the adverse reactions, if any, are of significant proportions. It has asked you to explore and answer some questions from the data.

The dataset `drug_safety.csv` was obtained from [Hbiostat](https://hbiostat.org/data/) courtesy of the Vanderbilt University Department of Biostatistics. It contained five adverse effects: headache, abdominal pain, dyspepsia, upper respiratory infection, chronic obstructive airway disease (COAD), demographic data, vital signs, lab measures, etc. The ratio of drug observations to placebo observations is 2 to 1.

For this project, the dataset has been modified to reflect the presence and absence of adverse effects `adverse_effects` and the number of adverse effects in a single individual `num_effects`.

The columns in the modified dataset are: 

| Column | Description |
|--------|-------------|
|`sex` | The gender of the individual |
|`age` | The age of the individual |
|`week` | The week of the drug testing |
|`trx` | The treatment (Drug) and control (Placebo) groups | 
|`wbc` | The count of white blood cells |
|`rbc` | The count of red blood cells |
|`adverse_effects` | The presence of at least a single adverse effect |
|`num_effects` | The number of adverse effects experienced by a single individual |

The original dataset can be found [here](https://hbiostat.org/data/repo/safety.rda).

Here is the sample data:
| age  | sex    | trx     | week  | wbc       | rbc        | adverse_effects  | num_effects  |
|------|--------|---------|-------|-----------|------------|------------------|--------------|
|   51 | female | Placebo |     0 | 4.0999999 |  5.0999999 |        No        |            0 |
|   68 |  male  | Placebo |     2 | 6.0999999 | 4.30000019 |        No        |            0 |
|   51 |  male  | Placebo |     0 | 5.9000001 | 4.30000019 |        No        |            0 |
|   70 |  male  |   Drug  |    20 |      null |       null |        No        |            0 |
|   72 |  male  |   Drug  |    20 |      null |       null |        No        |            0 |

Based on that data, I have to perform hypothesis tests to determine if the adverse effects of a pharmaceutical drug are significant!

----------------
## Scenario 1 : Determine if the proportion of adverse effects differs significantly between the Drug and Placebo groups.

Define hypothesis assignment:

Where:

    H0: Proportion data between these group is the same.
    H1: There is differentiation proportion with those group.

Then we conclude:

    P-value for this test is : 0.9639333330262475.
    We fail to reject the null hypothesis.

## Scenario 2 : Find out if the number of adverse effects is independent of the treatment and control groups.

Define hypothesis assignment:

Where:

    H0: There is no relationship or association between the two variables being tested.
    H1: There is relationship or association between them.

Then we conclude:

    P-Value for these columns is 0.6150123339426765.
    We fail to reject the null hypothesis.

## Scenario 3 : Examine if there is a significant difference between the ages of the Drug and Placebo groups.

Define hypothesis assignment:

Where:

    H0: There is no significant difference between both groups.
    H1: There is significant difference between both groups.

Then we conclude:

    Mann-Whitney U Result:
        Statistic: 29149339.5
        p-value: 0.25696267004066287
        
    There is no evidence for rejecting the null hypothesis, accept H0.

## Authors

- [@dickyalsyah](https://www.github.com/dickyalsyah)

