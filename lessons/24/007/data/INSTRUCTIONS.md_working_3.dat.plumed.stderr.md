Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[runnervm3jyl0:80219] *** Process received signal ***
[runnervm3jyl0:80219] Signal: Aborted (6)
[runnervm3jyl0:80219] Signal code:  (-6)
[runnervm3jyl0:80219] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc16f445330]
[runnervm3jyl0:80219] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc16f49eb2c]
[runnervm3jyl0:80219] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc16f44527e]
[runnervm3jyl0:80219] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc16f4288ff]
[runnervm3jyl0:80219] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc16f8a5ff5]
[runnervm3jyl0:80219] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc16f8bb0da]
[runnervm3jyl0:80219] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc16f8a5a55]
[runnervm3jyl0:80219] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc16f8a5a6f]
[runnervm3jyl0:80219] [ 8] plumed(+0x13209)[0x562924312209]
[runnervm3jyl0:80219] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc16f42a1ca]
[runnervm3jyl0:80219] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc16f42a28b]
[runnervm3jyl0:80219] [11] plumed(+0x134a5)[0x5629243124a5]
[runnervm3jyl0:80219] *** End of error message ***
</pre>
{% endraw %}
