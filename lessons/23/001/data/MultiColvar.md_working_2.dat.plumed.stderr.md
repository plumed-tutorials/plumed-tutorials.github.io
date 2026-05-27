Stderr for source:  MultiColvar.md_working_2.dat   
Download: [zipped raw stdout](MultiColvar.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[runnervmg397c:79085] *** Process received signal ***
[runnervmg397c:79085] Signal: Aborted (6)
[runnervmg397c:79085] Signal code:  (-6)
[runnervmg397c:79085] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f16f0c45330]
[runnervmg397c:79085] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f16f0c9eb2c]
[runnervmg397c:79085] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f16f0c4527e]
[runnervmg397c:79085] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f16f0c288ff]
[runnervmg397c:79085] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f16f10a5ff5]
[runnervmg397c:79085] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f16f10bb0da]
[runnervmg397c:79085] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f16f10a5a55]
[runnervmg397c:79085] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f16f10a5a6f]
[runnervmg397c:79085] [ 8] plumed(+0x13209)[0x55ccda189209]
[runnervmg397c:79085] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f16f0c2a1ca]
[runnervmg397c:79085] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f16f0c2a28b]
[runnervmg397c:79085] [11] plumed(+0x134a5)[0x55ccda1894a5]
[runnervmg397c:79085] *** End of error message ***
</pre>
{% endraw %}
