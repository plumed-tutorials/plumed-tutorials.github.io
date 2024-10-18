Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MORE_THAN LABEL=fcub ARG=cub SWITCH=SMAP R_0=0.45 D_0=0.0 A=8 B=8
Maybe a missing space or a typo?
[fv-az1530-405:70345] *** Process received signal ***
[fv-az1530-405:70345] Signal: Aborted (6)
[fv-az1530-405:70345] Signal code:  (-6)
[fv-az1530-405:70345] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f8df1e42520]
[fv-az1530-405:70345] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f8df1e969fc]
[fv-az1530-405:70345] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f8df1e42476]
[fv-az1530-405:70345] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f8df1e287f3]
[fv-az1530-405:70345] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f8df22a2b9e]
[fv-az1530-405:70345] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f8df22ae20c]
[fv-az1530-405:70345] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f8df22ae277]
[fv-az1530-405:70345] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f8df22ae52b]
[fv-az1530-405:70345] [ 8] plumed(+0x12f48)[0x55b9b2d77f48]
[fv-az1530-405:70345] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f8df1e29d90]
[fv-az1530-405:70345] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f8df1e29e40]
[fv-az1530-405:70345] [11] plumed(+0x131e5)[0x55b9b2d781e5]
[fv-az1530-405:70345] *** End of error message ***
</pre>
{% endraw %}
