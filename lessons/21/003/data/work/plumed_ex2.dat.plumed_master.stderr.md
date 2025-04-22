Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @38 : keyword ARG is compulsory for this action
[fv-az1279-640:06721] *** Process received signal ***
[fv-az1279-640:06721] Signal: Aborted (6)
[fv-az1279-640:06721] Signal code:  (-6)
[fv-az1279-640:06721] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd586445330]
[fv-az1279-640:06721] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd58649eb2c]
[fv-az1279-640:06721] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd58644527e]
[fv-az1279-640:06721] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd5864288ff]
[fv-az1279-640:06721] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd5868a5ff5]
[fv-az1279-640:06721] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd5868bb0da]
[fv-az1279-640:06721] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd5868a5a55]
[fv-az1279-640:06721] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd5868a5a6f]
[fv-az1279-640:06721] [ 8] plumed_master(+0x146dd)[0x5652370466dd]
[fv-az1279-640:06721] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd58642a1ca]
[fv-az1279-640:06721] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd58642a28b]
[fv-az1279-640:06721] [11] plumed_master(+0x15365)[0x565237047365]
[fv-az1279-640:06721] *** End of error message ***
</pre>
{% endraw %}
