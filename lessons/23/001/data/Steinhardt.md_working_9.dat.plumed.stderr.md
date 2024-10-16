Stderr for source:  Steinhardt.md_working_9.dat   
Download: [zipped raw stdout](Steinhardt.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIES=1-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0 VMEAN
Maybe a missing space or a typo?
[fv-az1426-552:05167] *** Process received signal ***
[fv-az1426-552:05167] Signal: Aborted (6)
[fv-az1426-552:05167] Signal code:  (-6)
[fv-az1426-552:05167] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff388642520]
[fv-az1426-552:05167] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff3886969fc]
[fv-az1426-552:05167] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff388642476]
[fv-az1426-552:05167] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff3886287f3]
[fv-az1426-552:05167] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff388aa2b9e]
[fv-az1426-552:05167] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff388aae20c]
[fv-az1426-552:05167] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff388aae277]
[fv-az1426-552:05167] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff388aae52b]
[fv-az1426-552:05167] [ 8] plumed(+0x12f48)[0x564ee5666f48]
[fv-az1426-552:05167] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff388629d90]
[fv-az1426-552:05167] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff388629e40]
[fv-az1426-552:05167] [11] plumed(+0x131e5)[0x564ee56671e5]
[fv-az1426-552:05167] *** End of error message ***
</pre>
{% endraw %}
