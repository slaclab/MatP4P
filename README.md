# MatPva: Integrate EPICS7 into MATLAB using PVAccess for Python (P4P) module

## Motivation
Many scientists in SLAC use MATLAB for data analysis. Thus, they need to use EPICS7 in the MATLAB environment. There were some efforts to integrate EPICS into MATLAB such as eget and labca. But, they are based on Java, and although PVAcess recommends JDK 8 or higher, MATLAB 2020a uses Java version 1.8 in the SLAC network. Therefore, MatPva is developed to integrate EPICS7 into MATLAB based on Python using the P4P module to use PVAcess.
<br /><br />

## Prerequisites
- Python: 3.8.13+
- p4p: 4.1.4+
- Matlab: 2020a+

> **Note**: Although MatPva is tested in Python 3.8.13, p4p 4.1.4, Matlab 2020a, there are still chances that some previous versions might work.

## Function and test scripts
Python scripts to run Test PVs: pva_testing_ioc.py, matlab_model_pvs.py

MATLAB scripts to test mpvaGet() and mpvaPut(): mpvaGet_test_script.m, mpvaPut_test_script.m 
<br /><br />

## Running test scripts
```
python pva_testing_ioc.py    # Most of PVs including NTScalar, NTScalarArray, NTTable data type
python matlab_model_pvs.py   # TWISS NTTable PV
```

## How to use
1. mpvaGet
```
[PV, ts, alarm] = mpvaGet(pvname)     # PV is NTScalar or NTScalarArray type.
[NTTable, NTStruct, ts, alarm] = mpvaGet(pvname)      # PV is NTTable type     
```
2. mpvaPut
```
mpvaPut(pvname, value)      # PV is NTScalar or NTScalarArray type.
mpvaPut(pvname, field1, value1, field2, value2, ...)      # PV is NTTable type
mpvaPut(pvname, struct/table)     # PV is NTTable type
```

## Documnetation
https://confluence.slac.stanford.edu/display/~ktkim/mpvaGet+and+mpvaPut%3A+Integrate+EPICS7+into+MATLAB+using+PVAccess+for+Python+%28P4P%29+module
