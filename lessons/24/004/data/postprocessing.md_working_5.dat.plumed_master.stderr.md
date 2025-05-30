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
[pkrvmf6wy0o8zjz:59466] *** Process received signal ***
[pkrvmf6wy0o8zjz:59466] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59466] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59466] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdca1c45330]
[pkrvmf6wy0o8zjz:59466] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdca1c9eb2c]
[pkrvmf6wy0o8zjz:59466] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdca1c4527e]
[pkrvmf6wy0o8zjz:59466] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdca1c288ff]
[pkrvmf6wy0o8zjz:59466] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdca20a5ff5]
[pkrvmf6wy0o8zjz:59466] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdca20bb0da]
[pkrvmf6wy0o8zjz:59466] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdca20a5a55]
[pkrvmf6wy0o8zjz:59466] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdca20a5a6f]
[pkrvmf6wy0o8zjz:59466] [ 8] plumed_master(+0x146dd)[0x559035b216dd]
[pkrvmf6wy0o8zjz:59466] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdca1c2a1ca]
[pkrvmf6wy0o8zjz:59466] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdca1c2a28b]
[pkrvmf6wy0o8zjz:59466] [11] plumed_master(+0x15365)[0x559035b22365]
[pkrvmf6wy0o8zjz:59466] *** End of error message ***
</pre>
{% endraw %}
