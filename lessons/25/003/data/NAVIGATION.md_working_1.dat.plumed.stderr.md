Stderr for source:  NAVIGATION.md_working_1.dat   
Download: [zipped raw stdout](NAVIGATION.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](NAVIGATION.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: METATOMIC LABEL=soap MODEL=soap-cv.pt EXTENSIONS_DIRECTORY=./extensions/ SPECIES1=1-38 SPECIES_TO_TYPES=18
Maybe a missing space or a typo?
[pkrvmbietmlfzoi:34586] *** Process received signal ***
[pkrvmbietmlfzoi:34586] Signal: Aborted (6)
[pkrvmbietmlfzoi:34586] Signal code:  (-6)
[pkrvmbietmlfzoi:34586] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6835845330]
[pkrvmbietmlfzoi:34586] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f683589eb2c]
[pkrvmbietmlfzoi:34586] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f683584527e]
[pkrvmbietmlfzoi:34586] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f68358288ff]
[pkrvmbietmlfzoi:34586] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6835ca5ff5]
[pkrvmbietmlfzoi:34586] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6835cbb0da]
[pkrvmbietmlfzoi:34586] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6835ca5a55]
[pkrvmbietmlfzoi:34586] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6835ca5a6f]
[pkrvmbietmlfzoi:34586] [ 8] plumed(+0x13209)[0x55bb46d59209]
[pkrvmbietmlfzoi:34586] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f683582a1ca]
[pkrvmbietmlfzoi:34586] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f683582a28b]
[pkrvmbietmlfzoi:34586] [11] plumed(+0x134a5)[0x55bb46d594a5]
[pkrvmbietmlfzoi:34586] *** End of error message ***
</pre>
{% endraw %}
