Stderr for source:  ./solutions/walker-0/plumed_reweight_newcv.dat   
Download: [zipped raw stdout](plumed_reweight_newcv.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight_newcv.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:59320] *** Process received signal ***
[pkrvmf6wy0o8zjz:59320] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59320] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59320] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f77ee845330]
[pkrvmf6wy0o8zjz:59320] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f77ee89eb2c]
[pkrvmf6wy0o8zjz:59320] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f77ee84527e]
[pkrvmf6wy0o8zjz:59320] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f77ee8288ff]
[pkrvmf6wy0o8zjz:59320] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f77eeca5ff5]
[pkrvmf6wy0o8zjz:59320] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f77eecbb0da]
[pkrvmf6wy0o8zjz:59320] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f77eeca5a55]
[pkrvmf6wy0o8zjz:59320] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f77eeca5a6f]
[pkrvmf6wy0o8zjz:59320] [ 8] plumed_master(+0x146dd)[0x557df3ba96dd]
[pkrvmf6wy0o8zjz:59320] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f77ee82a1ca]
[pkrvmf6wy0o8zjz:59320] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f77ee82a28b]
[pkrvmf6wy0o8zjz:59320] [11] plumed_master(+0x15365)[0x557df3baa365]
[pkrvmf6wy0o8zjz:59320] *** End of error message ***
</pre>
{% endraw %}
