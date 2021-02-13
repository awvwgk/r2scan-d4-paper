# r²SCAN-D4


## Functional Implementation

- r²SCAN-D4 is available in Turbomole 7.5.1 using the `r2scan` functional in the dft data group and the disp4 data group
```
$disp4
$dft
  functional r2scan
```

- r²SCAN can be used with [libxc version 5.1.0](https://www.tddft.org/programs/libxc/changes/#510---2021-01-19) as `MGGA_X_R2SCAN` (id=497), `MGGA_C_R2SCAN` (id=498)
- [XCFun 2.1.0](https://github.com/dftlibs/xcfun/releases/tag/v2.1.0) also implements support for the r²SCAN functional
- routines for r²SCAN functional implementation can be found at https://gitlab.com/dhamil/r2scan-subroutines (Fortran), routines for Vasp are included
- Libraries implementing DFT-D4 can be found at https://github.com/dftd4/dftd4 (Fortran) and https://github.com/dftd4/cpp-d4 (C++)


## Functional parameters

| method | s6 | s8 | s9 | a1 | a2/Bohr |
| --- | --- | --- | --- | --- | --- |
| r²SCAN-D4(EEQ)-ATM | 1 | 0.60187490 | 1 | 0.51559235 | 5.77342911 |
| r²SCAN-D3(BJ)-ATM | 1 | 0.78981345 | 1 | 0.49484001 | 5.73083694 |
| rSCAN-D4(EEQ)-ATM | 1 | 0.87728975 | 1 | 0.49116966 | 5.75859346 |
| rSCAN-D3(BJ)-ATM | 1 | 1.08859014 | 1 | 0.47023427 | 5.73408312 |

| method | b |
| --- | --- |
| r²SCAN-VV10 | 12.3 |
| rSCAN-VV10 | 10.8 |


## Benchmark Results

### NCIBLIND

Statistics in kcal/mol, Gini coefficients are dimensionless.

| method | MD | MAD | RMSD | SD | Gini |
| --- | ---:| ---:| ---:| ---:| ---: |
| r²SCAN-D4-ATM/def2-QZVP | –0.05 | 0.17 | 0.29 | 0.29 | 0.64 |
| r²SCAN-D3(BJ)-ATM/def2-QZVP | –0.05 | 0.18 | 0.31 | 0.31 | 0.65 |
| r²SCAN-VV10/def2-QZVP | –0.09 | 0.17 | 0.31 | 0.30 | 0.65 |
| rSCAN-D4-ATM/def2-QZVP | –0.06 | 0.16 | 0.30 | 0.30 | 0.67 |
| rSCAN-D3(BJ)-ATM/def2-QZVP | –0.06 | 0.17 | 0.32 | 0.32 | 0.68 |
| rSCAN-VV10/def2-QZVP | –0.13 | 0.20 | 0.38 | 0.36 | 0.70 |

### S22x5

Statistics in kcal/mol, Gini coefficients are dimensionless.

| method | MD | MAD | RMSD | SD | Gini |
| --- | ---:| ---:| ---:| ---:| ---: |
| r²SCAN-D4-ATM/def2-QZVP | –0.12 | 0.28 | 0.51 | 0.50 | 0.65 |
| r²SCAN-D3(BJ)-ATM/def2-QZVP | –0.12 | 0.29 | 0.53 | 0.52 | 0.65 |
| r²SCAN-VV10/def2-QZVP | –0.07 | 0.32 | 0.56 | 0.56 | 0.61 |
| rSCAN-D4-ATM/def2-QZVP | –0.13 | 0.30 | 0.57 | 0.56 | 0.67 |
| rSCAN-D3(BJ)-ATM/def2-QZVP | –0.12 | 0.31 | 0.59 | 0.58 | 0.69 |
| rSCAN-VV10/def2-QZVP | –0.11 | 0.35 | 0.65 | 0.64 | 0.66 |

### S66x8

Statistics in kcal/mol, Gini coefficients are dimensionless.

| method | MD | MAD | RMSD | SD | Gini |
| --- | ---:| ---:| ---:| ---:| ---: |
| r²SCAN-D4-ATM/def2-QZVP | –0.09 | 0.23 | 0.38 | 0.36 | 0.56 |
| r²SCAN-D3(BJ)-ATM/def2-QZVP | –0.11 | 0.23 | 0.38 | 0.37 | 0.58 |
| r²SCAN-VV10/def2-QZVP | –0.05 | 0.28 | 0.43 | 0.43 | 0.54 |
| rSCAN-D4-ATM/def2-QZVP | –0.10 | 0.23 | 0.41 | 0.40 | 0.59 |
| rSCAN-D3(BJ)-ATM/def2-QZVP | –0.13 | 0.24 | 0.42 | 0.40 | 0.60 |
| rSCAN-VV10/def2-QZVP | –0.10 | 0.29 | 0.49 | 0.48 | 0.57 |


### GMTKN55

Statistics in kcal/mol.

| method | WTMAD-2 | basic | react. | barriers | inter. NCI | intra. NCI | NCI |
| --- | ---:| ---:| ---:| ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 8.83 | 5.05 | 9.62 | 13.84 | 11.35 | 8.36 | 9.89
| r²SCAN-D4-ATM/def2-QZVP | 7.54 | 5.55 | 8.26 | 14.29 | 7.46 | 5.74 | 6.62
| rSCAN/def2-QZVP | 9.79 | 6.16 | 9.55 | 15.19 | 12.27 | 9.69 | 11.01 |
| rSCAN-D4-ATM/def2-QZVP | 8.25 | 6.72 | 8.95 | 15.70 | 7.39 | 6.09 | 6.75 |
| SCAN/def2-QZVP | 9.35 | 5.95 | 9.25 | 16.76 | 11.02 | 8.27 | 9.68 |
| SCAN-D4-ATM/def2-QZVP | 8.61 | 6.56 | 8.43 | 17.00 | 8.76 | 6.37 | 7.59 |

| method | WTMAD-1 | basic | react. | barriers | inter. NCI | intra. NCI | NCI |
| --- | ---:| ---:| ---:| ---:| ---:| ---:| ---:|
| r²SCAN/def2-QZVP | 5.36 | 4.40 | 5.30 | 5.98 | 6.58 | 5.25 | 6.01
| r²SCAN-D4-ATM/def2-QZVP | 4.43 | 4.46 | 4.85 | 6.15 | 3.87 | 3.33 | 3.64
| rSCAN/def2-QZVP | 6.04 | 5.55 | 5.36 | 6.40 | 7.13 | 5.99 | 6.64 |
| rSCAN-D4-ATM/def2-QZVP | 4.95 | 5.64 | 5.06 | 6.60 | 4.06 | 3.37 | 3.76 |
| SCAN/def2-QZVP | 5.59 | 5.36 | 4.91 | 6.52 | 6.38 | 4.94 | 5.76 |
| SCAN-D4-ATM/def2-QZVP | 4.99 | 5.49 | 4.67 | 6.61 | 4.66 | 3.52 | 4.17 |

The MADs of all GMTKN55 subsets in kcal/mol are given here.
Values for TPSS-D4, PBE-D4 and PBE0-D4 are taken from Caldeweyher et al. *J. Chem Phys*, **2019**, 150, 154122. DOI: [10.1063/1.5090222](https://doi.org/10.1063/1.5090222).

| subset | r²SCAN-D4 | rSCAN-D4 | SCAN-D4 | TPSS-D4 | PBE-D4 | PBE0-D4 |
| --- | ---:| ---:| ----:| ---:| ---:| ---:|
| W4-11 | 3.86 | 6.52 | 3.77 | 5.89 | 15.62 | 3.67 |
| G21EA | 5.64 | 6.96 | 6.94 | 2.12 | 3.59 | 2.57 |
| G21IP | 4.77 | 4.82 | 4.90 | 3.87 | 3.80 | 3.64 |
| DIPCS10 | 5.05 | 4.83 | 4.91 | 3.28 | 4.22 | 2.84 |
| PA26 | 2.51 | 1.99 | 3.06 | 4.08 | 1.85 | 2.42 |
| SIE4x4 | 18.13 | 18.39 | 17.95 | 21.81 | 23.62 | 14.31 |
| ALKBDE10 | 5.93 | 6.00 | 6.08 | 4.22 | 6.36 | 5.69 |
| YBDE18 | 3.34 | 17.69 | 17.11 | 4.49 | 4.87 | 0.99 |
| AL2X6 | 1.59 | 1.80 | 1.89 | 2.28 | 1.59 | 1.33 |
| HEAVYSB11 | 3.24 | 2.83 | 2.12 | 2.59 | 3.53 | 1.40 |
| NBPRC | 1.55 | 2.16 | 2.32 | 1.37 | 2.41 | 3.08 |
| ALK8 | 2.84 | 4.23 | 3.04 | 0.80 | 2.21 | 2.36 |
| RC21 | 4.85 | 5.23 | 5.81 | 4.41 | 6.75 | 5.37 |
| G2RC | 5.65 | 5.75 | 6.32 | 7.23 | 6.94 | 6.71 |
| BH76RC | 3.17 | 14.97 | 9.38 | 3.59 | 4.17 | 2.45 |
| FH51 | 4.58 | 4.62 | 5.02 | 6.34 | 5.07 | 4.68 |
| TAUT15 | 1.57 | 1.73 | 1.74 | 1.60 | 1.80 | 1.13 |
| DC13 | 7.85 | 8.17 | 6.98 | 8.11 | 8.93 | 8.43 |
| MB16-43 | 14.62 | 16.02 | 17.32 | 25.84 | 25.10 | 15.99 |
| DARC | 2.72 | 2.78 | 2.13 | 4.64 | 3.13 | 3.94 |
| RSE43 | 1.60 | 1.82 | 1.53 | 2.08 | 2.93 | 1.57 |
| BSR36 | 0.44 | 0.94 | 1.63 | 3.09 | 2.30 | 2.73 |
| CDIE20 | 1.62 | 1.62 | 1.48 | 1.72 | 1.70 | 1.29 |
| ISO34 | 1.30 | 1.32 | 1.33 | 2.31 | 1.49 | 1.43 |
| ISOL24 | 4.04 | 4.03 | 3.37 | 5.30 | 4.19 | 2.08 |
| C60ISO | 5.56 | 5.48 | 6.17 | 9.74 | 11.80 | 2.11 |
| PArel | 1.54 | 1.63 | 1.49 | 1.53 | 1.77 | 1.20 |
| BH76 | 7.34 | 14.97 | 9.38 | 9.25 | 9.61 | 4.99 |
| BHPERI | 4.67 | 4.62 | 5.24 | 5.89 | 6.82 | 3.30 |
| BHDIV10 | 6.12 | 6.39 | 6.57 | 7.00 | 8.89 | 4.81 |
| INV24 | 2.33 | 2.44 | 2.33 | 1.89 | 2.06 | 1.14 |
| BHROT27 | 0.76 | 0.83 | 0.84 | 0.53 | 0.47 | 0.58 |
| PX13 | 8.93 | 9.64 | 8.25 | 8.91 | 11.95 | 6.49 |
| WCPT18 | 6.11 | 6.59 | 6.14 | 6.36 | 9.29 | 4.29 |
| RG18 | 0.17 | 0.15 | 0.18 | 0.13 | 0.26 | 0.09 |
| ADIM6 | 0.36 | 0.12 | 0.49 | 0.38 | 0.09 | 0.19 |
| S22 | 0.29 | 0.34 | 0.40 | 0.33 | 0.42 | 0.41 |
| S66 | 0.30 | 0.32 | 0.41 | 0.33 | 0.38 | 0.36 |
| HEAVY28 | 0.29 | 0.22 | 0.28 | 0.38 | 0.47 | 0.28 |
| WATER27 | 6.72 | 6.67 | 9.12 | 4.16 | 8.28 | 5.35 |
| CARBHB12 | 1.13 | 1.41 | 1.30 | 1.36 | 1.84 | 1.36 |
| PNICO23 | 0.82 | 0.97 | 0.99 | 1.15 | 1.36 | 0.89 |
| HAL59 | 0.81 | 0.88 | 1.02 | 1.07 | 1.29 | 0.62 |
| AHB21 | 3.50 | 3.62 | 3.86 | 0.73 | 1.24 | 1.31 |
| CHB6 | 0.46 | 0.42 | 0.46 | 0.71 | 0.67 | 1.13 |
| IL16 | 0.76 | 0.88 | 1.02 | 0.35 | 0.96 | 0.50 |
| IDISP | 2.56 | 2.52 | 2.46 | 2.77 | 2.55 | 1.47 |
| ICONF | 0.30 | 0.29 | 0.31 | 0.16 | 0.31 | 0.27 |
| ACONF | 0.18 | 0.12 | 0.22 | 0.12 | 0.08 | 0.06 |
| AMINO20x4 | 0.19 | 0.21 | 0.22 | 0.36 | 0.33 | 0.25 |
| PCONF21 | 0.42 | 0.44 | 0.40 | 0.83 | 0.99 | 0.74 |
| MCONF | 0.45 | 0.50 | 0.43 | 0.44 | 0.47 | 0.27 |
| SCONF | 0.54 | 0.57 | 0.61 | 1.22 | 0.88 | 0.32 |
| UPU23 | 0.39 | 0.34 | 0.38 | 0.45 | 0.51 | 0.54 |
| BUT14DIOL | 0.27 | 0.31 | 0.37 | 0.47 | 0.59 | 0.31 |


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

### LB12

Statistics in pm.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | 1.81 | 3.57 | 5.67 | 5.61 |

### CCse21

Bond lengths. Statistics in pm.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | 0.03 | 0.38 | 0.56 | 0.57 |


Bond angles. Statistics in deg.

| method | MD | MAD | RMSD | SD |
| --- | ---:| ---:| ---:| ---:|
| r²SCAN-D4-ATM/def2-QZVP | 0.01 | 0.29 | 0.37 | 0.37 |



