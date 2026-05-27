Stderr for source:  PIV-PathCV_meta.md_working_3.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PRINT with label @0 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[runnervm3jyl0:79185] *** Process received signal ***
[runnervm3jyl0:79185] Signal: Aborted (6)
[runnervm3jyl0:79185] Signal code:  (-6)
[runnervm3jyl0:79185] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fac6f845330]
[runnervm3jyl0:79185] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fac6f89eb2c]
[runnervm3jyl0:79185] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fac6f84527e]
[runnervm3jyl0:79185] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fac6f8288ff]
[runnervm3jyl0:79185] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fac6fca5ff5]
[runnervm3jyl0:79185] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fac6fcbb0da]
[runnervm3jyl0:79185] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fac6fca5a55]
[runnervm3jyl0:79185] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fac6fca5a6f]
[runnervm3jyl0:79185] [ 8] plumed(+0x13209)[0x561c180dc209]
[runnervm3jyl0:79185] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fac6f82a1ca]
[runnervm3jyl0:79185] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fac6f82a28b]
[runnervm3jyl0:79185] [11] plumed(+0x134a5)[0x561c180dc4a5]
[runnervm3jyl0:79185] *** End of error message ***
</pre>
{% endraw %}
