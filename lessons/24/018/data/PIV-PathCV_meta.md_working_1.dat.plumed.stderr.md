Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: )
[runnervm3jyl0:47205] *** Process received signal ***
[runnervm3jyl0:47205] Signal: Aborted (6)
[runnervm3jyl0:47205] Signal code:  (-6)
[runnervm3jyl0:47205] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1271645330]
[runnervm3jyl0:47205] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f127169eb2c]
[runnervm3jyl0:47205] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f127164527e]
[runnervm3jyl0:47205] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f12716288ff]
[runnervm3jyl0:47205] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1271aa5ff5]
[runnervm3jyl0:47205] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1271abb0da]
[runnervm3jyl0:47205] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1271aa5a55]
[runnervm3jyl0:47205] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1271aa5a6f]
[runnervm3jyl0:47205] [ 8] plumed(+0x13209)[0x563bc9425209]
[runnervm3jyl0:47205] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f127162a1ca]
[runnervm3jyl0:47205] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f127162a28b]
[runnervm3jyl0:47205] [11] plumed(+0x134a5)[0x563bc94254a5]
[runnervm3jyl0:47205] *** End of error message ***
</pre>
{% endraw %}
