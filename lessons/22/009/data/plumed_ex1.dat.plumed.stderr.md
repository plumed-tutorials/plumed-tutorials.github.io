Stderr for source:  plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label metad : action cv has no component named cv (hint! the components in this actions are: cv.x cv.y cv.z )
[pkrvmf6wy0o8zjz:59881] *** Process received signal ***
[pkrvmf6wy0o8zjz:59881] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59881] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59881] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6449045330]
[pkrvmf6wy0o8zjz:59881] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f644909eb2c]
[pkrvmf6wy0o8zjz:59881] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f644904527e]
[pkrvmf6wy0o8zjz:59881] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f64490288ff]
[pkrvmf6wy0o8zjz:59881] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f64494a5ff5]
[pkrvmf6wy0o8zjz:59881] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f64494bb0da]
[pkrvmf6wy0o8zjz:59881] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f64494a5a55]
[pkrvmf6wy0o8zjz:59881] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f64494a5a6f]
[pkrvmf6wy0o8zjz:59881] [ 8] plumed(+0x13209)[0x55b13f857209]
[pkrvmf6wy0o8zjz:59881] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f644902a1ca]
[pkrvmf6wy0o8zjz:59881] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f644902a28b]
[pkrvmf6wy0o8zjz:59881] [11] plumed(+0x134a5)[0x55b13f8574a5]
[pkrvmf6wy0o8zjz:59881] *** End of error message ***
</pre>
{% endraw %}
