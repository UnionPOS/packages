# Package details
include ../../tasks/Makefile.package
include ../../tasks/Makefile.apk

ifeq ($(OS), darwin)
  OS=osx
  PACKAGE_FILE=$(PACKAGE_NAME)-$(OS)-$(ARCH)
else
  OS=linux64
  PACKAGE_FILE=$(PACKAGE_NAME)-$(OS)
endif

export VENDOR ?= stedolan
export APK_BUILD_TEMPLATE ?= APKBUILD.github-binary
export DOWNLOAD_URL ?= $(PACKAGE_REPO_URL)/releases/download/$(PACKAGE_NAME)-$(PACKAGE_VERSION)/$(PACKAGE_FILE)

install:
	$(call download_binary)

test:
	$(PACKAGE_EXE) --version
