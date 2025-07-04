Stderr for source:  work/plumed_ex3.dat   
Download: [zipped raw stdout](plumed_ex3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](plumed_ex3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action LANDMARK_SELECT_FPS with label fps : input analysis action was not specified use USE_OUTPUT_DATA_FROM
[pkrvmbietmlfzoi:36068] *** Process received signal ***
[pkrvmbietmlfzoi:36068] Signal: Aborted (6)
[pkrvmbietmlfzoi:36068] Signal code:  (-6)
[pkrvmbietmlfzoi:36068] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6c86a45330]
[pkrvmbietmlfzoi:36068] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6c86a9eb2c]
[pkrvmbietmlfzoi:36068] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6c86a4527e]
[pkrvmbietmlfzoi:36068] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6c86a288ff]
[pkrvmbietmlfzoi:36068] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6c86ea5ff5]
[pkrvmbietmlfzoi:36068] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6c86ebb0da]
[pkrvmbietmlfzoi:36068] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6c86ea5a55]
[pkrvmbietmlfzoi:36068] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6c86ea5a6f]
[pkrvmbietmlfzoi:36068] [ 8] plumed(+0x13209)[0x5638e8871209]
[pkrvmbietmlfzoi:36068] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6c86a2a1ca]
[pkrvmbietmlfzoi:36068] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6c86a2a28b]
[pkrvmbietmlfzoi:36068] [11] plumed(+0x134a5)[0x5638e88714a5]
[pkrvmbietmlfzoi:36068] *** End of error message ***
</pre>
{% endraw %}
