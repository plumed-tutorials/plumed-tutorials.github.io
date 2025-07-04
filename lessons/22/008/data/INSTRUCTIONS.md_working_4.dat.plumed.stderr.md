Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: CMUMD LABEL=left GROUP=lj NSV=1 FIXED=0.4 DCR=0.25 CRSIZE=0.1 WF=0.0001 ASYMM=-1 NINT=0.1 NZ=291
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:35621] *** Process received signal ***
[pkrvmbietmlfzoi:35621] Signal: Aborted (6)
[pkrvmbietmlfzoi:35621] Signal code:  (-6)
[pkrvmbietmlfzoi:35621] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f39e1a45330]
[pkrvmbietmlfzoi:35621] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f39e1a9eb2c]
[pkrvmbietmlfzoi:35621] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f39e1a4527e]
[pkrvmbietmlfzoi:35621] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f39e1a288ff]
[pkrvmbietmlfzoi:35621] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f39e1ea5ff5]
[pkrvmbietmlfzoi:35621] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f39e1ebb0da]
[pkrvmbietmlfzoi:35621] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f39e1ea5a55]
[pkrvmbietmlfzoi:35621] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f39e1ea5a6f]
[pkrvmbietmlfzoi:35621] [ 8] plumed(+0x13209)[0x55b0c647a209]
[pkrvmbietmlfzoi:35621] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f39e1a2a1ca]
[pkrvmbietmlfzoi:35621] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f39e1a2a28b]
[pkrvmbietmlfzoi:35621] [11] plumed(+0x134a5)[0x55b0c647a4a5]
[pkrvmbietmlfzoi:35621] *** End of error message ***
</pre>
{% endraw %}
