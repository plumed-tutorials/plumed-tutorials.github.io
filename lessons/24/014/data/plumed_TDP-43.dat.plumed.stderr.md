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
[pkrvmbietmlfzoi:35455] *** Process received signal ***
[pkrvmbietmlfzoi:35455] Signal: Aborted (6)
[pkrvmbietmlfzoi:35455] Signal code:  (-6)
[pkrvmbietmlfzoi:35455] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5123245330]
[pkrvmbietmlfzoi:35455] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f512329eb2c]
[pkrvmbietmlfzoi:35455] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f512324527e]
[pkrvmbietmlfzoi:35455] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f51232288ff]
[pkrvmbietmlfzoi:35455] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f51236a5ff5]
[pkrvmbietmlfzoi:35455] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f51236bb0da]
[pkrvmbietmlfzoi:35455] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f51236a5a55]
[pkrvmbietmlfzoi:35455] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f51236a5a6f]
[pkrvmbietmlfzoi:35455] [ 8] plumed(+0x13209)[0x55ccd3599209]
[pkrvmbietmlfzoi:35455] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f512322a1ca]
[pkrvmbietmlfzoi:35455] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f512322a28b]
[pkrvmbietmlfzoi:35455] [11] plumed(+0x134a5)[0x55ccd35994a5]
[pkrvmbietmlfzoi:35455] *** End of error message ***
</pre>
{% endraw %}
