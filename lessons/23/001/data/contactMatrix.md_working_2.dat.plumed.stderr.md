Stderr for source:  contactMatrix.md_working_2.dat   
Download: [zipped raw stdout](contactMatrix.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[pkrvmbietmlfzoi:34942] *** Process received signal ***
[pkrvmbietmlfzoi:34942] Signal: Aborted (6)
[pkrvmbietmlfzoi:34942] Signal code:  (-6)
[pkrvmbietmlfzoi:34942] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1011645330]
[pkrvmbietmlfzoi:34942] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f101169eb2c]
[pkrvmbietmlfzoi:34942] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f101164527e]
[pkrvmbietmlfzoi:34942] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f10116288ff]
[pkrvmbietmlfzoi:34942] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1011aa5ff5]
[pkrvmbietmlfzoi:34942] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1011abb0da]
[pkrvmbietmlfzoi:34942] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1011aa5a55]
[pkrvmbietmlfzoi:34942] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1011aa5a6f]
[pkrvmbietmlfzoi:34942] [ 8] plumed(+0x13209)[0x558b16709209]
[pkrvmbietmlfzoi:34942] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f101162a1ca]
[pkrvmbietmlfzoi:34942] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f101162a28b]
[pkrvmbietmlfzoi:34942] [11] plumed(+0x134a5)[0x558b167094a5]
[pkrvmbietmlfzoi:34942] *** End of error message ***
</pre>
{% endraw %}
