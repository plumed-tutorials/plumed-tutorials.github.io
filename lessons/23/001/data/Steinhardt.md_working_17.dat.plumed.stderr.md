Stderr for source:  Steinhardt.md_working_17.dat   
Download: [zipped raw stdout](Steinhardt.md_working_17.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_17.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:35780] *** Process received signal ***
[pkrvmbietmlfzoi:35780] Signal: Aborted (6)
[pkrvmbietmlfzoi:35780] Signal code:  (-6)
[pkrvmbietmlfzoi:35780] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2d1f645330]
[pkrvmbietmlfzoi:35780] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2d1f69eb2c]
[pkrvmbietmlfzoi:35780] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2d1f64527e]
[pkrvmbietmlfzoi:35780] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2d1f6288ff]
[pkrvmbietmlfzoi:35780] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2d1faa5ff5]
[pkrvmbietmlfzoi:35780] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2d1fabb0da]
[pkrvmbietmlfzoi:35780] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2d1faa5a55]
[pkrvmbietmlfzoi:35780] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2d1faa5a6f]
[pkrvmbietmlfzoi:35780] [ 8] plumed(+0x13209)[0x557ff3ccc209]
[pkrvmbietmlfzoi:35780] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2d1f62a1ca]
[pkrvmbietmlfzoi:35780] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2d1f62a28b]
[pkrvmbietmlfzoi:35780] [11] plumed(+0x134a5)[0x557ff3ccc4a5]
[pkrvmbietmlfzoi:35780] *** End of error message ***
</pre>
{% endraw %}
