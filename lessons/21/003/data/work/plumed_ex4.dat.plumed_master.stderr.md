Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:60869] *** Process received signal ***
[pkrvmf6wy0o8zjz:60869] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60869] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60869] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa7da845330]
[pkrvmf6wy0o8zjz:60869] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa7da89eb2c]
[pkrvmf6wy0o8zjz:60869] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa7da84527e]
[pkrvmf6wy0o8zjz:60869] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa7da8288ff]
[pkrvmf6wy0o8zjz:60869] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa7daca5ff5]
[pkrvmf6wy0o8zjz:60869] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa7dacbb0da]
[pkrvmf6wy0o8zjz:60869] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa7daca5a55]
[pkrvmf6wy0o8zjz:60869] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa7daca5a6f]
[pkrvmf6wy0o8zjz:60869] [ 8] plumed_master(+0x146dd)[0x56427a5bc6dd]
[pkrvmf6wy0o8zjz:60869] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa7da82a1ca]
[pkrvmf6wy0o8zjz:60869] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa7da82a28b]
[pkrvmf6wy0o8zjz:60869] [11] plumed_master(+0x15365)[0x56427a5bd365]
[pkrvmf6wy0o8zjz:60869] *** End of error message ***
</pre>
{% endraw %}
