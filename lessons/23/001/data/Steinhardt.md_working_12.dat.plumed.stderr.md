Stderr for source:  Steinhardt.md_working_12.dat   
Download: [zipped raw stdout](Steinhardt.md_working_12.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_12.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervmg397c:79868] *** Process received signal ***
[runnervmg397c:79868] Signal: Aborted (6)
[runnervmg397c:79868] Signal code:  (-6)
[runnervmg397c:79868] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f20b2845330]
[runnervmg397c:79868] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f20b289eb2c]
[runnervmg397c:79868] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f20b284527e]
[runnervmg397c:79868] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f20b28288ff]
[runnervmg397c:79868] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f20b2ca5ff5]
[runnervmg397c:79868] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f20b2cbb0da]
[runnervmg397c:79868] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f20b2ca5a55]
[runnervmg397c:79868] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f20b2ca5a6f]
[runnervmg397c:79868] [ 8] plumed(+0x13209)[0x55ed5f838209]
[runnervmg397c:79868] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f20b282a1ca]
[runnervmg397c:79868] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f20b282a28b]
[runnervmg397c:79868] [11] plumed(+0x134a5)[0x55ed5f8384a5]
[runnervmg397c:79868] *** End of error message ***
</pre>
{% endraw %}
