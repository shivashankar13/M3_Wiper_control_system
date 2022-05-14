# INTRODUCTION
Wiper is an essential component that is used to wipe raindrops or any water from the windscreen. Wipers are designed and made to clear the water from a windscreen. Most cars have two wipers on the windscreen, one on the rear window and the other on each headlight. The wiper parts visible from outside the car are the rubber blade, the wiper arm holding the blade, a spring linkage, and parts of the wiper pivots. The wiper itself has about six parts called pressure points or claws that are small arms under the wiper

The existing system uses a control stalk to activate the wiper and the process of pulling up the wiper is difficult.r needs to switch on and off the control stalk and it will reduce the driver’s concentration during the driving. Thus, this system is proposed to solve all these problems. The concept of this wiper system is similar to other conventional wipers, yet this system will be upgraded to an automatic control system by using a controller.When water hits a dedicated sensor located on the windscreen, it triggers the wiper motor to move. is not detected by sensor, the wiper will automatically stop. This will help the driver to give more concentration and reduce the car accident probability.

In this project, there were two innovations reviewed as the literature review. The two were designed with different concepts and operating mechanism however with same objective of working principle of the car wiper. The rain sensor was a highly versatile device for automatic wiping of vehicle windscreen when it is wet due to moisture, raindrops or even mud. It worked by reflecting harmonious light beams within the windscreen. When raindrops fall onto the windscreen, this harmony light is disturbed and creating a drop in the light beam intensity. The system then activated the wipers to be operated in full automatic mode. It has a response time of 0.1 seconds. It allowed for a quick reaction when it is a sudden splashes of water that will make the driver totally ‘blinds’ when the situation happened. With the automatic wiper, the driver can avert the risk of an accident. The automatic wiper is important during heavy traffic, e.g. in town, city, school zone and other public places. A driver may be subjected to many distractions with bad weather, dangerous road conditions and fatigue. The Rain Sensor reduced the driver’s burden by making driving more comfortable. Trailing a wet car is no longer a nuisance as detection of even 0.005 milliliters of water is possible.

# COMPONENTS AND SUPPLIES:
1. STM32F407 Discovery Board
2. Push Button
3. LEDs
4. Resistors
5. Power Supply

# ADVANTAGES:
* To save money during wet seasons, turn off the irrigation system. Electricity bills are lowered as a consequence.
* Rain sensors store water during rain events, allowing it to be available throughout the summer and winter.
* As a consequence, rain sensor-based equipment like vehicle wipers and irrigation systems last longer since they only work when needed.
* It is quite simple to use.
* As a consequence, less energy is consumed.
* Rain sensor-based systems are extremely simple to install.
* Individual rain sensors are fairly inexpensive.

# Disadvantages:
* When water falls squarely on the rain sensor, the mechanism activates.
* The entire system cost rises when more components, including a rain sensor, are required.
* Rain sensors must make a decision within a few minutes to avoid erroneous detection of rain. 

