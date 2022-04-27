# Project 1: Analysing Trends in SAT Participation Rate and their Relationship with SAT Scores


## Problem Statement:
- Analyse trends in SAT participation rate to identify states where participation rates have declined significantly over the years; and their relationship with SAT scores.
---

## Background:
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). 

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

### Datasets selected:
- sat_2017.csv
- sat_2018.csv
- sat_2019.csv 

- The datasets provides data on the participation rate of high school students in each state who took the SAT in 2017, 2018 and 2019, and their average scores aggregated at state-level. It will be used to identify states where participation rates have declined significantly over the years.
---

## Additional Information:

- SAT Score Components: The SAT is scored out of 1600 and is a combination of the section scores (800 for reading/writing and math respectively). The essay is optional and will not be factored into the overall SAT score. The essay scores will be shown separately on the report [(source)](https://www.khanacademy.org/test-prep/sat/new-sat-tips-planning/new-sat-about-sat/a/scoring-on-the-redesigned-sat).
- SAT is not compulsory for all States and requires a registration fee, hence some States may have lower participation rates [(source)](https://collegereadiness.collegeboard.org/sat/register/fees).
- Students can take the SAT multiple times, and most colleges consider a student's highest SAT score when making admission decisions. And if they get a total SAT score by at least 100 points higher than their previous SAT score, they could be eligible to earn an Improve Your Score scholarship worth 2,000 dollars [(source)](https://parents.collegeboard.org/faq/how-many-times-can-student-take-sat-when-should-take). 
- Many schools use a process called "superscoring", which combines a student's highest Math section score with their highest Evidence-Based Reading and Writing section score, even if those scores are from different test dates, to come up with the student's total SAT score [(source)](https://parents.collegeboard.org/faq/how-many-times-can-student-take-sat-when-should-take). 

- One way to increase SAT participation rate is to cover all or part of exam fees: fee waivers are available for low‐income students, particularly those to whom exam fees would present an undue burden. The College Board also provides a free tool for school counselors to track students’ progress in registering for the SAT and using fee waivers. The College Board reports that fee waivers are more common than ever and supported 23 percent of SAT takers in 2013. However, obtaining a fee waiver does not guarantee test participation. The College Board found that the two most common reasons for test day absenteeism among fee‐waiver recipients were 1) feeling unprepared and 2) not having transportation. Fee‐waiver recipients indicated that the school counselor was the most important influence in deciding whether to register, and they would have been more likely to be present on test day with more encouragement, increased accessibility to test centers, and more preparation." - [(source)](https://www.hanoverresearch.com/media/Best-Practices-to-Increase-SAT-Participation-1.pdf)


**States that require the SAT [(source)](https://blog.collegevine.com/states-that-require-sat/)**:
 - Colorado high school juniors have been required to take the SAT since the 2016-2017 school year and sophomores are administered the PSAT. 
 - In the 2015-2016 academic year, taking the SAT became a graduation requirement for Connecticut high schoolers, replacing the Smarter Balanced Assessment Consortium (SBAC) exam. 
 - Delaware has provided the SAT free of charge to students since 2011, but in 2016, it replaced its Smarter Balanced Assessment exam with the SAT. 
 - Idaho students must take either the SAT or ACT before the completion of 11th grade—the state offers the SAT for free to high school juniors and the PSAT for free to sophomores.
 - As of 2017, all Illinois juniors are required to take the SAT. 
 - The SAT is a requirement in the state of Maine—the state still provides the exam for free to third-year high school students. 
 - Michagan moved away from the ACT and began administering the SAT in 2016. 
 - In 2016, New Hampshire transitioned from using Smarter Balanced exams to the SAT. 
 - All Ohio juniors are required to take either a state-funded ACT or SAT exam. 
 - In 2018, the SAT and PSAT became graduation requirements in Rhode Island. 
 - The SAT is mandatory for all West Virginia 11th graders with the exception of students with cognitive disabilities who are given the West Virginia Alternate Assessment.
 - Florida offers free SAT for Florida Public High School Students, and has compulsory SAT requirement [(source)](https://www.orlandosentinel.com/news/education/os-fsa-algebra-passing-scores-alternative-20180330-story.html).

**States that provide SAT for free**:
 - Washington, D.C., does not require high schoolers to take the SAT, but it has provided the exam—as well as the PSAT—for free since 2013. 
 - Oklahoma provides funding for every public school junior to take either the ACT or SAT for free on a specific testing date.
 - South Carolina does not require either the SAT or the ACT; however, it provides both exams to 11th graders at no cost.  
 - All Tennessee high school students in 11th grade are required to take either the SAT or ACT—school districts are given the choice of which test to provide or may offer both exams. 
---

## Data Dictionary:

|Feature|Type|Dataset|Description|
|---|---|---|---| 
|state|*object*|modified_sat_merged.csv|States where the high school graduates who took the SAT reside in.| 
|participation_rate_2017|*float*|modified_sat_merged.csv|Percentage (in 2 decimal places) of the state's high school graduates who took the SAT in 2017, e.g. 0.25 means 25%.| 
|ebrw_score_2017|*integer*|modified_sat_merged.csv|Average Evidence-Based Reading and Writing (EBRW) score (200-800) of high school graduates by state in 2017.| 
|math_score_2017|*integer*|modified_sat_merged.csv|Average Math score (200-800) of high school graduates by state in 2017.|
|total_score_2017|*integer*|modified_sat_merged.csv|Average Total (EBRW + Math) score (400-1,600) of high school graduates by state in 2017.| 
|participation_rate_2018|*float*|modified_sat_merged.csv|Percentage (in 2 decimal places) of the state's high school graduates who took the SAT in 2018, e.g. 0.25 means 25%.| 
|ebrw_score_2018|*integer*|modified_sat_merged.csv|Average Evidence-Based Reading and Writing (EBRW) score (200-800) of high school graduates by state in 2018.| 
|math_score_2018|*integer*|modified_sat_merged.csv|Average Math score (200-800) of high school graduates by state in 2018.|
|total_score_2018|*integer*|modified_sat_merged.csv|Average Total (EBRW + Math) score (400-1,600) of high school graduates by state in 2018.| 
|participation_rate_2019|*float*|modified_sat_merged.csv|Percentage (in 2 decimal places) of the state's high school graduates who took the SAT in 2019, e.g. 0.25 means 25%.| 
|ebrw_score_2019|*integer*|modified_sat_merged.csv|Average Evidence-Based Reading and Writing (EBRW) score (200-800) of high school graduates by state in 2019.| 
|math_score_2019|*integer*|modified_sat_merged.csv|Average Math score (200-800) of high school graduates by state in 2019.|
|total_score_2019|*integer*|modified_sat_merged.csv|Average Total (EBRW + Math) score (400-1,600) of high school graduates by state in 2019.|
|delta_1718|*float*|modified_sat_merged.csv|Percentage change (in 2 decimal places) in state's participation rate from 2017 to 2018.| 
|delta_1819|*float*|modified_sat_merged.csv|Percentage change (in 2 decimal places) in state's participation rate from 2018 to 2019.| 

---

## Findings:
- North Dakota, Mississippi, and Iowa had the lowest participation rate of 2% in 2017. Their participation rates remained stable over the years, ranging from 2-3%. 
- The states with the lowest participation rate also have state average scores that are above the overall aggregated score in 2017 (overall average in 2017: 1,127 (total), 558 (math), 570 (ebrw)), suggesting an inverse relationship between participation rate and scores.

- Michigan, Connecticut, Delaware, and District of Columbia had the highest participation rate of 100% in 2017. This means that every high school graduate in those states took the SAT.
- Comparing across years, Michigan, Connecticut and Delaware had 100% participation rate for all 3 years, as SAT is compulsory for these states.
- The participation rate for District of Columbia and New Hampshire remained stable over the years, consistently >90%.
- The states with the highest participation rate also have state average scores that are below the overall aggregated score in 2017. The 2017 data suggests an inverse relationship between participation rate and scores.
- Similarly, the 2018 and 2019 data suggests an inverse relationship between participation rate and scores as states with lowest participation rates have state average score that are above the overall aggregated score.

- Florida and District of Columbia (DC)'s participation rate dropped by more than 5 percentage points between 2017 and 2018. Participation rate in Florida seems to flucuate over the years, with a 27 percentage point drop from 83% in 2017 to 56% in 2018, then a 44 percentage point increase to full participation in 2019 as the state had made SAT compulsory subsequently. For DC, even though there was a drop, the participation rate remains high (>90%) over the years.
- Illinois and Colorado's participation rate increased significantly by about 90 percentage points from 2017 to 2018. This suggests that it is possible to change behaviour and boost SAT participation rates.

---

## Conclusions/Recommendations:
- Overall, the participation rate for the SAT have increased over the years. However, there are still states with consistently low participation rate. This could be because the SAT involves a cost, and students do not see the incentive/benefits of taking the SAT. However, there are no states with significant decline in participation rate that requires immediate intervention.
- There is an inverse relationship between SAT scores and participation rates. Lower participation rate typically have higher state average score, and vice versa. This is likely due to biased data in states with low participation rate, as the students who took the test are probably well prepared hence applied for the SAT voluntarily. <br>


- There is merit in boosting SAT participation rate as it can be used as an objective measure of students' performance on a national level. Grading by GPA might not be fully fair as different schools have varying assessment criteria. 
- To boost participation rate, the College Board may wish to consider the following:
1. Make SAT compulsory; or 
2. Provide the SAT for free/at a subsidised rate; or
3. Dedicate some class time to guide students on SAT preparations/resources; or
4. Highlight the benefits of SAT to students, e.g. SAT has a section on Math which will be beneficial for students who are aiming to enter a college major on Statistics.
- If the participation rate for all states are high, the College Board will be able to get data that is representative of the population and have a better understanding of states' performance so that additional resources could be allocated, where necessary. 
