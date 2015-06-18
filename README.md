
### how to execute Server from commandline 
java -server -classpath gemfire-assembly/build/install/apache-geode/lib/gemfire-core-dependencies.jar \
-Dgemfire.default.locators=localhost[10334] \
-Dgemfire.use-cluster-configuration=true \
-Dgemfire.launcher.registerSignalHandlers=true \
-Djava.awt.headless=true \
-Dsun.rmi.dgc.server.gcInterval=9223372036854775806 \
com.gemstone.gemfire.distributed.ServerLauncher start server --redirect-output --server-port=40404 &



