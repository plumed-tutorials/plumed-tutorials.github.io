Stderr for source:  Behler.md_working_1.dat   
Download: [zipped raw stdout](Behler.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervm3jyl0:48185] *** Process received signal ***
[runnervm3jyl0:48185] Signal: Aborted (6)
[runnervm3jyl0:48185] Signal code:  (-6)
[runnervm3jyl0:48185] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f73e8c45330]
[runnervm3jyl0:48185] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f73e8c9eb2c]
[runnervm3jyl0:48185] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f73e8c4527e]
[runnervm3jyl0:48185] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f73e8c288ff]
[runnervm3jyl0:48185] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f73e90a5ff5]
[runnervm3jyl0:48185] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f73e90bb0da]
[runnervm3jyl0:48185] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f73e90a5a55]
[runnervm3jyl0:48185] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f73e90a5a6f]
[runnervm3jyl0:48185] [ 8] plumed(+0x13209)[0x56453f64e209]
[runnervm3jyl0:48185] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f73e8c2a1ca]
[runnervm3jyl0:48185] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f73e8c2a28b]
[runnervm3jyl0:48185] [11] plumed(+0x134a5)[0x56453f64e4a5]
[runnervm3jyl0:48185] *** End of error message ***
</pre>
{% endraw %}
