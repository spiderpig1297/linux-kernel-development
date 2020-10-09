MODULENAME := <module_name>

obj-m += $(MODULENAME).o

ifeq ($(DEBUG), 1)
ccflags-y += -DDEBUG
endif

ccflags-y += -O0 -Wno-declaration-after-statement -Wno-discarded-qualifiers

$(MODULENAME)-y += <file>

KBUILD_CFLAGS := $(filter-out -pg,$(KBUILD_CFLAGS))
KBUILD_CFLAGS := $(filter-out -mfentry,$(KBUILD_CFLAGS))