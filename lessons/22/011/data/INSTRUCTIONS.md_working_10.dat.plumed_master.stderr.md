Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmf6wy0o8zjz:60060] *** Process received signal ***
[pkrvmf6wy0o8zjz:60060] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60060] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60060] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f822a845330]
[pkrvmf6wy0o8zjz:60060] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f822a89eb2c]
[pkrvmf6wy0o8zjz:60060] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f822a84527e]
[pkrvmf6wy0o8zjz:60060] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f822a8288ff]
[pkrvmf6wy0o8zjz:60060] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f822aca5ff5]
[pkrvmf6wy0o8zjz:60060] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f822acbb0da]
[pkrvmf6wy0o8zjz:60060] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f822aca5a55]
[pkrvmf6wy0o8zjz:60060] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f822aca5a6f]
[pkrvmf6wy0o8zjz:60060] [ 8] plumed_master(+0x146dd)[0x55d2cd1ac6dd]
[pkrvmf6wy0o8zjz:60060] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f822a82a1ca]
[pkrvmf6wy0o8zjz:60060] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f822a82a28b]
[pkrvmf6wy0o8zjz:60060] [11] plumed_master(+0x15365)[0x55d2cd1ad365]
[pkrvmf6wy0o8zjz:60060] *** End of error message ***
</pre>
{% endraw %}
