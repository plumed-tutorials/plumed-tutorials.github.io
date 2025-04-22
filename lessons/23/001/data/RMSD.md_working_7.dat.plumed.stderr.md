Stderr for source:  RMSD.md_working_7.dat   
Download: [zipped raw stdout](RMSD.md_working_7.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_7.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: PDB2CONSTANT LABEL=rmsd_ref REFERENCE=reference.pdb
Maybe a missing space or a typo?
[fv-az1315-757:08518] *** Process received signal ***
[fv-az1315-757:08518] Signal: Aborted (6)
[fv-az1315-757:08518] Signal code:  (-6)
[fv-az1315-757:08518] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc919245330]
[fv-az1315-757:08518] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc91929eb2c]
[fv-az1315-757:08518] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc91924527e]
[fv-az1315-757:08518] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc9192288ff]
[fv-az1315-757:08518] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc9196a5ff5]
[fv-az1315-757:08518] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc9196bb0da]
[fv-az1315-757:08518] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc9196a5a55]
[fv-az1315-757:08518] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc9196a5a6f]
[fv-az1315-757:08518] [ 8] plumed(+0x13209)[0x5606a6202209]
[fv-az1315-757:08518] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc91922a1ca]
[fv-az1315-757:08518] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc91922a28b]
[fv-az1315-757:08518] [11] plumed(+0x134a5)[0x5606a62024a5]
[fv-az1315-757:08518] *** End of error message ***
</pre>
{% endraw %}
