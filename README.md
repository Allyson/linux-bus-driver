Project description:

|------------|
|            |    Data bus (8 bits)    |--------| Data bus (8 bits) |--------|
|    MIPS    |============//===========|        |========//=========|  DSP   |
| Processor  |        CS_N             | BUFFER |                   |        |
|            |-------------------------|        |                   |        |
|            |       Interrupt         |        |                   |        |
|            |------------------       |        |        -----------|        |
|------------|                 |       |--------|        |          |--------|
                               |                         |
                               |-------------------------|


This project will be a device driver that allow access to MIPS data bus. This device driver must support the interruption, because when the DSP in question needs to send a data to DSP that writes the data on the data bus and triggers the interrupt, it will cause the devide driver to activate the the chip select that buffer release the data to the data bus.


Este projeto deverá ser um device dirver para linux que permita acesso ao barramento de dados do processador MIPS. Este device driver deve dar suporte à interrupção, pois quando o DSP em questão necessita enviar um dado ao MIPS este DSP escreve o dado no barramento de dados e aciona a interrupção, isso fará com que o device driver acione o chip select para que o buffer libere o dado par ao barramento de dados.
