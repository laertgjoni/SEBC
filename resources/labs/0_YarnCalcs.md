Changed OS memory, now the multiplier it's 0.064 instead of 0.3, because the memory given to the OS was way higher than what is normally required.

By changing the memory required by the OS, YARN resources now has more memory to use.

Reduced number of vcores for the OS to 1, which is the minimum required; this increases the yarn cpu vcores available.

yarn.scheduler.maximum-allocation-vcores set to 4 vcores, which is less than the maximum number of vcores available, to ensure that no single task consumes alla available memory.

yarn.scheduler.maximum-allocation-mb has been changed to a maximum of 8gb which is the default value.

yarn.app.mapreduce.am.resource.mb was set to 1mb, this value is way too low, new value is 1024

mapreduce.map.java.opts.max.heap changed to match the 80% of mapreduce.map.memory.mb

WorkLoad Factor affects the mapreduce jobs, a value of 2 is a standard because it give mapreduce jobs the possibility to use the maximum number of vcores available for yarn.