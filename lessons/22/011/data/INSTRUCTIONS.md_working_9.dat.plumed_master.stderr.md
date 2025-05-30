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
[pkrvmf6wy0o8zjz:60016] *** Process received signal ***
[pkrvmf6wy0o8zjz:60016] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60016] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60016] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7faf5aa45330]
[pkrvmf6wy0o8zjz:60016] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7faf5aa9eb2c]
[pkrvmf6wy0o8zjz:60016] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7faf5aa4527e]
[pkrvmf6wy0o8zjz:60016] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7faf5aa288ff]
[pkrvmf6wy0o8zjz:60016] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7faf5aea5ff5]
[pkrvmf6wy0o8zjz:60016] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7faf5aebb0da]
[pkrvmf6wy0o8zjz:60016] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7faf5aea5a55]
[pkrvmf6wy0o8zjz:60016] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7faf5aea5a6f]
[pkrvmf6wy0o8zjz:60016] [ 8] plumed_master(+0x146dd)[0x55f5c868e6dd]
[pkrvmf6wy0o8zjz:60016] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7faf5aa2a1ca]
[pkrvmf6wy0o8zjz:60016] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7faf5aa2a28b]
[pkrvmf6wy0o8zjz:60016] [11] plumed_master(+0x15365)[0x55f5c868f365]
[pkrvmf6wy0o8zjz:60016] *** End of error message ***
</pre>
{% endraw %}
