Stderr for source:  histograms.md_working_8.dat   
Download: [zipped raw stdout](histograms.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCES with label d1 : keyword ATOMS could not be read correctly
[runnervm3jyl0:49103] *** Process received signal ***
[runnervm3jyl0:49103] Signal: Aborted (6)
[runnervm3jyl0:49103] Signal code:  (-6)
[runnervm3jyl0:49103] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff846845330]
[runnervm3jyl0:49103] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff84689eb2c]
[runnervm3jyl0:49103] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff84684527e]
[runnervm3jyl0:49103] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff8468288ff]
[runnervm3jyl0:49103] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff846ca5ff5]
[runnervm3jyl0:49103] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff846cbb0da]
[runnervm3jyl0:49103] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff846ca5a55]
[runnervm3jyl0:49103] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff846ca5a6f]
[runnervm3jyl0:49103] [ 8] plumed(+0x13209)[0x561678b05209]
[runnervm3jyl0:49103] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff84682a1ca]
[runnervm3jyl0:49103] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff84682a28b]
[runnervm3jyl0:49103] [11] plumed(+0x134a5)[0x561678b054a5]
[runnervm3jyl0:49103] *** End of error message ***
</pre>
{% endraw %}
