Stderr for source:  work/plumed_ex8.dat   
Download: [zipped raw stdout](plumed_ex8.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex8.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @49 : keyword ARG is compulsory for this action
[fv-az1690-151:07040] *** Process received signal ***
[fv-az1690-151:07040] Signal: Aborted (6)
[fv-az1690-151:07040] Signal code:  (-6)
[fv-az1690-151:07040] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f44b4e45330]
[fv-az1690-151:07040] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f44b4e9eb2c]
[fv-az1690-151:07040] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f44b4e4527e]
[fv-az1690-151:07040] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f44b4e288ff]
[fv-az1690-151:07040] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f44b52a5ff5]
[fv-az1690-151:07040] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f44b52bb0da]
[fv-az1690-151:07040] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f44b52a5a55]
[fv-az1690-151:07040] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f44b52a5a6f]
[fv-az1690-151:07040] [ 8] plumed_master(+0x146dd)[0x557cf78bb6dd]
[fv-az1690-151:07040] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f44b4e2a1ca]
[fv-az1690-151:07040] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f44b4e2a28b]
[fv-az1690-151:07040] [11] plumed_master(+0x15365)[0x557cf78bc365]
[fv-az1690-151:07040] *** End of error message ***
</pre>
{% endraw %}
