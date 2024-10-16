Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[fv-az1426-552:05982] *** Process received signal ***
[fv-az1426-552:05982] Signal: Aborted (6)
[fv-az1426-552:05982] Signal code:  (-6)
[fv-az1426-552:05982] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f6a94442520]
[fv-az1426-552:05982] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f6a944969fc]
[fv-az1426-552:05982] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f6a94442476]
[fv-az1426-552:05982] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f6a944287f3]
[fv-az1426-552:05982] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f6a948a2b9e]
[fv-az1426-552:05982] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f6a948ae20c]
[fv-az1426-552:05982] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f6a948ae277]
[fv-az1426-552:05982] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f6a948ae52b]
[fv-az1426-552:05982] [ 8] plumed(+0x12f48)[0x55b77e132f48]
[fv-az1426-552:05982] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f6a94429d90]
[fv-az1426-552:05982] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f6a94429e40]
[fv-az1426-552:05982] [11] plumed(+0x131e5)[0x55b77e1331e5]
[fv-az1426-552:05982] *** End of error message ***
</pre>
{% endraw %}
