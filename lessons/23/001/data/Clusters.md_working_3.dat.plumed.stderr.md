Stderr for source:  Clusters.md_working_3.dat   
Download: [zipped raw stdout](Clusters.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1426-552:06418] *** Process received signal ***
[fv-az1426-552:06418] Signal: Aborted (6)
[fv-az1426-552:06418] Signal code:  (-6)
[fv-az1426-552:06418] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fdd33e42520]
[fv-az1426-552:06418] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fdd33e969fc]
[fv-az1426-552:06418] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fdd33e42476]
[fv-az1426-552:06418] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fdd33e287f3]
[fv-az1426-552:06418] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fdd342a2b9e]
[fv-az1426-552:06418] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fdd342ae20c]
[fv-az1426-552:06418] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fdd342ae277]
[fv-az1426-552:06418] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fdd342ae52b]
[fv-az1426-552:06418] [ 8] plumed(+0x12f48)[0x564332bf6f48]
[fv-az1426-552:06418] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fdd33e29d90]
[fv-az1426-552:06418] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fdd33e29e40]
[fv-az1426-552:06418] [11] plumed(+0x131e5)[0x564332bf71e5]
[fv-az1426-552:06418] *** End of error message ***
</pre>
{% endraw %}
