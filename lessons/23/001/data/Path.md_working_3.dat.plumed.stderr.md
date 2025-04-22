Stderr for source:  Path.md_working_3.dat   
Download: [zipped raw stdout](Path.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GPATH LABEL=pp ARG=t1,t2 REFERENCE=epath.pdb
Maybe a missing space or a typo?
[fv-az1315-757:08601] *** Process received signal ***
[fv-az1315-757:08601] Signal: Aborted (6)
[fv-az1315-757:08601] Signal code:  (-6)
[fv-az1315-757:08601] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcee2a45330]
[fv-az1315-757:08601] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcee2a9eb2c]
[fv-az1315-757:08601] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcee2a4527e]
[fv-az1315-757:08601] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcee2a288ff]
[fv-az1315-757:08601] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcee2ea5ff5]
[fv-az1315-757:08601] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcee2ebb0da]
[fv-az1315-757:08601] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcee2ea5a55]
[fv-az1315-757:08601] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcee2ea5a6f]
[fv-az1315-757:08601] [ 8] plumed(+0x13209)[0x55a1c455d209]
[fv-az1315-757:08601] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcee2a2a1ca]
[fv-az1315-757:08601] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcee2a2a28b]
[fv-az1315-757:08601] [11] plumed(+0x134a5)[0x55a1c455d4a5]
[fv-az1315-757:08601] *** End of error message ***
</pre>
{% endraw %}
