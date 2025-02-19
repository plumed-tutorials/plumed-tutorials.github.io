Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[fv-az1755-505:08149] *** Process received signal ***
[fv-az1755-505:08149] Signal: Aborted (6)
[fv-az1755-505:08149] Signal code:  (-6)
[fv-az1755-505:08149] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd809a45330]
[fv-az1755-505:08149] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd809a9eb2c]
[fv-az1755-505:08149] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd809a4527e]
[fv-az1755-505:08149] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd809a288ff]
[fv-az1755-505:08149] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd809ea5ff5]
[fv-az1755-505:08149] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd809ebb0da]
[fv-az1755-505:08149] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd809ea5a55]
[fv-az1755-505:08149] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd809ea5a6f]
[fv-az1755-505:08149] [ 8] plumed_master(+0x146dd)[0x55a0257a86dd]
[fv-az1755-505:08149] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd809a2a1ca]
[fv-az1755-505:08149] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd809a2a28b]
[fv-az1755-505:08149] [11] plumed_master(+0x15365)[0x55a0257a9365]
[fv-az1755-505:08149] *** End of error message ***
</pre>
{% endraw %}
