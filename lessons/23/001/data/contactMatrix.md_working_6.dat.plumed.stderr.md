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
[fv-az1535-978:69865] *** Process received signal ***
[fv-az1535-978:69865] Signal: Aborted (6)
[fv-az1535-978:69865] Signal code:  (-6)
[fv-az1535-978:69865] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8053e42520]
[fv-az1535-978:69865] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8053e969fc]
[fv-az1535-978:69865] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8053e42476]
[fv-az1535-978:69865] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8053e287f3]
[fv-az1535-978:69865] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f80542a2b9e]
[fv-az1535-978:69865] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f80542ae20c]
[fv-az1535-978:69865] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f80542ae277]
[fv-az1535-978:69865] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f80542ae52b]
[fv-az1535-978:69865] [ 8] plumed(+0x12f48)[0x5615bbff6f48]
[fv-az1535-978:69865] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8053e29d90]
[fv-az1535-978:69865] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8053e29e40]
[fv-az1535-978:69865] [11] plumed(+0x131e5)[0x5615bbff71e5]
[fv-az1535-978:69865] *** End of error message ***
</pre>
{% endraw %}
