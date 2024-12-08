Stderr for source:  GAT_SAFE_README.md_working_2.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYFUNCTION LABEL=fPY IMPORT=pycvfunc CALCULATE=plumedCalculate ARG=d1,d2
Maybe a missing space or a typo?
[fv-az1778-96:04395] *** Process received signal ***
[fv-az1778-96:04395] Signal: Aborted (6)
[fv-az1778-96:04395] Signal code:  (-6)
[fv-az1778-96:04395] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f0034e42520]
[fv-az1778-96:04395] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f0034e969fc]
[fv-az1778-96:04395] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f0034e42476]
[fv-az1778-96:04395] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f0034e287f3]
[fv-az1778-96:04395] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f00352a2b9e]
[fv-az1778-96:04395] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f00352ae20c]
[fv-az1778-96:04395] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f00352ae277]
[fv-az1778-96:04395] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f00352ae52b]
[fv-az1778-96:04395] [ 8] plumed(+0x12f48)[0x562f5cc7df48]
[fv-az1778-96:04395] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f0034e29d90]
[fv-az1778-96:04395] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f0034e29e40]
[fv-az1778-96:04395] [11] plumed(+0x131e5)[0x562f5cc7e1e5]
[fv-az1778-96:04395] *** End of error message ***
</pre>
{% endraw %}
