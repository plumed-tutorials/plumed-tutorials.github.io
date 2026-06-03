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
[runnervm3jyl0:48278] *** Process received signal ***
[runnervm3jyl0:48278] Signal: Aborted (6)
[runnervm3jyl0:48278] Signal code:  (-6)
[runnervm3jyl0:48278] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7ae4645330]
[runnervm3jyl0:48278] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7ae469eb2c]
[runnervm3jyl0:48278] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7ae464527e]
[runnervm3jyl0:48278] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7ae46288ff]
[runnervm3jyl0:48278] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7ae4aa5ff5]
[runnervm3jyl0:48278] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7ae4abb0da]
[runnervm3jyl0:48278] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7ae4aa5a55]
[runnervm3jyl0:48278] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7ae4aa5a6f]
[runnervm3jyl0:48278] [ 8] plumed(+0x13209)[0x559b5c5c2209]
[runnervm3jyl0:48278] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7ae462a1ca]
[runnervm3jyl0:48278] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7ae462a28b]
[runnervm3jyl0:48278] [11] plumed(+0x134a5)[0x559b5c5c24a5]
[runnervm3jyl0:48278] *** End of error message ***
</pre>
{% endraw %}
