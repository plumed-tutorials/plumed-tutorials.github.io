Stderr for source:  GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cvPY ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
Maybe a missing space or a typo?
[fv-az1279-640:05332] *** Process received signal ***
[fv-az1279-640:05332] Signal: Aborted (6)
[fv-az1279-640:05332] Signal code:  (-6)
[fv-az1279-640:05332] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2fc3845330]
[fv-az1279-640:05332] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2fc389eb2c]
[fv-az1279-640:05332] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2fc384527e]
[fv-az1279-640:05332] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2fc38288ff]
[fv-az1279-640:05332] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2fc3ca5ff5]
[fv-az1279-640:05332] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2fc3cbb0da]
[fv-az1279-640:05332] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2fc3ca5a55]
[fv-az1279-640:05332] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2fc3ca5a6f]
[fv-az1279-640:05332] [ 8] plumed(+0x13209)[0x55ab46772209]
[fv-az1279-640:05332] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2fc382a1ca]
[fv-az1279-640:05332] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2fc382a28b]
[fv-az1279-640:05332] [11] plumed(+0x134a5)[0x55ab467724a5]
[fv-az1279-640:05332] *** End of error message ***
</pre>
{% endraw %}
