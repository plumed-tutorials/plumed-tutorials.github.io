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
[fv-az1315-757:08248] *** Process received signal ***
[fv-az1315-757:08248] Signal: Aborted (6)
[fv-az1315-757:08248] Signal code:  (-6)
[fv-az1315-757:08248] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f433b845330]
[fv-az1315-757:08248] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f433b89eb2c]
[fv-az1315-757:08248] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f433b84527e]
[fv-az1315-757:08248] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f433b8288ff]
[fv-az1315-757:08248] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f433bca5ff5]
[fv-az1315-757:08248] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f433bcbb0da]
[fv-az1315-757:08248] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f433bca5a55]
[fv-az1315-757:08248] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f433bca5a6f]
[fv-az1315-757:08248] [ 8] plumed_master(+0x146dd)[0x5561f99416dd]
[fv-az1315-757:08248] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f433b82a1ca]
[fv-az1315-757:08248] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f433b82a28b]
[fv-az1315-757:08248] [11] plumed_master(+0x15365)[0x5561f9942365]
[fv-az1315-757:08248] *** End of error message ***
</pre>
{% endraw %}
