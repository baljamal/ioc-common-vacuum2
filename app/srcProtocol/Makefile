# Makefile for copying streamDevice protocol files during build.
# Author: Jason Tiller

T_A=$(EPICS_HOST_ARCH)
TOP=../..
include $(TOP)/configure/CONFIG

######################################################################
# Specify what files should be copied and where.

# What protocol files should be copied as part of the build.
# Enable this line to install thermotek.proto to $(TOP)/protocol
# However, this is not necessary as long as your st.cmd sets
# the env var STREAM_PROTOCOL_PATH to $(TOP)/app/srcProtocol
COPY_FILES += $(QPC)/app/srcProtocol/qpc.proto
COPY_FILES += mks937a.proto
COPY_FILES += mks937a_v2.proto
COPY_FILES += mks937b.proto.db
COPY_FILES += agilent.proto
COPY_FILES += srg3.proto

# What subdirectory should hold the protcol files.  For this example,
# $INSTALL_LOCATION/protocol will be created.
COPY_SUBDIR = protocol

# Uncomment this if you only want to copy when *not* installing to
# your development area.  Useful for iocBoot, where the source and
# target directories are actually the same.
# COPY_ONLY_IF_NON_LOCAL=1

######################################################################
# Don't change these.
include $(TOP)/configure/RULES
-include $(TOP)/configure/RULES.copy

######################################################################
# Add additional RULES files, if necessary.
