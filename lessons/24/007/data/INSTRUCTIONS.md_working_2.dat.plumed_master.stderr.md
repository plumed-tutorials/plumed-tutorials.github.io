Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az1690-151:06201] *** Process received signal ***
[fv-az1690-151:06201] Signal: Aborted (6)
[fv-az1690-151:06201] Signal code:  (-6)
[fv-az1690-151:06201] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1c3c645330]
[fv-az1690-151:06201] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1c3c69eb2c]
[fv-az1690-151:06201] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1c3c64527e]
[fv-az1690-151:06201] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1c3c6288ff]
[fv-az1690-151:06201] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1c3caa5ff5]
[fv-az1690-151:06201] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1c3cabb0da]
[fv-az1690-151:06201] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1c3caa5a55]
[fv-az1690-151:06201] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1c3caa5a6f]
[fv-az1690-151:06201] [ 8] plumed_master(+0x146dd)[0x563d16d386dd]
[fv-az1690-151:06201] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1c3c62a1ca]
[fv-az1690-151:06201] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1c3c62a28b]
[fv-az1690-151:06201] [11] plumed_master(+0x15365)[0x563d16d39365]
[fv-az1690-151:06201] *** End of error message ***
</pre>
{% endraw %}
