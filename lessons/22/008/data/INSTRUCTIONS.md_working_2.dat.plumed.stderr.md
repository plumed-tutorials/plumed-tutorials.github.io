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
[pkrvmf6wy0o8zjz:59961] *** Process received signal ***
[pkrvmf6wy0o8zjz:59961] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59961] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59961] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f18c4645330]
[pkrvmf6wy0o8zjz:59961] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f18c469eb2c]
[pkrvmf6wy0o8zjz:59961] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f18c464527e]
[pkrvmf6wy0o8zjz:59961] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f18c46288ff]
[pkrvmf6wy0o8zjz:59961] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f18c4aa5ff5]
[pkrvmf6wy0o8zjz:59961] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f18c4abb0da]
[pkrvmf6wy0o8zjz:59961] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f18c4aa5a55]
[pkrvmf6wy0o8zjz:59961] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f18c4aa5a6f]
[pkrvmf6wy0o8zjz:59961] [ 8] plumed(+0x13209)[0x5634199db209]
[pkrvmf6wy0o8zjz:59961] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f18c462a1ca]
[pkrvmf6wy0o8zjz:59961] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f18c462a28b]
[pkrvmf6wy0o8zjz:59961] [11] plumed(+0x134a5)[0x5634199db4a5]
[pkrvmf6wy0o8zjz:59961] *** End of error message ***
</pre>
{% endraw %}
