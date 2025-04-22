Stderr for source:  04_metaD.md_working_1.dat   
Download: [zipped raw stdout](04_metaD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](04_metaD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: [TORSION](HTTPS://WWW.PLUMED.ORG/DOC-MASTER/USER-DOC/HTML/_T_O_R_S_I_O_N.HTML) LABEL=t1 ATOMS=1,6,4,5
Maybe a missing space or a typo?
[fv-az2211-783:05700] *** Process received signal ***
[fv-az2211-783:05700] Signal: Aborted (6)
[fv-az2211-783:05700] Signal code:  (-6)
[fv-az2211-783:05700] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdb26645330]
[fv-az2211-783:05700] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdb2669eb2c]
[fv-az2211-783:05700] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdb2664527e]
[fv-az2211-783:05700] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdb266288ff]
[fv-az2211-783:05700] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdb26aa5ff5]
[fv-az2211-783:05700] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdb26abb0da]
[fv-az2211-783:05700] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdb26aa5a55]
[fv-az2211-783:05700] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdb26aa5a6f]
[fv-az2211-783:05700] [ 8] plumed(+0x13209)[0x55baca082209]
[fv-az2211-783:05700] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdb2662a1ca]
[fv-az2211-783:05700] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdb2662a28b]
[fv-az2211-783:05700] [11] plumed(+0x134a5)[0x55baca0824a5]
[fv-az2211-783:05700] *** End of error message ***
</pre>
{% endraw %}
