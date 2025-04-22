Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[fv-az1279-640:06235] *** Process received signal ***
[fv-az1279-640:06235] Signal: Aborted (6)
[fv-az1279-640:06235] Signal code:  (-6)
[fv-az1279-640:06235] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1ccda45330]
[fv-az1279-640:06235] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1ccda9eb2c]
[fv-az1279-640:06235] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1ccda4527e]
[fv-az1279-640:06235] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1ccda288ff]
[fv-az1279-640:06235] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1ccdea5ff5]
[fv-az1279-640:06235] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1ccdebb0da]
[fv-az1279-640:06235] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1ccdea5a55]
[fv-az1279-640:06235] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1ccdea5a6f]
[fv-az1279-640:06235] [ 8] plumed_master(+0x146dd)[0x5623140f06dd]
[fv-az1279-640:06235] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1ccda2a1ca]
[fv-az1279-640:06235] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1ccda2a28b]
[fv-az1279-640:06235] [11] plumed_master(+0x15365)[0x5623140f1365]
[fv-az1279-640:06235] *** End of error message ***
</pre>
{% endraw %}
