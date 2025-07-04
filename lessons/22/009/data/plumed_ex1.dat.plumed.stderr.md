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
[pkrvmbietmlfzoi:35450] *** Process received signal ***
[pkrvmbietmlfzoi:35450] Signal: Aborted (6)
[pkrvmbietmlfzoi:35450] Signal code:  (-6)
[pkrvmbietmlfzoi:35450] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4be7a45330]
[pkrvmbietmlfzoi:35450] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4be7a9eb2c]
[pkrvmbietmlfzoi:35450] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4be7a4527e]
[pkrvmbietmlfzoi:35450] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4be7a288ff]
[pkrvmbietmlfzoi:35450] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4be7ea5ff5]
[pkrvmbietmlfzoi:35450] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4be7ebb0da]
[pkrvmbietmlfzoi:35450] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4be7ea5a55]
[pkrvmbietmlfzoi:35450] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4be7ea5a6f]
[pkrvmbietmlfzoi:35450] [ 8] plumed(+0x13209)[0x55c7ab2d0209]
[pkrvmbietmlfzoi:35450] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4be7a2a1ca]
[pkrvmbietmlfzoi:35450] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4be7a2a28b]
[pkrvmbietmlfzoi:35450] [11] plumed(+0x134a5)[0x55c7ab2d04a5]
[pkrvmbietmlfzoi:35450] *** End of error message ***
</pre>
{% endraw %}
