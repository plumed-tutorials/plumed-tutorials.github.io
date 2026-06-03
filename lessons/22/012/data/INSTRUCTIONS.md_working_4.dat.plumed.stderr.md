Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action OPES_METAD with label opes : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[runnervm3jyl0:48004] *** Process received signal ***
[runnervm3jyl0:48004] Signal: Aborted (6)
[runnervm3jyl0:48004] Signal code:  (-6)
[runnervm3jyl0:48004] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1f34e45330]
[runnervm3jyl0:48004] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1f34e9eb2c]
[runnervm3jyl0:48004] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1f34e4527e]
[runnervm3jyl0:48004] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1f34e288ff]
[runnervm3jyl0:48004] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1f352a5ff5]
[runnervm3jyl0:48004] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1f352bb0da]
[runnervm3jyl0:48004] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1f352a5a55]
[runnervm3jyl0:48004] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1f352a5a6f]
[runnervm3jyl0:48004] [ 8] plumed(+0x13209)[0x56458773e209]
[runnervm3jyl0:48004] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1f34e2a1ca]
[runnervm3jyl0:48004] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1f34e2a28b]
[runnervm3jyl0:48004] [11] plumed(+0x134a5)[0x56458773e4a5]
[runnervm3jyl0:48004] *** End of error message ***
</pre>
{% endraw %}
