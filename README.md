# ase-20-rp
Replication package for ASE 2020 submission

## BLIZZARD replication

Directory `blizzard` contains:

1. Replication of the results reported by the [BLIZZARD authors][1] in `blizzard-replication.csv`.
2. We had to reverse-engineer the Lucene index that BLIZZARD uses. To verify the results, we evaluated the original systems using our implementation of the index. Results in `blizzard-re.csv`

## Reformulated queries

`reformulated-queries` contains the non-preprocessed reformulated queries which correspond to the 1,405 low-quality queries used in our study. There is one csv file corresponding to each strategy evaluated in sec. 4.5 (970), with the addition of `ALL_TEXT.csv` (containing the full text of each bug report), and `BLIZZARD--ALL_TEXT.csv` (the result of running BLIZZARD on the full text of the bug reports).

Each file contains the queries that contain all the components that are part of the corresponding strategy, e.g., if a query does not contain OB, it will not appear in `OB.csv`, `BLIZZARD-OB.csv`, `EB--OB.csv`, etc.

## Results

The `results` directory contains:

1. `trbl-results.csv` contains the results for each combination of technique, threshold (N), granularity, and strategy. (WARNING: large file)
2. `result-summary-*.csv` contains a summary of all strategies (Table 7), for both combinatorial and conjunctive reformulations.
3. `stat-tests` contains the full results of the statistical tests presented in section 4.
4. `query-stats.csv` contains the full Table 10.

[1]: https://doi.org/10.1145/3236024.3236065
