Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az2211-783:05983] *** Process received signal ***
[fv-az2211-783:05983] Signal: Aborted (6)
[fv-az2211-783:05983] Signal code:  (-6)
[fv-az2211-783:05983] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdcc9645330]
[fv-az2211-783:05983] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdcc969eb2c]
[fv-az2211-783:05983] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdcc964527e]
[fv-az2211-783:05983] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdcc96288ff]
[fv-az2211-783:05983] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdcc9aa5ff5]
[fv-az2211-783:05983] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdcc9abb0da]
[fv-az2211-783:05983] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdcc9aa5a55]
[fv-az2211-783:05983] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdcc9aa5a6f]
[fv-az2211-783:05983] [ 8] plumed_master(+0x146dd)[0x5617886ba6dd]
[fv-az2211-783:05983] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdcc962a1ca]
[fv-az2211-783:05983] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdcc962a28b]
[fv-az2211-783:05983] [11] plumed_master(+0x15365)[0x5617886bb365]
[fv-az2211-783:05983] *** End of error message ***
</pre>
{% endraw %}
