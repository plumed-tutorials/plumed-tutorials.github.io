Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: timestep kBT posx posy posz Masses Charges Box driver )
[pkrvmbietmlfzoi:34826] *** Process received signal ***
[pkrvmbietmlfzoi:34826] Signal: Aborted (6)
[pkrvmbietmlfzoi:34826] Signal code:  (-6)
[pkrvmbietmlfzoi:34826] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fca4c445330]
[pkrvmbietmlfzoi:34826] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fca4c49eb2c]
[pkrvmbietmlfzoi:34826] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fca4c44527e]
[pkrvmbietmlfzoi:34826] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fca4c4288ff]
[pkrvmbietmlfzoi:34826] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fca4c8a5ff5]
[pkrvmbietmlfzoi:34826] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fca4c8bb0da]
[pkrvmbietmlfzoi:34826] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fca4c8a5a55]
[pkrvmbietmlfzoi:34826] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fca4c8a5a6f]
[pkrvmbietmlfzoi:34826] [ 8] plumed_master(+0x146dd)[0x55b7033f06dd]
[pkrvmbietmlfzoi:34826] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fca4c42a1ca]
[pkrvmbietmlfzoi:34826] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fca4c42a28b]
[pkrvmbietmlfzoi:34826] [11] plumed_master(+0x15365)[0x55b7033f1365]
[pkrvmbietmlfzoi:34826] *** End of error message ***
</pre>
{% endraw %}
