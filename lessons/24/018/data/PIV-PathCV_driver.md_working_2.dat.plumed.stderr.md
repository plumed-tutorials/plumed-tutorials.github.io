Stderr for source:  PIV-PathCV_driver.md_working_2.dat   
Download: [zipped raw stdout](PIV-PathCV_driver.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_driver.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action FUNCPATHMSD with label p1 : cannot find action named c1 (hint! the actions with value in this ActionSet are: )
[pkrvmbietmlfzoi:34810] *** Process received signal ***
[pkrvmbietmlfzoi:34810] Signal: Aborted (6)
[pkrvmbietmlfzoi:34810] Signal code:  (-6)
[pkrvmbietmlfzoi:34810] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7aeea45330]
[pkrvmbietmlfzoi:34810] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7aeea9eb2c]
[pkrvmbietmlfzoi:34810] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7aeea4527e]
[pkrvmbietmlfzoi:34810] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7aeea288ff]
[pkrvmbietmlfzoi:34810] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7aeeea5ff5]
[pkrvmbietmlfzoi:34810] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7aeeebb0da]
[pkrvmbietmlfzoi:34810] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7aeeea5a55]
[pkrvmbietmlfzoi:34810] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7aeeea5a6f]
[pkrvmbietmlfzoi:34810] [ 8] plumed(+0x13209)[0x55aa6bb6d209]
[pkrvmbietmlfzoi:34810] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7aeea2a1ca]
[pkrvmbietmlfzoi:34810] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7aeea2a28b]
[pkrvmbietmlfzoi:34810] [11] plumed(+0x134a5)[0x55aa6bb6d4a5]
[pkrvmbietmlfzoi:34810] *** End of error message ***
</pre>
{% endraw %}
