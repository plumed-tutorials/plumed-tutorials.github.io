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
[pkrvmf6wy0o8zjz:59825] *** Process received signal ***
[pkrvmf6wy0o8zjz:59825] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59825] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59825] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f072fe45330]
[pkrvmf6wy0o8zjz:59825] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f072fe9eb2c]
[pkrvmf6wy0o8zjz:59825] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f072fe4527e]
[pkrvmf6wy0o8zjz:59825] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f072fe288ff]
[pkrvmf6wy0o8zjz:59825] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f07302a5ff5]
[pkrvmf6wy0o8zjz:59825] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f07302bb0da]
[pkrvmf6wy0o8zjz:59825] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f07302a5a55]
[pkrvmf6wy0o8zjz:59825] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f07302a5a6f]
[pkrvmf6wy0o8zjz:59825] [ 8] plumed_master(+0x146dd)[0x55d89a2246dd]
[pkrvmf6wy0o8zjz:59825] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f072fe2a1ca]
[pkrvmf6wy0o8zjz:59825] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f072fe2a28b]
[pkrvmf6wy0o8zjz:59825] [11] plumed_master(+0x15365)[0x55d89a225365]
[pkrvmf6wy0o8zjz:59825] *** End of error message ***
</pre>
{% endraw %}
