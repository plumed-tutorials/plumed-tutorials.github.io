Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(vesselbase/Vessel.cpp:157) void PLMD::vesselbase::Vessel::error(const std::string&)
ERROR for keyword MORE_THAN in action CLUSTER_DISTRIBUTION with label nclust : could not parse D_0
[runnervm3jyl0:48237] *** Process received signal ***
[runnervm3jyl0:48237] Signal: Aborted (6)
[runnervm3jyl0:48237] Signal code:  (-6)
[runnervm3jyl0:48237] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f703d245330]
[runnervm3jyl0:48237] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f703d29eb2c]
[runnervm3jyl0:48237] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f703d24527e]
[runnervm3jyl0:48237] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f703d2288ff]
[runnervm3jyl0:48237] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f703d6a5ff5]
[runnervm3jyl0:48237] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f703d6bb0da]
[runnervm3jyl0:48237] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f703d6a5a55]
[runnervm3jyl0:48237] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f703d6a5a6f]
[runnervm3jyl0:48237] [ 8] plumed(+0x13209)[0x55fed03be209]
[runnervm3jyl0:48237] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f703d22a1ca]
[runnervm3jyl0:48237] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f703d22a28b]
[runnervm3jyl0:48237] [11] plumed(+0x134a5)[0x55fed03be4a5]
[runnervm3jyl0:48237] *** End of error message ***
</pre>
{% endraw %}
