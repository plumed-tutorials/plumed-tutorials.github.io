Stderr for source:  Steinhardt.md_working_4.dat   
Download: [zipped raw stdout](Steinhardt.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: Q1 LABEL=q1 SPECIESA=1 SPECIESB=2-100 SWITCH=RATIONAL D_0=2.0 R_0=1.0
Maybe a missing space or a typo?
[fv-az1535-978:70213] *** Process received signal ***
[fv-az1535-978:70213] Signal: Aborted (6)
[fv-az1535-978:70213] Signal code:  (-6)
[fv-az1535-978:70213] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f52e2842520]
[fv-az1535-978:70213] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f52e28969fc]
[fv-az1535-978:70213] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f52e2842476]
[fv-az1535-978:70213] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f52e28287f3]
[fv-az1535-978:70213] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f52e2ca2b9e]
[fv-az1535-978:70213] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f52e2cae20c]
[fv-az1535-978:70213] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f52e2cae277]
[fv-az1535-978:70213] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f52e2cae52b]
[fv-az1535-978:70213] [ 8] plumed(+0x12f48)[0x556a0e8e7f48]
[fv-az1535-978:70213] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f52e2829d90]
[fv-az1535-978:70213] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f52e2829e40]
[fv-az1535-978:70213] [11] plumed(+0x131e5)[0x556a0e8e81e5]
[fv-az1535-978:70213] *** End of error message ***
</pre>
{% endraw %}
