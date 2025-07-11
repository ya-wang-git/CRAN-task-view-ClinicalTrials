# ClinicalTrials


Some task views may include packages that are also relevant to clinical
trials and will be listed within the grouping categories. Please refer
to task views `​r view("ExperimentalDesign")`, `​r view("Meta-analysis")`,
`​r view("MissingData")`, `​r view("Pharmacokinetics")`,
`​r view("Survival")` for a more comprehensive list of R packages related
to these topics. Note that while the `​r view("Pharmacokinetics")` task
view packages are closely related to clinical trials, they are not
explicitly listed under the grouping categories in this task view to
avoid duplication.

Contributions are always welcome and encouraged. You can contribute by
emailing the maintainer directly or by submitting an issue or pull
request in the GitHub repository linked above. For further details see
the [Contributing
guide](https://github.com/cran-task-views/ctv/blob/main/Contributing.md).

### Design

#### *Adaptive Designs*

-   `​r pkg("adaptr")` facilitates simulation and comparison of adaptive
    clinical trial designs. It supports a flexible number of arms, use
    of a common control arm, pre-specified and user-defined outcome- and
    posterior probability distribution-generating functions, fixed- and
    response-adaptive randomisation, various adaptation rules for arm
    dropping and stopping, calculation of trial design performance
    metrics, and visualisation of results.

-   `​r pkg("adaptTest", priority = "core")` The functions defined in
    this program serve for implementing adaptive two-stage tests.
    Currently, four tests are included: Bauer and Koehne (1994),
    Lehmacher and Wassmer (1999), Vandemeulebroecke (2006), and the
    horizontal conditional error function. User-defined tests can also
    be implemented.

-   `​r pkg("adestr")` provides methods to evaluate the performance
    characteristics of various point and interval estimators for optimal
    adaptive two-stage designs. Specifically, this package is written to
    work with trial designs created by the `adoptr` package (Kunzmann et
    al. (2021)
    \<[doi:10.18637/jss.v098.i09](https://doi.org/10.18637/jss.v098.i09)\>;
    Pilz et al. (2021)
    \<[doi:10.1002/sim.8953](https://doi.org/10.1002/sim.8953)\>).

-   `​r pkg("adpss")` provides the functions for planning and conducting
    a clinical trial with adaptive sample size determination. Maximal
    statistical efficiency will be exploited even when dramatic or
    multiple adaptations are made.

-   `​r pkg("asd", priority = "core")` runs simulations for adaptive
    seamless designs with and without early outcomes for treatment
    selection and subpopulation type designs. It allows sample size
    modification in subpopulation selection.

-   `​r pkg("ASSISTant")` Clinical trial design for subgroup selection in
    three-stage group sequential trial as described in Lai et al. (2014)
    \<[doi:10.1016/j.cct.2014.09.001](https://doi.org/10.1016/j.cct.2014.09.001)\>.
    It includes facilities for design, exploration and analysis of such
    trials.

-   `​r pkg("BDP2")` Tools and workflow to choose design parameters in
    Bayesian adaptive single-arm phase II trial designs with binary
    endpoint (response, success) with possible stopping for efficacy and
    futility at interim analyses; and also contains routines to
    determine and visualize operating characteristics. See
    Kopp-Schneider et al. (2018)
    \<[doi:10.1002/bimj.201700209](https://doi.org/10.1002/bimj.201700209)\>.

-   `​r pkg("Cats")` {#Cats} simulates a cohort platform trial design
    whereby every cohort consists of two arms (control and experimental
    treatment). Endpoints are co-primary binary endpoints and decisions
    are made using either Bayesian or frequentist decision rules; and
    realistic trial trajectories are simulated with the operating
    characteristics of the designs calculated.

-   `​r pkg("CohortPlat")` is a collection of functions dedicated to
    simulating staggered entry platform trials whereby the treatment
    under investigation is a combination of two active compounds. A more
    detailed description of the design can be found in Meyer et
    al. \<[doi:10.1002/pst.2194](https://doi:10.1002/pst.2194)\> and a
    manual in Meyer et
    al. \<[doi:10.48550/arXiv.2202.02182](https://doi:10.48550/arXiv.2202.02182)\>.

-   `​r pkg("esDesign")` is developed to implement the adaptive
    enrichment designs with sample size re-estimation presented in Lin
    et al. (2021)
    \<[doi:10.1016/j.cct.2020.106216](https://doi.org/10.1016/j.cct.2020.106216)\>.
    In details, three-proposed trial designs are provided, including the
    AED1-SSR (or ES1-SSR), AED2-SSR (or ES2-SSR), AED3-SSR (or ES3-SSR);
    additionally, several widely used adaptive designs, such as the
    Marker Sequential Test (MaST) design proposed Freidlin et al. (2014)
    \<[doi:10.1177/1740774513503739](https://doi.org/10.1177/1740774513503739)\>,
    the adaptive enrichment designs without early stopping (AED or ES),
    the sample size re-estimation procedure (SSR) based on the
    conditional power proposed by Proschan and Hunsberger (1995).

-   `​r pkg("eselect")` Endpoint selection and sample size reassessment
    for multiple binary endpoints based on blinded and/or unblinded
    data. The implemented design is proposed in Roig et al. (2022)
    \<[doi:10.48550/arXiv.2206.09639](https://doi.org/10.48550/arXiv.2206.09639)\>.

-   `​r pkg("gMCP")` provides functions and a graphical user interface
    for graphical described multiple test procedures. Examples of
    weighted tests that are available in gMCP are the weighted
    Bonferroni, parametric and Simes tests.

-   `​r pkg("graphicalMCP")` is a low-dependency implementation of
    graphical MCPs which allow mixed types of tests. It also includes
    power simulations and visualization of graphical MCPs.

-   `​r pkg("gsMAMS")` It provides functions to generate operating
    characteristics and to calculate Sequential Conditional Probability
    Ratio Tests(SCPRT) efficacy and futility boundary values along with
    sample/event size of Multi-Arm Multi-Stage(MAMS) trials for
    different outcomes. The package is based on Wu et al. (2023)
    \<[doi:10.1002/sim.9682](https://doi.org/10.1002/sim.9682)\>, Wu and
    Li (2023) \<[doi:
    10.1002/sim.9682](https://doi.org/10.1002/sim.9682)\>, and Wu et
    al. (2023) “Group Sequential Multi-Arm Multi-Stage Trial Design with
    Ordinal Endpoints”(In preparation).

-   `​r pkg("MABOUST")` conducts and simulates the MABOUST design,
    including making interim decisions to stop a treatment for
    inferiority or stop the trial early for superiority or equivalency.

-   `​r pkg("MAMS")` designs multi-arm multi-stage studies with
    (asymptotically) normal endpoints and known variance. It could be
    used to determine the boundaries of a multi-arm multi-stage study
    for a given boundary shape and finds the required number of
    subjects, as well as simulates multi-arm multi-stage designs and
    estimates power and expected sample size.

-   `​r pkg("MinEDfind")` The nonparametric two-stage Bayesian adaptive
    design is a novel phase II clinical trial design for finding the
    minimum effective dose (MinED) in single-agent trials. This design
    is motivated by the top priority and concern of clinicians when
    testing a new drug, which is to effectively treat patients and
    minimize the chance of exposing them to subtherapeutic or overly
    toxic doses.

-   `​r pkg("NCC")` is an R package that allows users to simulate
    platform trials and perform treatment–control comparisons using
    non-concurrent control data (Krotka et al. (2023)
    \<[doi:10.1016/j.softx.2023.101437](https://doi.org/10.1016/j.softx.2023.101437)\>).
    The package supports simulation of complex platform trial designs
    with continuous or binary endpoints and a flexible number of
    treatment arms that enter the trial at different time points and
    accommodates different treatment effects among the arms and includes
    several patterns for time trends using frequentist approach (e.g.,
    regression model adjusting for time as a fixed effect mixed model
    adjusting for time as a random factor, and regression splines), the
    Bayesian time machine a meta-analytic predictive prior separate
    analysis, and pooled analysis.

-   `​r pkg("rpact", priority = "core")` Design and analysis of
    confirmatory adaptive clinical trials with continuous, binary, and
    survival endpoints according to the methods described in the
    monograph by Wassmer and Brannath (2016). This includes classical
    group sequential as well as multi-stage adaptive hypotheses tests
    that are based on the combination testing principle.

-   `​r pkg("SAME")` Design a Bayesian seamless multi-arm
    biomarker-enriched phase II/III design with the survival endpoint
    with allowing sample size re-estimation. Wason et al. (2015)
    \<[doi:10.1038/bjc.2015.278](https://doi.org/10.1038/bjc.2015.278)\>.
    Yin et al. (2018)
    \<[doi:10.1007/s12561-017-9199-7](https://doi.org/10.1007/s12561-017-9199-7)\>.
    Yuan et al. (2016)
    \<[doi:10.1002/sim.6971](https://doi.org/10.1002/sim.6971)\>.

#### *Bioequivalence*

-   `​r pkg("adaptIVPT")` contains functions carrying out adaptive
    procedures using mixed scaling approach to establish bioequivalence
    for in-vitro permeation test (IVPT) data. Currently, the package
    provides procedures based on parallel replicate design and balanced
    data, according to the U.S. Food and Drug Administration’s “[Draft
    Guidance on
    Acyclovir](https://www.accessdata.fda.gov/drugsatfda_docs/psg/PSG_021478.pdf)”.

-   `​r pkg("PK")` contains methods to estimate PK parameters using
    non-compartmental theory and provides facilities to obtain
    confidence intervals and perform tests for single analysis as well
    as bioequivalence studies.

-   `​r pkg("PowerTOST", priority = "core")` contains functions to
    calculate power and sample size for various study designs used for
    bioequivalence studies. See function known.designs() for study
    designs covered.

-   `​r pkg("replicateBE")` Performs comparative bioavailability
    calculations for Average Bioequivalence with Expanding Limits
    (ABEL). Implemented are ‘Method A’ and ‘Method B’ and the detection
    of outliers.

#### *Dose-Finding*

-   `​r pkg("bcrm", priority = "core")` This package implements a wide
    variety of one and two-parameter Bayesian CRM designs. The program
    can run interactively, allowing the user to enter outcomes after
    each cohort has been recruited, or via simulation to assess
    operating characteristics.

-   `​r pkg("crmPack")` Implements a wide range of model-based dose
    escalation designs, ranging from classical and modern continual
    reassessment methods (CRMs) based on dose-limiting toxicity
    endpoints to dual-endpoint designs taking into account a
    biomarker/efficacy outcome. The focus is on Bayesian inference,
    making it very easy to setup a new design with its own JAGS code.

-   `​r pkg("dfcrm", priority = "core")` This package provides functions
    to run the CRM and TITE-CRM in phase I trials and calibration tools
    for trial planning purposes.

-   `​r pkg("DTAT")` Dose Titration Algorithm Tuning (DTAT) is a
    methodologic framework allowing dose individualization to be
    conceived as a continuous learning process that begins in
    early-phase clinical trials and continues throughout drug
    development, on into clinical practice. This package includes code
    that researchers may use to reproduce or extend key results of the
    DTAT research programme, plus tools for trialists to design and
    simulate a ‘3+3/PC’ dose-finding study.

-   `​r pkg("ewoc")` An implementation of a variety of escalation with
    overdose control designs introduced by Babb et al. (1998)
    \<[doi:10.1002/(SICI)1097-0258(19980530)17:10%3C1103::AID-SIM793%3E3.0.CO;2-9](https://dx.doi.org/10.1002/(SICI)1097-0258(19980530)17:10%3C1103::AID-SIM793%3E3.0.CO;2-9)\>.
    It calculates the next dose as a clinical trial proceeds as well as
    performs simulations to obtain operating characteristics.

-   `​r pkg("OncoBayes2")` Bayesian Logistic Regression for Oncology
    Dose-Escalation Trials. It provides flexible functions for Bayesian
    meta-analytic modeling of the incidence of Dose Limiting Toxicities
    (DLTs) by dose level, under treatment regimes involving any number
    of combination partners.

-   `​r pkg("UnifiedDoseFinding")` In many phase I trials, the design
    goal is to find the dose associated with a certain target toxicity
    rate, or the goal can be to find the dose with a certain weighted
    sum of rates of various toxicity grades, or to find the dose with a
    certain mean value of a continuous response. This package provides
    the setup and calculations needed to run a dose-finding trial with
    non-binary endpoints and performs simulations to assess design’s
    operating characteristics under various scenarios.

-   `​r pkg("dfped")` A unified method for designing and analysing
    dose-finding trials in paediatrics, while bridging information from
    adults, is proposed in the dfped package. The dose range can be
    calculated under three extrapolation methods: linear, allometry and
    maturation adjustment, using pharmacokinetic (PK) data, assuming
    that target exposures are the same in both populations.

-   `​r pkg("DoseFinding")` provides functions for the design and
    analysis of dose-finding experiments (for example pharmaceutical
    Phase II clinical trials). It provides functions for: multiple
    contrast tests, fitting non-linear dose-response models, calculating
    optimal designs and an implementation of the `​r pkg("MCPMod")`
    methodology, but currently only normally distributed homoscedastic
    endpoints are supported.

-   `​r pkg("pocrm")` implements functions to implement and simulate the
    partial order continual reassessment method (PO-CRM) for use in
    Phase I trials of combinations of agents.

-   `​r pkg("escalation")` Implements a range of different approaches for
    dose-finding clinical trials including the continual reassessment
    method (CRM), the modified TPI (mTPI) design, the Bayesian optimal
    interval design (BOIN), EffTox and the 3+3 design.

-   `​r pkg("MCPMod")` This package implements a methodology for the
    design and analysis of dose-response studies that combines aspects
    of multiple comparison procedures and modeling approaches (Bretz et
    al. (2005)
    \<[doi:10.1111/j.1541-0420.2005.00344.x](https://doi.org/10.1111/j.1541-0420.2005.00344.x)\>).
    Please note: The ‘MCPMod’ package will not be further developed, all
    future development of the MCP-Mod methodology will be done in
    `​r pkg("DoseFinding")`.

-   `​r pkg("TEQR", priority = "core")` The TEQR package contains
    software to calculate the operating characteristics for the TEQR and
    the ACT designs. The TEQR (toxicity equivalence range) design is a
    toxicity based cumulative cohort design with added safety rules; the
    ACT (Activity constrained for toxicity) design is also a cumulative
    cohort design with additional safety rules with the unique feature
    of this design is that dose is escalated based on lack of activity
    rather than on lack of toxicity and is de-escalated only if an
    unacceptable level of toxicity is experienced.

-   `​r pkg("BOIN")` The Bayesian optimal interval (BOIN) design is a
    novel phase I clinical trial design for finding the maximum
    tolerated dose (MTD). It can be used to design both single-agent and
    drug-combination trials. The BOIN design yields an average
    performance that is comparable to that of the continual reassessment
    method (CRM, one of the best model-based designs) in terms of
    selecting the MTD, but has a substantially lower risk of assigning
    patients to subtherapeutic or overly toxic doses. For tutorial,
    please check Yan et al. (2020)
    \<[doi:10.18637/jss.v094.i13](https://doi.org/10.18637/jss.v094.i13)\>.

-   `​r pkg("SEARS")` A seamless design that combines phase I dose
    escalation based on toxicity with phase II dose expansion and dose
    comparison based on efficacy. A rich set of parameters can be used
    to explore various real scenarios. It can generate operating
    characteristics via simulation to examine the design’s property.

-   [`​r pkg("MinEDfind")`](#MinEDfind).

-   `​r pkg("dfmta")` Phase I/II adaptive dose-finding design for
    single-agent Molecularly Targeted Agent (MTA), according to the
    paper “Phase I/II Dose-Finding Design for Molecularly Targeted
    Agent: Plateau Determination using Adaptive Randomization”, Riviere
    Marie-Karelle et al. (2016)
    \<[doi:10.1177/0962280216631763](https://doi.org/10.1177/0962280216631763)\>.

-   `​r pkg("iAdapt")` Simulate and implement early phase two-stage
    adaptive dose-finding design for binary and quasi-continuous
    toxicity endpoints. See Chiuzan et al. (2018)
    \<[doi:10.1080/19466315.2018.1462727](https://doi.org/10.1080/19466315.2018.1462727)\>
    for further reading.

#### *Factorial Designs*

-   `​r pkg("conf.design")` This small package contains a series of
    simple tools for constructing and manipulating confounded and
    fractional factorial designs.

-   `​r pkg("FrF2")` This package creates regular and non-regular
    Fractional Factorial designs. Furthermore, analysis tools for
    Fractional Factorial designs with 2-level factors are offered (main
    effects and interaction plots for all factors simultaneously, cube
    plot for looking at the simultaneous effects of three factors, full
    or half normal plot, alias structure in a more readable format than
    with the built-in function alias).

#### *Group Sequential Designs*

-   `​r pkg("clinfun", priority = "core")` has functions for both design
    and analysis of clinical trials. For phase II trials, it has
    functions to calculate sample size, effect size, and power based on
    Fisher’s exact test, the operating characteristics of a two-stage
    boundary, Optimal and Minimax 2-stage Phase II designs given by
    Richard Simon, the exact 1-stage Phase II design and can compute a
    stopping rule and its operating characteristics for toxicity
    monitoring based repeated significance testing; and can calculate
    sample size for Phase III group sequential designs.

-   `​r pkg("GroupSeq")` computes probabilities related to group
    sequential designs for normally distributed test statistics. Enables
    to derive critical boundaries, power, drift, and confidence
    intervals of such designs. Supports the alpha spending approach by
    Lan-DeMets (1994)
    \<[doi:10.1002/sim.4780131308](https://doi.org/10.1002/sim.4780131308)\>.

-   `​r pkg("gsDesign")` derives group sequential clinical trial designs
    and describes their properties. Particular focus on time-to-event,
    binary, and continuous outcomes. Largely based on methods described
    in the book *Group Sequential Methods with Applications to Clinical
    Trials* by Jennison et al. (2000) (ISBN:0-8493-0316-8).

-   `​r pkg("ldbounds", priority = "core")` uses Lan-DeMets Method for
    group sequential trial; its functions calculate bounds and
    probabilities of a group sequential trial.

-   `​r pkg("lrstat")` performs power and sample size calculation for
    non-proportional hazards model using the Fleming-Harrington family
    of weighted log-rank tests. The package can also be used for
    continuous, binary, and count data.

-   [`​r pkg("rpact", priority = "core")`](#rpact).

#### *Randomization*

-   `​r pkg("blockrand", priority = "core")` creates randomizations for
    block random clinical trials. It can also produce a PDF file of
    randomization cards.

-   `​r pkg("experiment", priority = "core")` contains tools for clinical
    experiments, e.g., a randomization tool, and it provides a few
    special analysis options for clinical trials.

-   `​r pkg("randomizeR")` This tool enables the user to choose a
    randomization procedure based on sound scientific criteria. It
    comprises the generation of randomization sequences as well the
    assessment of randomization procedures based on carefully selected
    criteria.

#### *Response Adaptive Randomization*

-   `​r pkg("BAR")` Bayesian adaptive randomization is also called
    outcome adaptive randomization, which is increasingly used in
    clinical trials.

-   `​r pkg("brada")` provides access to a range of functions for
    analyzing, applying and visualizing Bayesian response-adaptive trial
    designs for a binary endpoint. Includes the predictive probability
    approach and the predictive evidence value designs for binary
    endpoints.

-   `​r pkg("carat")` provides functions and command-line user interface
    to generate allocation sequence by covariate-adaptive randomization
    for clinical trials. The package currently supports six
    covariate-adaptive randomization procedures. See Ma et al. (2023)
    \<[doi:10.18637/jss.v107.i02](https://doi.org/10.18637/jss.v107.i02)\>
    for details.

-   `​r pkg("CARM")` In randomized controlled trial (RCT), balancing
    covariate is often one of the most important concern. CARM package
    provides functions to balance the covariates and generate allocation
    sequence by covariate-adjusted Adaptive Randomization via
    Mahalanobis-distance (ARM) for RCT. For details, please see Yang et
    al. (2023)
    \<[doi:10.1016/j.csda.2022.107642](https://doi.org/10.1016/j.csda.2022.107642)\>.

-   `​r pkg("covadap")` Implements seven Covariate-Adaptive Randomization
    to assign patients to two treatments. Given a set of covariates, the
    user can generate a single sequence of allocations or replicate the
    design multiple times by simulating the patients’ covariate
    profiles. See Antognini et al. (2022)
    \<[doi:10.1007/s00362-022-01381-1](https://doi.org/10.1007/s00362-022-01381-1)\>
    for details.

-   `​r pkg("grouprar")` implements group response-adaptive randomization
    procedures, which also integrates standard non-group
    response-adaptive randomization methods as specialized instances. It
    is also uniquely capable of managing complex scenarios, including
    those with delayed and missing responses, thereby expanding its
    utility in real-world applications.

-   `​r pkg("RABR")` conduct simulations of the Response Adaptive Block
    Randomization (RABR) design to evaluate its type I error rate, power
    and operating characteristics for binary and continuous endpoints.
    For more details of the proposed method, please refer to Zhan et
    al. (2021)
    \<[doi:10.1002/sim.9104](https://doi.org/10.1002/sim.9104)\>.

-   `​r pkg("RARfreq")` provides functions and command-line user
    interface to generate allocation sequence by response-adaptive
    randomization for clinical trials. The package currently supports
    two families of frequentist response-adaptive randomization
    procedures, Doubly Adaptive Biased Coin Design (‘DBCD’) and
    Sequential Estimation-adjusted Urn Model (‘SEU’), for binary and
    normal endpoints.

#### *Sample Size and Power Calculations*

-   `​r pkg("BayesCTDesign")` A set of functions to help clinical trial
    researchers calculate power and sample size for two-arm Bayesian
    randomized clinical trials that do or do not incorporate historical
    control data. Outcomes considered are Gaussian, Poisson, Bernoulli,
    Lognormal, Weibull, and Piecewise Exponential. The methods are
    described in Eggleston et al. (2021)
    \<[doi:10.18637/jss.v100.i21](https://doi.org/10.18637/jss.v100.i21)\>.

-   [`​r pkg("clinfun", priority = "core")`](#clinfun).

-   `​r pkg("cosa")` Implements bound constrained optimal sample
    allocation (BCOSA) framework described in Bulus & Dong (2019) for
    power analysis of multilevel regression discontinuity designs
    (MRDDs) and multilevel randomized trials (MRTs) with continuous
    outcomes. Separate tools for statistical power and minimum
    detectable effect size computations are provided.

-   `​r pkg("longpower", priority = "core")`Compute power and sample size
    for linear models of longitudinal data. Supported models include
    mixed-effects models and models fit by generalized least squares and
    generalized estimating equations. The package is described in Iddi
    and Donohue (2022)
    \<[doi:10.32614/RJ-2022-022](https://journal.r-project.org/articles/RJ-2022-022/)\>.

-   [`​r pkg("lrstat")`](#lrstat).

-   [`​r pkg("PowerTOST", priority = "core")`](#PowerTOST).

-   `​r pkg("PowerUpR")` Includes tools to calculate statistical power,
    minimum detectable effect size (MDES), MDES difference (MDESD), and
    minimum required sample size for various multilevel randomized
    experiments with continuous outcomes. Some of the functions can
    assist with planning two- and three-level cluster-randomized trials
    (CRTs) sensitive to multilevel moderation and mediation (2-1-1,
    2-2-1, and 3-2-1).

-   `​r pkg("presize")` Bland (2009) recommended to base study sizes on
    the width of the confidence interval rather the power of a
    statistical test. The goal of ‘presize’ is to provide functions for
    such precision based sample size calculations. For a given sample
    size, the functions will return the precision (width of the
    confidence interval), and vice versa.

-   `​r pkg("pwr", priority = "core")` Power calculations along the lines
    of Cohen (1988) using in particular the same notations for effect
    sizes. Examples from the book are given.

-   `​r pkg("samplesize")` computes sample size for Student’s t-test with
    equal and nonequal variances and for the Wilcoxon-Mann-Whitney test
    for categorical data with and without ties.

-   `​r pkg("ssanv")` is a set of functions to calculate sample size for
    two-sample difference in means tests. Does adjustments for either
    nonadherence or variability that comes from using data to estimate
    parameters.

-   `​r pkg("TrialSize", priority = "core")` This package has more than
    80 functions from the book *Sample Size Calculations in Clinical
    Research* by Chow et al. (2007)
    \<[doi:10.1201/9781584889830](https://doi.org/10.1201/9781584889830)\>.

#### *Simulation*

-   `​r pkg("adaptDiag")` simulate clinical trials for diagnostic test
    devices and evaluate the operating characteristics under an adaptive
    design with futility assessment determined via the posterior
    predictive probabilities.

-   `​r pkg("airship")`is an R package that contains an R Shiny App
    designed to plot simulation results of clinical trials. Its main
    feature is allowing users to simultaneously investigate the impact
    of several simulation input dimensions through dynamic filtering of
    the simulation results. A more detailed description of the core app
    can be found in Meyer et al. (2023)
    \<[doi:10.1016/j.softx.2023.101347](https://doi.org/10.1016/j.softx.2023.101347)\>.

-   [`​r pkg("asd", priority = "core")`](#asd).

-   [`​r pkg("BayesCT")`](BayesCT).

-   [`​r pkg("bcrm", priority = "core")`](bcrm).

-   [`​r pkg("Cats")`](#Cats).

-   [`​r pkg("CohortPlat")`](#CohortPlat).

-   [`​r pkg("dfped")`](#dfped).

-   [`​r pkg("esDesign")`](#esDesign).

-   [`​r pkg("ewoc")`](#ewoc).

-   `​r pkg("Mediana")` Provides a general framework for clinical trial
    simulations based on the Clinical Scenario Evaluation (CSE)
    approach. The package supports a broad class of data models
    (including clinical trials with continuous, binary, survival-type
    and count-type endpoints as well as multivariate outcomes that are
    based on combinations of different endpoints), analysis strategies
    and commonly used evaluation criteria.

-   [`​r pkg("NCC")`](#NCC).

-   [`​r pkg("RABR")`](#RABR).

-   [`​r pkg("rpact", priority = "core")`](#rpact).

-   `​r pkg("simglm")` Simulates regression models, including both simple
    regression and generalized linear mixed models with up to three
    level of nesting. Power simulations that are flexible allowing the
    specification of missing data, unbalanced designs, and different
    random error distributions are built into the package.

-   [`​r pkg("UnifiedDoseFinding")`](#UnifiedDoseFinding).

### Analysis

#### *General Analysis*

-   `​r pkg("coin")` offers conditional inference procedures for the
    general independence problem including two-sample, K-sample
    (non-parametric ANOVA), correlation, censored, ordered and
    multivariate problems.

-   `​r pkg("ctrdata")` is a system for querying, retrieving and
    analyzing protocol- and results-related information on clinical
    trials from four public registers.

-   `​r pkg("epibasix")` has functions such as `diffdetect`, `n4means`
    for continuous outcome and `n4props` and functions for matched pairs
    analysis in randomized trials.

-   `​r pkg("HH")` is support software for Statistical Analysis and Data
    Display (Second Edition, Springer, ISBN 978-1-4939-2121-8, 2015) and
    (First Edition, Springer, ISBN 0-387-40270-5, 2004) by Richard M.
    Heiberger and Burt Holland. `ae.dotplot` shows a two-panel display
    of the most frequently occurring adverse events in the active arm of
    a clinical study.

-   `​r pkg("logistf")` Firth’s Bias-Reduced Logistic Regression. Firth’s
    method was proposed as ideal solution to the problem of separation
    in logistic regression.

-   `​r pkg("maic")` In MAIC, unbiased comparison between outcomes of two
    trials is facilitated by weighting the subject-level outcomes of one
    trial with weights derived such that the weighted aggregate measures
    of the prognostic or effect modifying variables are equal to those
    of the sample in the comparator trial.

-   `​r pkg("multcomp")` Provides simultaneous tests and confidence
    intervals for general linear hypotheses in parametric models,
    including linear, GLM, mixed-effects, and survival models.

-   Base R, especially the `​r pkg("stats")` package, has a lot of
    functionality useful for design and analysis of clinical trials. For
    example, `chisq.test`, `prop.test`, `binom.test`, `t.test`,
    `wilcox.test`, `kruskal.test`, `mcnemar.test`, `cor.test`,
    `power.t.test`, `power.prop.test`, `power.anova.test`, `lm`, `glm`,
    `nls`, `anova` (and its `lm` and `glm` methods) among many others.

-   `​r pkg("TestDesign")` uses the optimal test design approach by
    Birnbaum (1968) (ISBN:9781593119348) and van der Linden (2018)
    \<[doi:10.1201/9781315117430](https://doi.org/10.1201/9781315117430)\>
    to construct fixed, adaptive, and parallel tests. Supports the
    following mixed-integer programming (MIP) solver packages:
    `​rsymphony`, `gurobi`, `lpSolve`, and `​rglpk`. The `gurobi` package
    is not available from CRAN; see <https://www.gurobi.com/downloads/>.

#### *Longitudinal Data Analysis*

-   `​r pkg("brms.mmrm")` is a powerful and versatile package for fitting
    Bayesian regression models. It leverages ‘brms’ to run MMRMs, and it
    supports a simplified interfaced to reduce difficulty and align with
    the best practices of the life sciences.

-   `​r pkg("glmmTMB")` fits linear and generalized linear mixed models
    with various extensions, including zero-inflation.

-   `​r pkg("lme4")` fits linear and generalized linear mixed-effects
    models.

-   `​r pkg("mmrm")` Implements mixed models for repeated measures
    (MMRM), a popular choice for analyzing longitudinal continuous
    outcomes in randomized clinical trials and beyond.

-   `​r pkg("multcomp")` Provides simultaneous tests and confidence
    intervals for general linear hypotheses in parametric models,
    including linear, GLM, mixed-effects, and survival models.

-   `​r pkg("nlme")` fits and compare Gaussian linear and nonlinear
    mixed-effects models.

#### *Meta-Analysis*

This task view focuses on packages relevant to clinical trials. For a
more comprehensive list of packages on this topic, please refer to the
`​r view("Meta-analysis")` task view.

-   `​r pkg("meta")` is a user-friendly package offering standard
    meta-analysis methods as described in the book *Meta-Analysis with
    R* by Schwarzer et al. (2015) \<[doi:
    10.1007/978-3-319-21416-0](https://doi.org/10.1007/978-3-319-21416-0)\>,
    featuring common and random effects models, various plots (e.g.,
    forest, funnel), advanced models (e.g., three-level, GLMM), bias
    evaluation, meta-regression, cumulative and leave-one-out analysis,
    and subgroup forest plot summaries.

-   `​r pkg("metafor")` is a comprehensive package for meta-analyses,
    providing functions to calculate effect sizes, fit various (e.g.,
    fixed-, and random-effects) models, perform
    moderator/meta-regression analyses, create meta-analytical plots,
    apply specialized methods (e.g., Mantel-Haenszel method, Peto’s
    method), and fit meta-analytic multivariate/multilevel models
    accounting for non-independent sampling errors or clustering.

-   `​r pkg("metaLik")` Likelihood inference in meta-analysis and
    meta-regression models.

-   `​r pkg("metasens")` is a package for statistical methods to model
    and adjust for bias in meta-analysis.

-   `​r pkg("netmeta")` provides a comprehensive set of functions for
    frequentist methods in network meta-analysis, including additive
    models, analysis of binary data, ranking methods (SUCRA, P-scores),
    consistency checks, league tables, funnel plots, evidence flow
    measures, network graphs, treatment ranking diagrams, contribution
    matrices, meta-regression, and subgroup analysis.

-   `​r pkg("RBesT")` Tool-set to support Bayesian evidence synthesis. It
    facilitate the use of historical information in clinical trials.
    Once relevant historical information has been identified, it
    supports the derivation of informative priors via the
    Meta-Analytic-Predictive (MAP) approach and the evaluation of the
    trial’s operating characteristics.

-   `​r pkg("rmeta")` has functions for simple fixed and random effects
    meta-analysis for two-sample comparisons and cumulative
    meta-analyses. Draws standard summary plots, funnel plots, and
    computes summaries and tests for association and heterogeneity.

#### *Missing Data Imputation*

This task view focuses on packages relevant to clinical trials. For a
more comprehensive list of packages on this topic, please refer to the
`​r view("MissingData")` task view.

-   `​r pkg("mice")` implements multiple imputation by chained equations
    using Fully Conditional Specification (FCS) implemented by the MICE
    algorithm as described in Van Buuren and Groothuis-Oudshoorn (2011)
    \<[doi:10.18637/jss.v045.i03](https://doi.org/10.18637/jss.v045.i03)\>

-   `​r pkg("rbmi")` implements standard and reference based multiple
    imputation allowing for the imputation of longitudinal datasets
    using predefined strategies. The package is described in Gower-Page
    et al. (2022) \<[doi:
    10.21105/joss.04251](https://doi.org/10.21105/joss.04251)\>.

-   `​r pkg("remiod")` implements Reference-based multiple imputation of
    ordinal and binary responses under Bayesian framework, as described
    in Wang and Liu (2022)
    \<[doi:10.48550/arXiv.2203.02771](https://doi.org/10.48550/arXiv.2203.02771)\>.
    Methods for missing-not-at-random include Jump-to-Reference (J2R),
    Copy Reference (CR), and Delta Adjustment which can generate tipping
    point analysis.

#### *Survival Analysis*

This task view focuses on packages relevant to clinical trials. For a
more comprehensive list of packages on this topic, please refer to the
`​r view("Survival")` task view.

-   `​r pkg("ipcwswitch")` contains functions for formatting clinical
    trials data and implementing inverse probability of censoring
    weights to handle treatment switches when estimating causal
    treatment effect in randomized clinical trials.

-   `​r pkg("multcomp")` Provides simultaneous tests and confidence
    intervals for general linear hypotheses in parametric models,
    including linear, GLM, mixed-effects, and survival models.

-   `​r pkg("nphRCT")` Non-Proportional Hazards in Randomized Controlled
    Trials. Perform a stratified weighted log-rank test in a randomized
    controlled trial.

-   `​r pkg("rpsftm")` provides functions to fit a rank preserving
    structural failure time model to a two-arm clinical trial with
    survival outcomes.

-   `​r pkg("survival", priority = "core")` contains descriptive
    statistics, two-sample tests, parametric accelerated failure models,
    Cox model. Delayed entry (truncation) allowed for all models;
    interval censoring for parametric models. Case-cohort designs.

-   [`​r pkg("rpact", priority = "core")`](#rpact).

#### *Other Analysis for Specific Designs*

-   `​r pkg("clinicalsignificance")` The goal of this package is to
    provide all necessary tools for analyses of clinical significance in
    clinical intervention studies. In contrast to statistical
    significance, which assesses if it is probable that there is a
    treatment effect, clinical significance can be used to determine if
    a treatment effect is of practical use or meaningful for patients.

-   `​r pkg("clinsig")` This package contains functions to calculate both
    parametric and non-parametric versions of the Jacobson-Truax
    estimates of clinical significance.

-   `​r pkg("MatchIt")` is an R package that selects matched samples of
    the original treated and control groups with similar covariate
    distributions. It can be used to match exactly on covariates, to
    match on propensity scores, or perform a variety of other matching
    procedures. The package also implements a series of recommendations
    offered in Ho et al. (2007)
    \<[doi:10.1093/pan/mpl013](https://doi.org/10.1093/pan/mpl013)\>.

-   `​r pkg("nppbib")` implements a nonparametric statistical test for
    rank or score data from partially-balanced incomplete block-design
    experiments.

-   `​r pkg("speff2trial", priority = "core")` performs estimation and
    testing of the treatment effect in a 2-group randomized clinical
    trial with a quantitative or dichotomous endpoint.

-   `​r pkg("ThreeGroups")` This package implements the Maximum
    Likelihood estimator for three-group designs proposed by Gerber et
    al. (2010).

### Monitoring

-   `​r pkg("accrualPlot")` Tracking accrual in clinical trials is
    important for trial success. `accrualPlot` provides functions to aid
    the tracking of accrual and predict when a trial will reach it’s
    intended sample size.

-   [`​r pkg("asd", priority = "core")`](#asd).

-   [`​r pkg("esDesign")`](#esDesign).

-   `​r pkg("monitOS")` Monitoring Overall Survival in Pivotal Trials in
    Indolent Cancers.

-   `​r pkg("PwrGSD")` provides tools for the evaluation of interim
    analysis plans for sequentially monitored trials on a survival
    endpoint; tools to construct efficacy and futility boundaries, for
    deriving power of a sequential design at a specified alternative,
    template for evaluating the performance of candidate plans at a set
    of time varying alternatives.

-   [`​r pkg("rpact", priority = "core")`](#rpact).

-   [`​r pkg("SAME")`](#SAME).

-   `​r pkg("seqmon")` provides sequential monitoring of clinical trials.
    It calculates the efficacy and futility boundaries at each look. It
    allows modifying the design and tracking the design update history.
