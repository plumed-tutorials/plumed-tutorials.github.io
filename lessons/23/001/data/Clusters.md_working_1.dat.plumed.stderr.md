Stderr for source:  Clusters.md_working_1.dat   
Download: [zipped raw stdout](Clusters.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[runnervm3jyl0:49140] *** Process received signal ***
[runnervm3jyl0:49140] Signal: Aborted (6)
[runnervm3jyl0:49140] Signal code:  (-6)
[runnervm3jyl0:49140] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1f66045330]
[runnervm3jyl0:49140] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1f6609eb2c]
[runnervm3jyl0:49140] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1f6604527e]
[runnervm3jyl0:49140] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1f660288ff]
[runnervm3jyl0:49140] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1f664a5ff5]
[runnervm3jyl0:49140] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1f664bb0da]
[runnervm3jyl0:49140] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1f664a5a55]
[runnervm3jyl0:49140] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1f664a5a6f]
[runnervm3jyl0:49140] [ 8] plumed(+0x13209)[0x564207540209]
[runnervm3jyl0:49140] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1f6602a1ca]
[runnervm3jyl0:49140] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1f6602a28b]
[runnervm3jyl0:49140] [11] plumed(+0x134a5)[0x5642075404a5]
[runnervm3jyl0:49140] *** End of error message ***
</pre>
{% endraw %}
