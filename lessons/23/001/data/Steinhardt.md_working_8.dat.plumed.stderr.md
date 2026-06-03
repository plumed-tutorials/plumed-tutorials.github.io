Stderr for source:  Steinhardt.md_working_8.dat   
Download: [zipped raw stdout](Steinhardt.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervm3jyl0:47708] *** Process received signal ***
[runnervm3jyl0:47708] Signal: Aborted (6)
[runnervm3jyl0:47708] Signal code:  (-6)
[runnervm3jyl0:47708] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd4d1645330]
[runnervm3jyl0:47708] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd4d169eb2c]
[runnervm3jyl0:47708] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd4d164527e]
[runnervm3jyl0:47708] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd4d16288ff]
[runnervm3jyl0:47708] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd4d1aa5ff5]
[runnervm3jyl0:47708] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd4d1abb0da]
[runnervm3jyl0:47708] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd4d1aa5a55]
[runnervm3jyl0:47708] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd4d1aa5a6f]
[runnervm3jyl0:47708] [ 8] plumed(+0x13209)[0x560fb3d0c209]
[runnervm3jyl0:47708] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd4d162a1ca]
[runnervm3jyl0:47708] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd4d162a28b]
[runnervm3jyl0:47708] [11] plumed(+0x134a5)[0x560fb3d0c4a5]
[runnervm3jyl0:47708] *** End of error message ***
</pre>
{% endraw %}
