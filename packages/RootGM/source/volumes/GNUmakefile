# $Id: GNUmakefile 652 2009-02-12 17:17:06Z ihrivnac $

# -----------------------------------------------------------------------
# The makefile for a sub-package of the Virtual Geometry Model
# Copyright (C) 2007, Ivana Hrivnacova               
# All rights reserved. 
#           
# For the licensing terms see vgm/LICENSE.
# Contact: ivana@ipno.in2p3.fr
# -----------------------------------------------------------------------

# Based on Geant4 makefiles

name := RootGM_volumes

ifndef VGM_INSTALL
  VGM_INSTALL = ../../../..
endif

include $(VGM_INSTALL)/config/architecture.gmk

CPPFLAGS += -I$(VGM_BASE)/VGM/include
CPPFLAGS += -I$(VGM_BASE)/BaseVGM/include
CPPFLAGS += -I$(VGM_BASE)/RootGM/include
INTYLIBS += -lRootGM_common -lRootGM_solids -lRootGM_materials

include $(VGM_INSTALL)/config/root.gmk

include $(VGM_INSTALL)/config/common.gmk

.PHONY: global
 
global: lib

