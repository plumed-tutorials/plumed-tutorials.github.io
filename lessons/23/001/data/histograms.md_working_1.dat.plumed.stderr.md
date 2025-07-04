Stderr for source:  histograms.md_working_1.dat   
Download: [zipped raw stdout](histograms.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](histograms.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @2 : keyword GRID is compulsory for this action
[pkrvmbietmlfzoi:36693] *** Process received signal ***
[pkrvmbietmlfzoi:36693] Signal: Aborted (6)
[pkrvmbietmlfzoi:36693] Signal code:  (-6)
[pkrvmbietmlfzoi:36693] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff059045330]
[pkrvmbietmlfzoi:36693] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff05909eb2c]
[pkrvmbietmlfzoi:36693] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff05904527e]
[pkrvmbietmlfzoi:36693] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff0590288ff]
[pkrvmbietmlfzoi:36693] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff0594a5ff5]
[pkrvmbietmlfzoi:36693] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff0594bb0da]
[pkrvmbietmlfzoi:36693] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff0594a5a55]
[pkrvmbietmlfzoi:36693] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff0594a5a6f]
[pkrvmbietmlfzoi:36693] [ 8] plumed(+0x13209)[0x563fde5ad209]
[pkrvmbietmlfzoi:36693] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff05902a1ca]
[pkrvmbietmlfzoi:36693] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff05902a28b]
[pkrvmbietmlfzoi:36693] [11] plumed(+0x134a5)[0x563fde5ad4a5]
[pkrvmbietmlfzoi:36693] *** End of error message ***
</pre>
{% endraw %}
