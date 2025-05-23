Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[pkrvmf6wy0o8zjz:60188] *** Process received signal ***
[pkrvmf6wy0o8zjz:60188] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60188] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60188] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb822a45330]
[pkrvmf6wy0o8zjz:60188] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb822a9eb2c]
[pkrvmf6wy0o8zjz:60188] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb822a4527e]
[pkrvmf6wy0o8zjz:60188] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb822a288ff]
[pkrvmf6wy0o8zjz:60188] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb822ea5ff5]
[pkrvmf6wy0o8zjz:60188] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb822ebb0da]
[pkrvmf6wy0o8zjz:60188] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb822ea5a55]
[pkrvmf6wy0o8zjz:60188] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb822ea5a6f]
[pkrvmf6wy0o8zjz:60188] [ 8] plumed_master(+0x146dd)[0x56096dfcf6dd]
[pkrvmf6wy0o8zjz:60188] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb822a2a1ca]
[pkrvmf6wy0o8zjz:60188] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb822a2a28b]
[pkrvmf6wy0o8zjz:60188] [11] plumed_master(+0x15365)[0x56096dfd0365]
[pkrvmf6wy0o8zjz:60188] *** End of error message ***
</pre>
{% endraw %}
