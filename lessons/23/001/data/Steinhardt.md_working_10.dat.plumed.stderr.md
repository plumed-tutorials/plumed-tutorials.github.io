Stderr for source:  Steinhardt.md_working_10.dat   
Download: [zipped raw stdout](Steinhardt.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @2 : action lq6 has no component named lq6 (hint! the components in this actions are: )
[runnervmg397c:79806] *** Process received signal ***
[runnervmg397c:79806] Signal: Aborted (6)
[runnervmg397c:79806] Signal code:  (-6)
[runnervmg397c:79806] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2e28845330]
[runnervmg397c:79806] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2e2889eb2c]
[runnervmg397c:79806] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2e2884527e]
[runnervmg397c:79806] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2e288288ff]
[runnervmg397c:79806] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2e28ca5ff5]
[runnervmg397c:79806] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2e28cbb0da]
[runnervmg397c:79806] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2e28ca5a55]
[runnervmg397c:79806] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2e28ca5a6f]
[runnervmg397c:79806] [ 8] plumed(+0x13209)[0x55c6b8e4a209]
[runnervmg397c:79806] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2e2882a1ca]
[runnervmg397c:79806] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2e2882a28b]
[runnervmg397c:79806] [11] plumed(+0x134a5)[0x55c6b8e4a4a5]
[runnervmg397c:79806] *** End of error message ***
</pre>
{% endraw %}
