1)sudo -u hdfs hdfs dfs -mkdir /user/source_laertgjoni

2)sudo -u hdfs hdfs dfs -mkdir /user/target_Maurizio845

3)cd /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/

sudo -u hdfs hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.8.3.jar teragen 5000000 /user/source_laertgjoni

17/10/17 10:00:59 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-16-61.eu-central-1.compute.internal/172.31.16.61:8032
17/10/17 10:01:00 INFO terasort.TeraSort: Generating 5000000 using 2
17/10/17 10:01:00 INFO mapreduce.JobSubmitter: number of splits:2
17/10/17 10:01:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508232743010_0001
17/10/17 10:01:01 INFO impl.YarnClientImpl: Submitted application application_1508232743010_0001
17/10/17 10:01:01 INFO mapreduce.Job: The url to track the job: http://ip-172-31-16-61.eu-central-1.compute.internal:8088/proxy/application_1508232743010_0001/
17/10/17 10:01:01 INFO mapreduce.Job: Running job: job_1508232743010_0001
17/10/17 10:01:08 INFO mapreduce.Job: Job job_1508232743010_0001 running in uber mode : false
17/10/17 10:01:08 INFO mapreduce.Job:  map 0% reduce 0%
17/10/17 10:01:18 INFO mapreduce.Job:  map 50% reduce 0%
17/10/17 10:01:19 INFO mapreduce.Job:  map 100% reduce 0%
17/10/17 10:01:19 INFO mapreduce.Job: Job job_1508232743010_0001 completed successfully
17/10/17 10:01:19 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=244254
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=167
                HDFS: Number of bytes written=500000000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=15798
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=15798
                Total vcore-seconds taken by all map tasks=15798
                Total megabyte-seconds taken by all map tasks=16177152
        Map-Reduce Framework
                Map input records=5000000
                Map output records=5000000
                Input split bytes=167
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=181
                CPU time spent (ms)=13730
                Physical memory (bytes) snapshot=751423488
                Virtual memory (bytes) snapshot=3146444800
                Total committed heap usage (bytes)=852492288
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=10735710707299981
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=500000000


4)sudo -u hdfs hadoop distcp hdfs://ip-172-31-26-116.eu-central-1.compute.internal:8020/tmp/source_Maurizio845/* hdfs://ip-172-31-16-61.eu-central-1.compute.internal:8020/user/target_Maurizio845/


