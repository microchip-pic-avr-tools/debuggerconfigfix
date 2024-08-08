[![MCHP](images/microchip.png)](https://www.microchip.com)

# debuggerconfigfix binary releases
Easy-to-use solution for fixing/updating configuration of select Curiosity Nano debuggers

Supported kits:
- AVR16EB32 Curiosity Nano
- AVR64DU32 Curiosity Nano

Consult the Errata section of the Curiosity Nano User Guide for more information before using this utility.

## Getting Started

### Download
Download the [latest release](https://github.com/microchip-pic-avr-tools/debuggerconfigfix/releases/latest) and extract the binary from the appropriate archive for either Windows®, macOS® or Linux® operating systems.

### Fixing/updating configuration
Run the utility from a command-prompt/terminal:
```
debuggerconfigfix
```
Check for success by examining the output for:
```
*** Debugger configuration SUCCESS ***
```
A detailed log file is stored in the same path as the binary after execution.

### Additional information / advanced topics
To fix the configuration of a specific serial number:
```
debuggerconfigfix -s <serialnumber>
```

The debuggerconfigfix utility is a purpose-built binary wrapper around the [pydebuggerconfig](https://pypi.org/project/pydebuggerconfig/) utility.
pydebuggerconfig requires an installation of Python and can be installed using:
```
pip install pydebuggerconfig
```
This is only recommended for advanced users familiar with Python and the Curiosity Nano debugger ecosystem.

The debuggerconfigfix utility replaces only the User Configuration section in the Curiosity Nano debugger.  The Factory Configuration is preserved and can be restored using:
```
pydebuggerconfig restore
```
