

objs += \
	  $(ROOT)/cpu/$(CPU)/setup.o \
	  $(ROOT)/cpu/$(CPU)/pwm_led.o \
	  $(ROOT)/cpu/$(CPU)/iic_hw.o \
	  $(ROOT)/cpu/$(CPU)/iic_soft.o \
	  $(ROOT)/cpu/$(CPU)/uart_dev.o \
	  $(ROOT)/cpu/$(CPU)/spi.o \
	  $(ROOT)/cpu/$(CPU)/mcpwm.o \
	  $(ROOT)/cpu/$(CPU)/charge.o \
	  $(ROOT)/cpu/$(CPU)/chargestore.o \
      $(ROOT)/cpu/$(CPU)/ctmu.o \
      $(ROOT)/cpu/$(CPU)/port_wkup.o \
      $(ROOT)/cpu/$(CPU)/adc_api.o \


ifeq ($(APP_CASE),earphone)
objs += \
      $(ROOT)/cpu/$(CPU)/overlay_code.o \
	  $(ROOT)/cpu/$(CPU)/irflt.o \
	  $(ROOT)/cpu/$(CPU)/plcnt.o \

objs += \
	  $(ROOT)/cpu/$(CPU)/uart_test.o \
	  $(ROOT)/cpu/$(CPU)/spi_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_eeprom_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_slave_test.o
else ifeq ($(APP_CASE),soundbox)
objs += \
      $(ROOT)/cpu/$(CPU)/overlay_code.o \
	  $(ROOT)/cpu/$(CPU)/irflt.o \
	  $(ROOT)/cpu/$(CPU)/plcnt.o \
	  $(ROOT)/cpu/$(CPU)/chargebox_hw.o \
	  $(ROOT)/cpu/$(CPU)/app_timer.o \

objs += \
	  $(ROOT)/cpu/$(CPU)/uart_test.o \
	  $(ROOT)/cpu/$(CPU)/uart_bt_product.o \
	  $(ROOT)/cpu/$(CPU)/spi_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_eeprom_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_slave_test.o \
	  $(ROOT)/cpu/$(CPU)/clock_manager.o \

else ifeq ($(APP_CASE),ICrecorder)
objs += \
      $(ROOT)/cpu/$(CPU)/overlay_code.o \
	  $(ROOT)/cpu/$(CPU)/irflt.o \
	  $(ROOT)/cpu/$(CPU)/plcnt.o \
	  $(ROOT)/cpu/$(CPU)/chargebox_hw.o \
	  $(ROOT)/cpu/$(CPU)/app_timer.o \

objs += \
	  $(ROOT)/cpu/$(CPU)/uart_test.o \
	  $(ROOT)/cpu/$(CPU)/uart_bt_product.o \
	  $(ROOT)/cpu/$(CPU)/spi_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_eeprom_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_slave_test.o \
	  $(ROOT)/cpu/$(CPU)/clock_manager.o \



else ifeq ($(APP_CASE),dongle)
objs += \
      $(ROOT)/cpu/$(CPU)/overlay_code.o

ifeq ($(AUDIO_LITE_VERSION),n)
objs += \
        $(ROOT)/cpu/$(CPU)/clock_manager.o
endif


else ifeq ($(APP_CASE),gamebox)
objs += \
	  $(ROOT)/cpu/$(CPU)/clock_manager.o \
      $(ROOT)/cpu/$(CPU)/overlay_code.o \

else ifeq ($(APP_CASE),watch)
objs += \
      $(ROOT)/cpu/$(CPU)/overlay_code.o \
	  $(ROOT)/cpu/$(CPU)/app_timer.o \

objs += \
	  $(ROOT)/cpu/$(CPU)/uart_test.o \
	  $(ROOT)/cpu/$(CPU)/spi_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_eeprom_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_slave_test.o \
	  $(ROOT)/cpu/$(CPU)/clock_manager.o \

else ifeq ($(APP_CASE),adapter)
objs += \
      $(ROOT)/cpu/$(CPU)/overlay_code.o \
	  $(ROOT)/cpu/$(CPU)/irflt.o \
	  $(ROOT)/cpu/$(CPU)/plcnt.o \

objs += \
	  $(ROOT)/cpu/$(CPU)/uart_test.o \
	  $(ROOT)/cpu/$(CPU)/uart_bt_product.o \
	  $(ROOT)/cpu/$(CPU)/spi_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_eeprom_test.o \
	  $(ROOT)/cpu/$(CPU)/iic_slave_test.o \
	  $(ROOT)/cpu/$(CPU)/clock_manager.o \

endif

ifneq ($(APP_CASE),gamebox)
ifneq ($(APP_CASE),hid)
ifneq ($(APP_CASE),spp_and_le)
include $(ROOT)/cpu/$(CPU)/ui_driver/Makefile
include $(ROOT)/cpu/$(CPU)/audio_common/Makefile
include $(ROOT)/cpu/$(CPU)/audio_dec/Makefile
include $(ROOT)/cpu/$(CPU)/audio_enc/Makefile
include $(ROOT)/cpu/$(CPU)/audio_effect/Makefile
include $(ROOT)/cpu/$(CPU)/audio_mic/Makefile
include $(ROOT)/cpu/$(CPU)/localtws/Makefile
endif
endif
endif

ifeq ($(AUDIO_LITE_VERSION),y)
#include $(ROOT)/cpu/$(CPU)/audio_common/Makefile
#include $(ROOT)/cpu/$(CPU)/audio_dec/Makefile
#include $(ROOT)/cpu/$(CPU)/audio_enc/Makefile
objs += \
	  $(ROOT)/cpu/$(CPU)/clock_manager.o \
	  $(ROOT)/cpu/$(CPU)/audio_common/app_audio.o \
	  $(ROOT)/cpu/$(CPU)/audio_dec/audio_dec.o \
	  $(ROOT)/cpu/$(CPU)/audio_dec/tone_player.o \
	  $(ROOT)/cpu/$(CPU)/audio_dec/audio_dec_tone.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_adc_demo.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_mic_codec.o \

endif
