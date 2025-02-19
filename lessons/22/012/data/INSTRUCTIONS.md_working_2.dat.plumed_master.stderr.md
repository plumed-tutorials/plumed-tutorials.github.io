Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label @s9 : keyword SIGMA could not be read correctly
[fv-az1690-151:05968] *** Process received signal ***
[fv-az1690-151:05968] Signal: Aborted (6)
[fv-az1690-151:05968] Signal code:  (-6)
[fv-az1690-151:05968] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7cc7e45330]
[fv-az1690-151:05968] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7cc7e9eb2c]
[fv-az1690-151:05968] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7cc7e4527e]
[fv-az1690-151:05968] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7cc7e288ff]
[fv-az1690-151:05968] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7cc82a5ff5]
[fv-az1690-151:05968] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7cc82bb0da]
[fv-az1690-151:05968] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7cc82a5a55]
[fv-az1690-151:05968] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7cc82a5a6f]
[fv-az1690-151:05968] [ 8] plumed_master(+0x146dd)[0x55de906496dd]
[fv-az1690-151:05968] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7cc7e2a1ca]
[fv-az1690-151:05968] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7cc7e2a28b]
[fv-az1690-151:05968] [11] plumed_master(+0x15365)[0x55de9064a365]
[fv-az1690-151:05968] *** End of error message ***
</pre>
{% endraw %}
