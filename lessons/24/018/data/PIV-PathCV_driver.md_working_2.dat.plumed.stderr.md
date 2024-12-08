Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[fv-az1778-96:04085] *** Process received signal ***
[fv-az1778-96:04085] Signal: Aborted (6)
[fv-az1778-96:04085] Signal code:  (-6)
[fv-az1778-96:04085] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6f16c42520]
[fv-az1778-96:04085] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6f16c969fc]
[fv-az1778-96:04085] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6f16c42476]
[fv-az1778-96:04085] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6f16c287f3]
[fv-az1778-96:04085] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6f170a2b9e]
[fv-az1778-96:04085] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6f170ae20c]
[fv-az1778-96:04085] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6f170ae277]
[fv-az1778-96:04085] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6f170ae52b]
[fv-az1778-96:04085] [ 8] plumed(+0x12f48)[0x55a61e02bf48]
[fv-az1778-96:04085] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6f16c29d90]
[fv-az1778-96:04085] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6f16c29e40]
[fv-az1778-96:04085] [11] plumed(+0x131e5)[0x55a61e02c1e5]
[fv-az1778-96:04085] *** End of error message ***
</pre>
{% endraw %}
