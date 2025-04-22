Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az2211-783:06011] *** Process received signal ***
[fv-az2211-783:06011] Signal: Aborted (6)
[fv-az2211-783:06011] Signal code:  (-6)
[fv-az2211-783:06011] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd616e45330]
[fv-az2211-783:06011] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd616e9eb2c]
[fv-az2211-783:06011] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd616e4527e]
[fv-az2211-783:06011] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd616e288ff]
[fv-az2211-783:06011] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd6172a5ff5]
[fv-az2211-783:06011] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd6172bb0da]
[fv-az2211-783:06011] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd6172a5a55]
[fv-az2211-783:06011] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd6172a5a6f]
[fv-az2211-783:06011] [ 8] plumed(+0x13209)[0x5609e9a8b209]
[fv-az2211-783:06011] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd616e2a1ca]
[fv-az2211-783:06011] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd616e2a28b]
[fv-az2211-783:06011] [11] plumed(+0x134a5)[0x5609e9a8b4a5]
[fv-az2211-783:06011] *** End of error message ***
</pre>
{% endraw %}
