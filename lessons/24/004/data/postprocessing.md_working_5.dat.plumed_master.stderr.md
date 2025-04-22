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
[fv-az2211-783:06377] *** Process received signal ***
[fv-az2211-783:06377] Signal: Aborted (6)
[fv-az2211-783:06377] Signal code:  (-6)
[fv-az2211-783:06377] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4e29845330]
[fv-az2211-783:06377] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4e2989eb2c]
[fv-az2211-783:06377] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4e2984527e]
[fv-az2211-783:06377] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4e298288ff]
[fv-az2211-783:06377] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4e29ca5ff5]
[fv-az2211-783:06377] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4e29cbb0da]
[fv-az2211-783:06377] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4e29ca5a55]
[fv-az2211-783:06377] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4e29ca5a6f]
[fv-az2211-783:06377] [ 8] plumed_master(+0x146dd)[0x556fe772c6dd]
[fv-az2211-783:06377] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4e2982a1ca]
[fv-az2211-783:06377] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4e2982a28b]
[fv-az2211-783:06377] [11] plumed_master(+0x15365)[0x556fe772d365]
[fv-az2211-783:06377] *** End of error message ***
</pre>
{% endraw %}
