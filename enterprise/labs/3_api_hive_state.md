curl -X POST -u laertgjoni:cloudera 'http://35.157.161.230:7180/api/v1/clusters/laertgjoni/services/hive/commands/stop'
{
  "id" : 415,
  "name" : "Stop",
  "startTime" : "2017-10-18T12:21:13.442Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
} 



curl -X POST -u laertgjoni:cloudera 'http://35.157.161.230:7180/api/v1/clusters/laertgjoni/services/hive/commands/start'
{
  "id" : 419,
  "name" : "Start",
  "startTime" : "2017-10-18T12:22:03.016Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}


curl -u laertgjoni:cloudera 'http://35.157.161.230:7180/api/v1/clusters/laertgjoni/services/hive/'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-24-175.eu-central-1.compute.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false
} 