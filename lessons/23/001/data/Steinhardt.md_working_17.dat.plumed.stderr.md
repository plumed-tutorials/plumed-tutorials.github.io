Stderr for source:  Steinhardt.md_working_17.dat   
Download: [zipped raw stdout](Steinhardt.md_working_17.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_17.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervm3jyl0:47992] *** Process received signal ***
[runnervm3jyl0:47992] Signal: Aborted (6)
[runnervm3jyl0:47992] Signal code:  (-6)
[runnervm3jyl0:47992] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2803645330]
[runnervm3jyl0:47992] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f280369eb2c]
[runnervm3jyl0:47992] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f280364527e]
[runnervm3jyl0:47992] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f28036288ff]
[runnervm3jyl0:47992] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2803aa5ff5]
[runnervm3jyl0:47992] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2803abb0da]
[runnervm3jyl0:47992] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2803aa5a55]
[runnervm3jyl0:47992] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2803aa5a6f]
[runnervm3jyl0:47992] [ 8] plumed(+0x13209)[0x55df739bd209]
[runnervm3jyl0:47992] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f280362a1ca]
[runnervm3jyl0:47992] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f280362a28b]
[runnervm3jyl0:47992] [11] plumed(+0x134a5)[0x55df739bd4a5]
[runnervm3jyl0:47992] *** End of error message ***
</pre>
{% endraw %}
