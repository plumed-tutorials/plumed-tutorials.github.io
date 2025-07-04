Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmbietmlfzoi:34883] *** Process received signal ***
[pkrvmbietmlfzoi:34883] Signal: Aborted (6)
[pkrvmbietmlfzoi:34883] Signal code:  (-6)
[pkrvmbietmlfzoi:34883] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f32b4445330]
[pkrvmbietmlfzoi:34883] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f32b449eb2c]
[pkrvmbietmlfzoi:34883] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f32b444527e]
[pkrvmbietmlfzoi:34883] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f32b44288ff]
[pkrvmbietmlfzoi:34883] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f32b48a5ff5]
[pkrvmbietmlfzoi:34883] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f32b48bb0da]
[pkrvmbietmlfzoi:34883] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f32b48a5a55]
[pkrvmbietmlfzoi:34883] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f32b48a5a6f]
[pkrvmbietmlfzoi:34883] [ 8] plumed_master(+0x146dd)[0x56204e2be6dd]
[pkrvmbietmlfzoi:34883] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f32b442a1ca]
[pkrvmbietmlfzoi:34883] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f32b442a28b]
[pkrvmbietmlfzoi:34883] [11] plumed_master(+0x15365)[0x56204e2bf365]
[pkrvmbietmlfzoi:34883] *** End of error message ***
</pre>
{% endraw %}
