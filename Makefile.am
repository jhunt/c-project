AUTOMAKE_OPTIONS = foreign subdir-objects
ACLOCAL_AMFLAGS  = -I build

############################################################

AM_CFLAGS = @GCOV_CFLAGS@

############################################################

TESTS          = $(CTAP_TESTS) t/memcheck
BUILT_TESTS    = $(CTAP_TESTS)
check_PROGRAMS = $(CTAP_TESTS)

EXTRA_DIST  = README COPYING
EXTRA_DIST += bootstrap
EXTRA_DIST += t/run

############################################################



############################################################

.PHONY: coverage
if GCOV_ENABLED
coverage-clean:
	@lcov --directory . --zerocounters
coverage-report:
	@mkdir -p coverage
	@lcov --compat-libtool --directory . --base-directory . --capture --output-file coverage/app.info
	@genhtml -o coverage/ coverage/app.info
coverage:
	@make coverage-report
clean-local-cov:
	@make coverage-clean
check:
	@make coverage
else
coverage:
	@echo >&2 "code coverage not available.  try running \`./configure --enable-coverage\`"
clean-local-cov:
endif
