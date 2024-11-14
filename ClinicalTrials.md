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

Packages are deemed in scope if they provide tools to support the design, monitoring and analysis of clinical trials. Please refer to task views `r view("ExperimentalDesign")`, `r view("Survival")`, `r view("Meta-analysis")` for a more comprehensive list of R packages related to these topics.

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

-   `r pkg("AGSDest")` provides tools  and functions for parameter estimation in adaptive group sequential trials.

-   `r pkg("asd", priority = "core")` runs simulations for adaptive seamless designs with and without early outcomes for treatment selection and subpopulation type designs. It allows sample size modification in subpopulation selection.

-   `r pkg("ASSISTant")` Clinical trial design for subgroup selection in three-stage group sequential trial as described in Lai, Lavori and Liao (2014, <doi:10.1016/j.cct.2014.09.001>). Includes facilities for design, exploration and analysis of such trials. An implementation of the initial DEFUSE-3 trial is also provided as a vignette.

-   `r pkg("BATSS")` Defines operating characteristics of Bayesian Adaptive Trials considering a generalised linear model response via Monte Carlo simulations of Bayesian GLM fitted via integrated Laplace approximations (INLA).
  
-   `r pkg("BayesCT")` Simulation and analysis of Bayesian adaptive clinical trials for binomial, Gaussian, and time-to-event data types, incorporates historical data and allows early stopping for futility or early success. The package uses novel and efficient Monte Carlo methods for estimating Bayesian posterior probabilities, evaluation of loss to follow up, and imputation of incomplete data. The package has the functionality for dynamically incorporating historical data into the analysis via the power prior or non-informative priors.

-   `r pkg("BDP2")` Tools and workflow to choose design parameters in Bayesian adaptive single-arm phase II trial designs with binary endpoint (response, success) with possible stopping for efficacy and futility at interim analyses. Also contains routines to determine and visualize operating characteristics. See Kopp-Schneider et al. (2018) <doi:10.1002/bimj.201700209>. 

-   `r pkg("esDesign")` is developed to implement the adaptive enrichment designs with sample size re-estimation presented in Lin et al. (2021) <doi:10.1016/j.cct.2020.106216>. In details, three-proposed trial designs are provided, including the AED1-SSR (or ES1-SSR), AED2-SSR (or ES2-SSR) and AED3-SSR (or ES3-SSR). In addition, this package also contains several widely used adaptive designs, such as the Marker Sequential Test (MaST) design proposed Freidlin et al. (2014) <doi:10.1177/1740774513503739>, the adaptive enrichment designs without early stopping (AED or ES), the sample size re-estimation procedure (SSR) based on the conditional power proposed by Proschan and Hunsberger (1995), and some useful functions. In details, we can calculate the futility and/or efficacy stopping boundaries, the sample size required, calibrate the value of the threshold of the difference between subgroup-specific test statistics, conduct the simulation studies in AED, SSR, AED1-SSR, AED2-SSR and AED3-SSR.

-   `r pkg("eselect")` Endpoint selection and sample size reassessment for multiple binary endpoints based on blinded and/or unblinded data. Trial design that allows an adaptive modification of the primary endpoint based on blinded information obtained at an interim analysis. The decision rule chooses the endpoint with the lower estimated required sample size. Additionally, the sample size is reassessed using the estimated event probabilities and correlation between endpoints. The implemented design is proposed in Bofill Roig, M., GC3mez Melis, G., Posch, M., and Koenig, F. (2022). <doi:10.48550/arXiv.2206.09639>.

-   `r pkg("gMCP")` provides functions and a graphical user interface for graphical described multiple test procedures. Examples of weighted tests that are available in gMCP are the weighted Bonferroni, parametric and Simes tests.

-   `r pkg("graphicalMCP")` is a low-dependency implementation of graphical MCPs which allow mixed types of tests. It also includes power simulations and visualization of graphical MCPs.

-   `r pkg("gsMAMS")` It provides functions to generate operating characteristics and to calculate Sequential Conditional Probability Ratio Tests(SCPRT) efficacy and futility boundary values along with sample/event size of Multi-Arm Multi-Stage(MAMS) trials for different outcomes. The package is based on Jianrong Wu, Yimei Li, Liang Zhu (2023) <doi:10.1002/sim.9682>, Jianrong Wu, Yimei Li (2023) "Group Sequential Multi-Arm Multi-Stage Survival Trial Design with Treatment Selection"(Manuscript accepted for publication) and Jianrong Wu, Yimei Li, Shengping Yang (2023) "Group Sequential Multi-Arm Multi-Stage Trial Design with Ordinal Endpoints"(In preparation). 

-   `r pkg("MABOUST")` conducts and simulates the MABOUST design, including making interim decisions to stop a treatment for inferiority or stop the trial early for superiority or equivalency.