17/10/17 11:42:17 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[hdfs://ip-172-31-26-116.eu-central-1.compute.internal:8020/tmp/source_Maurizio845/*], targetPath=hdfs://ip-172-31-16-61.eu-central-1.compute.internal:8020/user/target_Maurizio845, targetPathExists=true, filtersFile='null'}
17/10/17 11:42:17 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-16-61.eu-central-1.compute.internal/172.31.16.61:8032
17/10/17 11:42:18 INFO tools.SimpleCopyListing: Paths (files+dirs) cnt = 3; dirCnt = 0
17/10/17 11:42:18 INFO tools.SimpleCopyListing: Build file listing completed.
17/10/17 11:42:18 INFO Configuration.deprecation: io.sort.mb is deprecated. Instead, use mapreduce.task.io.sort.mb
17/10/17 11:42:18 INFO Configuration.deprecation: io.sort.factor is deprecated. Instead, use mapreduce.task.io.sort.factor
17/10/17 11:42:18 INFO tools.DistCp: Number of paths in the copy list: 3
17/10/17 11:42:18 INFO tools.DistCp: Number of paths in the copy list: 3
17/10/17 11:42:18 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-16-61.eu-central-1.compute.internal/172.31.16.61:8032
17/10/17 11:42:18 INFO mapreduce.JobSubmitter: number of splits:3
17/10/17 11:42:19 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508232743010_0003
17/10/17 11:42:19 INFO impl.YarnClientImpl: Submitted application application_1508232743010_0003
17/10/17 11:42:19 INFO mapreduce.Job: The url to track the job: http://ip-172-31-16-61.eu-central-1.compute.internal:8088/proxy/application_1508232743010_0003/
17/10/17 11:42:19 INFO tools.DistCp: DistCp job-id: job_1508232743010_0003
17/10/17 11:42:19 INFO mapreduce.Job: Running job: job_1508232743010_0003
17/10/17 11:42:24 INFO mapreduce.Job: Job job_1508232743010_0003 running in uber mode : false
17/10/17 11:42:24 INFO mapreduce.Job:  map 0% reduce 0%
17/10/17 11:42:30 INFO mapreduce.Job:  map 33% reduce 0%
17/10/17 11:42:34 INFO mapreduce.Job:  map 100% reduce 0%
17/10/17 11:42:34 INFO mapreduce.Job: Job job_1508232743010_0003 completed successfully
17/10/17 11:42:34 INFO mapreduce.Job: Counters: 33
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=375135
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=500001643
                HDFS: Number of bytes written=500000000
                HDFS: Number of read operations=55
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=3
                Other local map tasks=3
                Total time spent by all maps in occupied slots (ms)=17162
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=17162
                Total vcore-seconds taken by all map tasks=17162
                Total megabyte-seconds taken by all map tasks=17573888
        Map-Reduce Framework
                Map input records=3
                Map output records=0
                Input split bytes=345
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=152
                CPU time spent (ms)=11130
                Physical memory (bytes) snapshot=683806720
                Virtual memory (bytes) snapshot=4733890560
                Total committed heap usage (bytes)=1074790400
        File Input Format Counters
                Bytes Read=1298
        File Output Format Counters
                Bytes Written=0
        org.apache.hadoop.tools.mapred.CopyMapper$Counter
                BYTESCOPIED=500000000
                BYTESEXPECTED=500000000
                COPY=3


5)[root@ip-172-31-18-79 hadoop-mapreduce]# hdfs fsck /user/source_laertgjoni/ -files -blocks
Connecting to namenode via http://ip-172-31-16-61.eu-central-1.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.18.79 for path /user/source_laertgjoni/ at Tue Oct 17 11:44:22 UTC 2017
/user/source_laertgjoni/ <dir>
/user/source_laertgjoni/_SUCCESS 0 bytes, 0 block(s):  OK

/user/source_laertgjoni/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-669652564-172.31.16.61-1508232682020:blk_1073741860_1036 len=134217728 Live_repl=3
1. BP-669652564-172.31.16.61-1508232682020:blk_1073741862_1038 len=115782272 Live_repl=3

/user/source_laertgjoni/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-669652564-172.31.16.61-1508232682020:blk_1073741861_1037 len=134217728 Live_repl=3
1. BP-669652564-172.31.16.61-1508232682020:blk_1073741863_1039 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 11:44:22 UTC 2017 in 3 milliseconds


The filesystem under path '/user/source_laertgjoni/' is HEALTHY




[root@ip-172-31-18-79 hadoop-mapreduce]# hdfs fsck /user/target_Maurizio845/ -files -blocks
Connecting to namenode via http://ip-172-31-16-61.eu-central-1.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.18.79 for path /user/target_Maurizio845/ at Tue Oct 17 11:44:57 UTC 2017
/user/target_Maurizio845/ <dir>
/user/target_Maurizio845/_SUCCESS 0 bytes, 0 block(s):  OK

/user/target_Maurizio845/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-669652564-172.31.16.61-1508232682020:blk_1073742000_1176 len=134217728 Live_repl=3
1. BP-669652564-172.31.16.61-1508232682020:blk_1073742002_1178 len=115782272 Live_repl=3

/user/target_Maurizio845/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-669652564-172.31.16.61-1508232682020:blk_1073742001_1177 len=134217728 Live_repl=3
1. BP-669652564-172.31.16.61-1508232682020:blk_1073742003_1179 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 11:44:57 UTC 2017 in 2 milliseconds


The filesystem under path '/user/target_Maurizio845/' is HEALTHY