---
name: ClinicalTrials
topic: Clinical Trial Design, Monitoring, and Analysis
maintainer: Ya Wang, Thomas Jaki, Orla Doyle, Elias Laurin Meyer, Laura Pascasio Harris, Wilmar Igl
email: ya.wang10@gilead.com
version: 2024-11-07
source: https://github.com/cran-task-views/ClinicalTrials/
---


### Get Started

This task view provides an overview of R packages relevant to the design, monitoring, and analysis of clinical trial data. 

Packages are grouped in the following categories:

-	[**Design**](#design): tools to support a variety of clinical trial designs. The packages are further categorized into subgroups, such as [*adaptive designs*](#adaptive-designs), [*bioequivalence study designs*](#bioequivalence), [*dose-finding designs*](#dose-finding), [*factorial designs*](#factorial-designs), [*group sequential designs*](#group-sequential-designs), [*randomization*](#randomization), [*response adaptive randomization*](#response-adaptive-randomization), [*sample size and power calculations*](#sample-size-and-power-calculations), and [*simulation*](#simulation) for clinical trial designs.

-	[**Monitoring**](#monitoring): tools dedicated to monitoring of clinical trials, such as computing the probability of crossing sequential boundaries along its interim analyses, sample size re-estimation, etc.

-	[**Analysis**](#analysis): tools for implementing commonly used analysis method in clinical trials. The packages are further categorized into subgroups, such as [*general analysis*](#general-analysis), [*longitudinal data analysis*](#longitudinal-data-analysis), [*survival analysis*](#survival-analysis), [*meta-analysis*](#meta-analysis), [*missing data imputation*](#missing-data-imputation), as well as [*analysis for specific designs*](#other-analysis-for-specific-designs).

Here are several foundational books on clinical trial design and analysis that can help users gain a deeper understanding of the methods implemented in the relevant R packages: [Clinical Trials: A Practical Approach](https://onlinelibrary.wiley.com/doi/book/10.1002/9781118793916), [Fundamentals of Clinical Trials](https://link.springer.com/book/10.1007/978-3-319-18539-2), [Sample Sizes for Clinical Trials](https://www.routledge.com/Sample-Sizes-for-Clinical-Trials/Julious/p/book/9781138587892?srsltid=AfmBOopllJ4lcXrd-J6q76oPSQl3Zae-X7LqAYmh1zbt_BY7_0ZD0gN0), [Group Sequential and Confirmatory Adaptive Designs in Clinical Trials](https://link.springer.com/book/10.1007/978-3-319-32562-0), [Bayesian Adaptive Methods for Clinical Trials](https://www.routledge.com/Bayesian-Adaptive-Methods-for-Clinical-Trials/Berry-Carlin-Lee-Muller/p/book/9781032922058?srsltid=AfmBOopPzoSaPFpQT8vTUc6WmJpn4_sNSQZQntvryGtRPPM6IgySOh7F).


### Inclusion Criteria

Packages are deemed in scope if they provide tools to support the design, monitoring and analysis of clinical trials. Please refer to task views `r view("ExperimentalDesign")`, `r view("Meta-analysis")`, `r view("MissingData")`, `r view("Pharmacokinetics")`, `r view("Survival")` for a more comprehensive list of R packages related to these topics.

Contributions are always welcome and encouraged. You can contribute by emailing the
maintainer directly or by submitting an issue or pull request in the GitHub
repository linked above.


### Design

#### *Adaptive Designs*

-   `r pkg("adaptr")` facilitates simulation and comparison of adaptive clinical trial designs. It supports a flexible number of arms, use of a common control arm, pre-specified and user-defined outcome- and posterior probability distribution-generating functions, fixed- and response-adaptive randomisation, various adaptation rules for arm dropping and stopping, calculation of trial design performance metrics, and visualisation of results.
    
-   `r pkg("adaptTest", priority = "core")` The functions
    defined in this program serve for implementing adaptive two-stage
    tests. Currently, four tests are included: Bauer and Koehne (1994),
    Lehmacher and Wassmer (1999), Vandemeulebroecke (2006), and the
    horizontal conditional error function. User-defined tests can also
    be implemented. Reference: Vandemeulebroecke, An investigation of
    two-stage tests, Statistica Sinica 2006.
    
-   `r pkg("adestr")` provides methods to evaluate the performance characteristics of various point and interval estimators for optimal adaptive two-stage designs. Specifically, this package is written to work with trial designs created by the 'adoptr' package (Kunzmann et al. (2021) <doi:10.18637/jss.v098.i09>; Pilz et al. (2021) <doi:10.1002/sim.8953>)). Apart from the a priori evaluation of performance characteristics, this package also allows for the evaluation of the implemented estimators on real datasets, and it implements methods to calculate p-values.

-   `r pkg("adpss")` provides the functions for planning and conducting a clinical trial with adaptive sample size determination. Maximal statistical efficiency will be exploited even when dramatic or multiple adaptations are made. Such a trial consists of adaptive determination of sample size at an interim analysis and implementation of frequentist statistical test at the interim and final analysis with a prefixed significance level. The required assumptions for the stage-wise test statistics are independent and stationary increments and normality. Predetermination of adaptation rule is not required.

-   `r pkg("AGSDest")`{#AGSDest} provides tools  and functions for parameter estimation in adaptive group sequential trials.

-   `r pkg("asd", priority = "core")`{#asd} runs simulations for adaptive seamless designs with and without early outcomes for treatment selection and subpopulation type designs. It allows sample size modification in subpopulation selection.

-   `r pkg("ASSISTant")` Clinical trial design for subgroup selection in three-stage group sequential trial as described in Lai, Lavori and Liao (2014, <doi:10.1016/j.cct.2014.09.001>). Includes facilities for design, exploration and analysis of such trials. An implementation of the initial DEFUSE-3 trial is also provided as a vignette.

-   `r pkg("BATSS")` Defines operating characteristics of Bayesian Adaptive Trials considering a generalised linear model response via Monte Carlo simulations of Bayesian GLM fitted via integrated Laplace approximations (INLA).
  
-   `r pkg("BayesCT")`{#BayesCT} Simulation and analysis of Bayesian adaptive clinical trials for binomial, Gaussian, and time-to-event data types, incorporates historical data and allows early stopping for futility or early success. The package uses novel and efficient Monte Carlo methods for estimating Bayesian posterior probabilities, evaluation of loss to follow up, and imputation of incomplete data. The package has the functionality for dynamically incorporating historical data into the analysis via the power prior or non-informative priors.

-   `r pkg("BDP2")` Tools and workflow to choose design parameters in Bayesian adaptive single-arm phase II trial designs with binary endpoint (response, success) with possible stopping for efficacy and futility at interim analyses. Also contains routines to determine and visualize operating characteristics. See Kopp-Schneider et al. (2018) <doi:10.1002/bimj.201700209>. 

-   `r pkg("Cats")`{#Cats} simulates a cohort platform trial design whereby every cohort consists of two arms (control and experimental treatment). Co-primary binary endpoints are used, and decisions at the interim or final analysis are made using either Bayesian or frequentist decision rules. Several options for sharing control data across cohorts are implemented. Realistic trial trajectories are simulated, and the operating characteristics of the designs are calculated. This package was used to derive the simulation results in Meyer et al. (2023) <doi:10.1371/journal.pone.0281674>.

-   `r pkg("CohortPlat")`{#CohortPlat} facilitates the simulation of cohort platform trials with binary endpoints, where each cohort consists of a combination treatment, the respective monotherapies, and control. Bayesian decision rules are used at the interim analysis (early futility or efficacy based on a surrogate endpoint) and at the final analysis to declare the combination therapy successful or futile. Sharing of the control and the backbone monotherapy data across cohorts is possible. The package offers extensive flexibility with respect to both platform trial trajectories, as well as treatment effect scenarios, and decision rules. This package was used to derive the simulation results in Meyer et al. (2022) <doi:10.1002/pst.2194>.

-   `r pkg("esDesign")`{#esDesign} is developed to implement the adaptive enrichment designs with sample size re-estimation presented in Lin et al. (2021) <doi:10.1016/j.cct.2020.106216>. In details, three-proposed trial designs are provided, including the AED1-SSR (or ES1-SSR), AED2-SSR (or ES2-SSR) and AED3-SSR (or ES3-SSR). In addition, this package also contains several widely used adaptive designs, such as the Marker Sequential Test (MaST) design proposed Freidlin et al. (2014) <doi:10.1177/1740774513503739>, the adaptive enrichment designs without early stopping (AED or ES), the sample size re-estimation procedure (SSR) based on the conditional power proposed by Proschan and Hunsberger (1995), and some useful functions. In details, we can calculate the futility and/or efficacy stopping boundaries, the sample size required, calibrate the value of the threshold of the difference between subgroup-specific test statistics, conduct the simulation studies in AED, SSR, AED1-SSR, AED2-SSR and AED3-SSR.

-   `r pkg("eselect")` Endpoint selection and sample size reassessment for multiple binary endpoints based on blinded and/or unblinded data. Trial design that allows an adaptive modification of the primary endpoint based on blinded information obtained at an interim analysis. The decision rule chooses the endpoint with the lower estimated required sample size. Additionally, the sample size is reassessed using the estimated event probabilities and correlation between endpoints. The implemented design is proposed in Bofill Roig, M., GC3mez Melis, G., Posch, M., and Koenig, F. (2022). <doi:10.48550/arXiv.2206.09639>.

-   `r pkg("gMCP")` provides functions and a graphical user interface for graphical described multiple test procedures. Examples of weighted tests that are available in gMCP are the weighted Bonferroni, parametric and Simes tests.

-   `r pkg("graphicalMCP")` is a low-dependency implementation of graphical MCPs which allow mixed types of tests. It also includes power simulations and visualization of graphical MCPs.

-   `r pkg("gsMAMS")` It provides functions to generate operating characteristics and to calculate Sequential Conditional Probability Ratio Tests(SCPRT) efficacy and futility boundary values along with sample/event size of Multi-Arm Multi-Stage(MAMS) trials for different outcomes. The package is based on Jianrong Wu, Yimei Li, Liang Zhu (2023) <doi:10.1002/sim.9682>, Jianrong Wu, Yimei Li (2023) "Group Sequential Multi-Arm Multi-Stage Survival Trial Design with Treatment Selection"(Manuscript accepted for publication) and Jianrong Wu, Yimei Li, Shengping Yang (2023) "Group Sequential Multi-Arm Multi-Stage Trial Design with Ordinal Endpoints"(In preparation). 

-   `r pkg("MABOUST")` conducts and simulates the MABOUST design, including making interim decisions to stop a treatment for inferiority or stop the trial early for superiority or equivalency.

-   `r pkg("MAMS")` designs multi-arm multi-stage studies with (asymptotically) normal endpoints and known variance. It could be used to determine the boundaries of a multi-arm multi-stage study for a given boundary shape and finds the required number of subjects, as well as simulates multi-arm multi-stage designs and estimates power and expected sample size. 

-   `r pkg("MinEDfind")`{#MinEDfind} The nonparametric two-stage
    Bayesian adaptive design is a novel phase II clinical trial design
    for finding the minimum effective dose (MinED). This design is
    motivated by the top priority and concern of clinicians when testing
    a new drug, which is to effectively treat patients and minimize the
    chance of exposing them to subtherapeutic or overly toxic doses. It
    is used to design single-agent trials.

-   `r pkg("NCC")`{#NCC} is an R package that allows users to simulate platform trials and perform treatment–control comparisons using non-concurrent control data (Krotka et al. (2023) <doi:10.1016/j.softx.2023.101437>). The package supports simulation of complex platform trial designs with continuous or binary endpoints and a flexible number of treatment arms that enter the trial at different time points. The software accommodates different treatment effects among the arms and includes several patterns for time trends. Analytic approaches currently implemented in the package cover frequentist modes (e.g., regression model adjusting for time as a fixed effect mixed model adjusting for time as a random factor, and regression splines), the Bayesian time machine a meta-analytic predictive prior separate analysis, and pooled analysis.

-   `r pkg("rpact", priority = "core")`{#rpact} Design and analysis of confirmatory
    adaptive clinical trials with continuous, binary, and survival
    endpoints according to the methods described in the monograph by
    Wassmer and Brannath (2016). This includes classical group
    sequential as well as multi-stage adaptive hypotheses tests that are
    based on the combination testing principle.

-   `r pkg("SAME")`{#SAME} Design a Bayesian seamless multi-arm biomarker-enriched phase II/III design with the survival endpoint with allowing sample size re-estimation. James M S Wason, Jean E Abraham, Richard D Baird, Ioannis Gournaris, Anne-Laure Vallier, James D Brenton, Helena M Earl, Adrian P Mander (2015) <doi:10.1038/bjc.2015.278>. Guosheng Yin, Nan Chen, J. Jack Lee (2018) <doi:10.1007/s12561-017-9199-7>. Ying Yuan, Beibei Guo, Mark Munsell, Karen Lu, Amir Jazaeri (2016) <doi:10.1002/sim.6971>.


#### *Bioequivalence*

-   `r pkg("adaptIVPT")` contains functions carrying out adaptive procedures using mixed scaling approach to establish bioequivalence for in-vitro permeation test (IVPT) data. Currently, the package provides procedures based on parallel replicate design and balanced data, according to the U.S. Food and Drug Administration's "Draft Guidance on Acyclovir" <https://www.accessdata.fda.gov/drugsatfda_docs/psg/Acyclovir_topical%20cream_RLD%2021478_RV12-16.pdf>. Potvin et al. (2008) <doi:10.1002/pst.294> provides the basis for our adaptive design (see Method B). For a comprehensive overview of the method, refer to Lim et al. (2023) <doi:10.1002/pst.2333>. This package reflects the views of the authors and should not be construed to represent the views or policies of the U.S. Food and Drug Administration.

-   `r pkg("PK")` contains methods to estimate PK parameters using non-compartmental theory and provides facilities to obtain confidence intervals and perform tests for single analysis as well as bioequivalence studies.

-   `r pkg("PowerTOST", priority = "core")`{#PowerTOST} contains
    functions to calculate power and sample size for various study
    designs used for bioequivalence studies. See function
    known.designs() for study designs covered. Moreover the package
    contains functions for power and sample size based on 'expected'
    power in case of uncertain (estimated) variability. Added are
    functions for the power and sample size for the ratio of two means
    with normally distributed data on the original scale (based on
    Fieller's confidence ('fiducial') interval).

-   `r pkg("replicateBE")` Performs comparative
    bioavailability calculations for Average Bioequivalence with
    Expanding Limits (ABEL). Implemented are 'Method A' and 'Method
    B' and the detection of outliers. If the design allows, assessment
    of the empiric Type I Error and iteratively adjusting alpha to
    control the consumer risk. Average Bioequivalence - optionally with
    a tighter (narrow therapeutic index drugs) or wider acceptance range
    (Gulf Cooperation Council, South Africa: Cmax) - is implemented as
    well.
    

#### *Dose-Finding*

-   `r pkg("bcrm", priority = "core")`{#bcrm} This package
    implements a wide variety of one and two-parameter Bayesian CRM
    designs. The program can run interactively, allowing the user to
    enter outcomes after each cohort has been recruited, or via
    simulation to assess operating characteristics.

-   `r pkg("crmPack")` Implements a wide range of
    model-based dose escalation designs, ranging from classical and
    modern continual reassessment methods (CRMs) based on dose-limiting
    toxicity endpoints to dual-endpoint designs taking into account a
    biomarker/efficacy outcome. The focus is on Bayesian inference,
    making it very easy to setup a new design with its own JAGS code.
    However, it is also possible to implement 3+3 designs for comparison
    or models with non-Bayesian estimation. The whole package is written
    in a modular form in the S4 class system, making it very flexible
    for adaptation to new models, escalation or stopping rules.
    
-   `r pkg("dfcrm", priority = "core")` This package provides
    functions to run the CRM and TITE-CRM in phase I trials and
    calibration tools for trial planning purposes.    
    
-   `r pkg("DTAT")` Dose Titration Algorithm Tuning (DTAT)
    is a methodologic framework allowing dose individualization to be
    conceived as a continuous learning process that begins in
    early-phase clinical trials and continues throughout drug
    development, on into clinical practice. This package includes code
    that researchers may use to reproduce or extend key results of the
    DTAT research programme, plus tools for trialists to design and
    simulate a '3+3/PC' dose-finding study.
    
-   `r pkg("ewoc")`{#ewoc} An implementation of a variety of
    escalation with overdose control designs introduced by Babb, Rogatko
    and Zacks (1998)
    [doi:10.1002/(SICI)1097-0258(19980530)17:10%3C1103::AID-SIM793%3E3.0.CO;2-9](https://dx.doi.org/10.1002/(SICI)1097-0258(19980530)17:10%3C1103::AID-SIM793%3E3.0.CO;2-9)
    . It calculates the next dose as a clinical trial proceeds as well
    as performs simulations to obtain operating characteristics.    
    
-   `r pkg("OncoBayes2")` Bayesian Logistic Regression for Oncology Dose-Escalation Trials. It provides flexible functions for Bayesian meta-analytic modeling of the incidence of Dose Limiting Toxicities (DLTs) by dose level, under treatment regimes involving any number of combination partners.

-   `r pkg("UnifiedDoseFinding")`{#UnifiedDoseFinding} In many phase I trials,
    the design goal is to find the dose associated with a certain target
    toxicity rate. In some trials, the goal can be to find the dose with
    a certain weighted sum of rates of various toxicity grades. For
    others, the goal is to find the dose with a certain mean value of a
    continuous response. This package provides the setup and
    calculations needed to run a dose-finding trial with non-binary
    endpoints and performs simulations to assess design's operating
    characteristics under various scenarios.

-   `r pkg("CRM")` implements the continual reassessment method (CRM) for dose finding in Phase I clinical trials. The operating characteristics of CRM are summarized through simulations.
    
-   `r pkg("dfpk")`{#dfpk} Statistical methods involving PK
    measures are provided, in the dose allocation process during a Phase
    I clinical trials. These methods enter pharmacokinetics (PK) in the
    dose finding designs in different ways, including covariates models,
    dependent variable or hierarchical models. This package provides
    functions to generate data from several scenarios and functions to
    run simulations which their objective is to determine the maximum
    tolerated dose (MTD).  
    
-   `r pkg("dfped")`{#dfped} A unified method for designing
    and analysing dose-finding trials in paediatrics, while bridging
    information from adults, is proposed in the dfped package. The dose
    range can be calculated under three extrapolation methods: linear,
    allometry and maturation adjustment, using pharmacokinetic (PK)
    data. To do this, it is assumed that target exposures are the same
    in both populations. The working model and prior distribution
    parameters of the dose-toxicity and dose-efficacy relationships can
    be obtained using early phase adult toxicity and efficacy data at
    several dose levels through dfped package. Priors are used into the
    dose finding process through a Bayesian model selection or adaptive
    priors, to facilitate adjusting the amount of prior information to
    differences between adults and children. This calibrates the model
    to adjust for misspecification if the adult and paediatric data are
    very different. User can use his/her own Bayesian model written in
    Stan code through the dfped package. A template of this model is
    proposed in the examples of the corresponding R functions in the
    package. Finally, in this package you can find a simulation function
    for one trial or for more than one trial.
    
-   `r pkg("DoseFinding")` provides functions for
    the design and analysis of dose-finding experiments (for example
    pharmaceutical Phase II clinical trials). It provides functions for:
    multiple contrast tests, fitting non-linear dose-response models,
    calculating optimal designs and an implementation of the
    `r pkg("MCPMod")` methodology. Currently only normally
    distributed homoscedastic endpoints are supported.


-   `r pkg("pocrm")` implements functions to implement and simulate the partial order continual reassessment method (PO-CRM) for use in Phase I trials of combinations of agents.

-   `r pkg("escalation")` Implements a range of different approaches for dose-finding clinical trials including the continual reassessment method (CRM), the modified TPI (mTPI) design, the Bayesian optimal interval design (BOIN), EffTox and the 3+3 design.

-   `r pkg("MCPMod")` This package implements a methodology
    for the design and analysis of dose-response studies that combines
    aspects of multiple comparison procedures and modeling approaches
    (Bretz, Pinheiro and Branson, 2005, Biometrics 61, 738-748). The
    package provides tools for the analysis of dose finding trials as
    well as a variety of tools necessary to plan a trial to be conducted
    with the MCPMod methodology.    
    
-   `r pkg("TEQR", priority = "core")` The target
    equivalence range (TEQR) design is a frequentist implementation of
    the modified toxicity probability interval (mTPI) design and a
    competitor to the standard 3+3 design (3+3). The 3+3 is the work
    horse design in Phase I. It is good at determining if a safe dose
    exits, but provides poor accuracy and precision in estimating the
    level of toxicity at the maximum tolerated dose (MTD). The TEQR is
    better than the 3+3 when compared on: 1) the number of times the
    dose at or nearest the target toxicity level was selected as the
    MTD, 2) the number of subjects assigned to doses levels, at or
    nearest the MTD, and 3) the overall trial DLT rate. TEQR more
    accurately and more precisely estimates the rate of toxicity at the
    MTD because a larger number of subjects are studied at the MTD dose.
    The TEQR on average uses fewer subjects and provide reasonably
    comparable results to the continual reassessment method (CRM) in the
    number of times the dose at or nearest the target toxicity level was
    selected as the MTD and the number of subjects assigned doses, at,
    or nearest the target and in overall DLT rate.
    
-   `r pkg("BOIN")` The Bayesian optimal interval (BOIN) design is a novel phase I clinical trial design for finding the maximum tolerated dose (MTD). It can be used to design both single-agent and drug-combination trials. The BOIN design is motivated by the top priority and concern of clinicians when testing a new drug, which is to effectively treat patients and minimize the chance of exposing them to subtherapeutic or overly toxic doses. The prominent advantage of the BOIN design is that it achieves simplicity and superior performance at the same time. The BOIN design is algorithm-based and can be implemented in a simple way similar to the traditional 3+3 design. The BOIN design yields an average performance that is comparable to that of the continual reassessment method (CRM, one of the best model-based designs) in terms of selecting the MTD, but has a substantially lower risk of assigning patients to subtherapeutic or overly toxic doses. For tutorial, please check Yan et al. (2020) <doi:10.18637/jss.v094.i13>.

-   `r pkg("SEARS")` A seamless design that combines phase I dose escalation based on toxicity with phase II dose expansion and dose comparison based on efficacy. A rich set of parameters can be used to explore various real scenarios. It can generate operating characteristics via simulation to examine the design's property.

-   [`r pkg("MinEDfind")`](#MinEDfind).
    
-   `r pkg("dfmta")` Phase I/II adaptive dose-finding design for single-agent Molecularly Targeted Agent (MTA), according to the paper "Phase I/II Dose-Finding Design for Molecularly Targeted Agent: Plateau Determination using Adaptive Randomization", Riviere Marie-Karelle et al. (2016) <doi:10.1177/0962280216631763>.

-   `r pkg("iAdapt")` Simulate and implement early phase two-stage adaptive dose-finding design for binary and quasi-continuous toxicity endpoints. See Chiuzan et al. (2018) for further reading <doi:10.1080/19466315.2018.1462727>.


#### *Factorial Designs*

-   `r pkg("conf.design")` This small package contains a
    series of simple tools for constructing and manipulating confounded
    and fractional factorial designs.

-   `r pkg("FrF2")` This package creates regular and
    non-regular Fractional Factorial designs. Furthermore, analysis
    tools for Fractional Factorial designs with 2-level factors are
    offered (main effects and interaction plots for all factors
    simultaneously, cube plot for looking at the simultaneous effects of
    three factors, full or half normal plot, alias structure in a more
    readable format than with the built-in function alias). The package
    is currently subject to intensive development. While much of the
    intended functionality is already available, some changes and
    improvements are still to be expected.
    

#### *Group Sequential Designs*

-   [`r pkg("AGSDest")`](#AGSDest).
    
-   `r pkg("clinfun", priority = "core")`{#clinfun} has
    functions for both design and analysis of clinical trials. For phase
    II trials, it has functions to calculate sample size, effect size,
    and power based on Fisher's exact test, the operating
    characteristics of a two-stage boundary, Optimal and Minimax 2-stage
    Phase II designs given by Richard Simon, the exact 1-stage Phase II
    design and can compute a stopping rule and its operating
    characteristics for toxicity monitoring based repeated significance
    testing. For phase III trials, it can calculate sample size for
    group sequential designs.    
    
-   `r pkg("GroupSeq")` computes probabilities related to group sequential designs for normally distributed test statistics. Enables to derive critical boundaries, power, drift, and confidence intervals of such designs. Supports the alpha spending approach by Lan-DeMets (1994) <doi:10.1002/sim.4780131308>.  

-   `r pkg("gsDesign")` derives group sequential clinical trial designs and describes their properties. Particular focus on time-to-event, binary, and continuous outcomes. Largely based on methods described in Jennison, Christopher and Turnbull, Bruce W., 2000, "Group Sequential Methods with Applications to Clinical Trials" (ISBN: 0-8493-0316-8).

-   `r pkg("ldbounds", priority = "core")` uses Lan-DeMets
    Method for group sequential trial; its functions calculate bounds
    and probabilities of a group sequential trial.

-   `r pkg("lrstat")`{#lrstat} performs power and sample size calculation for non-proportional hazards model using the Fleming-Harrington family of weighted log-rank tests. The package can also be used for continuous, binary, and count data. For continuous data, it can handle missing data through mixed-model for repeated measures (MMRM). In crossover designs, it can estimate direct treatment effects while accounting for carryover effects. For binary data, it can design Simon's 2-stage, modified toxicity probability-2 (mTPI-2), and Bayesian optimal interval (BOIN) trials. For count data, it can design group sequential trials for negative binomial endpoints with censoring. Additionally, it facilitates group sequential equivalence trials for all supported data types. Moreover, it can design adaptive group sequential trials for changes in sample size, error spending function, number and spacing or future looks. Finally, it offers various options for adjusted p-values, including graphical and gatekeeping procedures.

-   [`r pkg("rpact", priority = "core")`](#rpact).


#### *Randomization*

-   `r pkg("blockrand", priority = "core")` creates
    randomizations for block random clinical trials. It can also produce
    a PDF file of randomization cards.

-   `r pkg("experiment", priority = "core")` contains tools
    for clinical experiments, e.g., a randomization tool, and it
    provides a few special analysis options for clinical trials.
    
-   `r pkg("randomizeR")` This tool enables the user to
    choose a randomization procedure based on sound scientific criteria.
    It comprises the generation of randomization sequences as well the
    assessment of randomization procedures based on carefully selected
    criteria. Furthermore, `randomizeR` provides a function for the
    comparison of randomization procedures.


#### *Response Adaptive Randomization*

-   `r pkg("BAR")` Bayesian adaptive randomization is also called outcome adaptive randomization, which is increasingly used in clinical trials.

-   `r pkg("brada")` provides access to a range of functions for analyzing, applying and visualizing Bayesian response-adaptive trial designs for a binary endpoint. Includes the predictive probability approach and the predictive evidence value designs for binary endpoints.

-   `r pkg("carat")` provides functions and command-line user interface to generate allocation sequence by covariate-adaptive randomization for clinical trials. The package currently supports six covariate-adaptive randomization procedures. Three hypothesis testing methods that are valid and robust under covariate-adaptive randomization are also available in the package to facilitate the inference for treatment effect under the included randomization procedures. Additionally, the package provides comprehensive and efficient tools to allow one to evaluate and compare the performance of randomization procedures and tests based on various criteria. See Ma W, Ye X, Tu F, and Hu F (2023) <doi:10.18637/jss.v107.i02> for details. 

-   `r pkg("CARM")` In randomized controlled trial (RCT), balancing covariate is often one of the most important concern. CARM package provides functions to balance the covariates and generate allocation sequence by covariate-adjusted Adaptive Randomization via Mahalanobis-distance (ARM) for RCT. About what ARM is and how it works please see Y. Qin, Y. Li, W. Ma, H. Yang, and F. Hu (2022). "Adaptive randomization via Mahalanobis distance" Statistica Sinica. <doi:10.5705/ss.202020.0440>. In addition, the package is also suitable for the randomization process of multi-arm trials. For details, please see Yang H, Qin Y, Wang F, et al. (2023). "Balancing covariates in multi-arm trials via adaptive randomization" Computational Statistics & Data Analysis.<doi:10.1016/j.csda.2022.107642>.

-   `r pkg("covadapt")` iImplements seven Covariate-Adaptive Randomization to assign patients to two treatments. Three of these procedures can also accommodate quantitative and mixed covariates. Given a set of covariates, the user can generate a single sequence of allocations or replicate the design multiple times by simulating the patients' covariate profiles. At the end, an extensive assessment of the performance of the randomization procedures is provided, calculating several imbalance measures. See Baldi Antognini A, Frieri R, Zagoraiou M and Novelli M (2022) <doi:10.1007/s00362-022-01381-1> for details.

-   `r pkg("grouprar")` implement group response-adaptive randomization procedures, which also integrates standard non-group response-adaptive randomization methods as specialized instances. It is also uniquely capable of managing complex scenarios, including those with delayed and missing responses, thereby expanding its utility in real-world applications. This package offers 16 functions for simulating a variety of response adaptive randomization procedures. These functions are essential for guiding the selection of statistical methods in clinical trials, providing a flexible and effective approach to trial design. Some of the detailed methodologies and algorithms used in this package, please refer to the following references: LJ Wei (1979) <doi:10.1214/aos/1176344614> L. J. WEI and S. DURHAM (1978) <doi:10.1080/01621459.1978.10480109> Durham, S. D., FlournoY, N. AND LI, W. (1998) <doi:10.2307/3315771> Ivanova, A., Rosenberger, W. F., Durham, S. D. and Flournoy, N. (2000) <https://www.jstor.org/stable/25053121> Bai Z D, Hu F, Shen L. (2002) <doi:10.1006/jmva.2001.1987> Ivanova, A. (2003) <doi:10.1007/s001840200220> Hu, F., & Zhang, L. X. (2004) <doi:10.1214/aos/1079120137> Hu, F., & Rosenberger, W. F. (2006, ISBN:978-0-471-65396-7). Zhang, L. X., Chan, W. S., Cheung, S. H., & Hu, F. (2007) <https://www.jstor.org/stable/26432528> Zhang, L., & Rosenberger, W. F. (2006) <doi:10.1111/j.1541-0420.2005.00496.x> Hu, F., Zhang, L. X., Cheung, S. H., & Chan, W. S. (2008) <doi:10.1002/cjs.5550360404>.

-   `r pkg("RABR")`{#RABR} conduct simulations of the Response Adaptive Block Randomization (RABR) design to evaluate its type I error rate, power and operating characteristics for binary and continuous endpoints. For more details of the proposed method, please refer to Zhan et al. (2021) <doi:10.1002/sim.9104>.

-   `r pkg("RARfreq")` provides functions and command-line user interface to generate allocation sequence by response-adaptive randomization for clinical trials. The package currently supports two families of frequentist response-adaptive randomization procedures, Doubly Adaptive Biased Coin Design ('DBCD') and Sequential Estimation-adjusted Urn Model ('SEU'), for binary and normal endpoints. One-sided proportion (or mean) difference and Chi-square (or 'ANOVA') hypothesis testing methods are also available in the package to facilitate the inference for treatment effect. Additionally, the package provides comprehensive and efficient tools to allow one to evaluate and compare the performance of randomization procedures and tests based on various criteria. For example, plots for relationship among assumed treatment effects, sample size, and power are provided. Five allocation functions for 'DBCD' and six addition rule functions for 'SEU' are implemented to target allocations such as 'Neyman', 'Rosenberger' Rosenberger et al. (2001) <doi:10.1111/j.0006-341X.2001.00909.x> and 'Urn' allocations.


#### *Sample Size and Power Calculations*

-   `r pkg("BayesCTDesign")` A set of functions to help clinical trial researchers calculate power and sample size for two-arm Bayesian randomized clinical trials that do or do not incorporate historical control data. At some point during the design process, a clinical trial researcher who is designing a basic two-arm Bayesian randomized clinical trial needs to make decisions about power and sample size within the context of hypothesized treatment effects. Through simulation, the simple_sim() function will estimate power and other user specified clinical trial characteristics at user specified sample sizes given user defined scenarios about treatment effect,control group characteristics, and outcome. If the clinical trial researcher has access to historical control data, then the researcher can design a two-arm Bayesian randomized clinical trial that incorporates the historical data. In such a case, the researcher needs to work through the potential consequences of historical and randomized control differences on trial characteristics, in addition to working through issues regarding power in the context of sample size, treatment effect size, and outcome. If a researcher designs a clinical trial that will incorporate historical control data, the researcher needs the randomized controls to be from the same population as the historical controls. What if this is not the case when the designed trial is implemented? During the design phase, the researcher needs to investigate the negative effects of possible historic/randomized control differences on power, type one error, and other trial characteristics. Using this information, the researcher should design the trial to mitigate these negative effects. Through simulation, the historic_sim() function will estimate power and other user specified clinical trial characteristics at user specified sample sizes given user defined scenarios about historical and randomized control differences as well as treatment effects and outcomes. The results from historic_sim() and simple_sim() can be printed with print_table() and graphed with plot_table() methods. Outcomes considered are Gaussian, Poisson, Bernoulli, Lognormal, Weibull, and Piecewise Exponential. The methods are described in Eggleston et al. (2021) <doi:10.18637/jss.v100.i21>. 

-   `r pkg("binomSamSize")` is a suite of functions for
    computing confidence intervals and necessary sample sizes for the
    success probability parameter Bernoulli distribution under simple
    random sampling or under pooled sampling.
    
-   [`r pkg("clinfun", priority = "core")`](#clinfun). 

-   `r pkg("clusterPower")` Calculate power for cluster
    randomized trials (CRTs) that compare two means, two proportions, or
    two counts using closed-form solutions. In addition, calculate power
    for cluster randomized crossover trials using Monte Carlo methods.
    For more information, see Reich et al. (2012)
    [doi:10.1371/journal.pone.0035564](https://dx.doi.org/10.1371/journal.pone.0035564).
    
-   `r pkg("cosa")` Implements bound constrained optimal
    sample allocation (BCOSA) framework described in Bulus & Dong (2019)
    for power analysis of multilevel regression discontinuity designs
    (MRDDs) and multilevel randomized trials (MRTs) with continuous
    outcomes. Separate tools for statistical power and minimum
    detectable effect size computations are provided.
    
-   `r pkg("Hmisc")` contains around 200
    miscellaneous functions useful for such things as data analysis,
    high-level graphics, utility operations, functions for computing
    sample size and power, translating SAS datasets into S, imputing
    missing values, advanced table making, variable clustering,
    character string manipulation, conversion of S objects to LaTeX
    code, recoding variables, and bootstrap repeated measures analysis.
    
-   `r pkg("longpower", priority = "core")`Compute power and sample size 
    for linear models of longitudinal data. The package is described in 
    Iddi and Donohue (2022) <doi:10.32614/RJ-2022-022>. 
    
-   [`r pkg("lrstat")`](#lrstat).
    
-   [`r pkg("PowerTOST", priority = "core")`](#PowerTOST).
    
-   `r pkg("PowerUpR")` Includes tools to calculate
    statistical power, minimum detectable effect size (MDES), MDES
    difference (MDESD), and minimum required sample size for various
    multilevel randomized experiments with continuous outcomes. Some of
    the functions can assist with planning two- and three-level
    cluster-randomized trials (CRTs) sensitive to multilevel moderation
    and mediation (2-1-1, 2-2-1, and 3-2-1).
    
-   `r pkg("presize")` Bland (2009) recommended to base
    study sizes on the width of the confidence interval rather the power
    of a statistical test. The goal of 'presize' is to provide
    functions for such precision based sample size calculations. For a
    given sample size, the functions will return the precision (width of
    the confidence interval), and vice versa.

-   `r pkg("pwr", priority = "core")` has power analysis
    functions along the lines of Cohen (1988).
    
-   `r pkg("samplesize")` computes sample size for
    Student's t-test with equal and nonequal variances and for the
    Wilcoxon-Mann-Whitney test for categorical data with and without
    ties.
    
-   `r pkg("ssanv")` is a set of functions to calculate
    sample size for two-sample difference in means tests. Does
    adjustments for either nonadherence or variability that comes from
    using data to estimate parameters.
    
-   `r pkg("ThreeArmedTrials")` Design and analyze
    three-arm non-inferiority or superiority trials which follow a
    gold-standard design, i.e. trials with an experimental treatment, an
    active, and a placebo control.

-   `r pkg("TrialSize", priority = "core")` This package has
    more than 80 functions from the book *Sample Size Calculations in
    Clinical Research* (Chow & Wang & Shao, 2007, 2nd ed., Chapman
    &Hall/CRC).

    
#### *Simulation*

-   `r pkg("adaptDiag")` simulate clinical trials for diagnostic test devices and evaluate the operating characteristics under an adaptive design with futility assessment determined via the posterior predictive probabilities.

-   `r pkg("airship")`is an R package that contains an R Shiny App designed to plot simulation results of clinical trials. Its main feature is allowing users to simultaneously investigate the impact of several simulation input dimensions through dynamic filtering of the simulation results. A more detailed description of the core app can be found in Meyer et al. (2023) <doi:10.1016/j.softx.2023.101347>.

-   [`r pkg("asd", priority = "core")`](#asd).

-   [`r pkg("BayesCT")`](BayesCT).

-   [`r pkg("bcrm", priority = "core")`](bcrm).
    
-   [`r pkg("Cats")`](#Cats).
    
-   [`r pkg("CohortPlat")`](#CohortPlat). 
    
-   [`r pkg("dfped")`](#dfped).
    
-   [`r pkg("dfpk")`](#dfpk). 
    
-   [`r pkg("esDesign")`](#esDesign).   

-   [`r pkg("ewoc")`](#ewoc). 

-   `r pkg("Mediana")` Provides a general framework for
    clinical trial simulations based on the Clinical Scenario Evaluation
    (CSE) approach. The package supports a broad class of data models
    (including clinical trials with continuous, binary, survival-type
    and count-type endpoints as well as multivariate outcomes that are
    based on combinations of different endpoints), analysis strategies
    and commonly used evaluation criteria.

-   [`r pkg("NCC")`](#NCC).

-   [`r pkg("RABR")`](#RABR).

-   [`r pkg("rpact", priority = "core")`](#rpact).

-   `r pkg("simglm")` Simulates regression models, including
    both simple regression and generalized linear mixed models with up
    to three level of nesting. Power simulations that are flexible
    allowing the specification of missing data, unbalanced designs, and
    different random error distributions are built into the package.

-   [`r pkg("UnifiedDoseFinding")`](#UnifiedDoseFinding).


### Analysis

#### *General Analysis*

-   `r pkg("coin")` offers conditional inference procedures
    for the general independence problem including two-sample, K-sample
    (non-parametric ANOVA), correlation, censored, ordered and
    multivariate problems.
    
-   `r pkg("ctrdata")` is a system for querying, retrieving and analyzing 
    protocol- and results-related information on clinical trials from four public registers.
    
-   `r pkg("epibasix")` has functions such as `diffdetect`,
    `n4means` for continuous outcome and `n4props` and functions for
    matched pairs analysis in randomized trials.
    
-   `ae.dotplot` from `r pkg("HH")` shows a two-panel
    display of the most frequently occurring adverse events in the
    active arm of a clinical study.

-   `r pkg("Hmisc")` contains around 200
    miscellaneous functions useful for such things as data analysis,
    high-level graphics, utility operations, functions for computing
    sample size and power, translating SAS datasets into S, imputing
    missing values, advanced table making, variable clustering,
    character string manipulation, conversion of S objects to LaTeX
    code, recoding variables, and bootstrap repeated measures analysis.

-   `r pkg("logistf")` Firth's Bias-Reduced Logistic Regression. Firth's method was proposed as ideal solution to the problem of separation in logistic regression.

-   `r pkg("maic")` In MAIC, unbiased comparison between outcomes of two trials is facilitated by weighting the subject-level outcomes of one trial with weights derived such that the weighted aggregate measures of the prognostic or effect modifying variables are equal to those of the sample in the comparator trial.

-   `r pkg("multcomp")`{#multcomp} covers simultaneous tests and
    confidence intervals for general linear hypotheses in parametric
    models, including linear, generalized linear, linear mixed effects,
    and survival models.

-   Base R, especially the `r pkg("stats")` package, has a lot of functionality
    useful for design and analysis of clinical trials. For example,
    `chisq.test`, `prop.test`, `binom.test`, `t.test`, `wilcox.test`,
    `kruskal.test`, `mcnemar.test`, `cor.test`, `power.t.test`,
    `power.prop.test`, `power.anova.test`, `lm`, `glm`, `nls`, `anova`
    (and its `lm` and `glm` methods) among many others.
    
-   `r pkg("TestDesign")` uses the optimal test design approach by Birnbaum (1968, ISBN:9781593119348) and van der Linden (2018) <doi:10.1201/9781315117430> to construct fixed, adaptive, and parallel tests. Supports the following mixed-integer programming (MIP) solver packages: 'Rsymphony', 'gurobi', 'lpSolve', and 'Rglpk'. The 'gurobi' package is not available from CRAN; see <https://www.gurobi.com/downloads/>.
    

#### *Longitudinal Data Analysis*

-   `r pkg("brms.mmrm")` leverages 'brms' to run MMRMs, and it supports a simplified interfaced to reduce difficulty and align with the best practices of the life sciences.

-   `r pkg("glmmTMB")` fits linear and generalized linear mixed models with various extensions, including zero-inflation.

-   `r pkg("lme4")` fits linear and generalized linear mixed-effects models.

-   `r pkg("mmrm")` Implements mixed models for repeated measures (MMRM), 
    a popular choice for analyzing longitudinal continuous outcomes in 
    randomized clinical trials and beyond.

-   [`r pkg("multcomp")`](#multcomp).
    
-   `r pkg("nlme")` fits and compare Gaussian linear and nonlinear mixed-effects models.
    
    
#### *Meta-Analysis*

-   `r pkg("meta")` is for fixed and random effects
    meta-analysis. It has Functions for tests of bias, forest and funnel
    plot.
    
-   `r pkg("metafor")` consists of a collection of functions
    for conducting meta-analyses. Fixed- and random-effects models (with
    and without moderators) can be fitted via the general linear
    (mixed-effects) model. For 2x2 table data, the Mantel-Haenszel and
    Peto's method are also implemented.
    
-   `r pkg("metaLik")` Likelihood inference in meta-analysis
    and meta-regression models.

-   `r pkg("metasens")` is a package for statistical methods
    to model and adjust for bias in meta-analysis

-   `r pkg("RBesT")` Tool-set to support Bayesian evidence synthesis. It facilitate the use of historical information in clinical trials. Once relevant historical information has been identified, it supports the derivation of informative priors via the Meta-Analytic-Predictive (MAP) approach and the evaluation of the trial’s operating characteristics.

-   `r pkg("rmeta")` has functions for simple fixed and
    random effects meta-analysis for two-sample comparisons and
    cumulative meta-analyses. Draws standard summary plots, funnel
    plots, and computes summaries and tests for association and
    heterogeneity.
    

#### *Missing Data Imputation*

-   `r pkg("Hmisc")` contains around 200
    miscellaneous functions useful for such things as data analysis,
    high-level graphics, utility operations, functions for computing
    sample size and power, translating SAS datasets into S, imputing
    missing values, advanced table making, variable clustering,
    character string manipulation, conversion of S objects to LaTeX
    code, recoding variables, and bootstrap repeated measures analysis.

-   `r pkg("mice")` implements multiple imputation by chained equations using 
     Fully Conditional Specification (FCS) implemented by the MICE algorithm as 
     described in Van Buuren and Groothuis-Oudshoorn (2011) 
     <doi:10.18637/jss.v045.i03>

-   `r pkg("rbmi")` implements standard and reference based multiple 
    imputation allowing for the imputation of longitudinal datasets using 
    predefined strategies. The package is described in Gower-Page et al (2022) 
    <doi: 10.21105/joss.04251>.
    
-   `r pkg("remiod")` implements Reference-based multiple imputation of ordinal and binary responses under Bayesian framework, as described in Wang and Liu (2022) <doi:10.48550/arXiv.2203.02771>. Methods for missing-not-at-random include Jump-to-Reference (J2R), Copy Reference (CR), and Delta Adjustment which can generate tipping point analysis.
    
    
#### *Survival Analysis*

-   `r pkg("ipcwswitch")` contains functions for formatting clinical trials data and implementing inverse probability of censoring weights to handle treatment switches when estimating causal treatment effect in randomized clinical trials.

-   [`r pkg("multcomp")`](#multcomp).

-   `r pkg("nphRCT")` Non-Proportional Hazards in Randomized Controlled Trials. Perform a stratified weighted log-rank test in a randomized controlled trial.

-   `r pkg("rpsftm")` provides functions to fit a rank preserving structural failure time model to a two-arm clinical trial with survival outcomes.
    
-   `r pkg("survival", priority = "core")` contains
    descriptive statistics, two-sample tests, parametric accelerated
    failure models, Cox model. Delayed entry (truncation) allowed for
    all models; interval censoring for parametric models. Case-cohort
    designs.
  
-   [`r pkg("rpact", priority = "core")`](#rpact).

    
#### *Other Analysis for Specific Designs*  

-   `r pkg("clinicalsignificance")` The goal of this package is to provide all 
   necessary tools for analyses of clinical significance in clinical intervention studies. 
   In contrast to statistical significance, which assesses if it is probable that there 
   is a treatment effect, clinical significance can be used to determine if a treatment 
   effect is of practical use or meaningful for patients.
   
-   `r pkg("clinsig")` This function calculates both
    parametric and non-parametric versions of the Jacobson-Truax
    estimates of clinical significance.
  
-   `r pkg("MatchIt")` is an R package that selects matched samples of the original treated and control groups with similar covariate distributions.  It can be used to match exactly on covariates, to match on propensity scores, or perform a variety of other matching procedures.   The package also implements a series of recommendations offered in Ho, Imai, King, and Stuart (2007) <doi:10.1093/pan/mpl013>.   After appropriately preprocessing with MatchIt, researchers can use whatever parametric model they would have used without MatchIt and produce inferences that are more robust and less sensitive to modeling assumptions. Matching methods, assessing balance, and estimating effects after balance is described in the vignettes.

-   `r pkg("nppbib")` implements a nonparametric statistical
    test for rank or score data from partially-balanced incomplete
    block-design experiments.
    
-   `r pkg("speff2trial", priority = "core")`, the package
    performs estimation and testing of the treatment effect in a 2-group
    randomized clinical trial with a quantitative or dichotomous
    endpoint.
    
-   `r pkg("ThreeGroups")` This package implements the
    Maximum Likelihood estimator for three-group designs proposed by
    Gerber, Green, Kaplan, and Kern (2010).
    

### Monitoring

-   `r pkg("accrualPlot")` Tracking accrual in clinical trials is important for trial success.
    `accrualPlot` provides functions to aid the tracking of accrual and predict when a trial 
    will reach it's intended sample size.
    
-   [`r pkg("asd", priority = "core")`](#asd).

-   [`r pkg("esDesign")`](#esDesign).

-   `r pkg("monitOS")` Monitoring Overall Survival in Pivotal Trials in Indolent Cancers.

-   `r pkg("PwrGSD")` provides tools for the evaluation of interim analysis plans for sequentially monitored trials on a survival endpoint; tools to construct efficacy and futility boundaries, for deriving power of a sequential design at a specified alternative, template for evaluating the performance of candidate plans at a set of time varying alternatives.

-   [`r pkg("rpact", priority = "core")`](#rpact).

-   [`r pkg("SAME")`](#SAME).

-   `r pkg("seqmon")` provides sequential monitoring of clinical trials. It calculates the efficacy and futility boundaries at each look. It allows modifying the design and tracking the design update history.


### Links
-   [Regulatory Compliance and Validation Issues (A Guidance Document for the Use of R in Regulated Clinical Trial Environments)](http://www.R-project.org/doc/R-FDA.pdf)

