# Implementation Experience of the California COVID-19 Case Control Study

Paper: ***Mixed methods approach to examining the implementation experience of a phone-based survey for a SARS-CoV-2 test-negative case-control study in California***<br>
DOI: *pending* <br>
Context: Analysis and manuscript preparation took place in 2022 - 2023 <br>

Authors: Nozomi Fukui, MPH <sup>1,2,¶,^</sup>, Sophia S. Li, BS<sup>1,3,¶,^</sup>, Jennifer DeGuzman, MPH<sup>1,^</sup>, Jennifer F. Myers, MPH<sup>1</sup>, John Openshaw, MD<sup>1</sup>, Anjali Sharma, ScD<sup>4,5</sup>, James Watt, MD, MPH<sup>1</sup>, Joseph A. Lewnard, PhD<sup>2,6,7</sup>, Seema Jain, MD<sup>1</sup>, Kristin L. Andrejko, PhD<sup>1,3,&</sup>, Jake M. Pry, PhD, MPH,<sup>1,8,&</sup>, on behalf of the California COVID-19 Case-Control Study Team,<sup>1^</sup>

<sup>1</sup> California Department of Public Health, Richmond, California, USA   <br>
<sup>2</sup> Division of Epidemiology and Biostatistics, School of Public Health, University of California, Berkeley, California, USA <br>
<sup>3</sup> College of Agricultural and Environmental Sciences, University of California, Davis, California, USA <br>
<sup>4</sup> University of Washington, Hans Rosling Center, Global Health, Seattle, Washington, USA  <br>
<sup>5</sup> The Centre for Infectious Disease Research in Zambia (CIDRZ), Lusaka, Zambia <br>
<sup>6</sup> Division of Infectious Diseases & Vaccinology, School of Public Health, University of California, Berkeley, California, USA <br>
<sup>7</sup> Center for Computational Biology, College of Engineering, University of California, Berkeley, California, USA <br>
<sup>8</sup> Department of Public Health Sciences, School of Medicine, University of California, Davis, California, USA  <br>

<sup>¶</sup> These authors contributed equally to the study's work.  <br>
<sup>&</sup> J.M.P and K.L.A are joint senior authors and contributed equally to this work. <br>

<sup>^</sup>Membership of the California COVID-19 Case-Control Study Team includes: </br>Adrian Cornejo, Amanda Lam, Amanda Moe, Amandeep Kaur, Anna Fang, Ashly Dyke, Camilla Barbaduomo, Christine Wan, Diana Nicole Morales Felipe, Diana Poindexter, Erin Xavier, Hyemin Park, Helia Samani, Jennifer DeGuzman, Jessica Ni, Julia Cheunkarndee, Mahsa Javadi, Maya Spencer, Michelle Spinosa, Miriam Bermejo, Monique Miller, Najla Dabbagh, Natalie Dassian, Nikolina Walas, Nozomi Fukui, Paulina Frost, Savannah Corredor, Shrey Saretha, Sophia S. Li, Timothy Ho, Vivian Tran, Yang Zhou, Yasmine Abdulrahim, Zheng Dong. <br>


# Table of contents 

<table>
<tr>
  <td valign="top" width="15%">
    <h2 align="center">Folder</h3>
    <p align="center"><code>File</code></p>
  </td>
  <td valign="top" width="25%">
    <h2 align="center">Description</h3>
  </td>
  <td valign="top" width="60%">
    <h2 align="center">Output</h3>
  </td>
