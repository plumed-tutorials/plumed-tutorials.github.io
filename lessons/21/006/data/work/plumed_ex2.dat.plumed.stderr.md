Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action PCA with label pca : action cc has no component named cc (hint! the components in this actions are: )
[fv-az1778-96:05875] *** Process received signal ***
[fv-az1778-96:05875] Signal: Aborted (6)
[fv-az1778-96:05875] Signal code:  (-6)
[fv-az1778-96:05875] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7eff52e42520]
[fv-az1778-96:05875] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7eff52e969fc]
[fv-az1778-96:05875] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7eff52e42476]
[fv-az1778-96:05875] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7eff52e287f3]
[fv-az1778-96:05875] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7eff532a2b9e]
[fv-az1778-96:05875] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7eff532ae20c]
[fv-az1778-96:05875] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7eff532ae277]
[fv-az1778-96:05875] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7eff532ae52b]
[fv-az1778-96:05875] [ 8] plumed(+0x12f48)[0x55bfe47e6f48]
[fv-az1778-96:05875] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7eff52e29d90]
[fv-az1778-96:05875] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7eff52e29e40]
[fv-az1778-96:05875] [11] plumed(+0x131e5)[0x55bfe47e71e5]
[fv-az1778-96:05875] *** End of error message ***
</pre>
{% endraw %}
