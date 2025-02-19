Stderr for source:  GAT_SAFE_README.md_working_2.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYFUNCTION LABEL=fPY IMPORT=pycvfunc CALCULATE=plumedCalculate ARG=d1,d2
Maybe a missing space or a typo?
[fv-az1690-151:05397] *** Process received signal ***
[fv-az1690-151:05397] Signal: Aborted (6)
[fv-az1690-151:05397] Signal code:  (-6)
[fv-az1690-151:05397] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb833645330]
[fv-az1690-151:05397] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb83369eb2c]
[fv-az1690-151:05397] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb83364527e]
[fv-az1690-151:05397] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb8336288ff]
[fv-az1690-151:05397] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb833aa5ff5]
[fv-az1690-151:05397] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb833abb0da]
[fv-az1690-151:05397] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb833aa5a55]
[fv-az1690-151:05397] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb833aa5a6f]
[fv-az1690-151:05397] [ 8] plumed(+0x13209)[0x562c8fd82209]
[fv-az1690-151:05397] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb83362a1ca]
[fv-az1690-151:05397] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb83362a28b]
[fv-az1690-151:05397] [11] plumed(+0x134a5)[0x562c8fd824a5]
[fv-az1690-151:05397] *** End of error message ***
</pre>
{% endraw %}
