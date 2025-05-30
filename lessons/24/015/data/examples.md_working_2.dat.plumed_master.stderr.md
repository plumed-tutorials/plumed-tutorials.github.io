Stderr for source:  examples.md_working_2.dat   
Download: [zipped raw stdout](examples.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmf6wy0o8zjz:58968] *** Process received signal ***
[pkrvmf6wy0o8zjz:58968] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58968] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58968] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd6b3c45330]
[pkrvmf6wy0o8zjz:58968] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd6b3c9eb2c]
[pkrvmf6wy0o8zjz:58968] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd6b3c4527e]
[pkrvmf6wy0o8zjz:58968] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd6b3c288ff]
[pkrvmf6wy0o8zjz:58968] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd6b40a5ff5]
[pkrvmf6wy0o8zjz:58968] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd6b40bb0da]
[pkrvmf6wy0o8zjz:58968] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd6b40a5a55]
[pkrvmf6wy0o8zjz:58968] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd6b40a5a6f]
[pkrvmf6wy0o8zjz:58968] [ 8] plumed_master(+0x146dd)[0x55b61caec6dd]
[pkrvmf6wy0o8zjz:58968] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd6b3c2a1ca]
[pkrvmf6wy0o8zjz:58968] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd6b3c2a28b]
[pkrvmf6wy0o8zjz:58968] [11] plumed_master(+0x15365)[0x55b61caed365]
[pkrvmf6wy0o8zjz:58968] *** End of error message ***
</pre>
{% endraw %}
