# Target Layers for Arm FVP Models

This directory contains pre-configured target layers for Arm Fixed Virtual Platform simulation models.

## Directory Content

Each directory contains layer description (Target.clayer.yml), RTE configuration for the target device and
configuration parameters for the FVP model. Each layer targets a specific device platform. The below table
contains information about target platforms and how they map to the model executable.

| Directory | Target device             | Target platform                | Model executable               |
|:----------|:--------------------------|:-------------------------------|:-------------------------------|
| CM3       | Cortex-M3                 | Arm MPS2 (no v8M additions)    | FVP_MPS2_Cortex-M3             |

## Target Platform Memory Configuration

### Arm MPS2 (no v8M additions)
Arm MPS2 platform without v8M extensions is used by layers for Cortex-M0, Cortex-M0plus, Cortex-M3, Cortex-M4, and Cortex-M7.

Property   | Value
-----------|-----------
__ROM_BASE | 0x00000000
__ROM_SIZE | 0x00400000
__RAM_BASE | 0x20000000
__RAM_SIZE | 0x00400000
