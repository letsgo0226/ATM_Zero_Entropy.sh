# ATM_Zero_Entropy.sh

`ATM_Zero_Entropy.sh` is a 2KB one-line self-verifying universal dovetailer for ATM zero-entropy closure.

It reads two lines from stdin:

```text
N = finite machine/input prefix, blank defaults to 8
B = finite dovetailing stages, blank defaults to 16
```

The script enumerates a finite prefix of two-state/two-symbol Turing machines and unary inputs, fairly advances each `(M_i, X_j)`, records trace entries, and reports discovered `HALT` witnesses.

Its zero-entropy state is computed rather than merely declared:

```text
ZE_ATM = ENUM and FAIR and STEP and HALT and SELF and ZP[2] == 0
```

The `SELF` check reads the running script path `$0` and requires the source to contain the `ATM-ZE` marker. The output certificate is `ATM_Zero_Entropy.clcert`.

Within this formal system, `ATM(N,B)` is a completed self-observation window. When all checks close, the ATM has solved its own information zero-entropy state for that run.
