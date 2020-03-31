# stm32f3-basics

| Acronym |                                      |
|---------|--------------------------------------|
| EXTI    | EXTernal Interrupt                   |  
| NVIC    | Nested Vectored Interrupt Controller |

## Enable Interrupt for a Pin
1. [MX] Pinout view => set desired pin to mode EXTIx.
2. [MX] System Core => NVIC => enable EXTI line x interrupt
3. Create function

	HAL_GPIO_EXTI_Callback(uint16_t GPIO_Pin) { ... }
	
	It will be called each time a interrupt occurs, parameter GPIO_Pin is the pin that generated the interrupt