# 4W & H (WHO,WHAT,WHEN,WHERE,HOW)
# WHAT
The operational speed of a vehicle wiper is controlled by a wiper speed control mechanism based on rain conditions. To generate, the control system incorporates a rain sensor (30) that detects rain conditions. The amplitude of an analogue signal depends on the detected rain conditions.
# WHY
* To keep the windscreen clean enough to give adequate view at all times.
# WHEN
* The windshield wipers remove rain and snow from the windshield, while the headlights improve visibility at night.
# WHO
* A wiper speed control system for an automobile manages the wiper's functioning speed in response to weather conditions.
# HOW
* You can adjust the speed of the car wiper system according to the rainfall
# WHERE
* In general, car wipers are controlled by the stalk on the right side of the steering wheel.
# HIGH LEVEL REQUIREMENTS
| ID | Description | Status |
| ---|:------------|:-------|
| HL1 | car wiper using STM32F407VG | Implemented |
| HL2 | Led glowing in sequence| Implemented |
| HL3 | Car on and off | Implemented |
# LOW LEVEL REQUIREMENTS
| ID | Description | Status |
| ---|:------------|:-------|
| HL1-LL1 | Push Button | Implemented | 
| HL2-LL2 | Red,Green,Blue Leds | Implemented |
## SWOT ANALYSIS
# STRENGTH
* Low Budget
* Good Reputation
* High Bargaining Power Supliers
* Big Influence on the Market
# WEAKNESS
* Structural Inertia
* High Transaction Cost
* No Focus on Private Sector
* Week Focus on Process Innovations
# OPPRONUTIES
* Emerging New Markets 
* Technological Development
* Demand for Saver Equipments
* Technological Lock in of Product
# THREATS
* Low Bargaining Power Buyers
* Highly REgulated Industry
* Ethical Pressure
* Econimical Crisis
# Exploring STM32F407 Discovery Board
 ![STM32F407 BOARD ](https://user-images.githubusercontent.com/101395036/167911226-a6e681ca-9aaf-40b8-9f76-92a28865968b.png)
 
 This project gives almost all the basic information needed to get started with STM32F407 Discovery Board and also development of driver code.

* Hardware Used : STM32F4 DISCOVERY kit, for more information visit: STM32F4 DISCOVERY
* Software Tool : STM32cubeIDE, for more information visit: STM32CubeIDE
* For installation of STM32CubeIDE refer Youtube
* Note : As this microcontroller has many advanced features and the main aim of this project is to get all basic insights, during the driver development only the required functionalities are added and other advanced functionality is not added. I may update the driver and other functionality in the future.

Please find the STM32F4 Discovery User Manual,STM32F4xxx Reference Manual (RM0090) and other related documents inside a folder called Documents. I will be referring to these documents for information such as block diagrams, register details ect.
# Overview of STM32F407VGT6 Microcontroller
![Overview of STM32F407VGT6 Microcontroller](https://user-images.githubusercontent.com/101395036/167913344-4b240f0f-2b6d-4031-bf15-5ce021f42794.png)

The STM32F407 Discovery board uses STM32F407VGT6 Microcontroller which has ARM Cortex-M4F Processor, which is capable of running upto 168Mhz. This MCU has many peripherals such as GPIO ports, TIMERS, ADCs, DACs, Flash Memory, SRAM, SPI, UART ect. The processor and peripherals talk via BUS-Interface. There are three busses available

I-BUS (Instruction Bus)
D-BUS (Data Bus)
S-BUS (System Bus)
I-BUS This bus connects the Instruction bus of the Cortex®-M4 with FPU(Floating point unit) core to the BusMatrix. This bus is used by the core to fetch instructions. The target of this bus is a memory containing code (internal Flash memory/SRAM or external memories through the FSMC/FMC).

D-BUS This bus connects the databus of the Cortex®-M4 with FPU to the 64-Kbyte CCM data RAM to the BusMatrix. This bus is used by the core for literal load and debug access. The target of this bus is a memory containing code or data (internal Flash memory or external memories through the FSMC/FMC).

S-BUS This bus connects the system bus of the Cortex®-M4 with FPU core to a BusMatrix. This bus is used to access data located in a peripheral or in SRAM. Instructions may also be fetched on this bus (less efficient than ICode). The targets of this bus are the internal SRAM1, SRAM2 and SRAM3, the AHB1 peripherals including the APB peripherals, the AHB2 peripherals and the external memories through the FSMC/FMC.

So instructions and data use I-bus and D-bus respectively, All the other peripheral uses System bus. The Cortex-M4 processor contains three external Advanced High-performance Bus (AHB)-Lite bus interface and one Advanced Peripheral Bus (APB) interface. The GPIOs are connected to AHB1 bus which has a maximum speed of 150Mhz and is divided into two buses as APB1 and APB2. APB1 runs at 42Mhz(max) and APB2 runs at 82Mhz(max). The different peripherals such as SPI, UART, TIMERs, ADCs, DACs, etc are connected to either APB1/APB2 buses. And the AHB2(168Mhz max) is connected to Camera and USB OTG interfaces, AHB3 is connected to External memory controller.
# OUTPUT IMAGES
1. user button and hold it for two seconds
![ENGINE ON STATE](https://user-images.githubusercontent.com/101312396/168205845-9855cb85-3c2a-49ee-9e32-86cdc944a7c0.png)
2. WIPER SPEED LOW
![LOW](https://user-images.githubusercontent.com/101312396/168206233-b2fbccf2-1df2-4b97-9127-4e99626506cd.png)
3. WIPER SPEED MEDIUM

![G](https://user-images.githubusercontent.com/101312396/168206571-cfa61e88-18c1-4db7-a97f-23284b343cbe.png)

4. WIPER SPEED IS HIGH

![orange led on](https://user-images.githubusercontent.com/101312396/168262791-82c3814b-e03f-4937-8689-a085f7b701fe.png)


5. user button is pressed and held for 2 seconds, the red LED is off
![OFF](https://user-images.githubusercontent.com/101312396/168207080-f499c980-b029-48a1-becf-b28a336b77ce.png)
6. WIPER_SYSTEM 1

![wiper_system_1](https://user-images.githubusercontent.com/101312396/168263591-60d2e35f-b2f0-42ff-b817-deaf276ef828.png)
