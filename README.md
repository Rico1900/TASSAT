# TASSAT

### Environment
TASSAT depends on IBM cplex which is a proprietary library to perform linear programming. Therefore, before running TASSAT, it is necessary to buy IBM culex library and make sure that `cplex125.dll` is included in your Java path.

## Command

```bash
java -jar TASSAT.jar /path/to/TASSAT-protocol.json
```

### Experiment Protocol

There is an experimental protocol sample file `TASSAT-protocol.json` in this repository. When running TASSAT, the protocol file should be given through the program arguments. The meaning of the configuration is given as follow:

- type: the technique type including  TASS, TASSAT, and IIS_GEN.
- bound: the path bound.
- targets: the target node.
- baseDir: the directory path to the case.

# TASSAT-SMT

### Dependencies

TASSAT-SMT depends on SMT solvers Z3 and Yices2 through JNI, so please add the correspondent binaries and libraries to your Java path according your operating system.

## Command

```bash
java -jar TASSAT-SMT.jar /path/to/TASSAT-SMT-protocol.json
```

### Experiment Protocol

There is an experimental protocol sample file `TASSAT-SMT-protocol.json` in this repository. When running TASSAT-SMT, the protocol file should be given through the program arguments. The meaning of the configuration is given as follow:

- type: the technique type which is always "TASSAT-SMT".
- targets: the target node.
- bound: the path bound.
- solver: the SMT solver including Z3, Yices, and Interpol.
- inputFolder: the directory path to the case.