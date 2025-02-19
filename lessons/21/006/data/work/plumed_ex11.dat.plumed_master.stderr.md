Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @63 : keyword ARG is compulsory for this action
[fv-az1690-151:06678] *** Process received signal ***
[fv-az1690-151:06678] Signal: Aborted (6)
[fv-az1690-151:06678] Signal code:  (-6)
[fv-az1690-151:06678] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1992a45330]
[fv-az1690-151:06678] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1992a9eb2c]
[fv-az1690-151:06678] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1992a4527e]
[fv-az1690-151:06678] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1992a288ff]
[fv-az1690-151:06678] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1992ea5ff5]
[fv-az1690-151:06678] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1992ebb0da]
[fv-az1690-151:06678] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1992ea5a55]
[fv-az1690-151:06678] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1992ea5a6f]
[fv-az1690-151:06678] [ 8] plumed_master(+0x146dd)[0x55d9ec0496dd]
[fv-az1690-151:06678] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1992a2a1ca]
[fv-az1690-151:06678] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1992a2a28b]
[fv-az1690-151:06678] [11] plumed_master(+0x15365)[0x55d9ec04a365]
[fv-az1690-151:06678] *** End of error message ***
</pre>
{% endraw %}
