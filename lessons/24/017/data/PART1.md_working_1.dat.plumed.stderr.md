Stderr for source:  PART1.md_working_1.dat   
Download: [zipped raw stdout](PART1.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PART1.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: > ow: GROUP NDX_FILE=index.ndx NDX_GROUP=O_Water
Maybe a missing space or a typo?
[fv-az1778-96:03984] *** Process received signal ***
[fv-az1778-96:03984] Signal: Aborted (6)
[fv-az1778-96:03984] Signal code:  (-6)
[fv-az1778-96:03984] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f7802842520]
[fv-az1778-96:03984] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f78028969fc]
[fv-az1778-96:03984] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f7802842476]
[fv-az1778-96:03984] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f78028287f3]
[fv-az1778-96:03984] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f7802ca2b9e]
[fv-az1778-96:03984] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f7802cae20c]
[fv-az1778-96:03984] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f7802cae277]
[fv-az1778-96:03984] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f7802cae52b]
[fv-az1778-96:03984] [ 8] plumed(+0x12f48)[0x5613fa615f48]
[fv-az1778-96:03984] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f7802829d90]
[fv-az1778-96:03984] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f7802829e40]
[fv-az1778-96:03984] [11] plumed(+0x131e5)[0x5613fa6161e5]
[fv-az1778-96:03984] *** End of error message ***
</pre>
{% endraw %}
