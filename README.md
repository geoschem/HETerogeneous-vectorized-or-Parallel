## HETP: HETerogeneous-vectorized-or-Parallel 
 
HETP is an aerosol thermodynamic equilibrium solver written in modern Fortran based on ISORROPIA II (which is written in FORTRAN 77).  HETP solves only the 'forward' metastable state of the NH4+/Na+/Ca2+/K+/Mg2+/SO42–/NO3–/Cl–/H2O system.  The main publication for HETP is avaiable online at:  https://gmd.copernicus.org/preprints/gmd-2023-159/.

This repository contains the HETP case-by-case implementation, with a simple interface to call HETP for a single set of input conditions.  The file 'hetp_main.F90' is a Fortran script to interact with HETP, the file 'hetp_mod.F90' holds the HETP code and the file 'mach_hetp_mod.F90' holds parameters used in HETP.  Input required are the total gas + aerosol concentrations of eight precursor species with units of mol/m^3 air (i.e., sulfate, ammonium, nitrate, sodium, chloride, calcium, potassium, magnesium), the relative humidity (on a 0-1 scale) and the air temperature (units of K).
