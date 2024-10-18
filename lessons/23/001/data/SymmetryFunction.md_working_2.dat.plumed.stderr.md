Stderr for source:  SymmetryFunction.md_working_2.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1535-978:70860] *** Process received signal ***
[fv-az1535-978:70860] Signal: Aborted (6)
[fv-az1535-978:70860] Signal code:  (-6)
[fv-az1535-978:70860] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1be4642520]
[fv-az1535-978:70860] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f1be46969fc]
[fv-az1535-978:70860] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1be4642476]
[fv-az1535-978:70860] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f1be46287f3]
[fv-az1535-978:70860] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f1be4aa2b9e]
[fv-az1535-978:70860] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f1be4aae20c]
[fv-az1535-978:70860] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f1be4aae277]
[fv-az1535-978:70860] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f1be4aae52b]
[fv-az1535-978:70860] [ 8] plumed(+0x12f48)[0x562f2ed01f48]
[fv-az1535-978:70860] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1be4629d90]
[fv-az1535-978:70860] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1be4629e40]
[fv-az1535-978:70860] [11] plumed(+0x131e5)[0x562f2ed021e5]
[fv-az1535-978:70860] *** End of error message ***
</pre>
{% endraw %}
