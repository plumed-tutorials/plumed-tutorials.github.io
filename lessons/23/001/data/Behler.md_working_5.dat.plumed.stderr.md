Stderr for source:  Behler.md_working_5.dat   
Download: [zipped raw stdout](Behler.md_working_5.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Behler.md_working_5.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[pkrvmbietmlfzoi:36098] *** Process received signal ***
[pkrvmbietmlfzoi:36098] Signal: Aborted (6)
[pkrvmbietmlfzoi:36098] Signal code:  (-6)
[pkrvmbietmlfzoi:36098] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fbbef045330]
[pkrvmbietmlfzoi:36098] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fbbef09eb2c]
[pkrvmbietmlfzoi:36098] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fbbef04527e]
[pkrvmbietmlfzoi:36098] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fbbef0288ff]
[pkrvmbietmlfzoi:36098] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fbbef4a5ff5]
[pkrvmbietmlfzoi:36098] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fbbef4bb0da]
[pkrvmbietmlfzoi:36098] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fbbef4a5a55]
[pkrvmbietmlfzoi:36098] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fbbef4a5a6f]
[pkrvmbietmlfzoi:36098] [ 8] plumed(+0x13209)[0x55e87a727209]
[pkrvmbietmlfzoi:36098] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fbbef02a1ca]
[pkrvmbietmlfzoi:36098] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fbbef02a28b]
[pkrvmbietmlfzoi:36098] [11] plumed(+0x134a5)[0x55e87a7274a5]
[pkrvmbietmlfzoi:36098] *** End of error message ***
</pre>
{% endraw %}
