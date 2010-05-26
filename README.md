This repository contains useful scripts related to development and Erlang in particular.

eloc
----
Counts the number of executable lines of code (ELOC) in Erlang files. It can be used for other languages as well, but the comment character (`%`) is hard coded for now.

Usage:

    eloc <files>

Example:

    meck$ eloc
    ELOC	comments file
    ----	-------- ----
    301	110	 src/meck.erl
    6	0	 test/meck_test_module.erl
    7	0	 test/meck_tests.hrl
    293	24	 test/meck_tests.erl
    9	15	 util/make_doc.erl
    84	16	 util/run_test.erl

    700	165	 total
