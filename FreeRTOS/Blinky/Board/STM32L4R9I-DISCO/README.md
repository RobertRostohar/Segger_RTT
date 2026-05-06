# Board: STMicroelectronics [STM32L4R9I-DISCO](https://www.st.com/en/evaluation-tools/32l4r9idiscovery.html)

## Default Board Layer

Device: **STM32L4R9AII6**

System Core Clock: **120 MHz**

This setup is configured using **STM32CubeMX**, an interactive tool provided by STMicroelectronics for device configuration.
Refer to ["Configure STM32 Devices with CubeMX"](https://github.com/Open-CMSIS-Pack/cmsis-toolbox/blob/main/docs/CubeMX.md) for additional information.

### System Configuration

| System resource       | Setting
|:----------------------|:--------------------------------------
| Heap                  | 64 kB (configured in the STM32CubeMX)
| Stack (MSP)           |  1 kB (configured in the STM32CubeMX)

### STDIO mapping

**STDIO** is routed to Virtual COM port on the ST-LINK (using **USART2** peripheral)

### CMSIS-Driver mapping

| CMSIS-Driver          | Peripheral            | Board connector/component                     | Connection
|:----------------------|:----------------------|:----------------------------------------------|:------------------------------
| Driver_GPIO0          | GPIO                  | Arduino digital I/O pins D2..D10, D14..D19    | ARDUINO_UNO_D2..D10, D14..D19
| Driver_I2C3           | I2C3                  | Arduino I2C pins D20..D21                     | ARDUINO_UNO_I2C
| Driver_MCI1           | SDMMC1                | MicroSD slot (CN6)                            | CMSIS_MCI
| Driver_SPI2           | SPI2                  | Arduino SPI pins D10..D13                     | ARDUINO_UNO_SPI
| Driver_USART2         | USART2                | ST-LINK connector (CN13)                      | STDIN, STDOUT, STDERR
| Driver_USART3         | USART3                | STMOD+ pins PMOD#2..PMOD#3 (CN1)              | CMSIS_USART
| Driver_USART21        | LPUART1               | Arduino UART pins D0..D1                      | ARDUINO_UNO_UART
| Driver_USBD0          | USB_OTG_FS            | User USB connector (CN9)                      | CMSIS_USB_Device
| CMSIS-Driver VIO      | GPIO                  | LEDs (LD2) and Joystick select (B2)           | CMSIS_VIO

Reference to [Arduino UNO connector description](https://github.com/Open-CMSIS-Pack/cmsis-toolbox/blob/main/docs/ReferenceApplications.md#arduino-shield).

### CMSIS-Driver Virtual I/O mapping

| CMSIS-Driver VIO      | Board component
|:----------------------|:--------------------------------------
| vioBUTTON0            | Joystick select (B2)
| vioLED0               | LED green       (LD2)
