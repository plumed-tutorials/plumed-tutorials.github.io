Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az2211-783:06848] *** Process received signal ***
[fv-az2211-783:06848] Signal: Aborted (6)
[fv-az2211-783:06848] Signal code:  (-6)
[fv-az2211-783:06848] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f62b6645330]
[fv-az2211-783:06848] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f62b669eb2c]
[fv-az2211-783:06848] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f62b664527e]
[fv-az2211-783:06848] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f62b66288ff]
[fv-az2211-783:06848] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f62b6aa5ff5]
[fv-az2211-783:06848] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f62b6abb0da]
[fv-az2211-783:06848] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f62b6aa5a55]
[fv-az2211-783:06848] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f62b6aa5a6f]
[fv-az2211-783:06848] [ 8] plumed(+0x13209)[0x5647b634a209]
[fv-az2211-783:06848] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f62b662a1ca]
[fv-az2211-783:06848] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f62b662a28b]
[fv-az2211-783:06848] [11] plumed(+0x134a5)[0x5647b634a4a5]
[fv-az2211-783:06848] *** End of error message ***
</pre>
{% endraw %}
