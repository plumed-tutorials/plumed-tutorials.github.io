Stderr for source:  averaging.md_working_6.dat   
Download: [zipped raw stdout](averaging.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight
Maybe a missing space or a typo?
[fv-az1020-777:05808] *** Process received signal ***
[fv-az1020-777:05808] Signal: Aborted (6)
[fv-az1020-777:05808] Signal code:  (-6)
[fv-az1020-777:05808] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fe109442520]
[fv-az1020-777:05808] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fe1094969fc]
[fv-az1020-777:05808] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fe109442476]
[fv-az1020-777:05808] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fe1094287f3]
[fv-az1020-777:05808] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fe1098a2b9e]
[fv-az1020-777:05808] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fe1098ae20c]
[fv-az1020-777:05808] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fe1098ae277]
[fv-az1020-777:05808] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fe1098ae52b]
[fv-az1020-777:05808] [ 8] plumed(+0x12f48)[0x55ece1242f48]
[fv-az1020-777:05808] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fe109429d90]
[fv-az1020-777:05808] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fe109429e40]
[fv-az1020-777:05808] [11] plumed(+0x131e5)[0x55ece12431e5]
[fv-az1020-777:05808] *** End of error message ***
</pre>
{% endraw %}