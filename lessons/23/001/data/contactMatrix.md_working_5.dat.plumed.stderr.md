Stderr for source:  contactMatrix.md_working_5.dat   
Download: [zipped raw stdout](contactMatrix.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_5.dat.plumed.stderr.txt.zip) 
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
[fv-az1535-978:69827] *** Process received signal ***
[fv-az1535-978:69827] Signal: Aborted (6)
[fv-az1535-978:69827] Signal code:  (-6)
[fv-az1535-978:69827] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0087242520]
[fv-az1535-978:69827] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f00872969fc]
[fv-az1535-978:69827] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0087242476]
[fv-az1535-978:69827] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f00872287f3]
[fv-az1535-978:69827] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f00876a2b9e]
[fv-az1535-978:69827] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f00876ae20c]
[fv-az1535-978:69827] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f00876ae277]
[fv-az1535-978:69827] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f00876ae52b]
[fv-az1535-978:69827] [ 8] plumed(+0x12f48)[0x56472ac67f48]
[fv-az1535-978:69827] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0087229d90]
[fv-az1535-978:69827] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0087229e40]
[fv-az1535-978:69827] [11] plumed(+0x131e5)[0x56472ac681e5]
[fv-az1535-978:69827] *** End of error message ***
</pre>
{% endraw %}
