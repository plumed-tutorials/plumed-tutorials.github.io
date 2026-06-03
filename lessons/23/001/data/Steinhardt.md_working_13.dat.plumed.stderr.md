Stderr for source:  Steinhardt.md_working_13.dat   
Download: [zipped raw stdout](Steinhardt.md_working_13.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_13.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervm3jyl0:47866] *** Process received signal ***
[runnervm3jyl0:47866] Signal: Aborted (6)
[runnervm3jyl0:47866] Signal code:  (-6)
[runnervm3jyl0:47866] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1940c45330]
[runnervm3jyl0:47866] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1940c9eb2c]
[runnervm3jyl0:47866] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1940c4527e]
[runnervm3jyl0:47866] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1940c288ff]
[runnervm3jyl0:47866] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f19410a5ff5]
[runnervm3jyl0:47866] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f19410bb0da]
[runnervm3jyl0:47866] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f19410a5a55]
[runnervm3jyl0:47866] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f19410a5a6f]
[runnervm3jyl0:47866] [ 8] plumed(+0x13209)[0x55a171c05209]
[runnervm3jyl0:47866] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1940c2a1ca]
[runnervm3jyl0:47866] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1940c2a28b]
[runnervm3jyl0:47866] [11] plumed(+0x134a5)[0x55a171c054a5]
[runnervm3jyl0:47866] *** End of error message ***
</pre>
{% endraw %}
