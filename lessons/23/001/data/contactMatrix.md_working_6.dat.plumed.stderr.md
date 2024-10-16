Stderr for source:  contactMatrix.md_working_6.dat   
Download: [zipped raw stdout](contactMatrix.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones64 SIZE=64
Maybe a missing space or a typo?
[fv-az1426-552:04704] *** Process received signal ***
[fv-az1426-552:04704] Signal: Aborted (6)
[fv-az1426-552:04704] Signal code:  (-6)
[fv-az1426-552:04704] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f3997442520]
[fv-az1426-552:04704] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f39974969fc]
[fv-az1426-552:04704] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f3997442476]
[fv-az1426-552:04704] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f39974287f3]
[fv-az1426-552:04704] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f39978a2b9e]
[fv-az1426-552:04704] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f39978ae20c]
[fv-az1426-552:04704] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f39978ae277]
[fv-az1426-552:04704] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f39978ae52b]
[fv-az1426-552:04704] [ 8] plumed(+0x12f48)[0x5637f4fb4f48]
[fv-az1426-552:04704] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f3997429d90]
[fv-az1426-552:04704] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f3997429e40]
[fv-az1426-552:04704] [11] plumed(+0x131e5)[0x5637f4fb51e5]
[fv-az1426-552:04704] *** End of error message ***
</pre>
{% endraw %}
