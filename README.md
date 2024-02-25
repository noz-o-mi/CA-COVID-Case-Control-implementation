# Implementation Experience of the California COVID-19 Case Control Study

Paper: ***Mixed methods approach to examining the implementation experience of a phone-based survey for a SARS-CoV-2 test-negative case-control study in California***<br>
DOI: *pending*

Authors: Nozomi Fukui, MPH <sup>1,2,¶,^</sup>, Sophia S. Li, BS<sup>1,3,¶,^</sup>, Jennifer DeGuzman, MPH<sup>1,^</sup>, Jennifer F. Myers, MPH<sup>1</sup>, John Openshaw, MD<sup>1</sup>, Anjali Sharma, ScD<sup>4,5</sup>, James Watt, MD, MPH<sup>1</sup>, Joseph A. Lewnard, PhD<sup>2,6,7</sup>, Seema Jain, MD<sup>1</sup>, Kristin L. Andrejko, PhD<sup>1,3,&</sup>, Jake M. Pry, PhD, MPH,<sup>1,8,&</sup>, on behalf of the California COVID-19 Case-Control Study Team,<sup>1^</sup>

<sup>1</sup> California Department of Public Health, Richmond, CA, USA   <br>
<sup>2</sup> Division of Epidemiology and Biostatistics, School of Public Health, University of California, Berkeley, California, USA <br>
<sup>3</sup> College of Agricultural and Environmental Sciences, University of California, Davis, CA, USA <br>
<sup>4</sup> University of Washington, Hans Rosling Center, Global Health, Seattle, WA, USA  <br>
<sup>5</sup> The Centre for Infectious Disease Research in Zambia (CIDRZ), Lusaka, Zambia <br>
<sup>6</sup> Division of Infectious Diseases & Vaccinology, School of Public Health, University of California, Berkeley, California, USA <br>
<sup>7</sup> Center for Computational Biology, College of Engineering, University of California, Berkeley, California, USA <br>
<sup>8</sup> Department of Public Health Sciences, School of Medicine, University of California, Davis, California, USA  <br>

<sup>¶</sup> These authors contributed equally to the study's work.  <br>
<sup>&</sup> J.M.P and K.L.A are joint senior authors and contributed equally to this work. <br>

Corresponding Authors: <br>
Jake M. Pry, PhD, MPH <br>
E-mail: jmpry@ucdavis.edu  <br> 

Kristin L. Andrejko, PhD  <br>
Email: onp9@cdc.gov <br>


<sup>^</sup>Membership of the California COVID-19 Case-Control Study Team includes: </br>Adrian Cornejo, Amanda Lam, Amanda Moe, Amandeep Kaur, Anna Fang, Ashly Dyke, Camilla Barbaduomo, Christine Wan, Diana Nicole Morales Felipe, Diana Poindexter, Erin Xavier, Hyemin Park, Helia Samani, Jennifer DeGuzman, Jessica Ni, Julia Cheunkarndee, Mahsa Javadi, Maya Spencer, Michelle Spinosa, Miriam Bermejo, Monique Miller, Najla Dabbagh, Natalie Dassian, Nikolina Walas, Nozomi Fukui, Paulina Frost, Savannah Corredor, Shrey Saretha, Sophia S. Li, Timothy Ho, Vivian Tran, Yang Zhou, Yasmine Abdulrahim, Zheng Dong.


# Table of contents 

