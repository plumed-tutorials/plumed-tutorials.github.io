Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[fv-az2211-783:07063] *** Process received signal ***
[fv-az2211-783:07063] Signal: Aborted (6)
[fv-az2211-783:07063] Signal code:  (-6)
[fv-az2211-783:07063] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5487e45330]
[fv-az2211-783:07063] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5487e9eb2c]
[fv-az2211-783:07063] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5487e4527e]
[fv-az2211-783:07063] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5487e288ff]
[fv-az2211-783:07063] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f54882a5ff5]
[fv-az2211-783:07063] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f54882bb0da]
[fv-az2211-783:07063] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f54882a5a55]
[fv-az2211-783:07063] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f54882a5a6f]
[fv-az2211-783:07063] [ 8] plumed_master(+0x146dd)[0x55ff804a06dd]
[fv-az2211-783:07063] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5487e2a1ca]
[fv-az2211-783:07063] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5487e2a28b]
[fv-az2211-783:07063] [11] plumed_master(+0x15365)[0x55ff804a1365]
[fv-az2211-783:07063] *** End of error message ***
</pre>
{% endraw %}
