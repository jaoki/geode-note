### how to execute Locator from command line
java -server -classpath gemfire-assembly/build/install/apache-geode/lib/gemfire-core-dependencies.jar \
com.gemstone.gemfire.distributed.LocatorLauncher \
start Locator1 \
--redirect-output &
# --port=11235 \


### how to execute Server from command line 
java -server -classpath gemfire-assembly/build/install/apache-geode/lib/gemfire-core-dependencies.jar \
-Dgemfire.default.locators=localhost[10334] \
-Dgemfire.use-cluster-configuration=true \
-Dgemfire.launcher.registerSignalHandlers=true \
-Djava.awt.headless=true \
-Dsun.rmi.dgc.server.gcInterval=9223372036854775806 \
com.gemstone.gemfire.distributed.ServerLauncher start server \
--redirect-output \
--server-port=40404 &




### Flink Integration
Flink's DataSet (DataSet<String, String>) to Geode Region???
class GemFireRegionDataSet<K, V> extends DataSet<K, V>

### Actual Execution
ExecutionEnvironment.execute()
