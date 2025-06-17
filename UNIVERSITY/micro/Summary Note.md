
# connections

there are two type of connections: 
- `Serial` 
- `Parallel`
### serial connection 
 - **UART** (Universal Asynchronous Receiver-Transmitter)
 - **USART** (Universal Synchronous Asynchronous Receiver-Transmitter) 
 - **RS-232** (Serial port)
 - **USB** (Universal Serial Bus)
 - **SPI** (Serial peripheral Bus)

### parallel
- Parallel ATA (PATA) – old hard drive interface.
- Data buses inside CPUs and RAM.


# Architecture 

### Bus
-  **Harvard**:
	- **Separate memory** for **instructions** and **data**.
    - **Separate buses** for instruction fetch and data access.
- **Von Neumann**: 
- **Shared Memory**: One memory space for both **data** and **instructions**.
- **Single Bus**: Instructions and data travel along the **same bus**.
### Core 

- **CISC:** Complex Instruction Set Computer (80 instructions)
- **RISC:** Reduced Instruction Set Computer (30 instructions)
	-  made by **IBM**
	- introduced on **1974**

The difference between **RISC** and **CISC** lies in how they handle:
- **Data referencing (memory access)**
- **Precision and protection mechanisms**
- **Access types and instruction sets**


# History

- **MCU** (microcontroller)
- **MPU** (microprocessor) 

First made **MCU** was on **1971** by an engineer from **Texas Instruments** named **Gray Boone**.
**TMS1802NC**: 
- 128 bit **RAM**
- 3000 bit **ROM**
- used from **1972** to **1974** on **TI**

**TMS1000:**
- made on **1974**
- sold 100m up to **1983**
- 4-bit

on **1973** intel start making **MCUs** alongside with its **MPUs**
**0848:**
- from **MCS-48** series
- made on **1976**
- first intel MCU
**0851**:
- made on **1980**
- had programmable **IC**
- **MPU** + **RAM** + **I/O pins** + **MEM**
- **Harvard** architecture
	- 16-bit data BUS
	- 8-bit address BUS
- was used in:
	- Embedded Systems
	- Aviation
	- Spaceship technology
	- transportation management system
	- Robotics
	- Communication system
	- Cars

