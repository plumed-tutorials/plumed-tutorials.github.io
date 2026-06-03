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
[runnervm3jyl0:47695] *** Process received signal ***
[runnervm3jyl0:47695] Signal: Aborted (6)
[runnervm3jyl0:47695] Signal code:  (-6)
[runnervm3jyl0:47695] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7feedda45330]
[runnervm3jyl0:47695] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7feedda9eb2c]
[runnervm3jyl0:47695] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7feedda4527e]
[runnervm3jyl0:47695] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7feedda288ff]
[runnervm3jyl0:47695] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7feeddea5ff5]
[runnervm3jyl0:47695] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7feeddebb0da]
[runnervm3jyl0:47695] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7feeddea5a55]
[runnervm3jyl0:47695] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7feeddea5a6f]
[runnervm3jyl0:47695] [ 8] plumed(+0x13209)[0x55a5824a0209]
[runnervm3jyl0:47695] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7feedda2a1ca]
[runnervm3jyl0:47695] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7feedda2a28b]
[runnervm3jyl0:47695] [11] plumed(+0x134a5)[0x55a5824a04a5]
[runnervm3jyl0:47695] *** End of error message ***
</pre>
{% endraw %}
