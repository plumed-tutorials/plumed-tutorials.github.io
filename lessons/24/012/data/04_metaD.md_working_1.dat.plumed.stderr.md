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
[pkrvmbietmlfzoi:34849] *** Process received signal ***
[pkrvmbietmlfzoi:34849] Signal: Aborted (6)
[pkrvmbietmlfzoi:34849] Signal code:  (-6)
[pkrvmbietmlfzoi:34849] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbd1c445330]
[pkrvmbietmlfzoi:34849] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbd1c49eb2c]
[pkrvmbietmlfzoi:34849] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbd1c44527e]
[pkrvmbietmlfzoi:34849] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbd1c4288ff]
[pkrvmbietmlfzoi:34849] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbd1c8a5ff5]
[pkrvmbietmlfzoi:34849] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbd1c8bb0da]
[pkrvmbietmlfzoi:34849] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbd1c8a5a55]
[pkrvmbietmlfzoi:34849] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbd1c8a5a6f]
[pkrvmbietmlfzoi:34849] [ 8] plumed(+0x13209)[0x556264e3e209]
[pkrvmbietmlfzoi:34849] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbd1c42a1ca]
[pkrvmbietmlfzoi:34849] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbd1c42a28b]
[pkrvmbietmlfzoi:34849] [11] plumed(+0x134a5)[0x556264e3e4a5]
[pkrvmbietmlfzoi:34849] *** End of error message ***
</pre>
{% endraw %}
