Stderr for source:  tutorial/GAT_SAFE_README.md_working_1.dat   
Download: [zipped raw stdout](GAT_SAFE_README.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](GAT_SAFE_README.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: BAIES LABEL=baies ATOMS=batoms DATA_FILE=3-bAIes-setup/logn.out PRIOR=JEFFREYS TEMP=2.478541306
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:34562] *** Process received signal ***
[pkrvmbietmlfzoi:34562] Signal: Aborted (6)
[pkrvmbietmlfzoi:34562] Signal code:  (-6)
[pkrvmbietmlfzoi:34562] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f97f9a45330]
[pkrvmbietmlfzoi:34562] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f97f9a9eb2c]
[pkrvmbietmlfzoi:34562] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f97f9a4527e]
[pkrvmbietmlfzoi:34562] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f97f9a288ff]
[pkrvmbietmlfzoi:34562] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f97f9ea5ff5]
[pkrvmbietmlfzoi:34562] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f97f9ebb0da]
[pkrvmbietmlfzoi:34562] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f97f9ea5a55]
[pkrvmbietmlfzoi:34562] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f97f9ea5a6f]
[pkrvmbietmlfzoi:34562] [ 8] plumed(+0x13209)[0x5630fcca9209]
[pkrvmbietmlfzoi:34562] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f97f9a2a1ca]
[pkrvmbietmlfzoi:34562] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f97f9a2a28b]
[pkrvmbietmlfzoi:34562] [11] plumed(+0x134a5)[0x5630fcca94a5]
[pkrvmbietmlfzoi:34562] *** End of error message ***
</pre>
{% endraw %}