</tr> 
  <tr>
    <td valign="top">
      <h4 align="center"> :floppy_disk: data </h4>
      <p align="center"><code>raw.rdata</code> <br> <code>clean.rdata</code><br> <code>codebook.xlsx</code></p>
    </td>
    <td>
      Raw and cleaned deidentified data used in the analysis and visualization of this paper, as well as accompanying codebook.
    </td>
    <td valign="top">
      <p align="center">-</p>
    </td>
  </tr>
  <tr>
     <td valign="center">
       <h4 align="center"> :broom: processing </h4>
       <p align="center"><code>cleaning.R</code></p>
    </td>
    <td>
      Code used to clean the raw data and prepare the analytic dataset.
    </td>
    <td valign="center">
      Cleaned data file found in the data folder.
    </td>
  </tr>
  <tr>
     <td valign="center">
       <h4 align="center"> :mag_right: analysis </h4>
       <p align="center"><code>filename</code></p>
    </td>
    <td>
       ...
    </td>
    <td valign="center">
      Model files located in the models folder.
    </td>
  </tr>
  <tr>
     <td valign="center">
      <h4 align="center"> :computer: models</h4>
       <p align="center"><code>amod1_glmer</code><br><code>amod1_gee</code><br><code>amod1_geem</code><br><code>amod1_glm</code><br><code>amod1_x_glmer</code><br><code>amod1_x_gee</code><br><code>amod1_x_geem</code><br><code>amod1_x_glm</code><br><br><code>amod2_glmer</code><br><code>amod2_gee</code><br><code>amod2_geem</code><br><code>amod2_glm</code><br><code>amod2_x_glmer</code><br><code>amod2_x_gee</code><br><code>amod2_x_geem</code><br><code>amod2_x_glm</code><br><br></p>
    </td>
    <td valign="top">
       <br>Model outputs generated and used in analysis. "amod" indicates an adjusted model. "x" indicates an interaction was accounted for. "glmer" refers to generalized linear mixed-effects models. "glm" refers to generalized linear fixed-effects models. "gee" and "geem" indicate generalized estimating equations.
    </td>
    <td align="center">-</td>
  </tr>
  <tr>
     <td valign="top">
      <h4 align="center" valign="top"> :bar_chart:<a href="https://github.com/noz-o-mi/CA-COVID-Case-Control-implementation/tree/main/tables-figs">tables-figs</a></h4>
       <p align="center"><code>Table1.xlsx</code><br><code>Table2.xlsx</code><br><br><code>Fig1.pdf</code><br><code>Fig2.pdf</code><br><code>Fig3.pdf</code></p>
    </td>
    <td valign="top">
       <br>Main tables and figures in the paper. 
    </td>
    <td valign="center">
      <br>
      <b>Table 1.</b> Characteristics of SARS-CoV-2 test-seekers in California who were called, answered the phone, consented to participate, and completed the telephone survey. <br><b>Table 2.</b> Interviewer experience survey quotes. <br><br>
      <b>Fig 1.</b> Process diagram for recruitment, onboarding, and training interviewers. <br>
      <b>Fig 2.</b> Study timeline mapped against weekly enrollment trends by case-control status. <br>
      <b>Fig 3.</b> Predictors of participants answering the telephone and consenting to participate in the California COVID-19 Case Control study. 
    </td>
  </tr>
  <tr>
     <td valign="top">
      <h4 align="center" valign="top"> :card_file_box:<a href="https://github.com/noz-o-mi/CA-COVID-Case-Control-implementation/tree/main/supplement">supplement</a></h4>
       <p align="center"><code>S01-Table.xlsx</code><br><code>S02-Table.xlsx</code><br><code>S03-Table.xlsx</code><br><code>S04-Table.xlsx</code><br><code>S05-Table.xlsx</code><br><code>S06-Table.xlsx</code><br><code>S07-Table.xlsx</code><br><code>S08-Table.xlsx</code><br><br><code>S01-Fig.pdf</code><br><code>S02-Fig.pdf</code><br><code>S03-Fig.pdf</code><br><code>S04-Fig.pdf</code><br><code>S05-Fig.pdf</code><br><code>S06-Fig.pdf</code><br><code>S07-Fig.pdf</code><br><code>S08-Fig.pdf</code><br><code>S09-Fig.pdf</code><br><code>S10-Fig.pdf</code><br><code>S11-Fig.pdf</code><br><br><code>S01-Item.docx</code><br><code>S02-Item.docx</code><br>
    </td>
    <td valign="top">
       <br>Tables, figures, and items that provide supporting information to the paper.
    </td>
    <td valign="center">
      <br>
      <b>S1 Table.</b> Characteristics of interviewers. <br> 
      <b>S2 Table.</b> Model comparison using Bayesian Information Criterion. <br> 
      <b>S3 Table.</b> Predictors of answering the telephone and consenting to participate in a case-control study using mixed effects logistic regression. <br> 
      <b>S4 Table.</b> Predictors of answering the telephone, consenting to participate in a case-control study, and ultimately enrolling in the study, interacted with SARS-CoV-2 test result, using mixed effects logistic regression. <br> 
      <b>S5 Table.</b> Reasons for refusal to participate in the case-control study. <br> 
      <b>S6.</b> Predictors of citing time as a reason for refusing participation using mixed effects logistic regression. <br> 
      <b>S7 Table.</b> Characteristics of California population and composition of SARS-CoV-2 test seekers in California throughout the study period. <br> 
      <b>S8 Table.</b> 2020 U.S. Census Bureau American Community Survey Demographics of the State of California. <br> <br> 
      <b>S1 Fig.</b> Study regions. <br> 
      <b>S2 Fig.</b> Sampling process. <br> 
      <b>S3 Fig.</b> Enrollment of participants in the California COVID-19 Case-Control Study. <br> 
      <b>S4 Fig.</b> Calls to successfully enroll a case (SARS-CoV-2 positive) or control (SARS-CoV-2 negative). <br> 
      <b>S5 Fig.</b> Calls to enroll one case or control over the study period, overlayed with total cases reported across California each week. <br> 
      <b>S6 Fig.</b> Predominant reasons cited for not consenting to participate in the study, over the course of the study. <br> 
      <b>S7 Fig.</b> Comparison of household income and race/ethnicity demographics between the study population and California population. <br> 
      <b>S8 Fig.</b> Agreement with social distancing, face mask use, general anxiety about COVID-19, and attendance at indoor public settings month of study among participants who completed the survey. <br> 
      <b>S9 Fig.</b> Proportion of participants reporting attendance at indoor settings over the study period. <br> 
      <b>S10 Fig.</b> Area graph of population who was excluded due to previous SARS-CoV-2 positive over time. <br> 
      <b>S11 Fig.</b> Interviewer encounters with grief, anger, and demand for social service resources. <br> <br> 
      <b>S1 Item.</b> Survey questions and guide. <br> 
      <b>S2 Item.</b> Interviewer experience survey. 
    </td>
  </tr>
</table>


## Disclaimer
The findings and conclusions in this article are those of the author(s) and do not necessarily represent the views or opinions of the California Department of Public Health or the California Health and Human Services Agency.

