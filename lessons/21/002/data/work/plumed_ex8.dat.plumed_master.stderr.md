Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:372) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @37 : keyword ARG is compulsory for this action
[runnervm3jyl0:81491] *** Process received signal ***
[runnervm3jyl0:81491] Signal: Aborted (6)
[runnervm3jyl0:81491] Signal code:  (-6)
[runnervm3jyl0:81491] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7faf70c45330]
[runnervm3jyl0:81491] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7faf70c9eb2c]
[runnervm3jyl0:81491] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7faf70c4527e]
[runnervm3jyl0:81491] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7faf70c288ff]
[runnervm3jyl0:81491] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7faf710a5ff5]
[runnervm3jyl0:81491] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7faf710bb0da]
[runnervm3jyl0:81491] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7faf710a5a55]
[runnervm3jyl0:81491] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7faf710a5a6f]
[runnervm3jyl0:81491] [ 8] plumed_master(+0x146dd)[0x55604dd506dd]
[runnervm3jyl0:81491] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7faf70c2a1ca]
[runnervm3jyl0:81491] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7faf70c2a28b]
[runnervm3jyl0:81491] [11] plumed_master(+0x15365)[0x55604dd51365]
[runnervm3jyl0:81491] *** End of error message ***
</pre>
{% endraw %}