| **Folder** <br> `Files` | **Description**<br><br> | **Output**<br><br> |
| :----: | :- | :- |
| :floppy_disk:data <br> `raw.rdata` <br> `clean.rdata`| Raw and cleaned deidentified data used in the analysis and visualization of this paper. | <p align="center">-</p>  |
| :broom:processing <br> `cleaning.R` | Code used to clean the raw data and prepare the analytic dataset. | Cleaned data file found in the data folder. |
| :mag_right:analysis <br> `filename` | | Model files located in the models folder. |
| :computer:models <br> `amod1_glmer`<br> `amod1_gee`<br>`amod1_geem`<br>`amod1_glm`<br> `amod1_x_glmer`<br>`amod1_x_gee`<br>`amod1_x_geem`<br>`amod1_x_glm` <br><br> `amod2_glmer`<br> `amod2_gee`<br>`amod2_geem`<br>`amod2_glm` <br> `amod2_x_glmer`<br>`amod2_x_gee`<br>`amod2_x_geem`<br>`amod2_x_glm` <br><br> | Model outputs generated and used in analysis. | <p align="center">-</p> |
| :bar_chart:[tables-figs](https://github.com/noz-o-mi/CA-COVID-Case-Control-implementation/tree/main/tables-figs) <br><br>  `Table1.xlsx` <br> `Table2.xlsx` <br><br>  `Fig1.pdf` <br> `Fig2.pdf` <br> `Fig3.pdf` | Main tables and figures in the paper.  | **Table 1.** Characteristics of SARS-CoV-2 test-seekers in California who were called, answered the phone, consented to participate, and completed the telephone survey. <br>**Table 2.** Interviewer experience survey quotes. <br><br>  **Fig 1.** Process diagram for recruitment, onboarding, and training interviewers. <br>**Fig 2.** Study timeline mapped against weekly enrollment trends by case-control status. <br>**Fig 3.** Predictors of participants answering the telephone and consenting to participate in the California COVID-19 Case Control study. | 
| :card_file_box:[supplement](https://github.com/noz-o-mi/CA-COVID-Case-Control-implementation/tree/main/supplement) <br><br> `S01-Table.xlsx` <br> `S02-Table.xlsx` <br>  `S03-Table.xlsx` <br>  `S04-Table.xlsx` <br>  `S05-Table.xlsx` <br>  `S06-Table.xlsx` <br>  `S07-Table.xlsx` <br>  `S08-Table.xlsx` <br><br>  `S01-Fig.pdf` <br> `S02-Fig.pdf` <br> `S03-Fig.pdf` <br> `S04-Fig.pdf` <br> `S05-Fig.pdf` <br> `S06-Fig.pdf` <br> `S07-Fig.pdf` <br> `S08-Fig.pdf` <br> `S09-Fig.pdf` <br> `S10-Fig.pdf` <br> `S11-Fig.pdf` <br><br> `S01-Item.docx` <br> `S02-Item.docx` <br>| Tables, figures, and items that provide supporting information to the paper. |  **S1 Table.** Characteristics of interviewers. <br> **S2 Table.** Model comparison using Bayesian Information Criterion. <br> **S3 Table.** Predictors of answering the telephone and consenting to participate in a case-control study using mixed effects logistic regression. <br> **S4 Table.** Predictors of answering the telephone, consenting to participate in a case-control study, and ultimately enrolling in the study, interacted with SARS-CoV-2 test result, using mixed effects logistic regression. <br> **S5 Table.** Reasons for refusal to participate in the case-control study. <br> **S6.** Predictors of citing time as a reason for refusing participation using mixed effects logistic regression. <br> **S7 Table.** Characteristics of California population and composition of SARS-CoV-2 test seekers in California throughout the study period. <br> **S8 Table.** 2020 U.S. Census Bureau American Community Survey Demographics of the State of California. <br> <br> **S1 Fig.** Study regions. <br> **S2 Fig.** Sampling process. <br> **S3 Fig.** Enrollment of participants in the California COVID-19 Case-Control Study. <br> **S4 Fig.** Calls to successfully enroll a case (SARS-CoV-2 positive) or control (SARS-CoV-2 negative). <br> **S5 Fig.** Calls to enroll one case or control over the study period, overlayed with total cases reported across California each week. <br> **S6 Fig.** Predominant reasons cited for not consenting to participate in the study, over the course of the study. <br> **S7 Fig.** Comparison of household income and race/ethnicity demographics between the study population and California population. <br> **S8 Fig.** Agreement with social distancing, face mask use, general anxiety about COVID-19, and attendance at indoor public settings month of study among participants who completed the survey. <br> **S9 Fig.** Proportion of participants reporting attendance at indoor settings over the study period. <br> **S10 Fig.** Area graph of population who was excluded due to previous SARS-CoV-2 positive over time. <br> **S11 Fig.** Interviewer encounters with grief, anger, and demand for social service resources. <br> <br> **S1 Item.** Survey questions and guide. <br> **S2 Item.** Interviewer experience survey. | 
