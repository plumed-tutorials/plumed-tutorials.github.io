Stderr for source:  MultiColvarShortcut.md_working_4.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[runnervmg397c:79219] *** Process received signal ***
[runnervmg397c:79219] Signal: Aborted (6)
[runnervmg397c:79219] Signal code:  (-6)
[runnervmg397c:79219] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fb011445330]
[runnervmg397c:79219] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fb01149eb2c]
[runnervmg397c:79219] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fb01144527e]
[runnervmg397c:79219] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fb0114288ff]
[runnervmg397c:79219] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fb0118a5ff5]
[runnervmg397c:79219] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fb0118bb0da]
[runnervmg397c:79219] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fb0118a5a55]
[runnervmg397c:79219] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fb0118a5a6f]
[runnervmg397c:79219] [ 8] plumed(+0x13209)[0x55ec778ec209]
[runnervmg397c:79219] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fb01142a1ca]
[runnervmg397c:79219] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fb01142a28b]
[runnervmg397c:79219] [11] plumed(+0x134a5)[0x55ec778ec4a5]
[runnervmg397c:79219] *** End of error message ***
</pre>
{% endraw %}
