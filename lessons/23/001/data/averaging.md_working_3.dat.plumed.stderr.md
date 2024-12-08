Stderr for source:  averaging.md_working_3.dat   
Download: [zipped raw stdout](averaging.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1
Maybe a missing space or a typo?
[fv-az1020-777:05722] *** Process received signal ***
[fv-az1020-777:05722] Signal: Aborted (6)
[fv-az1020-777:05722] Signal code:  (-6)
[fv-az1020-777:05722] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7ff0f9e42520]
[fv-az1020-777:05722] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7ff0f9e969fc]
[fv-az1020-777:05722] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7ff0f9e42476]
[fv-az1020-777:05722] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7ff0f9e287f3]
[fv-az1020-777:05722] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7ff0fa2a2b9e]
[fv-az1020-777:05722] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7ff0fa2ae20c]
[fv-az1020-777:05722] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7ff0fa2ae277]
[fv-az1020-777:05722] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7ff0fa2ae52b]
[fv-az1020-777:05722] [ 8] plumed(+0x12f48)[0x55fbb9a80f48]
[fv-az1020-777:05722] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7ff0f9e29d90]
[fv-az1020-777:05722] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7ff0f9e29e40]
[fv-az1020-777:05722] [11] plumed(+0x131e5)[0x55fbb9a811e5]
[fv-az1020-777:05722] *** End of error message ***
</pre>
{% endraw %}
