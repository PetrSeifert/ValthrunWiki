---
title: Kernel Driver
---

# Valthrun Kernel Driver
## Loading the Valthrun Kernel Driver

Loading or mapping a driver, like the Valthrun Kernel Driver, is a complex process often hindered by strict security requirements. Typically, drivers are signed using an Extended Validation (EV) Code Signing Certificate. However, obtaining these certificates is challenging, and they are susceptible to blocking by third-party software, such as Valve Anti-Cheat (VAC). Due to these limitations, loading the Valthrun Kernel Driver requires unconventional methods. An overview and detailed descriptions of these methods are available in the [next section](#methods).

## Overview of Mapping Methods {#methods}
Here is a quick overview of various methods for loading the Valthrun Kernel Driver:

| Method | Complexity | Success Rate |
| --- | --- | --- |
| [Valthrun EFI loader](./efi-bootloader) | Medium | High |
| [Manual Mapping via KD-Mapper](./kdmapper) | Medium | Medium |
| [Manual Mapping via KDU](:/kdu)* | Medium | Medium |
| [Using Windows Test-Signing](./test-signing) | Low | Very High |

\* The wiki entry for this method has not yet been completed

Each method for loading the Valthrun Kernel Driver varies in complexity and success rate, and the optimal choice depends on specific requirements and system compatibility. Some methods may be more stable on certain configurations, while others offer increased reliability under restrictive conditions. For a deeper understanding and step-by-step guidance, consult the linked resources on each mapping method.

## Supported Windows Versions  
The Valthrun Kernel Driver is designed for compatibility across a broad spectrum of Windows versions, with support for recent versions ensured by dynamically resolving function calls and structure offsets. Testing confirms stability on the latest Windows 10 and Windows 11 versions, including 22H2, and user feedback suggests functionality on versions as far back as 20H2. Should you experience any issues, please submit an issue report with your Windows version and error description on the official [GitHub repository](https://github.com/Valthrun/valthrun).