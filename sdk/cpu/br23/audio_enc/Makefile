


objs += \

ifeq ($(APP_CASE),earphone)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_file.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_recoder.o \

else ifeq ($(APP_CASE),soundbox)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_file.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_recoder.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_sbc_codec.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_mic_codec.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_adc_demo.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_recorder_mix.o \

else ifeq ($(APP_CASE),dongle)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_recoder.o

ifeq ($(AUDIO_LITE_VERSION),n)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc.o
endif

else ifeq ($(APP_CASE),gamebox)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_recoder.o \

else ifeq ($(APP_CASE),watch)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_file.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_recoder.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_sbc_codec.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_mic_codec.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_adc_demo.o \

else ifeq ($(APP_CASE),ICrecorder)
objs += \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_file.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_enc_recoder.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_sbc_codec.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_mic_codec.o \
	  $(ROOT)/cpu/$(CPU)/audio_enc/audio_adc_demo.o \


endif
