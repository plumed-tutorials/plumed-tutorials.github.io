Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @12 : keyword ARG is compulsory for this action
[fv-az1690-151:06957] *** Process received signal ***
[fv-az1690-151:06957] Signal: Aborted (6)
[fv-az1690-151:06957] Signal code:  (-6)
[fv-az1690-151:06957] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9648645330]
[fv-az1690-151:06957] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f964869eb2c]
[fv-az1690-151:06957] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f964864527e]
[fv-az1690-151:06957] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f96486288ff]
[fv-az1690-151:06957] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9648aa5ff5]
[fv-az1690-151:06957] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9648abb0da]
[fv-az1690-151:06957] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9648aa5a55]
[fv-az1690-151:06957] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9648aa5a6f]
[fv-az1690-151:06957] [ 8] plumed_master(+0x146dd)[0x560893ba26dd]
[fv-az1690-151:06957] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f964862a1ca]
[fv-az1690-151:06957] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f964862a28b]
[fv-az1690-151:06957] [11] plumed_master(+0x15365)[0x560893ba3365]
[fv-az1690-151:06957] *** End of error message ***
</pre>
{% endraw %}
