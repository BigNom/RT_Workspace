## AECOsim build for Client

## Tasks carried out
Created start-up config file.

``
_MS_CONFIGPATH          = C:/Program Files (x86)/Bentley/AECOsimBuildingDesigner V8i Ss6/AECOsimBuildingDesigner/config/

%include ${_MS_CONFIGPATH}/msdir.cfg

_USTN_WORKSPACEROOT 	= N:/14_EngineeringServices/Drafting/Admin/Bentley/ClientBuilds/RT_Workspace/
_USTN_SYSTEMROOT        = $(_USTN_INSTALLED_WORKSPACEROOT)system/
_TF_WORKSPACEROOT       = $(_USTN_INSTALLED_WORKSPACEROOT)/

MSDIR : ${MSDIR_INSTALLED}

_AERISON_WORKSPACEROOT 	= $(_USTN_WORKSPACEROOT)
_AERISON_PROJECTS	    = N:/14_EngineeringServices/Drafting/_Projects/
_USTN_PROJECT		    = $(_AERISON_WORKSPACEROOT)PCF/
_USTN_PROJECTDATA	    = $(_AERISON_PROJECTS)$(_USTN_PROJECTNAME)/

_USTN_USERNAME          = $(USERNAME)

%if $(USERNAME)      == "sbiddle"
_USTN_DISPLAYALLCFGVARS = 1
%else 
_USTN_DISPLAYALLCFGVARS = 0
%endif

%include $(MSDIR)config/msconfig.cfg

``