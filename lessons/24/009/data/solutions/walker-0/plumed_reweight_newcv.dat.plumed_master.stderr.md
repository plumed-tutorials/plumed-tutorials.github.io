Stderr for source:  ./solutions/walker-0/plumed_reweight_newcv.dat   
Download: [zipped raw stdout](plumed_reweight_newcv.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight_newcv.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az2211-783:05819] *** Process received signal ***
[fv-az2211-783:05819] Signal: Aborted (6)
[fv-az2211-783:05819] Signal code:  (-6)
[fv-az2211-783:05819] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0bf1245330]
[fv-az2211-783:05819] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0bf129eb2c]
[fv-az2211-783:05819] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0bf124527e]
[fv-az2211-783:05819] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0bf12288ff]
[fv-az2211-783:05819] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0bf16a5ff5]
[fv-az2211-783:05819] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0bf16bb0da]
[fv-az2211-783:05819] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0bf16a5a55]
[fv-az2211-783:05819] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0bf16a5a6f]
[fv-az2211-783:05819] [ 8] plumed_master(+0x146dd)[0x55d483cba6dd]
[fv-az2211-783:05819] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0bf122a1ca]
[fv-az2211-783:05819] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0bf122a28b]
[fv-az2211-783:05819] [11] plumed_master(+0x15365)[0x55d483cbb365]
[fv-az2211-783:05819] *** End of error message ***
</pre>
{% endraw %}
