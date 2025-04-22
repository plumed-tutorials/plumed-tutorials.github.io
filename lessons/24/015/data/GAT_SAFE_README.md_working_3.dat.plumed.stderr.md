Stderr for source:  GAT_SAFE_README.md_working_3.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PYCVINTERFACE LABEL=cv1 ATOMS=@mdatoms IMPORT=pycvPersistentData CALCULATE=pydist INIT=pyinit
Maybe a missing space or a typo?
[fv-az1279-640:05422] *** Process received signal ***
[fv-az1279-640:05422] Signal: Aborted (6)
[fv-az1279-640:05422] Signal code:  (-6)
[fv-az1279-640:05422] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f421a445330]
[fv-az1279-640:05422] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f421a49eb2c]
[fv-az1279-640:05422] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f421a44527e]
[fv-az1279-640:05422] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f421a4288ff]
[fv-az1279-640:05422] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f421a8a5ff5]
[fv-az1279-640:05422] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f421a8bb0da]
[fv-az1279-640:05422] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f421a8a5a55]
[fv-az1279-640:05422] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f421a8a5a6f]
[fv-az1279-640:05422] [ 8] plumed(+0x13209)[0x5638ee9af209]
[fv-az1279-640:05422] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f421a42a1ca]
[fv-az1279-640:05422] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f421a42a28b]
[fv-az1279-640:05422] [11] plumed(+0x134a5)[0x5638ee9af4a5]
[fv-az1279-640:05422] *** End of error message ***
</pre>
{% endraw %}
