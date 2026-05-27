Stderr for source:  INSTRUCTIONS.md_working_5.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action MATHEVAL with label diff : cannot find action named cv (hint! the actions with value in this ActionSet are: q6 )
[runnervm3jyl0:80689] *** Process received signal ***
[runnervm3jyl0:80689] Signal: Aborted (6)
[runnervm3jyl0:80689] Signal code:  (-6)
[runnervm3jyl0:80689] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f00b1645330]
[runnervm3jyl0:80689] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f00b169eb2c]
[runnervm3jyl0:80689] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f00b164527e]
[runnervm3jyl0:80689] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f00b16288ff]
[runnervm3jyl0:80689] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f00b1aa5ff5]
[runnervm3jyl0:80689] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f00b1abb0da]
[runnervm3jyl0:80689] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f00b1aa5a55]
[runnervm3jyl0:80689] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f00b1aa5a6f]
[runnervm3jyl0:80689] [ 8] plumed(+0x13209)[0x5591ee782209]
[runnervm3jyl0:80689] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f00b162a1ca]
[runnervm3jyl0:80689] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f00b162a28b]
[runnervm3jyl0:80689] [11] plumed(+0x134a5)[0x5591ee7824a5]
[runnervm3jyl0:80689] *** End of error message ***
</pre>
{% endraw %}
