Stderr for source:  examples.md_working_4.dat   
Download: [zipped raw stdout](examples.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](examples.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmf6wy0o8zjz:59042] *** Process received signal ***
[pkrvmf6wy0o8zjz:59042] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59042] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59042] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f77ab245330]
[pkrvmf6wy0o8zjz:59042] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f77ab29eb2c]
[pkrvmf6wy0o8zjz:59042] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f77ab24527e]
[pkrvmf6wy0o8zjz:59042] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f77ab2288ff]
[pkrvmf6wy0o8zjz:59042] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f77ab6a5ff5]
[pkrvmf6wy0o8zjz:59042] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f77ab6bb0da]
[pkrvmf6wy0o8zjz:59042] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f77ab6a5a55]
[pkrvmf6wy0o8zjz:59042] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f77ab6a5a6f]
[pkrvmf6wy0o8zjz:59042] [ 8] plumed(+0x13209)[0x558a91718209]
[pkrvmf6wy0o8zjz:59042] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f77ab22a1ca]
[pkrvmf6wy0o8zjz:59042] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f77ab22a28b]
[pkrvmf6wy0o8zjz:59042] [11] plumed(+0x134a5)[0x558a917184a5]
[pkrvmf6wy0o8zjz:59042] *** End of error message ***
</pre>
{% endraw %}
