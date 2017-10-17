1)
useradd -m laertgjoni

groupadd SEBC

usermod -G SEBC laertgjoni


sudo -u hdfs hdfs dfs -mkdir /user/laertgjoni

sudo -u hdfs hdfs dfs -chown laertgjoni:laertgjoni /user/laertgjoni


su - laertgjoni

2)
time hadoop jar hadoop-examples.jar teragen -D mapreduce.job.maps=4 -D dfs.blocksize=33554432 100000000 /user/laertgjoni/files/


real    2m33.168s
user    0m5.850s
sys     0m0.305s


3)
time hadoop jar hadoop-examples.jar terasort /user/laertgjoni/files/ /user/laertgjoni/files_terasort/

real    6m57.439s
user    0m10.378s
sys     0m0.498s


