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
[fv-az1690-151:06229] *** Process received signal ***
[fv-az1690-151:06229] Signal: Aborted (6)
[fv-az1690-151:06229] Signal code:  (-6)
[fv-az1690-151:06229] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9850645330]
[fv-az1690-151:06229] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f985069eb2c]
[fv-az1690-151:06229] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f985064527e]
[fv-az1690-151:06229] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f98506288ff]
[fv-az1690-151:06229] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9850aa5ff5]
[fv-az1690-151:06229] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9850abb0da]
[fv-az1690-151:06229] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9850aa5a55]
[fv-az1690-151:06229] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9850aa5a6f]
[fv-az1690-151:06229] [ 8] plumed(+0x13209)[0x55a180a54209]
[fv-az1690-151:06229] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f985062a1ca]
[fv-az1690-151:06229] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f985062a28b]
[fv-az1690-151:06229] [11] plumed(+0x134a5)[0x55a180a544a5]
[fv-az1690-151:06229] *** End of error message ***
</pre>
{% endraw %}
