Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(vesselbase/Vessel.cpp:157) void PLMD::vesselbase::Vessel::error(const std::string&)
ERROR for keyword MORE_THAN in action CLUSTER_DISTRIBUTION with label nclust : could not parse D_0
[runnervm3jyl0:80878] *** Process received signal ***
[runnervm3jyl0:80878] Signal: Aborted (6)
[runnervm3jyl0:80878] Signal code:  (-6)
[runnervm3jyl0:80878] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3268645330]
[runnervm3jyl0:80878] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f326869eb2c]
[runnervm3jyl0:80878] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f326864527e]
[runnervm3jyl0:80878] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f32686288ff]
[runnervm3jyl0:80878] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3268aa5ff5]
[runnervm3jyl0:80878] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3268abb0da]
[runnervm3jyl0:80878] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3268aa5a55]
[runnervm3jyl0:80878] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3268aa5a6f]
[runnervm3jyl0:80878] [ 8] plumed(+0x13209)[0x55f3cbd90209]
[runnervm3jyl0:80878] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f326862a1ca]
[runnervm3jyl0:80878] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f326862a28b]
[runnervm3jyl0:80878] [11] plumed(+0x134a5)[0x55f3cbd904a5]
[runnervm3jyl0:80878] *** End of error message ***
</pre>
{% endraw %}
