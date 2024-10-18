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
[fv-az1535-978:71142] *** Process received signal ***
[fv-az1535-978:71142] Signal: Aborted (6)
[fv-az1535-978:71142] Signal code:  (-6)
[fv-az1535-978:71142] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f67d8a42520]
[fv-az1535-978:71142] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f67d8a969fc]
[fv-az1535-978:71142] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f67d8a42476]
[fv-az1535-978:71142] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f67d8a287f3]
[fv-az1535-978:71142] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f67d8ea2b9e]
[fv-az1535-978:71142] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f67d8eae20c]
[fv-az1535-978:71142] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f67d8eae277]
[fv-az1535-978:71142] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f67d8eae52b]
[fv-az1535-978:71142] [ 8] plumed(+0x12f48)[0x5602a6003f48]
[fv-az1535-978:71142] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f67d8a29d90]
[fv-az1535-978:71142] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f67d8a29e40]
[fv-az1535-978:71142] [11] plumed(+0x131e5)[0x5602a60041e5]
[fv-az1535-978:71142] *** End of error message ***
</pre>
{% endraw %}
