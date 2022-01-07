# ElectionAuditWareRepo
Repository for Google Group ElectionAuditWare, re post-election audit software and tools.

See Google Group:
    https://groups.google.com/forum/#!forum/electionauditware

## Existing related software

### General purpose auditing software

* [Arlo](https://github.com/votingworks/arlo): open-source software for Risk-Limiting Audits in the US, via [VotingWorks](https://voting.works). Should eventually handle most auditing methods and best practices.
* [FreeAndFair/ColoradoRLA: Software to facilitate risk-limiting audits at the state level, developed for the state of Colorado.](https://github.com/FreeAndFair/ColoradoRLA) - as used in Colorado 2017 and 2018 Primaray, and Orange County 2018, but see updated version at democracyworks:
  * [democracyworks/ColoradoRLA: Software to facilitate risk-limiting audits at the state level, developed for the state of Colorado.](https://github.com/democracyworks/ColoradoRLA) - as used in Colorado 2018, 2019 General election, to do multi-county audits and improve many other aspects.
* [Tools for Comparison Risk-Limiting Election Audits](https://www.stat.berkeley.edu/~stark/Vote/auditTools.htm) - when Cast Vote Records can be matched to paper ballots - Philip Stark's online web app
* [Tools for Ballot-Polling Risk-Limiting Election Audits](https://www.stat.berkeley.edu/~stark/Vote/ballotPollTools.htm) - when paper can't be matched to CVRs - Philip Stark's online web app

* [nealmcb/ocrla-2018p: Orange County California, ballot-polling risk-limiting audit of 2018 primary](https://github.com/nealmcb/ocrla-2018p) - working around limitations of ColoradoRLA to do ballot-polling audits.

* [nealmcb/kaplan\_markov: Kaplan-Markov Risk\-Limiting Batch Comparison Audits](https://github.com/nealmcb/kaplan_markov): Straightforward, flexible core library in Python 3, with example notebook - alpha release
* [ElectionAuditWare/audit-conductor: Conduct a risk-limiting election tabulation audit, integrating various related tools](https://github.com/ElectionAuditWare/audit-conductor) - for Rhode Island pilot in 2019
* [agupta231/RIWAVE: Rhode Island RLA project](https://github.com/agupta231/RIWAVE)
* [nealmcb/audit_cvrs: audit_cvrs helps auditors manage a ballot-level risk-limiting post-election audit](https://github.com/nealmcb/audit_cvrs) - Django-based 2013/2014 code for observing early pilots in Colorado  
* [FreeAndFair/OpenRLA: Free & Fair's open source RLA support software.](https://github.com/FreeAndFair/OpenRLA) - a 2016 Free & Fair prototype for ballot polling audits, before the ColoradoRLA contract.
* [nealmcb/electionaudits: Post-election risk-limiting audit implementation, for batch comparison risk-limiting audits of ballot tabulation outcomes](http://bcn.boulder.co.us/~neal/electionaudits/) (and [on github](https://github.com/nealmcb/electionaudits) - used in Boulder County, Colorado, 2008 and 2010

### Choosing random samples of precincts or ballots to audit

* [ron-rivest/consistent_sampler: Routine for providing 'consistent sampling' (intended for use in election audits)](https://github.com/ron-rivest/consistent_sampler) - allows efficient sampling from multiple overlapping districts (statewide, countywide, and arbitrary districts) or at multiple points in time.

* [Pseudo-Random Number Generator using SHA-256](https://www.stat.berkeley.edu/~stark/Java/Html/sha256Rand.htm) - web app for Rivest's sampler algorithm

* [nealmcb/rivest-sampler-tests: Test cases for Ronald L. Rivest's pseudo-random sampling algorithm](https://github.com/nealmcb/rivest-sampler-tests) - Rivest's classic "sampler" Python implementation of the algorithm underlying many risk-limiting audits
  * and [nealmcb/rivest-sampler-tests at python-test](https://github.com/nealmcb/rivest-sampler-tests/tree/python-test)

* [pbstark/BernoulliBallotPolling: Code for Bernoulli Ballot Polling paper](https://github.com/pbstark/BernoulliBallotPolling): geometric_skipping, SPRT, and state data for 2016 Presidential contest
* [Dice Binning Calculator](https://www.josephhall.org/dicebins.php) - Joeseph Lorenzo Hall's web app for picking precincts to audit directly via dice rolls


### Lower-level Audit calculations
* [SHANGRLA: Sets of Half-Average Nulls Generate Risk-Limiting Audits](https://github.com/pbstark/SHANGRLA) - a very general method of auditing a variety of election types, by expressing an apparent election outcome as a series of assertions. Works for plurality, IRV, Borda etc.
* [audit-irv-cp for generating and running ballot-level comparison audits for IRV elections](https://github.com/michelleblom/audit-irv-cp) - Used in conjunction with SHANGRLA for single-winner RCV contests.
* [rlacalc: Online Calculator for Risk-Limiting Audit Sample Sizes](http://bcn.boulder.co.us/~neal/electionaudits/rlacalc.html) - provides ballot-level comparison, ballot-polling and other calculations
  * source code at [audit_cvrs/rlacalc.py](https://github.com/nealmcb/audit_cvrs/blob/ballot-polling/audit_cvrs/rlacalc.py) - with general-purpose Python library
* [pbstark/DKDHondt14: Risk-limiting audit code for Proportional Representation via Highest Averages - D'Hondt etc.](https://github.com/pbstark/DKDHondt14/blob/master/danmark14EU.ipynb) - Stark and Teague, 2015. Handles many European elections. Probably a good starting point for auditing delegate allocation in US presidential primary elections, which can vary by state, but which tend to use [largest remainder methods](https://en.wikipedia.org/wiki/Largest_remainder_method)
* [r2b2 repo from George Washington University project on election auditing research](https://github.com/gwexploratoryaudits/r2b2) with Minerva and other Athena audits for improved efficiency in round-by-round ballot-polling audits, as described in [The Athena Class of Risk-Limiting Ballot Polling Audits](https://arxiv.org/abs/2008.02315) and [Risk-Limiting Bayesian Polling Audits for Two Candidate Elections by Poorvi Vora](http://arxiv.org/abs/1902.00999), along with other exploratory work at [gwexploratoryaudits/brla\_explore: exploratory code related to bayesian rlas](https://github.com/gwexploratoryaudits/brla_explore) including a MATLAB implementation of Minerva
* [filipzz/athena: Athena \- round by round Risk Limiting Audit](https://github.com/filipzz/athena) - another implementation of the Minerva and related Athena-class audits.
* [ron-rivest/2018-bptool](https://github.com/ron-rivest/2018-bptool) Bayesian ballot polling calculations
* [ron-rivest/2018-bctool](https://github.com/ron-rivest/2018-bctool) Bayesian ballot-level comparison calculations
* [ron-rivest/2017-bayes-audit: Repository for paper "Bayesian Tabulation Audits Explained and Extended"](https://github.com/ron-rivest/2017-bayes-audit) with extensive simulations
* [ron-rivest/2016-aus-senate-audit](https://github.com/ron-rivest/2016-aus-senate-audit) a Bayesian approach to support work on auditing the 2016 Australian Senate elections, which use the [Single transferable vote](https://en.wikipedia.org/wiki/Single_transferable_vote) method, one of many forms of ranked choice voting.

* [CORLA18: Risk-Limiting Audits by Stratified Union-Intersection Tests of Elections (SUITE)](https://github.com/pbstark/CORLA18) - Ottoboni / Stark code for combining ballot-polling and ballot-level comparison data, for WI pilot audit
* [ALPHA: Audit that Learns from Previously Hand-Audited Ballots](https://github.com/pbstark/alpha) - a generalization of BRAVO, particularly useful in combination with SUITE or SHANGRLA.
* [pr_voting_methods: Proportional Representation Voting Methods, Data, and Auditing](https://github.com/nealmcb/pr_voting_methods)
* [michelleblom/margin-stv: Code base and test suite for paper 'Towards Computing the Margin of Victory for STV Elections'](https://github.com/michelleblom/margin-stv) - Calculates upper and lower bounds on the margin of a Single-Transferrable Vote contest, and exact bounds for small ones.

### Election data standards, repositories and analyses
* [NIST SP 1500-100 election results reporting standard](https://www.nist.gov/itl/voting/interoperability/election-results-reporting-cdf)
* [usnistgov/CastVoteRecords: Common data format specification for cast vote records](https://github.com/usnistgov/CastVoteRecords)
* [epaulson/PyCastVoteRecords: Basic Python library to create a NIST Common Data Formats file for cast vote records](https://github.com/epaulson/PyCastVoteRecords)

* [Audit Data Formats for transparency, replication](https://github.com/democracyworks/ColoradoRLA/blob/master/docs/26_export_manual.md): The format of data produced by ColoradoRLA's `rla_export` tool for the [Public RLA Oversight Protocol](http://bcn.boulder.co.us/~neal/elections/PublicRLAOversightProtocol.pdf).
* [nealmcb/corla-2018-11: Analysis of Colorado risk-limiting audit for 2018-11 (general election)](https://github.com/nealmcb/corla-2018-11)

* [nealmcb/electionaudits-data: Data related to election auditing, including post-election risk-limiting audits of ballot tabulation outcomes](https://github.com/nealmcb/electionaudits-data)
* [OpenElections: Certified election results. For everyone.](http://www.openelections.net/)
* [openelections/specs: Specs for OpenElections Data](https://github.com/openelections/specs)
* [openelections/clarify: Discover and parse results for jurisdictions that use Clarity-based election systems.](https://github.com/openelections/clarify)
  * and perhaps [nealmcb/clarify at audit](https://github.com/nealmcb/clarify/tree/audit)

* [SOBA: Secrecy-preserving Observable Ballot-level Audit - arxiv 1105.5803](https://arxiv.org/abs/1105.5803) - would presumably need a modified CVR standard

* [GSWarrington/accumulation-chart: Interactive accumulation charts for IRV](https://github.com/GSWarrington/accumulation-chart) - a beautiful way to expose many details in IRV results as demonstrated at [Accumulation Charts demo](http://www.cems.uvm.edu/~gswarrin/accumulation-chart.html)
