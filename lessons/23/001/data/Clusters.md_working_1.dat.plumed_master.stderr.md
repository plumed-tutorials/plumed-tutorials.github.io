Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:37143] *** Process received signal ***
[pkrvmbietmlfzoi:37143] Signal: Aborted (6)
[pkrvmbietmlfzoi:37143] Signal code:  (-6)
[pkrvmbietmlfzoi:37143] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0b04445330]
[pkrvmbietmlfzoi:37143] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0b0449eb2c]
[pkrvmbietmlfzoi:37143] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0b0444527e]
[pkrvmbietmlfzoi:37143] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0b044288ff]
[pkrvmbietmlfzoi:37143] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0b048a5ff5]
[pkrvmbietmlfzoi:37143] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0b048bb0da]
[pkrvmbietmlfzoi:37143] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0b048a5a55]
[pkrvmbietmlfzoi:37143] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0b048a5a6f]
[pkrvmbietmlfzoi:37143] [ 8] plumed_master(+0x146dd)[0x561396dc16dd]
[pkrvmbietmlfzoi:37143] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0b0442a1ca]
[pkrvmbietmlfzoi:37143] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0b0442a28b]
[pkrvmbietmlfzoi:37143] [11] plumed_master(+0x15365)[0x561396dc2365]
[pkrvmbietmlfzoi:37143] *** End of error message ***
</pre>
{% endraw %}
