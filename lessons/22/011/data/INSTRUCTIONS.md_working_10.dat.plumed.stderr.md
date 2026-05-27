Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[runnervm3jyl0:79885] *** Process received signal ***
[runnervm3jyl0:79885] Signal: Aborted (6)
[runnervm3jyl0:79885] Signal code:  (-6)
[runnervm3jyl0:79885] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd25d845330]
[runnervm3jyl0:79885] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd25d89eb2c]
[runnervm3jyl0:79885] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd25d84527e]
[runnervm3jyl0:79885] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd25d8288ff]
[runnervm3jyl0:79885] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd25dca5ff5]
[runnervm3jyl0:79885] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd25dcbb0da]
[runnervm3jyl0:79885] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd25dca5a55]
[runnervm3jyl0:79885] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd25dca5a6f]
[runnervm3jyl0:79885] [ 8] plumed(+0x13209)[0x55a5497ee209]
[runnervm3jyl0:79885] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd25d82a1ca]
[runnervm3jyl0:79885] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd25d82a28b]
[runnervm3jyl0:79885] [11] plumed(+0x134a5)[0x55a5497ee4a5]
[runnervm3jyl0:79885] *** End of error message ***
</pre>
{% endraw %}
