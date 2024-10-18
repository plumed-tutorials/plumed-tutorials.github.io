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
[fv-az1535-978:71097] *** Process received signal ***
[fv-az1535-978:71097] Signal: Aborted (6)
[fv-az1535-978:71097] Signal code:  (-6)
[fv-az1535-978:71097] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7fc3f0442520]
[fv-az1535-978:71097] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7fc3f04969fc]
[fv-az1535-978:71097] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7fc3f0442476]
[fv-az1535-978:71097] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7fc3f04287f3]
[fv-az1535-978:71097] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7fc3f08a2b9e]
[fv-az1535-978:71097] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7fc3f08ae20c]
[fv-az1535-978:71097] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7fc3f08ae277]
[fv-az1535-978:71097] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7fc3f08ae52b]
[fv-az1535-978:71097] [ 8] plumed(+0x12f48)[0x5653a7893f48]
[fv-az1535-978:71097] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7fc3f0429d90]
[fv-az1535-978:71097] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7fc3f0429e40]
[fv-az1535-978:71097] [11] plumed(+0x131e5)[0x5653a78941e5]
[fv-az1535-978:71097] *** End of error message ***
</pre>
{% endraw %}
