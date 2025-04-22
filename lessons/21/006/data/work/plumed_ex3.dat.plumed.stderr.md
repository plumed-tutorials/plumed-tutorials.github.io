Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LANDMARK_SELECT_FPS with label fps : input analysis action was not specified use USE_OUTPUT_DATA_FROM
[fv-az2211-783:07239] *** Process received signal ***
[fv-az2211-783:07239] Signal: Aborted (6)
[fv-az2211-783:07239] Signal code:  (-6)
[fv-az2211-783:07239] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7196445330]
[fv-az2211-783:07239] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f719649eb2c]
[fv-az2211-783:07239] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f719644527e]
[fv-az2211-783:07239] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f71964288ff]
[fv-az2211-783:07239] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f71968a5ff5]
[fv-az2211-783:07239] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f71968bb0da]
[fv-az2211-783:07239] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f71968a5a55]
[fv-az2211-783:07239] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f71968a5a6f]
[fv-az2211-783:07239] [ 8] plumed(+0x13209)[0x55b62b0e6209]
[fv-az2211-783:07239] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f719642a1ca]
[fv-az2211-783:07239] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f719642a28b]
[fv-az2211-783:07239] [11] plumed(+0x134a5)[0x55b62b0e64a5]
[fv-az2211-783:07239] *** End of error message ***
</pre>
{% endraw %}
