Stderr for source:  RMSD.md_working_4.dat   
Download: [zipped raw stdout](RMSD.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(reference/MetricRegister.h:105) std::unique_ptr<_Tp> PLMD::MetricRegister::create(const std::string&, const PLMD::PDB&) [with T = PLMD::ReferenceConfiguration; std::string = std::__cxx11::basic_string<char>]
+++ assertion failed: rtype.length()>0
TYPE not specified in pdb input file
[pkrvmbietmlfzoi:37336] *** Process received signal ***
[pkrvmbietmlfzoi:37336] Signal: Aborted (6)
[pkrvmbietmlfzoi:37336] Signal code:  (-6)
[pkrvmbietmlfzoi:37336] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff213445330]
[pkrvmbietmlfzoi:37336] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff21349eb2c]
[pkrvmbietmlfzoi:37336] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff21344527e]
[pkrvmbietmlfzoi:37336] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff2134288ff]
[pkrvmbietmlfzoi:37336] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff2138a5ff5]
[pkrvmbietmlfzoi:37336] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff2138bb0da]
[pkrvmbietmlfzoi:37336] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff2138a5a55]
[pkrvmbietmlfzoi:37336] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff2138a5a6f]
[pkrvmbietmlfzoi:37336] [ 8] plumed(+0x13209)[0x5588be732209]
[pkrvmbietmlfzoi:37336] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff21342a1ca]
[pkrvmbietmlfzoi:37336] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff21342a28b]
[pkrvmbietmlfzoi:37336] [11] plumed(+0x134a5)[0x5588be7324a5]
[pkrvmbietmlfzoi:37336] *** End of error message ***
</pre>
{% endraw %}
