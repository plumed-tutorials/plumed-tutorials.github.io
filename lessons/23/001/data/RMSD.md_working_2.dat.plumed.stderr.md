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
[runnervmg397c:81303] *** Process received signal ***
[runnervmg397c:81303] Signal: Aborted (6)
[runnervmg397c:81303] Signal code:  (-6)
[runnervmg397c:81303] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f94dea45330]
[runnervmg397c:81303] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f94dea9eb2c]
[runnervmg397c:81303] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f94dea4527e]
[runnervmg397c:81303] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f94dea288ff]
[runnervmg397c:81303] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f94deea5ff5]
[runnervmg397c:81303] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f94deebb0da]
[runnervmg397c:81303] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f94deea5a55]
[runnervmg397c:81303] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f94deea5a6f]
[runnervmg397c:81303] [ 8] plumed(+0x13209)[0x55b13778e209]
[runnervmg397c:81303] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f94dea2a1ca]
[runnervmg397c:81303] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f94dea2a28b]
[runnervmg397c:81303] [11] plumed(+0x134a5)[0x55b13778e4a5]
[runnervmg397c:81303] *** End of error message ***
</pre>
{% endraw %}
