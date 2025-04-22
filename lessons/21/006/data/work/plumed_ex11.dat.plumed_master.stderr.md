Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @63 : keyword ARG is compulsory for this action
[fv-az2211-783:07442] *** Process received signal ***
[fv-az2211-783:07442] Signal: Aborted (6)
[fv-az2211-783:07442] Signal code:  (-6)
[fv-az2211-783:07442] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd762845330]
[fv-az2211-783:07442] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd76289eb2c]
[fv-az2211-783:07442] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd76284527e]
[fv-az2211-783:07442] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd7628288ff]
[fv-az2211-783:07442] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd762ca5ff5]
[fv-az2211-783:07442] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd762cbb0da]
[fv-az2211-783:07442] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd762ca5a55]
[fv-az2211-783:07442] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd762ca5a6f]
[fv-az2211-783:07442] [ 8] plumed_master(+0x146dd)[0x5568c7b4a6dd]
[fv-az2211-783:07442] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd76282a1ca]
[fv-az2211-783:07442] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd76282a28b]
[fv-az2211-783:07442] [11] plumed_master(+0x15365)[0x5568c7b4b365]
[fv-az2211-783:07442] *** End of error message ***
</pre>
{% endraw %}
