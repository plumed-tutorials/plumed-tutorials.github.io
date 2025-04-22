Stderr for source:  PIV-PathCV_meta.md_working_4.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GMX grompp -f md.mdp -c Liq.pdb -p TIP4P.top -o meta.tpr
Maybe a missing space or a typo?
[fv-az2211-783:05790] *** Process received signal ***
[fv-az2211-783:05790] Signal: Aborted (6)
[fv-az2211-783:05790] Signal code:  (-6)
[fv-az2211-783:05790] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcaf8845330]
[fv-az2211-783:05790] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcaf889eb2c]
[fv-az2211-783:05790] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcaf884527e]
[fv-az2211-783:05790] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcaf88288ff]
[fv-az2211-783:05790] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcaf8ca5ff5]
[fv-az2211-783:05790] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcaf8cbb0da]
[fv-az2211-783:05790] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcaf8ca5a55]
[fv-az2211-783:05790] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcaf8ca5a6f]
[fv-az2211-783:05790] [ 8] plumed(+0x13209)[0x557511ee9209]
[fv-az2211-783:05790] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcaf882a1ca]
[fv-az2211-783:05790] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcaf882a28b]
[fv-az2211-783:05790] [11] plumed(+0x134a5)[0x557511ee94a5]
[fv-az2211-783:05790] *** End of error message ***
</pre>
{% endraw %}
