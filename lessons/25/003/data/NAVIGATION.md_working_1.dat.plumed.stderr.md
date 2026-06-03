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
[runnervm3jyl0:46498] *** Process received signal ***
[runnervm3jyl0:46498] Signal: Aborted (6)
[runnervm3jyl0:46498] Signal code:  (-6)
[runnervm3jyl0:46498] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fda88a45330]
[runnervm3jyl0:46498] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fda88a9eb2c]
[runnervm3jyl0:46498] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fda88a4527e]
[runnervm3jyl0:46498] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fda88a288ff]
[runnervm3jyl0:46498] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fda88ea5ff5]
[runnervm3jyl0:46498] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fda88ebb0da]
[runnervm3jyl0:46498] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fda88ea5a55]
[runnervm3jyl0:46498] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fda88ea5a6f]
[runnervm3jyl0:46498] [ 8] plumed(+0x13209)[0x560d4a3db209]
[runnervm3jyl0:46498] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fda88a2a1ca]
[runnervm3jyl0:46498] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fda88a2a28b]
[runnervm3jyl0:46498] [11] plumed(+0x134a5)[0x560d4a3db4a5]
[runnervm3jyl0:46498] *** End of error message ***
</pre>
{% endraw %}
