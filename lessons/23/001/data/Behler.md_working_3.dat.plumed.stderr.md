Stderr for source:  Behler.md_working_3.dat   
Download: [zipped raw stdout](Behler.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[runnervm3jyl0:48247] *** Process received signal ***
[runnervm3jyl0:48247] Signal: Aborted (6)
[runnervm3jyl0:48247] Signal code:  (-6)
[runnervm3jyl0:48247] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fba07845330]
[runnervm3jyl0:48247] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fba0789eb2c]
[runnervm3jyl0:48247] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fba0784527e]
[runnervm3jyl0:48247] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fba078288ff]
[runnervm3jyl0:48247] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fba07ca5ff5]
[runnervm3jyl0:48247] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fba07cbb0da]
[runnervm3jyl0:48247] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fba07ca5a55]
[runnervm3jyl0:48247] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fba07ca5a6f]
[runnervm3jyl0:48247] [ 8] plumed(+0x13209)[0x5653792ae209]
[runnervm3jyl0:48247] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fba0782a1ca]
[runnervm3jyl0:48247] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fba0782a28b]
[runnervm3jyl0:48247] [11] plumed(+0x134a5)[0x5653792ae4a5]
[runnervm3jyl0:48247] *** End of error message ***
</pre>
{% endraw %}
