Stderr for source:  Behler.md_working_4.dat   
Download: [zipped raw stdout](Behler.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[runnervmg397c:80319] *** Process received signal ***
[runnervmg397c:80319] Signal: Aborted (6)
[runnervmg397c:80319] Signal code:  (-6)
[runnervmg397c:80319] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9250645330]
[runnervmg397c:80319] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f925069eb2c]
[runnervmg397c:80319] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f925064527e]
[runnervmg397c:80319] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f92506288ff]
[runnervmg397c:80319] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9250aa5ff5]
[runnervmg397c:80319] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9250abb0da]
[runnervmg397c:80319] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9250aa5a55]
[runnervmg397c:80319] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9250aa5a6f]
[runnervmg397c:80319] [ 8] plumed(+0x13209)[0x563cb5aa1209]
[runnervmg397c:80319] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f925062a1ca]
[runnervmg397c:80319] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f925062a28b]
[runnervmg397c:80319] [11] plumed(+0x134a5)[0x563cb5aa14a5]
[runnervmg397c:80319] *** End of error message ***
</pre>
{% endraw %}
