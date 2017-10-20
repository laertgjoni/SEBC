[ernest@ip-172-31-37-209 hadoop-0.20-mapreduce]$ time hadoop jar hadoop-examples.jar teragen -Dmapreduce.job.maps=6 51200000 user/ernest/results/tgen512m_0/
17/10/20 09:36:20 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-32-147.eu-central-1.compute.internal/172.31.32.147:8032
17/10/20 09:36:21 INFO terasort.TeraSort: Generating 51200000 using 6
17/10/20 09:36:21 INFO mapreduce.JobSubmitter: number of splits:6
17/10/20 09:36:21 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1508490936728_0002
17/10/20 09:36:21 INFO impl.YarnClientImpl: Submitted application application_1508490936728_0002
17/10/20 09:36:21 INFO mapreduce.Job: The url to track the job: http://ip-172-31-32-147.eu-central-1.compute.internal:8088/proxy/application_1508490936728_0002/
17/10/20 09:36:21 INFO mapreduce.Job: Running job: job_1508490936728_0002
17/10/20 09:36:27 INFO mapreduce.Job: Job job_1508490936728_0002 running in uber mode : false
17/10/20 09:36:27 INFO mapreduce.Job:  map 0% reduce 0%
17/10/20 09:36:38 INFO mapreduce.Job:  map 4% reduce 0%
17/10/20 09:36:39 INFO mapreduce.Job:  map 11% reduce 0%
17/10/20 09:36:41 INFO mapreduce.Job:  map 19% reduce 0%
17/10/20 09:36:42 INFO mapreduce.Job:  map 22% reduce 0%
17/10/20 09:36:44 INFO mapreduce.Job:  map 27% reduce 0%
17/10/20 09:36:45 INFO mapreduce.Job:  map 28% reduce 0%
17/10/20 09:36:47 INFO mapreduce.Job:  map 31% reduce 0%
17/10/20 09:36:50 INFO mapreduce.Job:  map 34% reduce 0%
17/10/20 09:36:51 INFO mapreduce.Job:  map 35% reduce 0%
17/10/20 09:36:53 INFO mapreduce.Job:  map 37% reduce 0%
17/10/20 09:36:54 INFO mapreduce.Job:  map 38% reduce 0%
17/10/20 09:36:56 INFO mapreduce.Job:  map 40% reduce 0%
17/10/20 09:36:57 INFO mapreduce.Job:  map 42% reduce 0%
17/10/20 09:37:00 INFO mapreduce.Job:  map 43% reduce 0%
17/10/20 09:37:01 INFO mapreduce.Job:  map 44% reduce 0%
17/10/20 09:37:03 INFO mapreduce.Job:  map 48% reduce 0%
17/10/20 09:37:04 INFO mapreduce.Job:  map 49% reduce 0%
17/10/20 09:37:06 INFO mapreduce.Job:  map 53% reduce 0%
17/10/20 09:37:08 INFO mapreduce.Job:  map 55% reduce 0%
17/10/20 09:37:09 INFO mapreduce.Job:  map 56% reduce 0%
17/10/20 09:37:10 INFO mapreduce.Job:  map 57% reduce 0%
17/10/20 09:37:11 INFO mapreduce.Job:  map 59% reduce 0%
17/10/20 09:37:12 INFO mapreduce.Job:  map 60% reduce 0%
17/10/20 09:37:14 INFO mapreduce.Job:  map 63% reduce 0%
17/10/20 09:37:15 INFO mapreduce.Job:  map 64% reduce 0%
17/10/20 09:37:17 INFO mapreduce.Job:  map 66% reduce 0%
17/10/20 09:37:18 INFO mapreduce.Job:  map 68% reduce 0%
17/10/20 09:37:20 INFO mapreduce.Job:  map 70% reduce 0%
17/10/20 09:37:21 INFO mapreduce.Job:  map 72% reduce 0%
17/10/20 09:37:23 INFO mapreduce.Job:  map 74% reduce 0%
17/10/20 09:37:24 INFO mapreduce.Job:  map 76% reduce 0%
17/10/20 09:37:26 INFO mapreduce.Job:  map 79% reduce 0%
17/10/20 09:37:29 INFO mapreduce.Job:  map 81% reduce 0%
17/10/20 09:37:30 INFO mapreduce.Job:  map 84% reduce 0%
17/10/20 09:37:32 INFO mapreduce.Job:  map 86% reduce 0%
17/10/20 09:37:33 INFO mapreduce.Job:  map 88% reduce 0%
17/10/20 09:37:35 INFO mapreduce.Job:  map 91% reduce 0%
17/10/20 09:37:36 INFO mapreduce.Job:  map 92% reduce 0%
17/10/20 09:37:39 INFO mapreduce.Job:  map 94% reduce 0%
17/10/20 09:37:40 INFO mapreduce.Job:  map 96% reduce 0%
17/10/20 09:37:41 INFO mapreduce.Job:  map 97% reduce 0%
17/10/20 09:37:42 INFO mapreduce.Job:  map 100% reduce 0%
17/10/20 09:37:43 INFO mapreduce.Job: Job job_1508490936728_0002 completed successfully
17/10/20 09:37:43 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=741696
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=511
                HDFS: Number of bytes written=5120000000
                HDFS: Number of read operations=24
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=12
        Job Counters
                Launched map tasks=6
                Other local map tasks=6
                Total time spent by all maps in occupied slots (ms)=424428
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=424428
                Total vcore-seconds taken by all map tasks=424428
                Total megabyte-seconds taken by all map tasks=434614272
        Map-Reduce Framework
                Map input records=51200000
                Map output records=51200000
                Input split bytes=511
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1049
                CPU time spent (ms)=99430
                Physical memory (bytes) snapshot=2074079232
                Virtual memory (bytes) snapshot=9517449216
                Total committed heap usage (bytes)=2150629376
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=109963291816450258
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=5120000000

real    1m24.703s
user    0m5.520s
sys     0m0.250s

#mistake [i made a mistake in the teragen command i used the whole path so the /user/ernest part is redundant]

[ernest@ip-172-31-37-209 hadoop-0.20-mapreduce]$ hdfs dfs -ls /user/ernest/user/ernest/results/tgen512m_0
Found 7 items
-rw-r--r--   3 ernest usa          0 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/_SUCCESS
-rw-r--r--   3 ernest usa  853333400 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/part-m-00000
-rw-r--r--   3 ernest usa  853333300 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/part-m-00001
-rw-r--r--   3 ernest usa  853333300 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/part-m-00002
-rw-r--r--   3 ernest usa  853333400 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/part-m-00003
-rw-r--r--   3 ernest usa  853333300 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/part-m-00004
-rw-r--r--   3 ernest usa  853333300 2017-10-20 09:37 /user/ernest/user/ernest/results/tgen512m_0/part-m-00005