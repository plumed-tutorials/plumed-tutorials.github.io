Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az1690-151:07014] *** Process received signal ***
[fv-az1690-151:07014] Signal: Aborted (6)
[fv-az1690-151:07014] Signal code:  (-6)
[fv-az1690-151:07014] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f44ce645330]
[fv-az1690-151:07014] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f44ce69eb2c]
[fv-az1690-151:07014] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f44ce64527e]
[fv-az1690-151:07014] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f44ce6288ff]
[fv-az1690-151:07014] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f44ceaa5ff5]
[fv-az1690-151:07014] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f44ceabb0da]
[fv-az1690-151:07014] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f44ceaa5a55]
[fv-az1690-151:07014] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f44ceaa5a6f]
[fv-az1690-151:07014] [ 8] plumed(+0x13209)[0x55d4671b8209]
[fv-az1690-151:07014] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f44ce62a1ca]
[fv-az1690-151:07014] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f44ce62a28b]
[fv-az1690-151:07014] [11] plumed(+0x134a5)[0x55d4671b84a5]
[fv-az1690-151:07014] *** End of error message ***
</pre>
{% endraw %}
