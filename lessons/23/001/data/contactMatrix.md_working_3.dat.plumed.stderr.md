Stderr for source:  contactMatrix.md_working_3.dat   
Download: [zipped raw stdout](contactMatrix.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1535-978:69753] *** Process received signal ***
[fv-az1535-978:69753] Signal: Aborted (6)
[fv-az1535-978:69753] Signal code:  (-6)
[fv-az1535-978:69753] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f94d4642520]
[fv-az1535-978:69753] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f94d46969fc]
[fv-az1535-978:69753] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f94d4642476]
[fv-az1535-978:69753] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f94d46287f3]
[fv-az1535-978:69753] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f94d4aa2b9e]
[fv-az1535-978:69753] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f94d4aae20c]
[fv-az1535-978:69753] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f94d4aae277]
[fv-az1535-978:69753] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f94d4aae52b]
[fv-az1535-978:69753] [ 8] plumed(+0x12f48)[0x55adbd42ef48]
[fv-az1535-978:69753] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f94d4629d90]
[fv-az1535-978:69753] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f94d4629e40]
[fv-az1535-978:69753] [11] plumed(+0x131e5)[0x55adbd42f1e5]
[fv-az1535-978:69753] *** End of error message ***
</pre>
{% endraw %}
