Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[runnervm3jyl0:47563] *** Process received signal ***
[runnervm3jyl0:47563] Signal: Aborted (6)
[runnervm3jyl0:47563] Signal code:  (-6)
[runnervm3jyl0:47563] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fde40c45330]
[runnervm3jyl0:47563] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fde40c9eb2c]
[runnervm3jyl0:47563] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fde40c4527e]
[runnervm3jyl0:47563] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fde40c288ff]
[runnervm3jyl0:47563] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fde410a5ff5]
[runnervm3jyl0:47563] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fde410bb0da]
[runnervm3jyl0:47563] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fde410a5a55]
[runnervm3jyl0:47563] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fde410a5a6f]
[runnervm3jyl0:47563] [ 8] plumed_master(+0x146dd)[0x557483a716dd]
[runnervm3jyl0:47563] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fde40c2a1ca]
[runnervm3jyl0:47563] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fde40c2a28b]
[runnervm3jyl0:47563] [11] plumed_master(+0x15365)[0x557483a72365]
[runnervm3jyl0:47563] *** End of error message ***
</pre>
{% endraw %}
