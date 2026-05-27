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
[runnervm3jyl0:79396] *** Process received signal ***
[runnervm3jyl0:79396] Signal: Aborted (6)
[runnervm3jyl0:79396] Signal code:  (-6)
[runnervm3jyl0:79396] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9cac845330]
[runnervm3jyl0:79396] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9cac89eb2c]
[runnervm3jyl0:79396] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9cac84527e]
[runnervm3jyl0:79396] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9cac8288ff]
[runnervm3jyl0:79396] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9cacca5ff5]
[runnervm3jyl0:79396] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9caccbb0da]
[runnervm3jyl0:79396] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9cacca5a55]
[runnervm3jyl0:79396] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9cacca5a6f]
[runnervm3jyl0:79396] [ 8] plumed(+0x13209)[0x55927916b209]
[runnervm3jyl0:79396] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9cac82a1ca]
[runnervm3jyl0:79396] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9cac82a28b]
[runnervm3jyl0:79396] [11] plumed(+0x134a5)[0x55927916b4a5]
[runnervm3jyl0:79396] *** End of error message ***
</pre>
{% endraw %}
