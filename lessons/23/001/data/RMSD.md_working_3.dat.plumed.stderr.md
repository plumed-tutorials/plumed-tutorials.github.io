Stderr for source:  RMSD.md_working_3.dat   
Download: [zipped raw stdout](RMSD.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(reference/MetricRegister.h:105) std::unique_ptr<_Tp> PLMD::MetricRegister::create(const std::string&, const PLMD::PDB&) [with T = PLMD::ReferenceConfiguration; std::string = std::__cxx11::basic_string<char>]
+++ assertion failed: rtype.length()>0
TYPE not specified in pdb input file
[pkrvmbietmlfzoi:37304] *** Process received signal ***
[pkrvmbietmlfzoi:37304] Signal: Aborted (6)
[pkrvmbietmlfzoi:37304] Signal code:  (-6)
[pkrvmbietmlfzoi:37304] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcff1645330]
[pkrvmbietmlfzoi:37304] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcff169eb2c]
[pkrvmbietmlfzoi:37304] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcff164527e]
[pkrvmbietmlfzoi:37304] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcff16288ff]
[pkrvmbietmlfzoi:37304] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcff1aa5ff5]
[pkrvmbietmlfzoi:37304] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcff1abb0da]
[pkrvmbietmlfzoi:37304] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcff1aa5a55]
[pkrvmbietmlfzoi:37304] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcff1aa5a6f]
[pkrvmbietmlfzoi:37304] [ 8] plumed(+0x13209)[0x55aa1fa31209]
[pkrvmbietmlfzoi:37304] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcff162a1ca]
[pkrvmbietmlfzoi:37304] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcff162a28b]
[pkrvmbietmlfzoi:37304] [11] plumed(+0x134a5)[0x55aa1fa314a5]
[pkrvmbietmlfzoi:37304] *** End of error message ***
</pre>
{% endraw %}
