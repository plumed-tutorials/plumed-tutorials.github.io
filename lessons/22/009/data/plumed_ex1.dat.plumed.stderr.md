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
[fv-az2211-783:07047] *** Process received signal ***
[fv-az2211-783:07047] Signal: Aborted (6)
[fv-az2211-783:07047] Signal code:  (-6)
[fv-az2211-783:07047] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f97a7245330]
[fv-az2211-783:07047] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f97a729eb2c]
[fv-az2211-783:07047] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f97a724527e]
[fv-az2211-783:07047] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f97a72288ff]
[fv-az2211-783:07047] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f97a76a5ff5]
[fv-az2211-783:07047] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f97a76bb0da]
[fv-az2211-783:07047] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f97a76a5a55]
[fv-az2211-783:07047] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f97a76a5a6f]
[fv-az2211-783:07047] [ 8] plumed(+0x13209)[0x561b00f60209]
[fv-az2211-783:07047] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f97a722a1ca]
[fv-az2211-783:07047] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f97a722a28b]
[fv-az2211-783:07047] [11] plumed(+0x134a5)[0x561b00f604a5]
[fv-az2211-783:07047] *** End of error message ***
</pre>
{% endraw %}
