Stderr for source:  plumed_TDP-43.dat   
Download: [zipped raw stdout](plumed_TDP-43.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_TDP-43.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action METAINFERENCE with label af_mi_rest_domains : REWEIGHT can only be used in parallel with 2 or more replicas
[fv-az1778-96:04272] *** Process received signal ***
[fv-az1778-96:04272] Signal: Aborted (6)
[fv-az1778-96:04272] Signal code:  (-6)
[fv-az1778-96:04272] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f01de242520]
[fv-az1778-96:04272] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f01de2969fc]
[fv-az1778-96:04272] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f01de242476]
[fv-az1778-96:04272] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f01de2287f3]
[fv-az1778-96:04272] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f01de6a2b9e]
[fv-az1778-96:04272] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f01de6ae20c]
[fv-az1778-96:04272] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f01de6ae277]
[fv-az1778-96:04272] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f01de6ae52b]
[fv-az1778-96:04272] [ 8] plumed(+0x12f48)[0x56202b83df48]
[fv-az1778-96:04272] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f01de229d90]
[fv-az1778-96:04272] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f01de229e40]
[fv-az1778-96:04272] [11] plumed(+0x131e5)[0x56202b83e1e5]
[fv-az1778-96:04272] *** End of error message ***
</pre>
{% endraw %}
