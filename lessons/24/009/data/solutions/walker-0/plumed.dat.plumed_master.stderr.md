Stderr for source:  ./solutions/walker-0/plumed.dat   
Download: [zipped raw stdout](plumed.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action HBOND_MATRIX with label hbmat1 : cannot understand the following words from the input line : SUM
[pkrvmf6wy0o8zjz:59248] *** Process received signal ***
[pkrvmf6wy0o8zjz:59248] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59248] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59248] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9f01c45330]
[pkrvmf6wy0o8zjz:59248] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9f01c9eb2c]
[pkrvmf6wy0o8zjz:59248] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9f01c4527e]
[pkrvmf6wy0o8zjz:59248] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9f01c288ff]
[pkrvmf6wy0o8zjz:59248] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9f020a5ff5]
[pkrvmf6wy0o8zjz:59248] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9f020bb0da]
[pkrvmf6wy0o8zjz:59248] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9f020a5a55]
[pkrvmf6wy0o8zjz:59248] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9f020a5a6f]
[pkrvmf6wy0o8zjz:59248] [ 8] plumed_master(+0x146dd)[0x563cac1f26dd]
[pkrvmf6wy0o8zjz:59248] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9f01c2a1ca]
[pkrvmf6wy0o8zjz:59248] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9f01c2a28b]
[pkrvmf6wy0o8zjz:59248] [11] plumed_master(+0x15365)[0x563cac1f3365]
[pkrvmf6wy0o8zjz:59248] *** End of error message ***
</pre>
{% endraw %}
