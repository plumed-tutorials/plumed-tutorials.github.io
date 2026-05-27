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
[runnervm3jyl0:80033] *** Process received signal ***
[runnervm3jyl0:80033] Signal: Aborted (6)
[runnervm3jyl0:80033] Signal code:  (-6)
[runnervm3jyl0:80033] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6bd3e45330]
[runnervm3jyl0:80033] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6bd3e9eb2c]
[runnervm3jyl0:80033] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6bd3e4527e]
[runnervm3jyl0:80033] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6bd3e288ff]
[runnervm3jyl0:80033] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6bd42a5ff5]
[runnervm3jyl0:80033] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6bd42bb0da]
[runnervm3jyl0:80033] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6bd42a5a55]
[runnervm3jyl0:80033] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6bd42a5a6f]
[runnervm3jyl0:80033] [ 8] plumed_master(+0x146dd)[0x55f18f20a6dd]
[runnervm3jyl0:80033] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6bd3e2a1ca]
[runnervm3jyl0:80033] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6bd3e2a28b]
[runnervm3jyl0:80033] [11] plumed_master(+0x15365)[0x55f18f20b365]
[runnervm3jyl0:80033] *** End of error message ***
</pre>
{% endraw %}
