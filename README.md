This repository contains useful scripts related to development and Erlang in particular.

eloc
----
Counts the number of executable lines of code (ELOC) in Erlang files. It can be used for other languages as well, but the comment character (`%`) is hard coded for now.

Usage:

    eloc <files>

Example:

    meck$ eloc
    ELOC   comments file
    ----   -------- ----
    301    110	    src/meck.erl
    6      0        test/meck_test_module.erl
    7      0	    test/meck_tests.hrl
    293    24	    test/meck_tests.erl
    9      15	    util/make_doc.erl
    84     16	    util/run_test.erl

    700    165	    total

erlang
------
This script switches a symlinked bin folder based on which Erlang
version you want to run.

Usage:

    erlang <version>

Example:

    $ erlang r14
    Switched to version R14B01
    $ erlang r13
    Switched to version R13B04
    $ erl
    Erlang R13B04 (erts-5.7.5) [source] [64-bit] [smp:2:2] [rq:2] [async-threads:0] [hipe] [kernel-poll:false]

    Eshell V5.7.5  (abort with ^G)
    1>

It requires the environment variable `ERLANG_DIR` to be set. It should
contain folders for each Erlang version (e.g. r13b04, r14b01
etc). Each of those folders should have a 'bin' folder inside. This
bin folder is then symlinked into the `ERLANG_DIR` directory. Add this
bin directory to your path.

The <version> parameter you supply on the command line should be a
prefix (or whole) of any of the directories in the `ERLANG_DIR`. The
newest Erlang version will be used unless specified.
