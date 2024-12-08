Stderr for source:  ./solutions/walker-0/plumed_reweight.dat   
Download: [zipped raw stdout](plumed_reweight.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @33 : keyword ARG is compulsory for this action
[fv-az1778-96:04689] *** Process received signal ***
[fv-az1778-96:04689] Signal: Aborted (6)
[fv-az1778-96:04689] Signal code:  (-6)
[fv-az1778-96:04689] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f4295a42520]
[fv-az1778-96:04689] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f4295a969fc]
[fv-az1778-96:04689] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f4295a42476]
[fv-az1778-96:04689] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f4295a287f3]
[fv-az1778-96:04689] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f4295ea2b9e]
[fv-az1778-96:04689] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f4295eae20c]
[fv-az1778-96:04689] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f4295eae277]
[fv-az1778-96:04689] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f4295eae52b]
[fv-az1778-96:04689] [ 8] plumed_master(+0x14254)[0x55de89c86254]
[fv-az1778-96:04689] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f4295a29d90]
[fv-az1778-96:04689] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f4295a29e40]
[fv-az1778-96:04689] [11] plumed_master(+0x14eb5)[0x55de89c86eb5]
[fv-az1778-96:04689] *** End of error message ***
</pre>
{% endraw %}
