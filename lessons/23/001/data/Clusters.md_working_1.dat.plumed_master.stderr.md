Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DFSCLUSTERING with label dfs : keyword ARG is compulsory for this action
[fv-az1020-777:06291] *** Process received signal ***
[fv-az1020-777:06291] Signal: Aborted (6)
[fv-az1020-777:06291] Signal code:  (-6)
[fv-az1020-777:06291] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f756c842520]
[fv-az1020-777:06291] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f756c8969fc]
[fv-az1020-777:06291] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f756c842476]
[fv-az1020-777:06291] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f756c8287f3]
[fv-az1020-777:06291] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f756cca2b9e]
[fv-az1020-777:06291] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f756ccae20c]
[fv-az1020-777:06291] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f756ccae277]
[fv-az1020-777:06291] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f756ccae52b]
[fv-az1020-777:06291] [ 8] plumed_master(+0x14254)[0x55e5bac53254]
[fv-az1020-777:06291] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f756c829d90]
[fv-az1020-777:06291] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f756c829e40]
[fv-az1020-777:06291] [11] plumed_master(+0x14eb5)[0x55e5bac53eb5]
[fv-az1020-777:06291] *** End of error message ***
</pre>
{% endraw %}
