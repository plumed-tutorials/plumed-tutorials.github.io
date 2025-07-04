Stderr for source:  PIV-PathCV_meta.md_working_4.dat   
Download: [zipped raw stdout](PIV-PathCV_meta.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](PIV-PathCV_meta.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GMX grompp -f md.mdp -c Liq.pdb -p TIP4P.top -o meta.tpr
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:34978] *** Process received signal ***
[pkrvmbietmlfzoi:34978] Signal: Aborted (6)
[pkrvmbietmlfzoi:34978] Signal code:  (-6)
[pkrvmbietmlfzoi:34978] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa3f2245330]
[pkrvmbietmlfzoi:34978] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa3f229eb2c]
[pkrvmbietmlfzoi:34978] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa3f224527e]
[pkrvmbietmlfzoi:34978] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa3f22288ff]
[pkrvmbietmlfzoi:34978] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa3f26a5ff5]
[pkrvmbietmlfzoi:34978] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa3f26bb0da]
[pkrvmbietmlfzoi:34978] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa3f26a5a55]
[pkrvmbietmlfzoi:34978] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa3f26a5a6f]
[pkrvmbietmlfzoi:34978] [ 8] plumed(+0x13209)[0x55ffa98cf209]
[pkrvmbietmlfzoi:34978] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa3f222a1ca]
[pkrvmbietmlfzoi:34978] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa3f222a28b]
[pkrvmbietmlfzoi:34978] [11] plumed(+0x134a5)[0x55ffa98cf4a5]
[pkrvmbietmlfzoi:34978] *** End of error message ***
</pre>
{% endraw %}