## **AVR**
**AVR**: Advanced Virtual RISC or Alf and Vegard’s RISC processor
- made by **Atmel** 
 - made on **1996**
 - **8-bit**
 - creators:
	 - [**Alf-Egil Bogen**](https://no.wikipedia.org/wiki/Alf-Egil_Bogen)
	 - [Vegard Wollan](https://no.wikipedia.org/wiki/Vegard_Wollan)
	
- **AT90S8515:**
	- first AVR based MCU
- **AT90S1200:**
	- made  on **1997**

**types:**
1. ***Tiny AVR***
	- simple processing power
2. ***Mega AVR***
	- medium processing power
3. ***Xmega AVR***
	- commercial use 
	- high computing power

### **ATMEGA32**

- **8-bit**
- Atmel® AVR®
	- high computing power
	- low power consumption (2.7-5.5)
- Advanced RISC Architecture 
	- Not to be confused with Advanced RISC Machine (ARM).
	- 32X8-bit general-purpose register
	- 16MHZ
	- 32kB FLASH
	- 1KB EEPROM
	- 2KB internal SRAM
- R/W cycle:
	- 10,000 for FLASH
	- 100,000  for EEPROM
- Data retention:
	- 20 years at 85°C
	- 100 years at 25°C
- Programming lock for software security
- **JTAG** (IEEE std. 1149.1 Compliant) interface for programming of
	-  Flash Memory
	- EEPROM
	- Fuses
	- Lock Bits
- supports Atmel QTouch® library
- **User Input Devices**:
	- Capacitive touch keys/buttons
	- Rotary encoders
	- Scroll wheels
- Up to 64 sensor channels
- Two 8-bit timers with separate prescaler, separate comparison modes, and capture modes [^8bit]
- One 16-bit timer with separate prescaler, comparison mode, and capture mode [^16bit]
- 4 PWM channels (output) 
- 8-channel ADC (8 analog inputs, multiplexed to a single ADC) 
- Programmable USART serial 
- MASTER/SLAVE SPI serial
- Programmable Watchdog timer with separate oscillator on the chip [^watchdog]
-  On-chip analog comparator [^comparator]:
- On-chip calibrated RC oscillator [^rcosc]:
- **6 sleep mode:**[^sleepmodes]
	- Idle Mode
	- ADC Noise Reduction Mode
	- Power-down Mode
	- Power-save Mode
	- Standby Mode
	- Extended Standby Mode
- internal **calibrated RC oscillator** with fixed internal clock
	- 1.0 MHz
	- 1.6 MHz
	- 2.1 MHz
	- 6.0 MHz
	- 8.1 MHz 


## **PIC MCUs**

- **Programmable Interface Controller** (PIC)
- Made by [Microchip Technology ](https://en.wikipedia.org/wiki/Microchip_Technology)
- Operating speed is **1/4** of the external frequency
	- e.g. if the frequency is 16 MHz, the PIC works at 4 MHz 
- **Low noise** (because it uses one-fourth of external frequency)
- Low power consumption
- Programming languages
	- **C/C++**
	- **asm**
- execute each instruction in few clock cycles
	- **efficient** to program
	- **fast** to learn


## **ARM**

- **Advanced RISC Machine** 
- made by [Advanced RISC Machines Ltd](https://en.wikipedia.org/wiki/Arm_Holdings) on 1990
- co-founders
	- [Acorn Computers](https://en.wikipedia.org/wiki/Acorn_Computers)
	- [Apple Computers](https://en.wikipedia.org/wiki/Apple_Inc.)
	- [VLSI Technology](https://en.wikipedia.org/wiki/VLSI_Technology)
- **VLSI (Very-large-scale integration):** 
	- refers to the integration of a large number of transistors on a single chip.
- **Apple Newton** computer was released in **1993** based on the ARM architecture
- The turning point for ARM was in **1993**, with the help of **Texas Instruments (TI)**.
	- With support from **Texas Instruments (TI)**
	- **TI recommended ARM** for use in **GSM mobile phone systems**
	- **Nokia** initially rejected ARM due to memory concerns
	- ARM responded with a **16-bit architecture** that reduced memory requirements
	- **TI licensed** the design and sold it to Nokia
- **First ARM-based GSM phone:**  
  - **Nokia 6110**, which was highly successful
- **ARM7 Architecture:**
  - Became the standard for mobile CPUs
  - Adopted by **165+ companies**
  - Over **10 billion ARM chips** produced by **1994**
- **Later ARM Families:**
  - **ARM9, ARM9E, ARM10, ARM11**
    - Improved processing performance
    - Reduced energy consumption
- **Cortex Family (introduced later):**
  - **Cortex-A:** High-performance (mobile & application processors)
  - **Cortex-R:** Real-time performance (automotive, robotics)
  - **Cortex-M:** Low-power microcontrollers (embedded systems)
- **big.LITTLE Architecture (2011):**
  - Combines a high-performance core (**big**) and a low-power core (**LITTLE**)
  - Dynamically switches based on processing needs


## **STM Series**

### **STM32H5**

- **32-bit** Arm Cortex-M33 core
- Up to **800 MHz** (highest in STM32)
- **Up to 2MB Flash**, **118KB SRAM**
- Zero-wait-state flash with integrated maintenance logic
- Operates in extended temp range: **-40°C to +125°C**
- Designed for:
    - Real-time edge computing
    - IoT and cybersecurity-critical devices
- Offered in packages from QFN32 to LQFP176

### **STM32F4**

- **32-bit** Arm Cortex-M4F core
- Up to **408 MHz** 
- Includes:
    - **DSP instructions**
    - **FPU** (Floating Point Unit)
    - **11KB CCM RAM** (zero-wait)
- Up to **1MB Flash**, **192KB SRAM**
- Up to **1000 DMIPS**
- Suitable for performance-oriented embedded systems

### **STM32F2**

- **32-bit** Arm Cortex-M3 core
- Max frequency: **120 MHz**
- Mid-range STM32 line
- Up to **1MB Flash**, **128KB SRAM**
- Includes battery-backed memory
- Unique hardware features (e.g., device ID)
- Real-time ready with low power balance

### **STM32F7**

- **32-bit** Arm Cortex-M7F core
- Up to **216 MHz**
- Upgrade over STM32F4
- Richer peripherals and interfaces
- Target: high-performance embedded applications

### **STM32H7**

- **32-bit** Arm Cortex-M7 core
- Built on **40nm** process
- Up to **480 MHz**
- Up to **4809 DMIPS**, **1880 CoreMark**
- First STM32 to break nanometer node barrier
- High-end real-time, control, and compute-heavy applications


# General information

[^8bit]:
	- **Two 8-bit timers (Timer0 & Timer2):**
	    - Each counts from 0 to 255 (8 bits).
	    - **Prescaler:** Allows running at different speeds by dividing the system clock.
	    - **Comparison modes:** Compare the timer’s value to a set number and trigger actions (e.g., PWM, events).
	    - **Capture modes:** Store timer value when an external event occurs (e.g., a pin goes high); useful for timing pulses.

[^16bit]:
	- **One 16-bit timer (Timer1):**
	    - Counts from 0 to 65,535 (16 bits) for longer/more precise timing.
	    - **Prescaler:** Set its own counting speed.
	    - **Comparison mode:** Compare current value with a set number to trigger actions.
	    - **Capture mode:** Store value on external event for accurate timing.
    - 
[^watchdog]:
	- **Programmable Watchdog Timer:**
	  - Resets the microcontroller if the program stops responding.
	  - Uses a dedicated on-chip oscillator, working independently from the main clock.

[^comparator]:
	- **Analog Comparator:**
	  - Compares two analog voltages and outputs which is higher.
	  - Useful for threshold detection or simple signal monitoring without using the ADC.

[^rcosc]:
	- **Calibrated RC Oscillator:**
	  - Internal clock source, factory-calibrated for accuracy.
	  - Provides a **stable system clock**, often removing the need for an external crystal.
	  

[^sleepmodes]:
	- **Idle Mode:** Stops the CPU; peripherals (timers, USART, SPI, ADC, etc.) keep running.  
	  *Use:* Low power, peripherals still needed.
	- **ADC Noise Reduction Mode:** Stops CPU & I/O except ADC and async timer.  
	  *Use:* Accurate ADC readings with less electrical noise.
	- **Power-down Mode:** Shuts down most functions; only external interrupts, watchdog, or reset wake it up.  
	  *Use:* Deep sleep, maximum battery saving.
	- **Power-save Mode:** Like Power-down, but async timer can run.  
	  *Use:* Low power, keep timer for clocks/timed wake-up.
	- **Standby Mode:** Like Power-down, but main oscillator stays on for faster wake-up.  
	  *Use:* Fast startup from sleep, still saves power.
	- **Extended Standby Mode:** Like Standby, but async timer also runs.  
	  *Use:* Ultra-low power, fast wake-up, timer running.


