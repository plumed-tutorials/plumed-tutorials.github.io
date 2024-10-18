Stderr for source:  contactMatrix.md_working_4.dat   
Download: [zipped raw stdout](contactMatrix.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1535-978:69789] *** Process received signal ***
[fv-az1535-978:69789] Signal: Aborted (6)
[fv-az1535-978:69789] Signal code:  (-6)
[fv-az1535-978:69789] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fb947242520]
[fv-az1535-978:69789] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fb9472969fc]
[fv-az1535-978:69789] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fb947242476]
[fv-az1535-978:69789] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fb9472287f3]
[fv-az1535-978:69789] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fb9476a2b9e]
[fv-az1535-978:69789] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fb9476ae20c]
[fv-az1535-978:69789] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fb9476ae277]
[fv-az1535-978:69789] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fb9476ae52b]
[fv-az1535-978:69789] [ 8] plumed(+0x12f48)[0x5578aa438f48]
[fv-az1535-978:69789] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fb947229d90]
[fv-az1535-978:69789] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fb947229e40]
[fv-az1535-978:69789] [11] plumed(+0x131e5)[0x5578aa4391e5]
[fv-az1535-978:69789] *** End of error message ***
</pre>
{% endraw %}
