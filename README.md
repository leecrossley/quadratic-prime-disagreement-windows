# Eightfold changes in a quadratic prime race

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24416495.svg)](https://doi.org/10.5281/zenodo.24416495)

This result is now maintained in [quadratic-mertens-first-crossings](https://github.com/leecrossley/quadratic-mertens-first-crossings/tree/main/results/quadratic-prime-disagreement-windows). This repository is archived and keeps its releases and DOI.

Take the primes that split in $`\mathbb Q(\sqrt d)`$ and stay inert in $`\mathbb Q(\sqrt5)`$. Subtract the primes that do the reverse. Weight each prime above $`y`$ by $`(1-y/p)/p`$ and multiply the difference by $`\sqrt y\log y`$. Call the result $`W(\log y)`$.

For every positive fundamental discriminant beyond an ineffective bound there are starting points below a single power of $`d`$ where multiplying $`y`$ by eight increases this lead by more than $`0.46`$, and others where it decreases it by more than $`0.46`$. Somewhere the absolute change is at least $`c\sqrt{\log d}`$ for an absolute $`c>0`$. These bounds use RH for $`\zeta`$ and the critical-line property of the two quadratic Dirichlet functions. Alpöge's announced Dirichlet GRH theorem supplies this input. Central zeros and close pairs are allowed. [Proof](PROOF.md) · [Announcement](https://alpo.ge/remark.pdf) · [Independent formal checks](https://math.mit.edu/~drew/grh/)

In a Yokoi field where the log-product average stays nonnegative up to this fixed power, the primes that split in the reference field and stay inert in the Yokoi field must acquire a lead of at least $`c_1\sqrt{\log d}`$ on a finite weighted window. Its top prime cutoff is only $`O(y\log d)`$. Proving that every sufficiently large Yokoi field has a negative average still requires control over the absolute level of the race. The exponents and asymptotic constants here are existential, and the threshold on $`d`$ is not effective. [Finite-window consequence](PROOF.md) · [Original problem 8](https://arxiv.org/pdf/2407.03530#page=4)

At $`d=533=23^2+4`$ the infinite weighted difference falls by between $`1.030`$ and $`1.033`$ from $`y=30`$ to $`240`$, and rises by between $`0.818`$ and $`0.822`$ from $`512`$ to $`4096`$. At $`y=30`$ the normalised average lies between $`-0.071674`$ and $`-0.071672`$. [Arithmetic certificates](CHECKS.md)

## Reproduce the checks

```sh
python3 -m venv .venv
.venv/bin/python -m pip install -r requirements.txt
PYTHON=.venv/bin/python sh verify-release.sh
```

The two calculations enclose the infinite prime tails separately. Lean checks the diagonal-square inequality, the orientation and taper identities, and the inference from a large change to a large adverse lead. The analysis connecting the zero series to primes is a written proof. [Check details and Lean replay](CHECKS.md) · [Prior work](PRIOR-WORK.md)
