Stderr for source:  plumed_TDP-43.dat   
Download: [zipped raw stdout](plumed_TDP-43.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_TDP-43.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAINFERENCE with label af_mi_rest_domains : REWEIGHT can only be used in parallel with 2 or more replicas
[pkrvmf6wy0o8zjz:59027] *** Process received signal ***
[pkrvmf6wy0o8zjz:59027] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59027] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59027] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f0b17645330]
[pkrvmf6wy0o8zjz:59027] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f0b1769eb2c]
[pkrvmf6wy0o8zjz:59027] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f0b1764527e]
[pkrvmf6wy0o8zjz:59027] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f0b176288ff]
[pkrvmf6wy0o8zjz:59027] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f0b17aa5ff5]
[pkrvmf6wy0o8zjz:59027] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f0b17abb0da]
[pkrvmf6wy0o8zjz:59027] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f0b17aa5a55]
[pkrvmf6wy0o8zjz:59027] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f0b17aa5a6f]
[pkrvmf6wy0o8zjz:59027] [ 8] plumed(+0x13209)[0x555b9f91a209]
[pkrvmf6wy0o8zjz:59027] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f0b1762a1ca]
[pkrvmf6wy0o8zjz:59027] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f0b1762a28b]
[pkrvmf6wy0o8zjz:59027] [11] plumed(+0x134a5)[0x555b9f91a4a5]
[pkrvmf6wy0o8zjz:59027] *** End of error message ***
</pre>
{% endraw %}
