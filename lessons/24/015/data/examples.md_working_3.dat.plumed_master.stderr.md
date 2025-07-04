Stderr for source:  examples.md_working_3.dat   
Download: [zipped raw stdout](examples.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](examples.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:373) void PLMD::Action::error(const std::string&) const
ERROR in input to action LOAD with label @0 : cannot understand the following words from the input line : GLOBAL
[pkrvmbietmlfzoi:35350] *** Process received signal ***
[pkrvmbietmlfzoi:35350] Signal: Aborted (6)
[pkrvmbietmlfzoi:35350] Signal code:  (-6)
[pkrvmbietmlfzoi:35350] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa41b845330]
[pkrvmbietmlfzoi:35350] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa41b89eb2c]
[pkrvmbietmlfzoi:35350] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa41b84527e]
[pkrvmbietmlfzoi:35350] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa41b8288ff]
[pkrvmbietmlfzoi:35350] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa41bca5ff5]
[pkrvmbietmlfzoi:35350] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa41bcbb0da]
[pkrvmbietmlfzoi:35350] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa41bca5a55]
[pkrvmbietmlfzoi:35350] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa41bca5a6f]
[pkrvmbietmlfzoi:35350] [ 8] plumed_master(+0x146dd)[0x559171ca96dd]
[pkrvmbietmlfzoi:35350] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa41b82a1ca]
[pkrvmbietmlfzoi:35350] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa41b82a28b]
[pkrvmbietmlfzoi:35350] [11] plumed_master(+0x15365)[0x559171caa365]
[pkrvmbietmlfzoi:35350] *** End of error message ***
</pre>
{% endraw %}
