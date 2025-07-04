Stderr for source:  ./solutions/walker-0/plumed_reweight.dat   
Download: [zipped raw stdout](plumed_reweight.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_reweight.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @32 : keyword ARG is compulsory for this action
[pkrvmbietmlfzoi:34839] *** Process received signal ***
[pkrvmbietmlfzoi:34839] Signal: Aborted (6)
[pkrvmbietmlfzoi:34839] Signal code:  (-6)
[pkrvmbietmlfzoi:34839] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6cebc45330]
[pkrvmbietmlfzoi:34839] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6cebc9eb2c]
[pkrvmbietmlfzoi:34839] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6cebc4527e]
[pkrvmbietmlfzoi:34839] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6cebc288ff]
[pkrvmbietmlfzoi:34839] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6cec0a5ff5]
[pkrvmbietmlfzoi:34839] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6cec0bb0da]
[pkrvmbietmlfzoi:34839] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6cec0a5a55]
[pkrvmbietmlfzoi:34839] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6cec0a5a6f]
[pkrvmbietmlfzoi:34839] [ 8] plumed_master(+0x146dd)[0x558084b356dd]
[pkrvmbietmlfzoi:34839] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6cebc2a1ca]
[pkrvmbietmlfzoi:34839] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6cebc2a28b]
[pkrvmbietmlfzoi:34839] [11] plumed_master(+0x15365)[0x558084b36365]
[pkrvmbietmlfzoi:34839] *** End of error message ***
</pre>
{% endraw %}
