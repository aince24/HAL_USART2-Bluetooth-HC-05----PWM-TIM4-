################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

BUILD_ARTIFACT_NAME := HAL_USART2(Bluetooth HC-05) -- PWM(TIM4)
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX := 
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME).$(BUILD_ARTIFACT_EXTENSION)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).list \

OBJCOPY_BIN += \
HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).bin \


# All Target
all:
	+@$(MAKE) --no-print-directory main-build && $(MAKE) --no-print-directory post-build

# Main-build Target
main-build: HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).elf secondary-outputs

# Tool invocations
HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).elf: $(OBJS) $(USER_OBJS) ../STM32F407VG_FLASH.ld
	arm-none-eabi-gcc -o "HAL_USART2(Bluetooth HC-05) -- PWM(TIM4).elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"../STM32F407VG_FLASH.ld" --specs=nosys.specs -Wl,-Map="HAL_USART2(Bluetooth HC-05) -- PWM(TIM4).map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "HAL_USART2(Bluetooth HC-05) -- PWM(TIM4).list"
	@echo 'Finished building: $@'
	@echo ' '

HAL_USART2(Bluetooth\ HC-05)\ --\ PWM(TIM4).bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "HAL_USART2(Bluetooth HC-05) -- PWM(TIM4).bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

post-build:
	arm-none-eabi-objcopy.exe -O ihex "HAL_USART2(Bluetooth HC-05) -- PWM(TIM4).elf" "HAL_USART2(Bluetooth HC-05) -- PWM(TIM4).hex"
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents fail-specified-linker-script-missing warn-no-linker-script-specified
.SECONDARY: post-build

-include ../makefile.targets
