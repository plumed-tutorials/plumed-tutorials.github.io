Stderr for source:  RMSD.md_working_6.dat   
Download: [zipped raw stdout](RMSD.md_working_6.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_6.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action RMSD with label rmsd : cannot understand the following words from the input line : DISPLACEMENT
[runnervm3jyl0:49389] *** Process received signal ***
[runnervm3jyl0:49389] Signal: Aborted (6)
[runnervm3jyl0:49389] Signal code:  (-6)
[runnervm3jyl0:49389] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4767645330]
[runnervm3jyl0:49389] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f476769eb2c]
[runnervm3jyl0:49389] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f476764527e]
[runnervm3jyl0:49389] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f47676288ff]
[runnervm3jyl0:49389] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4767aa5ff5]
[runnervm3jyl0:49389] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4767abb0da]
[runnervm3jyl0:49389] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4767aa5a55]
[runnervm3jyl0:49389] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4767aa5a6f]
[runnervm3jyl0:49389] [ 8] plumed(+0x13209)[0x557de681c209]
[runnervm3jyl0:49389] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f476762a1ca]
[runnervm3jyl0:49389] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f476762a28b]
[runnervm3jyl0:49389] [11] plumed(+0x134a5)[0x557de681c4a5]
[runnervm3jyl0:49389] *** End of error message ***
</pre>
{% endraw %}
