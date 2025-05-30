Stderr for source:  Path.md_working_3.dat   
Download: [zipped raw stdout](Path.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GPATH LABEL=pp ARG=t1,t2 REFERENCE=epath.pdb
Maybe a missing space or a typo?
[pkrvmf6wy0o8zjz:61878] *** Process received signal ***
[pkrvmf6wy0o8zjz:61878] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:61878] Signal code:  (-6)
[pkrvmf6wy0o8zjz:61878] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7facd6045330]
[pkrvmf6wy0o8zjz:61878] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7facd609eb2c]
[pkrvmf6wy0o8zjz:61878] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7facd604527e]
[pkrvmf6wy0o8zjz:61878] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7facd60288ff]
[pkrvmf6wy0o8zjz:61878] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7facd64a5ff5]
[pkrvmf6wy0o8zjz:61878] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7facd64bb0da]
[pkrvmf6wy0o8zjz:61878] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7facd64a5a55]
[pkrvmf6wy0o8zjz:61878] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7facd64a5a6f]
[pkrvmf6wy0o8zjz:61878] [ 8] plumed(+0x13209)[0x5585ed55f209]
[pkrvmf6wy0o8zjz:61878] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7facd602a1ca]
[pkrvmf6wy0o8zjz:61878] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7facd602a28b]
[pkrvmf6wy0o8zjz:61878] [11] plumed(+0x134a5)[0x5585ed55f4a5]
[pkrvmf6wy0o8zjz:61878] *** End of error message ***
</pre>
{% endraw %}
