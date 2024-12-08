Stderr for source:  ./solutions/walker-0/plumed.dat   
Download: [zipped raw stdout](plumed.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:309) void PLMD::Action::error(const string&) const
ERROR in input to action HBOND_MATRIX with label hbmat1 : cannot understand the following words from the input line : SUM
[fv-az1778-96:04658] *** Process received signal ***
[fv-az1778-96:04658] Signal: Aborted (6)
[fv-az1778-96:04658] Signal code:  (-6)
[fv-az1778-96:04658] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f784fa42520]
[fv-az1778-96:04658] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f784fa969fc]
[fv-az1778-96:04658] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f784fa42476]
[fv-az1778-96:04658] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f784fa287f3]
[fv-az1778-96:04658] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f784fea2b9e]
[fv-az1778-96:04658] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f784feae20c]
[fv-az1778-96:04658] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f784feae277]
[fv-az1778-96:04658] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f784feae52b]
[fv-az1778-96:04658] [ 8] plumed_master(+0x14254)[0x5609c005d254]
[fv-az1778-96:04658] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f784fa29d90]
[fv-az1778-96:04658] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f784fa29e40]
[fv-az1778-96:04658] [11] plumed_master(+0x14eb5)[0x5609c005deb5]
[fv-az1778-96:04658] *** End of error message ***
</pre>
{% endraw %}
