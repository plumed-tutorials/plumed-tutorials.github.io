Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @15 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:60695] *** Process received signal ***
[pkrvmf6wy0o8zjz:60695] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60695] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60695] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb5de045330]
[pkrvmf6wy0o8zjz:60695] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb5de09eb2c]
[pkrvmf6wy0o8zjz:60695] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb5de04527e]
[pkrvmf6wy0o8zjz:60695] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb5de0288ff]
[pkrvmf6wy0o8zjz:60695] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb5de4a5ff5]
[pkrvmf6wy0o8zjz:60695] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb5de4bb0da]
[pkrvmf6wy0o8zjz:60695] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb5de4a5a55]
[pkrvmf6wy0o8zjz:60695] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb5de4a5a6f]
[pkrvmf6wy0o8zjz:60695] [ 8] plumed_master(+0x146dd)[0x5643f08c06dd]
[pkrvmf6wy0o8zjz:60695] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb5de02a1ca]
[pkrvmf6wy0o8zjz:60695] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb5de02a28b]
[pkrvmf6wy0o8zjz:60695] [11] plumed_master(+0x15365)[0x5643f08c1365]
[pkrvmf6wy0o8zjz:60695] *** End of error message ***
</pre>
{% endraw %}
