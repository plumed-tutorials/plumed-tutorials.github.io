Stderr for source:  work/plumed_ex4.dat   
Download: [zipped raw stdout](plumed_ex4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DUMPPDB ATOMS=cc_data ATOM_INDICES=@nonhydrogens FILE=traj.pdb
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:36099] *** Process received signal ***
[pkrvmbietmlfzoi:36099] Signal: Aborted (6)
[pkrvmbietmlfzoi:36099] Signal code:  (-6)
[pkrvmbietmlfzoi:36099] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f1f32c45330]
[pkrvmbietmlfzoi:36099] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f1f32c9eb2c]
[pkrvmbietmlfzoi:36099] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f1f32c4527e]
[pkrvmbietmlfzoi:36099] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f1f32c288ff]
[pkrvmbietmlfzoi:36099] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f1f330a5ff5]
[pkrvmbietmlfzoi:36099] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f1f330bb0da]
[pkrvmbietmlfzoi:36099] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f1f330a5a55]
[pkrvmbietmlfzoi:36099] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f1f330a5a6f]
[pkrvmbietmlfzoi:36099] [ 8] plumed(+0x13209)[0x55e2bcaf6209]
[pkrvmbietmlfzoi:36099] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f1f32c2a1ca]
[pkrvmbietmlfzoi:36099] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f1f32c2a28b]
[pkrvmbietmlfzoi:36099] [11] plumed(+0x134a5)[0x55e2bcaf64a5]
[pkrvmbietmlfzoi:36099] *** End of error message ***
</pre>
{% endraw %}
