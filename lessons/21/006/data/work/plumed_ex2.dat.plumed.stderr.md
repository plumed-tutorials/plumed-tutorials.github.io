Stderr for source:  work/plumed_ex2.dat   
Download: [zipped raw stdout](plumed_ex2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action PCA with label pca : action cc has no component named cc (hint! the components in this actions are: )
[pkrvmbietmlfzoi:36037] *** Process received signal ***
[pkrvmbietmlfzoi:36037] Signal: Aborted (6)
[pkrvmbietmlfzoi:36037] Signal code:  (-6)
[pkrvmbietmlfzoi:36037] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f8d01c45330]
[pkrvmbietmlfzoi:36037] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f8d01c9eb2c]
[pkrvmbietmlfzoi:36037] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f8d01c4527e]
[pkrvmbietmlfzoi:36037] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f8d01c288ff]
[pkrvmbietmlfzoi:36037] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f8d020a5ff5]
[pkrvmbietmlfzoi:36037] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f8d020bb0da]
[pkrvmbietmlfzoi:36037] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f8d020a5a55]
[pkrvmbietmlfzoi:36037] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f8d020a5a6f]
[pkrvmbietmlfzoi:36037] [ 8] plumed(+0x13209)[0x55839a6d9209]
[pkrvmbietmlfzoi:36037] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f8d01c2a1ca]
[pkrvmbietmlfzoi:36037] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f8d01c2a28b]
[pkrvmbietmlfzoi:36037] [11] plumed(+0x134a5)[0x55839a6d94a5]
[pkrvmbietmlfzoi:36037] *** End of error message ***
</pre>
{% endraw %}
