include config/lang.am

EXTRA_DIST = \
	sipxpbx \
	stdprompts \
	sipxecs-lang-@LANG_ID@.spec

prompts_SOURCE = $(shell find $(srcdir)/stdprompts -name '*.wav' -type f -printf '%P\n')
conf_DATA = sipxecs-lang-@LANG_ID@.jar

install-data-hook :
	echo "$$Installer" | \
	  InstallFileList="$(prompts_SOURCE)" \
	  InstallSourceDir=$(srcdir)/stdprompts \
	  InstallDestDir=$(DESTDIR)$(promptsdir) \
	  bash