-   `r pkg("MAMS")` designs multi-arm multi-stage studies with (asymptotically) normal endpoints and known variance. It could be used to determine the boundaries of a multi-arm multi-stage study for a given boundary shape and finds the required number of subjects, as well as simulates multi-arm multi-stage designs and estimates power and expected sample size. 

-   `r pkg("MinEDfind")` The nonparametric two-stage
    Bayesian adaptive design is a novel phase II clinical trial design
    for finding the minimum effective dose (MinED). This design is
    motivated by the top priority and concern of clinicians when testing
    a new drug, which is to effectively treat patients and minimize the
    chance of exposing them to subtherapeutic or overly toxic doses. It
    is used to design single-agent trials.

-   `r pkg("rpact", priority = "core")` Design and analysis of confirmatory
    adaptive clinical trials with continuous, binary, and survival
    endpoints according to the methods described in the monograph by
    Wassmer and Brannath (2016). This includes classical group
    sequential as well as multi-stage adaptive hypotheses tests that are
    based on the combination testing principle.

-   `r pkg("SAME")` Design a Bayesian seamless multi-arm biomarker-enriched phase II/III design with the survival endpoint with allowing sample size re-estimation. James M S Wason, Jean E Abraham, Richard D Baird, Ioannis Gournaris, Anne-Laure Vallier, James D Brenton, Helena M Earl, Adrian P Mander (2015) <doi:10.1038/bjc.2015.278>. Guosheng Yin, Nan Chen, J. Jack Lee (2018) <doi:10.1007/s12561-017-9199-7>. Ying Yuan, Beibei Guo, Mark Munsell, Karen Lu, Amir Jazaeri (2016) <doi:10.1002/sim.6971>.


#### *Bioequivalence*

-   `r pkg("adaptIVPT")` contains functions carrying out adaptive procedures using mixed scaling approach to establish bioequivalence for in-vitro permeation test (IVPT) data. Currently, the package provides procedures based on parallel replicate design and balanced data, according to the U.S. Food and Drug Administration's "Draft Guidance on Acyclovir" <https://www.accessdata.fda.gov/drugsatfda_docs/psg/Acyclovir_topical%20cream_RLD%2021478_RV12-16.pdf>. Potvin et al. (2008) <doi:10.1002/pst.294> provides the basis for our adaptive design (see Method B). For a comprehensive overview of the method, refer to Lim et al. (2023) <doi:10.1002/pst.2333>. This package reflects the views of the authors and should not be construed to represent the views or policies of the U.S. Food and Drug Administration.

-   `r pkg("PK")` contains methods to estimate PK parameters using non-compartmental theory and provides facilities to obtain confidence intervals and perform tests for single analysis as well as bioequivalence studies.

-   `r pkg("PowerTOST", priority = "core")` contains
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

-   `r pkg("bcrm", priority = "core")` This package
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
    
-   `r pkg("ewoc")` An implementation of a variety of
    escalation with overdose control designs introduced by Babb, Rogatko
    and Zacks (1998)
    [doi:10.1002/(SICI)1097-0258(19980530)17:10%3C1103::AID-SIM793%3E3.0.CO;2-9](https://dx.doi.org/10.1002/(SICI)1097-0258(19980530)17:10%3C1103::AID-SIM793%3E3.0.CO;2-9)
    . It calculates the next dose as a clinical trial proceeds as well
    as performs simulations to obtain operating characteristics.    
    
-   `r pkg("OncoBayes2")` Bayesian Logistic Regression for Oncology Dose-Escalation Trials. It provides flexible functions for Bayesian meta-analytic modeling of the incidence of Dose Limiting Toxicities (DLTs) by dose level, under treatment regimes involving any number of combination partners.

-   `r pkg("UnifiedDoseFinding")` In many phase I trials,
    the design goal is to find the dose associated with a certain target
    toxicity rate. In some trials, the goal can be to find the dose with
    a certain weighted sum of rates of various toxicity grades. For
    others, the goal is to find the dose with a certain mean value of a
    continuous response. This package provides the setup and
    calculations needed to run a dose-finding trial with non-binary
    endpoints and performs simulations to assess design's operating
    characteristics under various scenarios.

-   `r pkg("CRM")` implements the continual reassessment method (CRM) for dose finding in Phase I clinical trials. The operating characteristics of CRM are summarized through simulations.
    
-   `r pkg("dfpk")` Statistical methods involving PK
    measures are provided, in the dose allocation process during a Phase
    I clinical trials. These methods enter pharmacokinetics (PK) in the
    dose finding designs in different ways, including covariates models,
    dependent variable or hierarchical models. This package provides
    functions to generate data from several scenarios and functions to
    run simulations which their objective is to determine the maximum
    tolerated dose (MTD).  
    
-   `r pkg("dfped")` A unified method for designing
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

-   `r pkg("SEARS")` A seamless design that combines phase I dose escalation based on toxicity with phase II dose expansion and dose comparison based on efficacy. A rich set of parameters can be used to explore various real scenarios. It can generate operating characteristics via simulation to examine the designb
