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
[pkrvmf6wy0o8zjz:60116] *** Process received signal ***
[pkrvmf6wy0o8zjz:60116] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:60116] Signal code:  (-6)
[pkrvmf6wy0o8zjz:60116] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0501045330]
[pkrvmf6wy0o8zjz:60116] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f050109eb2c]
[pkrvmf6wy0o8zjz:60116] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f050104527e]
[pkrvmf6wy0o8zjz:60116] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f05010288ff]
[pkrvmf6wy0o8zjz:60116] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f05014a5ff5]
[pkrvmf6wy0o8zjz:60116] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f05014bb0da]
[pkrvmf6wy0o8zjz:60116] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f05014a5a55]
[pkrvmf6wy0o8zjz:60116] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f05014a5a6f]
[pkrvmf6wy0o8zjz:60116] [ 8] plumed(+0x13209)[0x55685a308209]
[pkrvmf6wy0o8zjz:60116] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f050102a1ca]
[pkrvmf6wy0o8zjz:60116] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f050102a28b]
[pkrvmf6wy0o8zjz:60116] [11] plumed(+0x134a5)[0x55685a3084a5]
[pkrvmf6wy0o8zjz:60116] *** End of error message ***
</pre>
{% endraw %}
