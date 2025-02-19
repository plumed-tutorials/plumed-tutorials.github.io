Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[fv-az1690-151:07231] *** Process received signal ***
[fv-az1690-151:07231] Signal: Aborted (6)
[fv-az1690-151:07231] Signal code:  (-6)
[fv-az1690-151:07231] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f64a6a45330]
[fv-az1690-151:07231] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f64a6a9eb2c]
[fv-az1690-151:07231] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f64a6a4527e]
[fv-az1690-151:07231] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f64a6a288ff]
[fv-az1690-151:07231] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f64a6ea5ff5]
[fv-az1690-151:07231] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f64a6ebb0da]
[fv-az1690-151:07231] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f64a6ea5a55]
[fv-az1690-151:07231] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f64a6ea5a6f]
[fv-az1690-151:07231] [ 8] plumed_master(+0x146dd)[0x5628201d46dd]
[fv-az1690-151:07231] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f64a6a2a1ca]
[fv-az1690-151:07231] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f64a6a2a28b]
[fv-az1690-151:07231] [11] plumed_master(+0x15365)[0x5628201d5365]
[fv-az1690-151:07231] *** End of error message ***
</pre>
{% endraw %}
