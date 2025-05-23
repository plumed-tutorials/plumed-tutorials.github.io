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
[pkrvmf6wy0o8zjz:60233] *** Process received signal ***
[pkrvmf6wy0o8zjz:60233] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60233] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60233] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd217c45330]
[pkrvmf6wy0o8zjz:60233] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd217c9eb2c]
[pkrvmf6wy0o8zjz:60233] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd217c4527e]
[pkrvmf6wy0o8zjz:60233] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd217c288ff]
[pkrvmf6wy0o8zjz:60233] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd2180a5ff5]
[pkrvmf6wy0o8zjz:60233] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd2180bb0da]
[pkrvmf6wy0o8zjz:60233] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd2180a5a55]
[pkrvmf6wy0o8zjz:60233] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd2180a5a6f]
[pkrvmf6wy0o8zjz:60233] [ 8] plumed_master(+0x146dd)[0x55c4f2be46dd]
[pkrvmf6wy0o8zjz:60233] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd217c2a1ca]
[pkrvmf6wy0o8zjz:60233] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd217c2a28b]
[pkrvmf6wy0o8zjz:60233] [11] plumed_master(+0x15365)[0x55c4f2be5365]
[pkrvmf6wy0o8zjz:60233] *** End of error message ***
</pre>
{% endraw %}
