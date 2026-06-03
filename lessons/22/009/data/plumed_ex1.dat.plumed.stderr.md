Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[runnervm3jyl0:47547] *** Process received signal ***
[runnervm3jyl0:47547] Signal: Aborted (6)
[runnervm3jyl0:47547] Signal code:  (-6)
[runnervm3jyl0:47547] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f578fa45330]
[runnervm3jyl0:47547] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f578fa9eb2c]
[runnervm3jyl0:47547] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f578fa4527e]
[runnervm3jyl0:47547] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f578fa288ff]
[runnervm3jyl0:47547] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f578fea5ff5]
[runnervm3jyl0:47547] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f578febb0da]
[runnervm3jyl0:47547] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f578fea5a55]
[runnervm3jyl0:47547] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f578fea5a6f]
[runnervm3jyl0:47547] [ 8] plumed(+0x13209)[0x55dd6d3d5209]
[runnervm3jyl0:47547] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f578fa2a1ca]
[runnervm3jyl0:47547] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f578fa2a28b]
[runnervm3jyl0:47547] [11] plumed(+0x134a5)[0x55dd6d3d54a5]
[runnervm3jyl0:47547] *** End of error message ***
</pre>
{% endraw %}
