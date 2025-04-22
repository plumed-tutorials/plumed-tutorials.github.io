Stderr for source:  work/plumed_ex6.dat   
Download: [zipped raw stdout](plumed_ex6.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex6.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @53 : keyword ARG is compulsory for this action
[fv-az1279-640:06970] *** Process received signal ***
[fv-az1279-640:06970] Signal: Aborted (6)
[fv-az1279-640:06970] Signal code:  (-6)
[fv-az1279-640:06970] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2936a45330]
[fv-az1279-640:06970] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2936a9eb2c]
[fv-az1279-640:06970] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2936a4527e]
[fv-az1279-640:06970] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2936a288ff]
[fv-az1279-640:06970] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2936ea5ff5]
[fv-az1279-640:06970] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2936ebb0da]
[fv-az1279-640:06970] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2936ea5a55]
[fv-az1279-640:06970] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2936ea5a6f]
[fv-az1279-640:06970] [ 8] plumed_master(+0x146dd)[0x55912ce7d6dd]
[fv-az1279-640:06970] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2936a2a1ca]
[fv-az1279-640:06970] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2936a2a28b]
[fv-az1279-640:06970] [11] plumed_master(+0x15365)[0x55912ce7e365]
[fv-az1279-640:06970] *** End of error message ***
</pre>
{% endraw %}
