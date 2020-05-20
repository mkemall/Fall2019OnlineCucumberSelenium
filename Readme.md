To run tests over the jenkins , specify following maven top level targer as build part :
than type clean test -Dcucumber.options="--tags @driver" or other tag as well

you can specify any tags that are available in your project

To run smoke test use : 
clean test -P Smoke


To start regression execute : 

clean test -P Regression

To run feature files in parallel without limiting number of threads:
<parallel>methods</parallel>
<useUnlimitedThreads>true</useUnlimitedThread>
    <includes>
    <!-- for run class or classes-->
    <include>**/RegressionRunner.java</include>
    </includes>
           