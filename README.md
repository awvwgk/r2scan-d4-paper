# r²SCAN-D4


## Functional parameters

| method | s6 | s8 | s9 | a1 | a2/Bohr |
| --- | --- | --- | --- | --- | --- |
| r²SCAN-D4(EEQ)-ATM | 1 | 0.60187490 | 1 | 0.51559235 | 5.77342911 |
| r²SCAN-D3(BJ)-ATM | 1 | 0.78981345 | 1 | 0.49484001 | 5.73083694 |
| rSCAN-D4(EEQ)-ATM | 1 | 0.87728975 | 1 | 0.49116966 | 5.75859346 |
| rSCAN-D3(BJ)-ATM | 1 | 1.08859014 | 1 | 0.47023427 | 5.73408312 |


## Benchmark Results

### GMTKN55

Statistics in kcal/mol.

| method | WTMAD-2 | basic | react. | barriers | inter. NCI | intra. NCI | NCI |
| --- | ---:| ---:| ---:| ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 9.00 | 5.50 | 9.62 | 13.94 | 11.41 | 8.36 | 9.92 |
| r²SCAN-D4-ATM/def2-QZVP | 7.71 | 6.00 | 8.26 | 14.40 | 7.53 | 5.74 | 6.65 |
| rSCAN/def2-QZVP | 9.79 | 6.16 | 9.55 | 15.19 | 12.27 | 9.69 | 11.01 |
| rSCAN-D4-ATM/def2-QZVP | 8.25 | 6.72 | 8.95 | 15.70 | 7.39 | 6.09 | 6.75 |
| SCAN/def2-QZVP | 9.35 | 5.95 | 9.25 | 16.76 | 11.02 | 8.27 | 9.68 |
| SCAN-D4-ATM/def2-QZVP | 8.61 | 6.56 | 8.43 | 17.00 | 8.76 | 6.37 | 7.59 |

| method | WTMAD-1 | basic | react. | barriers | inter. NCI | intra. NCI | NCI |
| --- | ---:| ---:| ---:| ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 5.51 | 4.86 | 5.30 | 6.05 | 6.54 | 5.25 | 5.99 |
| r²SCAN-D4-ATM/def2-QZVP | 4.58 | 4.92 | 4.85 | 6.22 | 3.84 | 3.33 | 3.62 |
| rSCAN/def2-QZVP | 6.04 | 5.55 | 5.36 | 6.40 | 7.13 | 5.99 | 6.64 |
| rSCAN-D4-ATM/def2-QZVP | 4.95 | 5.64 | 5.06 | 6.60 | 4.06 | 3.37 | 3.76 |
| SCAN/def2-QZVP | 5.59 | 5.36 | 4.91 | 6.52 | 6.38 | 4.94 | 5.76 |
| SCAN-D4-ATM/def2-QZVP | 4.99 | 5.49 | 4.67 | 6.61 | 4.66 | 3.52 | 4.17 |

### MOR41

Statistics in kcal/mol.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 2.10 | 4.45 | 5.94 | 5.63 |
| r²SCAN-D4-ATM/def2-QZVP | –0.21 | 3.29 | 4.27 | 4.32 |
| rSCAN/def2-QZVP | 2.24 | 4.66 | 6.24 | 5.90 |
| rSCAN-D4-ATM/def2-QZVP | –0.49 | 3.22 | 4.36 | 4.38 |

### L7

Statistics in kcal/mol.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 9.26 | 9.26 | 10.36 | 5.01 |
| r²SCAN-D4-ATM/def2-QZVP | 0.51 | 0.86 | 1.00 | 0.93 |
| rSCAN/def2-QZVP | 10.33 | 10.33 | 11.58 | 5.65 |
| rSCAN-D4-ATM/def2-QZVP | 0.40 | 0.66 | 0.78 | 0.72 |
| SCAN/def2-QZVP | 8.02 | 8.02 | 9.07 | 4.54 |
| SCAN-D4-ATM/def2-QZVP | 1.13 | 1.29 | 1.59 | 1.21 |

### S30L

Statistics in kcal/mol.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 12.86 | 12.86 | 15.24 | 8.32 |
| r²SCAN-D4-ATM/def2-QZVP | –1.82 | 1.93 | 2.60 | 1.88 |
| rSCAN/def2-QZVP | 14.63 | 14.63 | 17.41 | 9.61 |
| rSCAN-D4-ATM/def2-QZVP | –2.04 | 2.09 | 2.75 | 1.89 |

### X40x10

Statistics in kcal/mol.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 0.29 | 0.61 | 0.97 | 0.93 |
| r²SCAN-D4-ATM/def2-QZVP | –0.16 | 0.36 | 0.67 | 0.65 |
| SCAN/def2-QZVP | –0.03 | 0.57 | 0.91 | 0.91 |
| SCAN-D4-ATM/def2-QZVP | –0.34 | 0.46 | 0.84 | 0.77 |
| PBE0-D4-ATM/def2-QZVP | –0.22 | 0.38 | 0.67 | 0.63 |
| TPSS-D4-ATM/def2-QZVP | –0.20 | 0.38 | 0.61 | 0.57 |
| PBE-D4-ATM/def2-QZVP | –0.45 | 0.48 | 0.80 | 0.72 |

### LMGB35

Statistics in pm.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | –0.12 | 0.68 | 1.01 | 1.02 |

### HMGB11

Statistics in pm.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | 0.51 | 1.17 | 1.34 | 1.29 |

### TMC32

Statistics in pm.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | –1.57 | 1.89 | 2.35 | 1.77 |

### ROT34

Statistics in MHz.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | –3.22 | 4.64 | 5.88 | 4.99 |
