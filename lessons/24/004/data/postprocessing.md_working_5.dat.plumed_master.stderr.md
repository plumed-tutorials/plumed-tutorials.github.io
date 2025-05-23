Stderr for source:  postprocessing.md_working_5.dat   
Download: [zipped raw stdout](postprocessing.md_working_5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](postprocessing.md_working_5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @18 : keyword ARG is compulsory for this action
[pkrvmf6wy0o8zjz:59806] *** Process received signal ***
[pkrvmf6wy0o8zjz:59806] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59806] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59806] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7efeb4845330]
[pkrvmf6wy0o8zjz:59806] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7efeb489eb2c]
[pkrvmf6wy0o8zjz:59806] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7efeb484527e]
[pkrvmf6wy0o8zjz:59806] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7efeb48288ff]
[pkrvmf6wy0o8zjz:59806] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7efeb4ca5ff5]
[pkrvmf6wy0o8zjz:59806] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7efeb4cbb0da]
[pkrvmf6wy0o8zjz:59806] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7efeb4ca5a55]
[pkrvmf6wy0o8zjz:59806] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7efeb4ca5a6f]
[pkrvmf6wy0o8zjz:59806] [ 8] plumed_master(+0x146dd)[0x55b41f0366dd]
[pkrvmf6wy0o8zjz:59806] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7efeb482a1ca]
[pkrvmf6wy0o8zjz:59806] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7efeb482a28b]
[pkrvmf6wy0o8zjz:59806] [11] plumed_master(+0x15365)[0x55b41f037365]
[pkrvmf6wy0o8zjz:59806] *** End of error message ***
</pre>
{% endraw %}
