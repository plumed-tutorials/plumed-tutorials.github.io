Stderr for source:  Path.md_working_2.dat   
Download: [zipped raw stdout](Path.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: LOWEST LABEL=p_mindist ARG=p_data
Maybe a missing space or a typo?
[fv-az1020-777:06617] *** Process received signal ***
[fv-az1020-777:06617] Signal: Aborted (6)
[fv-az1020-777:06617] Signal code:  (-6)
[fv-az1020-777:06617] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1a98842520]
[fv-az1020-777:06617] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f1a988969fc]
[fv-az1020-777:06617] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1a98842476]
[fv-az1020-777:06617] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f1a988287f3]
[fv-az1020-777:06617] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f1a98ca2b9e]
[fv-az1020-777:06617] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f1a98cae20c]
[fv-az1020-777:06617] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f1a98cae277]
[fv-az1020-777:06617] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f1a98cae52b]
[fv-az1020-777:06617] [ 8] plumed(+0x12f48)[0x55c03379ef48]
[fv-az1020-777:06617] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1a98829d90]
[fv-az1020-777:06617] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1a98829e40]
[fv-az1020-777:06617] [11] plumed(+0x131e5)[0x55c03379f1e5]
[fv-az1020-777:06617] *** End of error message ***
</pre>
{% endraw %}
