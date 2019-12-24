1. An investigator would like to conduct a study to understand whether the group intervention (i.e., the intervention will be delivered in group sessions) they developed can successfully reduce the number of unprotected sex occasions for MSM (men had sex with men) population. They plan to recruit participants and randomize them to two study arms: one intervention arm and one control arm. The plan is to conduct the intervention in an average group size of 11 and follow the subjects for 6 months. The primary outcome for the study is defined as the change of number unprotected sex occasions (in the previous 3 months prior to interview) from baseline to 6 months after intervention. From their previous pilot study without group intervention, they found the standard deviation for that change score was 10 occasions, they had a 90% retention rate, a cross-over rate of about 5% for both groups.
==================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

(1) Suppose they would like to plan the study using the information obtained from the pilot study and aim to have 80% power to detect a difference of 7 occasions in a two-sided t-test at alpha=.05 level, what is the total sample size they need for the study assuming equal sample size for the two intervention arms? In your answers to the questions, please make sure you also explain why you choose such design parameters. If the pilot study did not obtain some design parameter you think you need for sample size calculation, you can assume a number and explain/justify how you obtain the information.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Based on this two-sample two-sided t-test design, we first assume that:

-   intervention and control group have the same s.d. as pilot study
    group, because they all draw from the same population

-   intra-class correlation (ICC) = 0.01, because we got a relatively
    large average cluster size (*n*<sub>*W*</sub>)

We then calculate the designed sample size we need

$$
\\begin{split}
D 
&= (Z\_{\\alpha/2} + Z\_{\\beta})\\sigma\\sqrt{\\frac{1}{n\_{T}} + \\frac{1}{n\_{C}}} \\\\
&= (Z\_{\\alpha/2} + Z\_{\\beta})\\sigma\\sqrt{\\frac{2}{n}} \\\\
where: \\\\
&D = 7 \\\\
n &= n\_{T} = n\_{C} \\\\
\\alpha &= 0.05, Z\_{0.025} = 1.96 \\\\
\\beta &= 0.8, Z\_{0.8} = 0.84 \\\\
\\sigma &= 10
\\end{split}
$$

Finally, we calculate the final `n` we need based on retention and ICC:

-   get designed n

-   adjust for ICC: *V**I**F* = 1 + (*n*<sub>*W*</sub> − 1)*I**C**C*,
    *n*′=*n* ⋅ *V**I**F*

-   adjust for retention: *n*″=*n*′/0.9

-   adjust for cross-over:
    $n''' = \\frac{n''}{(1 - p\_{T} - p\_{C}) ^ 2}$

We calculate the final *n*‴= 48.285 , so in total the sample size we
need ≈ 98.

(2) If the investigator followed your recommendation to choose the design parameters, and a reviewer of this grant proposal came back and questioned your choice of effect size by saying “For this type of intervention, the effect size is usually smaller than that (i.e., 7 occasions).” How do you response to such critique?
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Based on "minimal clinical meaningful worthwhile", if we found the true
effect size smaller than DA, than we shouldn't consider it worthwhile to
conduct the study.

(3) If another reviewer had completely different opinion by saying “You had assumed a too small effect size, the actual effect should be bigger than that. I don’t think you need such a large sample size.” What will be your response to that critique?
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

We calculate the standardized effect size for this design:
$d = \\frac{D}{\\sigma} =$ 0.7. Based on that, if we assume a even
bigger effect size, the standardized effect size might be too large and
cause us failing to reject *H*<sub>0</sub>. So we still assume the
effect size = DA.

(4) After the study got funded, the investigator started the intervention. However, in the beginning of the study, when they are piloting the procedure, it was found that only 2/3 of the participants in the intervention arm actually participated to the intervention group session (i.e., they did not actually get the intervention), nevertheless, the majority of them still completed their assessments. So the investigator wants to change the study design from a 1:1 randomization to 2:1 randomization (2 intervention and 1 control) to get sufficient number of participants to actually “receive the intervention”. Will such change fix the problem (i.e., does the statistic power remains the same as the original study de you agree with such change?)
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

No it won't fix the problem. Because based on the formula:

$$
\\begin{split}
D 
&= (Z\_{\\alpha/2} + Z\_{\\beta})\\sigma\\sqrt{\\frac{1}{n\_{T}} + \\frac{1}{n\_{C}}} \\\\
&= (Z\_{\\alpha/2} + Z\_{\\beta})\\sigma\\sqrt{\\frac{2}{n}} \\\\
\\end{split}
$$

if we now just randomize the 2n samples into 2:1, then
$n\_{T}' = 2n \\cdot \\frac{2}{3} \\cdot \\frac{2}{3} = \\frac{8}{9}n$,
$n\_{C}' = 2n \\cdot \\frac{1}{3} = \\frac{2}{3}n$,

$$
\\begin{split}
D 
&= (Z\_{\\alpha/2} + Z{'}\_{\\beta})\\sigma\\sqrt{\\frac{9}{8n} + \\frac{3}{2n}} \\\\
&= (Z\_{\\alpha/2} + Z{'}\_{\\beta})\\sigma\\sqrt{\\frac{21}{8n}} \\\\
\\end{split}
$$

If all the other parameters remain the same, we can see that
*Z*′<sub>*β*</sub> will be smaller than *Z*<sub>*β*</sub>, which means
the power will decrease.

(5) From (4), if you feel the change will not fix the problem, what will you recommend to the investigator to preserve the statistical power for the study?
-----------------------------------------------------------------------------------------------------------------------------------------------------------

The best way would be start the whole study all over again and recruit
more people. But if that's implausible, and the sample size is fixed,
the only way to preserve the power will be increase the *α* level.

(6) Assume that the investigator considers a subject who either has 0 unprotected sex occasion at both baseline and 6 months follow up (i.e., stay safe) or has improvement over time (i.e., decreased his unprotected sex occasions) as a successful outcome and suppose the proportion of control group participants with successful outcome is 30%. Using the same design parameters (i.e., same type I error rate, retention rate, ect.), do you think your proposed sample size from (1) will give you sufficient power (i.e., at least 80%) to declare a 35 percentage points difference as statistically significant?
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Here we treat the data as binary data and use the successful rate p as
outcome, then by using normal approximation:

$$
\\begin{split}
p\_{T} &\\sim N(\\overline{p\_{T}}, \\frac{\\overline{p\_{T}}(1-\\overline{p\_{T}})}{n\_{T}}) \\\\
p\_{C} &\\sim N(\\overline{p\_{C}}, \\frac{\\overline{p\_{C}}(1-\\overline{p\_{C}})}{n\_{C}}) \\\\
where: \\\\
DA &= 0.35 \\\\
\\overline{p\_{C}} &= \\overline{p\_{T}} = 0.3 \\\\
n\_{C} &= n\_{T} = n \\\\
\\end{split}
$$

The formula would adapted into
$DA = (Z\_{\\alpha/2} + Z\_{\\beta})\\sqrt{\\frac{\\overline{p\_{T}}(1-\\overline{p\_{T}})}{n\_{T}} + \\frac{\\overline{p\_{C}}(1-\\overline{p\_{C}})}{n\_{C}}}$.
And after adjusted for retention, VIF and ICC, we calculate the
*Z*<sub>*β*</sub> = 1.095, so the power = 86.3 %. So the proposed sample
size from (1) will still give us sufficient power to declare a 35
percentage points difference as statistically significant.
