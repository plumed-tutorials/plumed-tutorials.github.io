Stderr for source:  SymmetryFunction.md_working_2.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[runnervm3jyl0:48483] *** Process received signal ***
[runnervm3jyl0:48483] Signal: Aborted (6)
[runnervm3jyl0:48483] Signal code:  (-6)
[runnervm3jyl0:48483] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2802e45330]
[runnervm3jyl0:48483] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2802e9eb2c]
[runnervm3jyl0:48483] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2802e4527e]
[runnervm3jyl0:48483] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2802e288ff]
[runnervm3jyl0:48483] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f28032a5ff5]
[runnervm3jyl0:48483] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f28032bb0da]
[runnervm3jyl0:48483] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f28032a5a55]
[runnervm3jyl0:48483] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f28032a5a6f]
[runnervm3jyl0:48483] [ 8] plumed(+0x13209)[0x562b9c3be209]
[runnervm3jyl0:48483] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2802e2a1ca]
[runnervm3jyl0:48483] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2802e2a28b]
[runnervm3jyl0:48483] [11] plumed(+0x134a5)[0x562b9c3be4a5]
[runnervm3jyl0:48483] *** End of error message ***
</pre>
{% endraw %}
