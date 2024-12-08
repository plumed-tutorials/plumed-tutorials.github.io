Stderr for source:  averaging.md_working_10.dat   
Download: [zipped raw stdout](averaging.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1g ARG=d1
Maybe a missing space or a typo?
[fv-az1020-777:05948] *** Process received signal ***
[fv-az1020-777:05948] Signal: Aborted (6)
[fv-az1020-777:05948] Signal code:  (-6)
[fv-az1020-777:05948] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8c19242520]
[fv-az1020-777:05948] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8c192969fc]
[fv-az1020-777:05948] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8c19242476]
[fv-az1020-777:05948] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8c192287f3]
[fv-az1020-777:05948] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f8c196a2b9e]
[fv-az1020-777:05948] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f8c196ae20c]
[fv-az1020-777:05948] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f8c196ae277]
[fv-az1020-777:05948] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f8c196ae52b]
[fv-az1020-777:05948] [ 8] plumed(+0x12f48)[0x559ce2215f48]
[fv-az1020-777:05948] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8c19229d90]
[fv-az1020-777:05948] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8c19229e40]
[fv-az1020-777:05948] [11] plumed(+0x131e5)[0x559ce22161e5]
[fv-az1020-777:05948] *** End of error message ***
</pre>
{% endraw %}
