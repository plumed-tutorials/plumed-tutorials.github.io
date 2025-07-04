Stderr for source:  MultiColvarShortcut.md_working_2.dat   
Download: [zipped raw stdout](MultiColvarShortcut.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvarShortcut.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[pkrvmbietmlfzoi:34800] *** Process received signal ***
[pkrvmbietmlfzoi:34800] Signal: Aborted (6)
[pkrvmbietmlfzoi:34800] Signal code:  (-6)
[pkrvmbietmlfzoi:34800] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa7c6e45330]
[pkrvmbietmlfzoi:34800] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa7c6e9eb2c]
[pkrvmbietmlfzoi:34800] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa7c6e4527e]
[pkrvmbietmlfzoi:34800] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa7c6e288ff]
[pkrvmbietmlfzoi:34800] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa7c72a5ff5]
[pkrvmbietmlfzoi:34800] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa7c72bb0da]
[pkrvmbietmlfzoi:34800] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa7c72a5a55]
[pkrvmbietmlfzoi:34800] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa7c72a5a6f]
[pkrvmbietmlfzoi:34800] [ 8] plumed(+0x13209)[0x559375eef209]
[pkrvmbietmlfzoi:34800] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa7c6e2a1ca]
[pkrvmbietmlfzoi:34800] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa7c6e2a28b]
[pkrvmbietmlfzoi:34800] [11] plumed(+0x134a5)[0x559375eef4a5]
[pkrvmbietmlfzoi:34800] *** End of error message ***
</pre>
{% endraw %}
