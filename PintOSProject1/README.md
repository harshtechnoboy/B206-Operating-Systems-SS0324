Running a single PintOS test:

Open a terminal and navigate to a project folder i.e., $PINTOS_HOME/pintos/src/threads.

Build the threads project using make

make
Building the project will generate a new folder called build.

Tests for each project are locate in the folder $PINTOS_HOME/pintos/src/tests/. 

Each project has a sub-folder that contains all its tests, for example, $PINTOS_HOME/pintos/src/tests/threads contains all the tests for the threads project (or project 1 for our class). 

After building a project, all of its tests are copied over into the build folder.

Using your terminal, navigate to the threads build folder and run the following command

make tests/threads/alarm-single.result

The command will run the tests alarm-single and will generate the following files

$PINTOS_HOME/pintos/src/threads/build/tests/threads/alarm-single.output contains anything that the test outputs during its run

$PINTOS_HOME/pintos/src/threads/build/tests/threads/alarm-single.errors contains any errors that occurred during the tests' run

$PINTOS_HOME/pintos/src/threads/build/tests/threads/alarm-single.result contains the test’s result, typically the word FAIL or PASS

If you would like to run the tests and see the output on your terminal, as well as store it in the .output file run your tests by passing VERBOSE=1, e.g.

make VERBOSE=1 tests/threads/alarm-single.result