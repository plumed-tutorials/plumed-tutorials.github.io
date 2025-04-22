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
[fv-az2211-783:05639] *** Process received signal ***
[fv-az2211-783:05639] Signal: Aborted (6)
[fv-az2211-783:05639] Signal code:  (-6)
[fv-az2211-783:05639] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff35cc45330]
[fv-az2211-783:05639] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff35cc9eb2c]
[fv-az2211-783:05639] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff35cc4527e]
[fv-az2211-783:05639] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff35cc288ff]
[fv-az2211-783:05639] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff35d0a5ff5]
[fv-az2211-783:05639] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff35d0bb0da]
[fv-az2211-783:05639] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff35d0a5a55]
[fv-az2211-783:05639] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff35d0a5a6f]
[fv-az2211-783:05639] [ 8] plumed(+0x13209)[0x564b4ed56209]
[fv-az2211-783:05639] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff35cc2a1ca]
[fv-az2211-783:05639] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff35cc2a28b]
[fv-az2211-783:05639] [11] plumed(+0x134a5)[0x564b4ed564a5]
[fv-az2211-783:05639] *** End of error message ***
</pre>
{% endraw %}
