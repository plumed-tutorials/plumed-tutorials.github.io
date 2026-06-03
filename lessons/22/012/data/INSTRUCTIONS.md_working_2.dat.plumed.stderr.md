Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label s : keyword SIGMA could not be read correctly
[runnervm3jyl0:47940] *** Process received signal ***
[runnervm3jyl0:47940] Signal: Aborted (6)
[runnervm3jyl0:47940] Signal code:  (-6)
[runnervm3jyl0:47940] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9b5bc45330]
[runnervm3jyl0:47940] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9b5bc9eb2c]
[runnervm3jyl0:47940] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9b5bc4527e]
[runnervm3jyl0:47940] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9b5bc288ff]
[runnervm3jyl0:47940] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9b5c0a5ff5]
[runnervm3jyl0:47940] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9b5c0bb0da]
[runnervm3jyl0:47940] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9b5c0a5a55]
[runnervm3jyl0:47940] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9b5c0a5a6f]
[runnervm3jyl0:47940] [ 8] plumed(+0x13209)[0x55779698d209]
[runnervm3jyl0:47940] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9b5bc2a1ca]
[runnervm3jyl0:47940] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9b5bc2a28b]
[runnervm3jyl0:47940] [11] plumed(+0x134a5)[0x55779698d4a5]
[runnervm3jyl0:47940] *** End of error message ***
</pre>
{% endraw %}
