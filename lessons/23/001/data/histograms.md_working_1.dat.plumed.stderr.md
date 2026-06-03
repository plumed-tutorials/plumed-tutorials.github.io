Stderr for source:  histograms.md_working_1.dat   
Download: [zipped raw stdout](histograms.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @2 : keyword GRID is compulsory for this action
[runnervm3jyl0:48865] *** Process received signal ***
[runnervm3jyl0:48865] Signal: Aborted (6)
[runnervm3jyl0:48865] Signal code:  (-6)
[runnervm3jyl0:48865] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6faea45330]
[runnervm3jyl0:48865] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6faea9eb2c]
[runnervm3jyl0:48865] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6faea4527e]
[runnervm3jyl0:48865] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6faea288ff]
[runnervm3jyl0:48865] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6faeea5ff5]
[runnervm3jyl0:48865] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6faeebb0da]
[runnervm3jyl0:48865] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6faeea5a55]
[runnervm3jyl0:48865] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6faeea5a6f]
[runnervm3jyl0:48865] [ 8] plumed(+0x13209)[0x56550b6f3209]
[runnervm3jyl0:48865] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6faea2a1ca]
[runnervm3jyl0:48865] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6faea2a28b]
[runnervm3jyl0:48865] [11] plumed(+0x134a5)[0x56550b6f34a5]
[runnervm3jyl0:48865] *** End of error message ***
</pre>
{% endraw %}
