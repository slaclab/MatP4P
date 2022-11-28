# MatP4P: Integrate EPICS7 into MATLAB using PVAccess for Python (P4P) module

## Motivation
Many scientists in SLAC use MATLAB for data analysis. Thus, they need to use EPICS7 in the MATLAB environment. There were some efforts to integrate EPICS into MATLAB such as eget and labca. But, they are based on Java, and although PVAcess recommends JDK 8 or higher, MATLAB 2020a uses Java version 1.8 in the SLAC network. Therefore, MatP4P is developed to integrate EPICS7 into MATLAB based on Python using the P4P module to use PVAcess.

## How to use
1. MatP4Pget
```
[PV, ts, alarm] = MatP4Pget(pvname)     # PV is NTScalar or NTScalarArray type.
[NTTable, NTStruct, ts, alarm] = MatP4Pget(pvname)      # PV is NTTable type     
```
2. MatP4Pput
```
MatP4Pput(pvname, value)      # PV is NTScalar or NTScalarArray type.
MatP4Pput(pvname, field1, value1, field2, value2, ...)      # PV is NTTable type
MatP4Pput(pvname, struct/table)     # PV is NTTable type
```



## Documnetation
https://confluence.slac.stanford.edu/display/~ktkim/MatP4Pget+and+MatP4Pput%3A+Integrate+EPICS7+into+MATLAB+using+PVAccess+for+Python+%28P4P%29+module
