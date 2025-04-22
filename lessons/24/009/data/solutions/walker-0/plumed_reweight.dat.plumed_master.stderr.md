Stderr for source:  ./solutions/walker-0/plumed_reweight.dat   
Download: [zipped raw stdout](plumed_reweight.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az2211-783:05786] *** Process received signal ***
[fv-az2211-783:05786] Signal: Aborted (6)
[fv-az2211-783:05786] Signal code:  (-6)
[fv-az2211-783:05786] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc471c45330]
[fv-az2211-783:05786] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc471c9eb2c]
[fv-az2211-783:05786] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc471c4527e]
[fv-az2211-783:05786] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc471c288ff]
[fv-az2211-783:05786] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc4720a5ff5]
[fv-az2211-783:05786] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc4720bb0da]
[fv-az2211-783:05786] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc4720a5a55]
[fv-az2211-783:05786] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc4720a5a6f]
[fv-az2211-783:05786] [ 8] plumed_master(+0x146dd)[0x562af2a176dd]
[fv-az2211-783:05786] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc471c2a1ca]
[fv-az2211-783:05786] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc471c2a28b]
[fv-az2211-783:05786] [11] plumed_master(+0x15365)[0x562af2a18365]
[fv-az2211-783:05786] *** End of error message ***
</pre>
{% endraw %}
