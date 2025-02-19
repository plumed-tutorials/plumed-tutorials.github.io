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
[fv-az1690-151:05352] *** Process received signal ***
[fv-az1690-151:05352] Signal: Aborted (6)
[fv-az1690-151:05352] Signal code:  (-6)
[fv-az1690-151:05352] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5715245330]
[fv-az1690-151:05352] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f571529eb2c]
[fv-az1690-151:05352] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f571524527e]
[fv-az1690-151:05352] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f57152288ff]
[fv-az1690-151:05352] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f57156a5ff5]
[fv-az1690-151:05352] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f57156bb0da]
[fv-az1690-151:05352] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f57156a5a55]
[fv-az1690-151:05352] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f57156a5a6f]
[fv-az1690-151:05352] [ 8] plumed(+0x13209)[0x55f9bb7b3209]
[fv-az1690-151:05352] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f571522a1ca]
[fv-az1690-151:05352] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f571522a28b]
[fv-az1690-151:05352] [11] plumed(+0x134a5)[0x55f9bb7b34a5]
[fv-az1690-151:05352] *** End of error message ***
</pre>
{% endraw %}
