Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @50 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:59973] *** Process received signal ***
[pkrvmf6wy0o8zjz:59973] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59973] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59973] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7feb7c445330]
[pkrvmf6wy0o8zjz:59973] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7feb7c49eb2c]
[pkrvmf6wy0o8zjz:59973] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7feb7c44527e]
[pkrvmf6wy0o8zjz:59973] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7feb7c4288ff]
[pkrvmf6wy0o8zjz:59973] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7feb7c8a5ff5]
[pkrvmf6wy0o8zjz:59973] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7feb7c8bb0da]
[pkrvmf6wy0o8zjz:59973] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7feb7c8a5a55]
[pkrvmf6wy0o8zjz:59973] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7feb7c8a5a6f]
[pkrvmf6wy0o8zjz:59973] [ 8] plumed_master(+0x146dd)[0x5607b8cb66dd]
[pkrvmf6wy0o8zjz:59973] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7feb7c42a1ca]
[pkrvmf6wy0o8zjz:59973] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7feb7c42a28b]
[pkrvmf6wy0o8zjz:59973] [11] plumed_master(+0x15365)[0x5607b8cb7365]
[pkrvmf6wy0o8zjz:59973] *** End of error message ***
</pre>
{% endraw %}
