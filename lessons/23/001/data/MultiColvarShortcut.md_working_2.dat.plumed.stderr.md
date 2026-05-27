Stderr for source:  MultiColvarShortcut.md_working_2.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[runnervmg397c:79167] *** Process received signal ***
[runnervmg397c:79167] Signal: Aborted (6)
[runnervmg397c:79167] Signal code:  (-6)
[runnervmg397c:79167] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8a58245330]
[runnervmg397c:79167] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8a5829eb2c]
[runnervmg397c:79167] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8a5824527e]
[runnervmg397c:79167] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8a582288ff]
[runnervmg397c:79167] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8a586a5ff5]
[runnervmg397c:79167] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8a586bb0da]
[runnervmg397c:79167] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8a586a5a55]
[runnervmg397c:79167] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8a586a5a6f]
[runnervmg397c:79167] [ 8] plumed(+0x13209)[0x5564cb44a209]
[runnervmg397c:79167] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8a5822a1ca]
[runnervmg397c:79167] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8a5822a28b]
[runnervmg397c:79167] [11] plumed(+0x134a5)[0x5564cb44a4a5]
[runnervmg397c:79167] *** End of error message ***
</pre>
{% endraw %}
