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
[runnervm3jyl0:49275] *** Process received signal ***
[runnervm3jyl0:49275] Signal: Aborted (6)
[runnervm3jyl0:49275] Signal code:  (-6)
[runnervm3jyl0:49275] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb71de45330]
[runnervm3jyl0:49275] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb71de9eb2c]
[runnervm3jyl0:49275] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb71de4527e]
[runnervm3jyl0:49275] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb71de288ff]
[runnervm3jyl0:49275] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb71e2a5ff5]
[runnervm3jyl0:49275] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb71e2bb0da]
[runnervm3jyl0:49275] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb71e2a5a55]
[runnervm3jyl0:49275] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb71e2a5a6f]
[runnervm3jyl0:49275] [ 8] plumed(+0x13209)[0x56175cb20209]
[runnervm3jyl0:49275] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb71de2a1ca]
[runnervm3jyl0:49275] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb71de2a28b]
[runnervm3jyl0:49275] [11] plumed(+0x134a5)[0x56175cb204a5]
[runnervm3jyl0:49275] *** End of error message ***
</pre>
{% endraw %}
