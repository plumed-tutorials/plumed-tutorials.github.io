Stderr for source:  Steinhardt.md_working_15.dat   
Download: [zipped raw stdout](Steinhardt.md_working_15.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_15.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35716] *** Process received signal ***
[pkrvmbietmlfzoi:35716] Signal: Aborted (6)
[pkrvmbietmlfzoi:35716] Signal code:  (-6)
[pkrvmbietmlfzoi:35716] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5442a45330]
[pkrvmbietmlfzoi:35716] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5442a9eb2c]
[pkrvmbietmlfzoi:35716] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5442a4527e]
[pkrvmbietmlfzoi:35716] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5442a288ff]
[pkrvmbietmlfzoi:35716] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5442ea5ff5]
[pkrvmbietmlfzoi:35716] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5442ebb0da]
[pkrvmbietmlfzoi:35716] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5442ea5a55]
[pkrvmbietmlfzoi:35716] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5442ea5a6f]
[pkrvmbietmlfzoi:35716] [ 8] plumed(+0x13209)[0x5624dca7e209]
[pkrvmbietmlfzoi:35716] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5442a2a1ca]
[pkrvmbietmlfzoi:35716] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5442a2a28b]
[pkrvmbietmlfzoi:35716] [11] plumed(+0x134a5)[0x5624dca7e4a5]
[pkrvmbietmlfzoi:35716] *** End of error message ***
</pre>
{% endraw %}
