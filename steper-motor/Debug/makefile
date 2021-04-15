################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: steper-motor.axf

# Tool invocations
steper-motor.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"S:\UNLaM\Tecnicas Digitales II\step-motor-workspace\lpc_board_nxp_lpcxpresso_1769\Debug" -L"S:\UNLaM\Tecnicas Digitales II\step-motor-workspace\lpc_chip_175x_6x\Debug" -Xlinker -Map="steper-motor.map" -Xlinker --cref -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "steper-motor_Debug.ld" -o "steper-motor.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) steper-motor.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "steper-motor.axf"; # arm-none-eabi-objcopy -v -O binary "steper-motor.axf" "steper-motor.bin" ; # checksum -p LPC1769 -d "steper-motor.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
