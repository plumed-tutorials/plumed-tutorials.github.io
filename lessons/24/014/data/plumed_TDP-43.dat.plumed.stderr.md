Stderr for source:  plumed_TDP-43.dat   
Download: [zipped raw stdout](plumed_TDP-43.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_TDP-43.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAINFERENCE with label af_mi_rest_domains : REWEIGHT can only be used in parallel with 2 or more replicas
[runnervm3jyl0:46907] *** Process received signal ***
[runnervm3jyl0:46907] Signal: Aborted (6)
[runnervm3jyl0:46907] Signal code:  (-6)
[runnervm3jyl0:46907] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f48b4245330]
[runnervm3jyl0:46907] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f48b429eb2c]
[runnervm3jyl0:46907] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f48b424527e]
[runnervm3jyl0:46907] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f48b42288ff]
[runnervm3jyl0:46907] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f48b46a5ff5]
[runnervm3jyl0:46907] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f48b46bb0da]
[runnervm3jyl0:46907] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f48b46a5a55]
[runnervm3jyl0:46907] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f48b46a5a6f]
[runnervm3jyl0:46907] [ 8] plumed(+0x13209)[0x56262d537209]
[runnervm3jyl0:46907] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f48b422a1ca]
[runnervm3jyl0:46907] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f48b422a28b]
[runnervm3jyl0:46907] [11] plumed(+0x134a5)[0x56262d5374a5]
[runnervm3jyl0:46907] *** End of error message ***
</pre>
{% endraw %}
