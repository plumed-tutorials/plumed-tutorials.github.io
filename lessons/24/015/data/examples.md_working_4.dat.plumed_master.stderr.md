Stderr for source:  examples.md_working_4.dat   
Download: [zipped raw stdout](examples.md_working_4.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_4.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmbietmlfzoi:35394] *** Process received signal ***
[pkrvmbietmlfzoi:35394] Signal: Aborted (6)
[pkrvmbietmlfzoi:35394] Signal code:  (-6)
[pkrvmbietmlfzoi:35394] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc685a45330]
[pkrvmbietmlfzoi:35394] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc685a9eb2c]
[pkrvmbietmlfzoi:35394] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc685a4527e]
[pkrvmbietmlfzoi:35394] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc685a288ff]
[pkrvmbietmlfzoi:35394] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc685ea5ff5]
[pkrvmbietmlfzoi:35394] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc685ebb0da]
[pkrvmbietmlfzoi:35394] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc685ea5a55]
[pkrvmbietmlfzoi:35394] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc685ea5a6f]
[pkrvmbietmlfzoi:35394] [ 8] plumed_master(+0x146dd)[0x562732fda6dd]
[pkrvmbietmlfzoi:35394] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc685a2a1ca]
[pkrvmbietmlfzoi:35394] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc685a2a28b]
[pkrvmbietmlfzoi:35394] [11] plumed_master(+0x15365)[0x562732fdb365]
[pkrvmbietmlfzoi:35394] *** End of error message ***
</pre>
{% endraw %}
