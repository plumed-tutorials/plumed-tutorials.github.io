Stderr for source:  GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cvPY ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
Maybe a missing space or a typo?
[fv-az1778-96:04372] *** Process received signal ***
[fv-az1778-96:04372] Signal: Aborted (6)
[fv-az1778-96:04372] Signal code:  (-6)
[fv-az1778-96:04372] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f5ba0242520]
[fv-az1778-96:04372] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f5ba02969fc]
[fv-az1778-96:04372] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f5ba0242476]
[fv-az1778-96:04372] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f5ba02287f3]
[fv-az1778-96:04372] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f5ba06a2b9e]
[fv-az1778-96:04372] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f5ba06ae20c]
[fv-az1778-96:04372] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f5ba06ae277]
[fv-az1778-96:04372] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f5ba06ae52b]
[fv-az1778-96:04372] [ 8] plumed(+0x12f48)[0x55e4941def48]
[fv-az1778-96:04372] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f5ba0229d90]
[fv-az1778-96:04372] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f5ba0229e40]
[fv-az1778-96:04372] [11] plumed(+0x131e5)[0x55e4941df1e5]
[fv-az1778-96:04372] *** End of error message ***
</pre>
{% endraw %}
