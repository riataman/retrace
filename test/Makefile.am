AM_CFLAGS = $(TESTS_CFLAGS) -I../src/v1 -g

dist_check_SCRIPTS = runtests.sh
noinst_PROGRAMS =
TESTS =

# run comocka tests only on Linux
if CMOCKA
if LINUX
noinst_PROGRAMS += cmockatest
TESTS += cmockatest
cmockatest_CFLAGS = $(CMOCKA_CFLAGS) -I../src/v1
cmockatest_LDADD = $(CMOCKA_LDFLAGS) $(CMOCKA_LIBS)
endif
endif

if ENABLE_TESTS
noinst_PROGRAMS += id env time fork exit malloc str pipe sock sock_srv file trace pledge scanf dlopen dir exec printf popen char mmap sbrk getaddrinfo log memcpy temp config perror setlocale strinject recvmsg writev readv
TESTS += $(dist_check_SCRIPTS)
endif
