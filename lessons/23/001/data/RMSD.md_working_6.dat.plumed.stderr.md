Stderr for source:  RMSD.md_working_6.dat   
Download: [zipped raw stdout](RMSD.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action RMSD with label rmsd : cannot understand the following words from the input line : DISPLACEMENT
[runnervmg397c:81415] *** Process received signal ***
[runnervmg397c:81415] Signal: Aborted (6)
[runnervmg397c:81415] Signal code:  (-6)
[runnervmg397c:81415] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f684fe45330]
[runnervmg397c:81415] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f684fe9eb2c]
[runnervmg397c:81415] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f684fe4527e]
[runnervmg397c:81415] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f684fe288ff]
[runnervmg397c:81415] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f68502a5ff5]
[runnervmg397c:81415] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f68502bb0da]
[runnervmg397c:81415] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f68502a5a55]
[runnervmg397c:81415] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f68502a5a6f]
[runnervmg397c:81415] [ 8] plumed(+0x13209)[0x563fd4f2c209]
[runnervmg397c:81415] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f684fe2a1ca]
[runnervmg397c:81415] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f684fe2a28b]
[runnervmg397c:81415] [11] plumed(+0x134a5)[0x563fd4f2c4a5]
[runnervmg397c:81415] *** End of error message ***
</pre>
{% endraw %}
