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
[runnervm3jyl0:79120] *** Process received signal ***
[runnervm3jyl0:79120] Signal: Aborted (6)
[runnervm3jyl0:79120] Signal code:  (-6)
[runnervm3jyl0:79120] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3531e45330]
[runnervm3jyl0:79120] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3531e9eb2c]
[runnervm3jyl0:79120] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3531e4527e]
[runnervm3jyl0:79120] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3531e288ff]
[runnervm3jyl0:79120] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f35322a5ff5]
[runnervm3jyl0:79120] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f35322bb0da]
[runnervm3jyl0:79120] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f35322a5a55]
[runnervm3jyl0:79120] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f35322a5a6f]
[runnervm3jyl0:79120] [ 8] plumed(+0x13209)[0x559a9a828209]
[runnervm3jyl0:79120] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3531e2a1ca]
[runnervm3jyl0:79120] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3531e2a28b]
[runnervm3jyl0:79120] [11] plumed(+0x134a5)[0x559a9a8284a5]
[runnervm3jyl0:79120] *** End of error message ***
</pre>
{% endraw %}
