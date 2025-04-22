Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az2211-783:05967] *** Process received signal ***
[fv-az2211-783:05967] Signal: Aborted (6)
[fv-az2211-783:05967] Signal code:  (-6)
[fv-az2211-783:05967] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3e57645330]
[fv-az2211-783:05967] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3e5769eb2c]
[fv-az2211-783:05967] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3e5764527e]
[fv-az2211-783:05967] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3e576288ff]
[fv-az2211-783:05967] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f3e57aa5ff5]
[fv-az2211-783:05967] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f3e57abb0da]
[fv-az2211-783:05967] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f3e57aa5a55]
[fv-az2211-783:05967] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f3e57aa5a6f]
[fv-az2211-783:05967] [ 8] plumed(+0x13209)[0x55ce1f3a3209]
[fv-az2211-783:05967] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3e5762a1ca]
[fv-az2211-783:05967] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3e5762a28b]
[fv-az2211-783:05967] [11] plumed(+0x134a5)[0x55ce1f3a34a5]
[fv-az2211-783:05967] *** End of error message ***
</pre>
{% endraw %}
