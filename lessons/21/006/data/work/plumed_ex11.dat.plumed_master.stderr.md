Stderr for source:  work/plumed_ex11.dat   
Download: [zipped raw stdout](plumed_ex11.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex11.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @64 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:36285] *** Process received signal ***
[pkrvmbietmlfzoi:36285] Signal: Aborted (6)
[pkrvmbietmlfzoi:36285] Signal code:  (-6)
[pkrvmbietmlfzoi:36285] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd042645330]
[pkrvmbietmlfzoi:36285] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd04269eb2c]
[pkrvmbietmlfzoi:36285] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd04264527e]
[pkrvmbietmlfzoi:36285] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd0426288ff]
[pkrvmbietmlfzoi:36285] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd042aa5ff5]
[pkrvmbietmlfzoi:36285] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd042abb0da]
[pkrvmbietmlfzoi:36285] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd042aa5a55]
[pkrvmbietmlfzoi:36285] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd042aa5a6f]
[pkrvmbietmlfzoi:36285] [ 8] plumed_master(+0x146dd)[0x563c42e566dd]
[pkrvmbietmlfzoi:36285] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd04262a1ca]
[pkrvmbietmlfzoi:36285] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd04262a28b]
[pkrvmbietmlfzoi:36285] [11] plumed_master(+0x15365)[0x563c42e57365]
[pkrvmbietmlfzoi:36285] *** End of error message ***
</pre>
{% endraw %}
