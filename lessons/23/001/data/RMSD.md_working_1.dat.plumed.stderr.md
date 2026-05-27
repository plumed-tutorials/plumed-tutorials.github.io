Stderr for source:  RMSD.md_working_1.dat   
Download: [zipped raw stdout](RMSD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONSTANT with label v : cannot understand the following words from the input line : NCOLS=12, NROWS=2
[runnervmg397c:81272] *** Process received signal ***
[runnervmg397c:81272] Signal: Aborted (6)
[runnervmg397c:81272] Signal code:  (-6)
[runnervmg397c:81272] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc901845330]
[runnervmg397c:81272] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc90189eb2c]
[runnervmg397c:81272] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc90184527e]
[runnervmg397c:81272] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc9018288ff]
[runnervmg397c:81272] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc901ca5ff5]
[runnervmg397c:81272] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc901cbb0da]
[runnervmg397c:81272] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc901ca5a55]
[runnervmg397c:81272] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc901ca5a6f]
[runnervmg397c:81272] [ 8] plumed(+0x13209)[0x564182558209]
[runnervmg397c:81272] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc90182a1ca]
[runnervmg397c:81272] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc90182a28b]
[runnervmg397c:81272] [11] plumed(+0x134a5)[0x5641825584a5]
[runnervmg397c:81272] *** End of error message ***
</pre>
{% endraw %}
