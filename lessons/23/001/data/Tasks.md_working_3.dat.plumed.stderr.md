Stderr for source:  Tasks.md_working_3.dat   
Download: [zipped raw stdout](Tasks.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones SIZE=100
Maybe a missing space or a typo?
[fv-az1426-552:04845] *** Process received signal ***
[fv-az1426-552:04845] Signal: Aborted (6)
[fv-az1426-552:04845] Signal code:  (-6)
[fv-az1426-552:04845] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fc6fa842520]
[fv-az1426-552:04845] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fc6fa8969fc]
[fv-az1426-552:04845] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fc6fa842476]
[fv-az1426-552:04845] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fc6fa8287f3]
[fv-az1426-552:04845] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fc6faca2b9e]
[fv-az1426-552:04845] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fc6facae20c]
[fv-az1426-552:04845] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fc6facae277]
[fv-az1426-552:04845] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fc6facae52b]
[fv-az1426-552:04845] [ 8] plumed(+0x12f48)[0x56200a43ff48]
[fv-az1426-552:04845] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fc6fa829d90]
[fv-az1426-552:04845] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fc6fa829e40]
[fv-az1426-552:04845] [11] plumed(+0x131e5)[0x56200a4401e5]
[fv-az1426-552:04845] *** End of error message ***
</pre>
{% endraw %}
