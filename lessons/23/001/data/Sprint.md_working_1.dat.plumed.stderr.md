Stderr for source:  Sprint.md_working_1.dat   
Download: [zipped raw stdout](Sprint.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label s1 : keyword MATRIX is compulsory for this action
[runnervmg397c:79423] *** Process received signal ***
[runnervmg397c:79423] Signal: Aborted (6)
[runnervmg397c:79423] Signal code:  (-6)
[runnervmg397c:79423] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd1b4045330]
[runnervmg397c:79423] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd1b409eb2c]
[runnervmg397c:79423] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd1b404527e]
[runnervmg397c:79423] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd1b40288ff]
[runnervmg397c:79423] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd1b44a5ff5]
[runnervmg397c:79423] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd1b44bb0da]
[runnervmg397c:79423] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd1b44a5a55]
[runnervmg397c:79423] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd1b44a5a6f]
[runnervmg397c:79423] [ 8] plumed(+0x13209)[0x56392ab2c209]
[runnervmg397c:79423] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd1b402a1ca]
[runnervmg397c:79423] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd1b402a28b]
[runnervmg397c:79423] [11] plumed(+0x134a5)[0x56392ab2c4a5]
[runnervmg397c:79423] *** End of error message ***
</pre>
{% endraw %}
