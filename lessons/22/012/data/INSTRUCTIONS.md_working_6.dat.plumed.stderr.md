Stderr for source:  INSTRUCTIONS.md_working_6.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action UPPER_WALLS with label uwall : cannot find action named cv (hint! the actions with value in this ActionSet are: )
[runnervm3jyl0:48092] *** Process received signal ***
[runnervm3jyl0:48092] Signal: Aborted (6)
[runnervm3jyl0:48092] Signal code:  (-6)
[runnervm3jyl0:48092] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9a12845330]
[runnervm3jyl0:48092] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9a1289eb2c]
[runnervm3jyl0:48092] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9a1284527e]
[runnervm3jyl0:48092] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9a128288ff]
[runnervm3jyl0:48092] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9a12ca5ff5]
[runnervm3jyl0:48092] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9a12cbb0da]
[runnervm3jyl0:48092] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9a12ca5a55]
[runnervm3jyl0:48092] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9a12ca5a6f]
[runnervm3jyl0:48092] [ 8] plumed(+0x13209)[0x5639f8f00209]
[runnervm3jyl0:48092] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9a1282a1ca]
[runnervm3jyl0:48092] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9a1282a28b]
[runnervm3jyl0:48092] [11] plumed(+0x134a5)[0x5639f8f004a5]
[runnervm3jyl0:48092] *** End of error message ***
</pre>
{% endraw %}
