Stderr for source:  histograms.md_working_1.dat   
Download: [zipped raw stdout](histograms.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:240) void PLMD::Action::error(const string&) const
ERROR in input to action DUMPGRID with label @2 : keyword GRID is compulsory for this action
[fv-az1426-552:06063] *** Process received signal ***
[fv-az1426-552:06063] Signal: Aborted (6)
[fv-az1426-552:06063] Signal code:  (-6)
[fv-az1426-552:06063] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f90f4a42520]
[fv-az1426-552:06063] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f90f4a969fc]
[fv-az1426-552:06063] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f90f4a42476]
[fv-az1426-552:06063] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f90f4a287f3]
[fv-az1426-552:06063] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f90f4ea2b9e]
[fv-az1426-552:06063] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f90f4eae20c]
[fv-az1426-552:06063] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f90f4eae277]
[fv-az1426-552:06063] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f90f4eae52b]
[fv-az1426-552:06063] [ 8] plumed(+0x12f48)[0x557351403f48]
[fv-az1426-552:06063] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f90f4a29d90]
[fv-az1426-552:06063] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f90f4a29e40]
[fv-az1426-552:06063] [11] plumed(+0x131e5)[0x5573514041e5]
[fv-az1426-552:06063] *** End of error message ***
</pre>
{% endraw %}
