# Coverage-based-Query-Rewriting

The proposed Coverage-based Query Rewriting approach automatically rewrites a back-end transformation, defined in terms of a Select-Project-Join query, whose result violates some coverage constraints, into the "closest" query satisfying those constraints.

The proposed approach is approximate and relies on a sample-based cardinality estimation, thus it introduces a trade-off between the accuracy and the efficiency of the process.
For evaluating and quantifying the error that can be generated three grioups of measures have been introduced: the grid-based, the solution-based and the sample-based accuracy measures.

This repository contains both the code for running the proposed Coverage-based Query Rewriting algorithm and the proposed accuracy measures.

The code is written in Python3.
PostgreSQL is required to run this code (you can extend it to other DBMS)


### Organization of the repository
This repository is organized as follows:

- *1_coverage_rewriting_sql.py* : this file contains the code for running CRBase and all the improved versions (CRBaseP, CRBaseI, CRBaseIP). Notice that in the code you will find also additional information needed for the experimental evaluation.
- *2_calc_measures_sol.py* : this file contains the grid-based and the solution-based measures that have been defined for evaluating the solution of the proposed approach (for more details see the reference paper)
- *2_calc_measures_sample.py* : this file contains the measures for evaluating the impact of the sample. Notice that you need to add the computation of the average values for obtaining the sample-based measures as discussed in the reference paper


### References

- **Coverage-based Rewriting for Data Preparation**, C. Accinelli, S. Minisi and B. Catania. EDBT Workshop 2020

- **The impact of rewriting on coverage constraint satisfaction** C. Accinelli, B. Catania, G. Guerrini and S. Minisi. EDBT Workshop 2021.

- **covRew: a Python Toolkit for Pre-Processing Pipeline Rewriting Ensuring Coverage Constraint Satisfaction** C. Accinelli, B. Catania, G. Guerrini and S. Minisi. EDBT 2021.
