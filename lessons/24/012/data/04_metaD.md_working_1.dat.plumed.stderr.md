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
[fv-az1690-151:05726] *** Process received signal ***
[fv-az1690-151:05726] Signal: Aborted (6)
[fv-az1690-151:05726] Signal code:  (-6)
[fv-az1690-151:05726] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6a63045330]
[fv-az1690-151:05726] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6a6309eb2c]
[fv-az1690-151:05726] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6a6304527e]
[fv-az1690-151:05726] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6a630288ff]
[fv-az1690-151:05726] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6a634a5ff5]
[fv-az1690-151:05726] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6a634bb0da]
[fv-az1690-151:05726] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6a634a5a55]
[fv-az1690-151:05726] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6a634a5a6f]
[fv-az1690-151:05726] [ 8] plumed(+0x13209)[0x55e26f4b1209]
[fv-az1690-151:05726] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6a6302a1ca]
[fv-az1690-151:05726] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6a6302a28b]
[fv-az1690-151:05726] [11] plumed(+0x134a5)[0x55e26f4b14a5]
[fv-az1690-151:05726] *** End of error message ***
</pre>
{% endraw %}
