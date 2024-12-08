Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[fv-az1778-96:04196] *** Process received signal ***
[fv-az1778-96:04196] Signal: Aborted (6)
[fv-az1778-96:04196] Signal code:  (-6)
[fv-az1778-96:04196] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fed5ae42520]
[fv-az1778-96:04196] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fed5ae969fc]
[fv-az1778-96:04196] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fed5ae42476]
[fv-az1778-96:04196] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fed5ae287f3]
[fv-az1778-96:04196] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fed5b2a2b9e]
[fv-az1778-96:04196] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fed5b2ae20c]
[fv-az1778-96:04196] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fed5b2ae277]
[fv-az1778-96:04196] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fed5b2ae52b]
[fv-az1778-96:04196] [ 8] plumed_master(+0x14254)[0x55ca962f5254]
[fv-az1778-96:04196] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fed5ae29d90]
[fv-az1778-96:04196] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fed5ae29e40]
[fv-az1778-96:04196] [11] plumed_master(+0x14eb5)[0x55ca962f5eb5]
[fv-az1778-96:04196] *** End of error message ***
</pre>
{% endraw %}
