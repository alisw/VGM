# $Id: GNUmakefile 674 2010-12-21 16:20:43Z ihrivnac $

# -----------------------------------------------------------------------
# The makefile for the Virtual Geometry Model test
# Copyright (C) 2007, Ivana Hrivnacova               
# All rights reserved. 
#           
# For the licensing terms see vgm/LICENSE.
# Contact: ivana@ipno.in2p3.fr
# -----------------------------------------------------------------------

# --------------------------------------------------------------
# Based on Geant4 makefiles
# GNUmakefile for examples module.  Gabriele Cosmo, 06/04/98.
# --------------------------------------------------------------

name := vgm_test
G4TARGET := $(name)
G4EXLIB := true

ifndef G4INSTALL
  G4INSTALL = ../../..
endif

.PHONY: all
all: lib bin

CPPFLAGS += -I$(shell root-config --incdir) 
EXTRALIBS = $(shell root-config --glibs) -lGeomPainter -lGeom
ifndef VGM_NO_G4ROOT
  CPPFLAGS += -DVGM_WITH_G4ROOT
endif

#G4ROOT
CPPFLAGS += -I${G4VMC}/include/g4root
EXTRALIBS += -L${G4VMC}/lib/tgt_linuxx8664gcc -lg4root

CPPFLAGS  += -I$(VGM_INSTALL)/packages/VGM/include
CPPFLAGS  += -I$(VGM_INSTALL)/packages/ClhepVGM/include
CPPFLAGS  += -I$(VGM_INSTALL)/packages/BaseVGM/include
CPPFLAGS  += -I$(VGM_INSTALL)/packages/Geant4GM/include
CPPFLAGS  += -I$(VGM_INSTALL)/packages/RootGM/include
CPPFLAGS  += -I$(VGM_INSTALL)/packages/XmlVGM/include
EXTRALIBS += -L$(VGM_INSTALL)/lib/$(VGM_SYSTEM)
EXTRALIBS += -lGeant4GM -lRootGM  -lBaseVGM -lClhepVGM -lXmlVGM

include $(G4INSTALL)/config/binmake.gmk

visclean:
	rm -f g4*.prim g4*.eps g4*.wrl
	rm -f .DAWN_*

