Stderr for source:  PIV-PathCV_meta.md_working_1.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label res : cannot find action named p1 (hint! the actions with value in this ActionSet are: )
[pkrvmbietmlfzoi:34867] *** Process received signal ***
[pkrvmbietmlfzoi:34867] Signal: Aborted (6)
[pkrvmbietmlfzoi:34867] Signal code:  (-6)
[pkrvmbietmlfzoi:34867] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f5c95a45330]
[pkrvmbietmlfzoi:34867] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f5c95a9eb2c]
[pkrvmbietmlfzoi:34867] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f5c95a4527e]
[pkrvmbietmlfzoi:34867] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f5c95a288ff]
[pkrvmbietmlfzoi:34867] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f5c95ea5ff5]
[pkrvmbietmlfzoi:34867] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f5c95ebb0da]
[pkrvmbietmlfzoi:34867] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f5c95ea5a55]
[pkrvmbietmlfzoi:34867] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f5c95ea5a6f]
[pkrvmbietmlfzoi:34867] [ 8] plumed(+0x13209)[0x558484c69209]
[pkrvmbietmlfzoi:34867] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f5c95a2a1ca]
[pkrvmbietmlfzoi:34867] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f5c95a2a28b]
[pkrvmbietmlfzoi:34867] [11] plumed(+0x134a5)[0x558484c694a5]
[pkrvmbietmlfzoi:34867] *** End of error message ***
</pre>
{% endraw %}
