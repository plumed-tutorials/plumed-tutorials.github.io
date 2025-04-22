Stderr for source:  RMSD.md_working_2.dat   
Download: [zipped raw stdout](RMSD.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DISPLACEMENT LABEL=disp ARG1=d1,d2,d3 ARG2=d1_ref,d2_ref,d3_ref
Maybe a missing space or a typo?
[fv-az1315-757:08373] *** Process received signal ***
[fv-az1315-757:08373] Signal: Aborted (6)
[fv-az1315-757:08373] Signal code:  (-6)
[fv-az1315-757:08373] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa1de445330]
[fv-az1315-757:08373] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa1de49eb2c]
[fv-az1315-757:08373] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa1de44527e]
[fv-az1315-757:08373] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa1de4288ff]
[fv-az1315-757:08373] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa1de8a5ff5]
[fv-az1315-757:08373] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa1de8bb0da]
[fv-az1315-757:08373] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa1de8a5a55]
[fv-az1315-757:08373] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa1de8a5a6f]
[fv-az1315-757:08373] [ 8] plumed(+0x13209)[0x55e06ae52209]
[fv-az1315-757:08373] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa1de42a1ca]
[fv-az1315-757:08373] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa1de42a28b]
[fv-az1315-757:08373] [11] plumed(+0x134a5)[0x55e06ae524a5]
[fv-az1315-757:08373] *** End of error message ***
</pre>
{% endraw %}
