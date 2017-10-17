1)
su - laertgjoni

scp -i KP01.pem SEBC-master.zip centos@ec2-18-194-212-169.eu-central-1.compute.amazonaws.com:/tmp/

hdfs dfs -put /tmp/SEBC-master.zip /user/laertgjoni/precious/

[laertgjoni@ip-172-31-18-79 ~]$ hdfs dfs -rm /user/laertgjoni/precious/SEBC-master.zip
17/10/17 14:06:32 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-16-61.eu-central-1.compute.internal:8020/user/laertgjoni/precious/SEBC-master.zip' to trash at: hdfs://ip-172-31-16-61.eu-central-1.compute.internal:8020/user/laertgjoni/.Trash/Current/user/laertgjoni/precious/SEBC-master.zip

[laertgjoni@ip-172-31-18-79 ~]$ hdfs dfs -rm -r /user/laertgjoni/precious/
rm: Failed to move to trash: hdfs://ip-172-31-16-61.eu-central-1.compute.internal:8020/user/laertgjoni/precious: The directory /user/laertgjoni/precious cannot be deleted since /user/laertgjoni/precious is snapshottable and already has snapshots
