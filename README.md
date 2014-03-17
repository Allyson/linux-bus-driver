
Project description:

<pre>

|-----------|
|           | Data bus (8 bits) |--------| Data bus (8 bits) |-----|
|    MIPS   |&#60;==========//=====&#62;|        |&#60;=======//========&#62;|     |
| Processor |        CS_N       |        |                   |     |
|           |------------------&#62;| Buffer |                   | DSP |
|           |       Interrupt   |        |                   |     |
|           |&#60;----------|       |        |        |----------|     |
|-----------|           |       |--------|        |          |-----|
                        |                         |
                        |-------------------------|

Buffer -&#62; Bidirectional Buffer/LATCH 8 bits

</pre>

This project will be a device driver that allow access to MIPS data bus. This device driver must support the interruption, because when the DSP in question needs to send a data to DSP that writes the data on the data bus and triggers the interrupt, it will cause the device driver to activate the the chip select that buffer release the data to the data bus.


Este projeto deverá ser um device dirver para linux que permita acesso ao barramento de dados do processador MIPS. Este device driver deve dar suporte à interrupção, pois quando o DSP em questão necessita enviar um dado ao MIPS este DSP escreve o dado no barramento de dados e aciona a interrupção, isso fará com que o device driver acione o chip select para que o buffer libere o dado par ao barramento de dados.


